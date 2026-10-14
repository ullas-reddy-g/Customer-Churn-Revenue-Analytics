# Customer Churn & Revenue Analytics Dashboard

## 1. Project Overview

The Customer Churn & Revenue Analytics Dashboard is a data analytics project designed to analyse customer churn patterns, understand revenue-related trends, and identify factors associated with customer attrition.

The project combines Python, SQL, and Microsoft Power BI to transform raw customer data into meaningful insights that can support customer retention and business decision-making.

The dashboard presents customer metrics, churn patterns, revenue-related analysis, and business recommendations through interactive visualizations.

## 2. Problem Statement

Customer churn can affect recurring revenue, customer relationships, and business growth. Understanding why customers leave and which customer segments have higher churn rates can help businesses develop better retention strategies.

This project analyses customer demographics, contract types, internet services, payment methods, tenure, and monthly charges to identify patterns associated with customer churn.

The results are presented through an interactive Power BI dashboard to support data-driven business decisions.

## 3. Project Objectives

- Analyse customer churn and retention rates.
- Identify customer segments with higher churn rates.
- Examine churn patterns across contract types and tenure groups.
- Analyse churn across internet services and payment methods.
- Explore monthly charges and revenue-related patterns.
- Use SQL queries to extract meaningful business insights.
- Develop an interactive Power BI dashboard.
- Recommend strategies that may help improve customer retention.

## 4. Dataset

**Dataset:** IBM Telco Customer Churn

**Dataset source:** IBM Telco Customer Churn sample dataset.

The dataset contains 7,043 customer records and 21 columns describing customer demographics, subscribed services, account information, billing details, and churn status.

Important attributes include:

- `customerID`
- `gender`
- `SeniorCitizen`
- `Partner`
- `Dependents`
- `tenure`
- `InternetService`
- `Contract`
- `PaymentMethod`
- `MonthlyCharges`
- `TotalCharges`
- `Churn`

The dataset was used to investigate customer behaviour and identify patterns associated with customer attrition.

Dataset repository: https://github.com/IBM/telco-customer-churn-on-icp4d

## 5. Technologies Used

### Programming and Data Analysis
- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn

### Database and Querying
- MySQL
- SQL

### Business Intelligence and Visualization
- Microsoft Power BI
- DAX

### Development Environment
- Jupyter Notebook
- Visual Studio Code

## 6. Data Cleaning and Preprocessing

Data cleaning and preprocessing were performed using Python and Pandas.

The following steps were completed:

1. Loaded the original CSV dataset.
2. Examined the dataset dimensions and column data types.
3. Checked for missing values and duplicate records.
4. Removed unnecessary whitespace from text fields.
5. Converted `TotalCharges` from a text data type to a numeric data type.
6. Identified 11 blank values in `TotalCharges`.
7. Verified that the affected records belonged to customers with zero tenure and no recorded churn.
8. Replaced the missing `TotalCharges` values with zero because those customers had zero tenure.
9. Rechecked the dataset for missing values and duplicate records.
10. Saved the cleaned dataset for further analysis and database operations.

### Final Dataset Validation

- Total records: 7,043
- Total columns: 21
- Missing values after cleaning: 0
- Duplicate rows: 0
- Duplicate customer IDs: 0

The cleaned dataset was subsequently used for exploratory analysis, SQL analysis, and Power BI reporting.

## 7. Exploratory Data Analysis

Exploratory Data Analysis (EDA) was performed to understand customer characteristics and identify patterns associated with churn.

The analysis examined:

- Overall churn distribution
- Churn by contract type
- Churn by tenure group
- Churn by internet service
- Churn by payment method
- Average monthly charges by churn status
- Average monthly charges by contract type
- Monthly charges across customer segments
- Differences between churned and retained customers

Python visualizations were used to examine these patterns before incorporating the findings into the Power BI dashboard.

## 8. SQL Analysis

MySQL was used to store and analyse the customer dataset.

SQL queries were developed to investigate the following business questions:

- How many customers are present in the dataset?
- How many customers have churned?
- How many customers have been retained?
- What is the overall customer churn rate?
- Which contract types have higher churn rates?
- How does churn vary by payment method?
- How does churn vary by internet service?
- How does churn vary across tenure groups?
- What are the average monthly charges for churned and retained customers?
- What are the total monthly charges associated with each churn status?

The SQL results were compared with the Python analysis to help validate the calculated customer metrics.

## 9. Key Findings

The analysis produced the following results:

| Metric | Result |
|---|---:|
| Total Customers | 7,043 |
| Churned Customers | 1,869 |
| Retained Customers | 5,174 |
| Churn Rate | 26.54% |
| Retention Rate | 73.46% |
| Average Monthly Charges per Customer | 64.76 |
| Total Monthly Charges Across All Customers | 456,116.60 |
| Monthly Charges Associated with Churned Customers | 139,130.85 |

The dataset's monetary values are expressed in its recorded currency units.

### Churn by Contract Type

| Contract Type | Customers | Churned Customers | Churn Rate |
|---|---:|---:|---:|
| Month-to-month | 3,875 | 1,655 | 42.71% |
| One year | 1,473 | 166 | 11.27% |
| Two year | 1,695 | 48 | 2.83% |

