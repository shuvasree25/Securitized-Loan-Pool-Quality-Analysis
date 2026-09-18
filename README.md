# Securitized-Loan-Pool-Quality-Analysis
Securitized loan pool quality and risk analysis using Python, Pandas, NumPy, and Matplotlib to evaluate loan quality, portfolio exposure, defaults, delinquency, and risk trends.
Project Overview:
This project analyzes a securitized loan pool using Python, Pandas, NumPy, and Matplotlib.
The objective is to clean and validate loan-level data, analyze loan quality and exposure, identify default and delinquency patterns, and generate business insights through statistical analysis and visualizations.
The project follows a practical data analytics workflow:
Data Import → Data Inspection → Data Cleaning → Data Validation → Business Analysis → Visualization → Business Insights
Business Objective:
The objective of this project is to assess the quality and risk characteristics of a securitized loan pool by analyzing:
Total loan exposure
Loan volume and average loan size
Current, delinquent, and default loans
Credit score and interest rate patterns
Loan exposure by state
Loan exposure by loan type
Loan exposure by employment type
Default and delinquency percentages
Default distribution by loan type
Delinquent loan exposure by state
Loan origination trends over time
Dataset:
The project uses:
Securitized_Loan_Pool_Quality.csv
The dataset contains loan-level information such as:
Loan ID
Customer ID
Customer Name
Gender
Country
State
Age
Employment Type
Loan Type
Loan Amount
Loan Term
Income
Credit Score
Interest Rate
Loan Status
Origination Date
Data Cleaning & Preparation:
The dataset was prepared using Pandas through the following steps:
1. Data Inspection:
Checked the first and last records
Checked dataset shape
Reviewed column names
Inspected data types
Reviewed the structure of the dataset
2. Missing Value Analysis:
Missing values were identified in:
income
credit_score
interest_rate
Numeric columns were converted using pd.to_numeric() and missing values were handled before further analysis.
3. Data Type Conversion:
Examples include:
df["loan_id"] = df["loan_id"].astype(str)
df["customer_id"] = df["customer_id"].astype(str)
df["age"] = df["age"].astype(int)
The origination date was converted into a proper datetime format:
df["origination_date"] = pd.to_datetime(
    df["origination_date"],
    errors="coerce"
)
4. Column Standardization
The original date column was renamed:
df = df.rename(columns={"origination_date": "loan_date"})
5. Text Cleaning
Extra spaces were removed from categorical fields using:
.str.strip()
Text values were also standardized using string formatting operations.
6. Duplicate Check
Duplicate records were identified and removed:
df.duplicated().sum()
df = df.drop_duplicates()
7. Final Data Quality Check
The final dataset was checked for:
Dataset shape
Missing values
Data types
Sample records
Business Questions:
The cleaned dataset was analyzed to answer the following business questions:
Loan Portfolio Analysis:
What is the total loan amount?
What is the average loan amount?
What is the total loan count?
How many current loans are there?
How many delinquent loans are there?
How many default loans are there?
Credit & Interest Analysis:
What is the average credit score?
What is the average interest rate?
How does average credit score vary by loan status?
Exposure Analysis:
Which state has the highest loan exposure?
Which loan type has the highest loan exposure?
Which employment type has the highest loan exposure?
What is the number of loans by loan type?
Risk Analysis:
What percentage of loans are delinquent?
What percentage of loans are in default?
Which loan types have the highest number of defaults?
Which states have the highest delinquent loan exposure?
Time Analysis:
How does loan amount change by year?
Which year has the highest loan amount?
Visualizations
Matplotlib was used to create visualizations for key portfolio and risk metrics.
1. Loan Status Distribution
Shows the distribution of loans across different status.
2. Loan Exposure by Loan Type
Compares total loan exposure across different loan categories.
3. Top 10 States by Loan Exposure
Identifies states with the highest total loan exposure.
4. Default Loans by Loan Type
Shows the number of defaulted loans across loan types.
5. Average Credit Score by Loan Status
Compares average credit scores across different loan statuses.
6. Loan Origination Trend
Shows changes in total loan amount by year.
Key Analytical Areas
The project focuses on four major areas:
Portfolio Quality
Analyzed loan status distribution to understand the composition of current, delinquent, and default loans.
Loan Exposure
Analyzed loan amounts across:
States
Loan types
Employment types
Credit Risk
Used credit scores, loan status, and default/delinquency metrics to examine loan quality.
Portfolio Trends
Analyzed yearly loan amounts to identify changes in loan origination volume over time.
Business Insights:
The analysis helps identify:
The overall size of the loan portfolio
Major sources of loan exposure
Current versus delinquent and default loans
Loan types contributing to default activity
Geographic concentration of loan exposure
Credit score differences across loan statuses
Changes in loan origination over time
These insights can support portfolio monitoring, risk assessment, and securitized loan pool quality analysis.
Project Outcome:
This project was developed as a practical financial data analytics and risk analysis project, with a focus on applying Python-based data analysis techniques to a loan portfolio environment.It demonstrates the complete process from raw loan data preparation to business focused analysis and visualization.