The results show that month-to-month customers had a substantially higher churn rate than customers on one-year and two-year contracts.

The analysis also identified differences in churn rates across internet service types, payment methods, and tenure groups.

**Revenue interpretation:** Monthly charges associated with churned customers represent the sum of their recorded monthly charges. This figure is not a verified measure of historical revenue lost over a specific period.

## 10. Power BI Dashboard

An interactive Power BI dashboard was developed to present customer churn metrics, revenue-related patterns, and business recommendations.

The report contains three pages.

### Page 1: Customer Churn & Revenue Analytics

This page provides an overview of customer retention and churn.

It includes:

- Total customers
- Churned customers
- Overall churn rate
- Retention rate
- Customer retention overview
- Customer churn by contract type
- Customer churn by tenure
- Customer churn by internet service

### Page 2: Customer Revenue Analysis

This page examines monthly charges and their relationship with customer churn.

It includes:

- Average monthly charges by churn status
- Customer churn by payment method
- Average monthly charges by contract type
- Average customer tenure
- Average monthly charges by internet service
- Total monthly charges by churn status
- Monthly charges associated with churned customers

### Page 3: Business Insights & Recommendations

This page summarises the main findings and presents recommendations based on the observed patterns.

It includes:

- Key analytical findings
- Contract-related churn observations
- Customer retention recommendations
- Pricing and service review suggestions
- Churn KPI monitoring recommendations

## 11. Business Recommendations

Based on the observed patterns, the following recommendations are proposed.

### 1. Encourage Long-Term Contracts

Explore suitable incentives for customers to choose one-year or two-year contracts, as these groups showed lower churn rates in the analysed dataset.

### 2. Improve Customer Retention

Identify customer segments associated with higher churn and evaluate targeted retention offers.

### 3. Review Pricing and Service Combinations

Investigate whether higher monthly charges or particular service combinations are associated with customer attrition.

### 4. Improve Customer Support

Review customer support services and identify opportunities to improve customer satisfaction and service quality.

### 5. Monitor Churn KPIs

Regularly monitor churn rate, retention rate, customer counts, and monthly charges to identify changing customer behaviour.

These recommendations are based on observed associations in the dataset. Their effectiveness should be evaluated using additional business data before implementation.

## 12. Project Workflow

The project followed these major stages:

1. Dataset collection
2. Data loading and inspection
3. Data cleaning and preprocessing using Python
4. Exploratory Data Analysis
5. SQL-based business analysis
6. KPI calculation and validation
7. Power BI dashboard development
8. Dashboard and result validation
9. Project documentation

## 13. Project Structure

The repository contains the dataset, analysis notebook, SQL queries, dashboard, and supporting screenshots.

```text
Customer-Churn-Revenue-Analytics/
|
|-- data/
|   |-- raw/
|   |   `-- Telco-Customer-Churn.csv
|   |
|   `-- processed/
|       |-- telco_customer_churn_cleaned.csv
|       `-- telco_customer_churn_mysql.csv
|
|-- images/
|   |-- dashboard_overview.png
|   |-- revenue_analysis.png
|   `-- business_recommendations.png
|
|-- notebooks/
|   `-- customer_churn_analysis.ipynb
|
|-- sql/
|   `-- customer_churn_analysis.sql
|
|-- Customer_Churn_Revenue_Analytics.pbix
`-- README.md
```

## 14. Limitations

- The dataset represents a sample of telecom customers and may not represent every business or customer population.
- The analysis identifies associations but does not establish that a particular factor causes customer churn.
- The dataset does not provide a defined historical period for calculating actual revenue lost after churn.
- The analysis is based on the available customer attributes and billing information.
- The project is an analytical dashboard, not a deployed real-time churn prediction system.
- The business recommendations require further evaluation before implementation.

## 15. Future Enhancements

Potential future improvements include:

- Developing a machine learning model to predict customer churn.
- Introducing customer-level churn risk segmentation.
- Automating dataset refresh and dashboard reporting.
- Adding customer lifetime value analysis.
- Evaluating the effectiveness of retention strategies using additional business data.
- Publishing the dashboard through an appropriate sharing platform.

These enhancements are possible future extensions and are not claimed as completed features of the current project.

## 16. Conclusion

The Customer Churn & Revenue Analytics Dashboard demonstrates how Python, SQL, and Microsoft Power BI can be combined to analyse customer churn and revenue-related patterns.

The project includes data cleaning, exploratory analysis, SQL queries, KPI calculations, interactive visualizations, and business recommendations.

The analysis identified an overall churn rate of 26.54% and showed that month-to-month contract customers had a higher churn rate than customers with longer-term contracts.

The dashboard presents these findings in an accessible format and demonstrates how data analytics can support customer retention analysis and data-driven business decisions.

---

**Project Title:** Customer Churn & Revenue Analytics Dashboard

**Tools:** Python, Pandas, NumPy, Matplotlib, Seaborn, MySQL, SQL, Power BI, DAX

**Dataset:** IBM Telco Customer Churn
