# Customer Segmentation Analysis

## Project Overview

This project develops an end-to-end customer segmentation solution using customer demographic, transaction, customer address, and new customer data. The project follows a complete data analytics workflow, including data quality assessment, data cleaning, SQL analysis, exploratory data analysis (EDA), RFM (Recency, Frequency, Monetary) analysis, customer segmentation, and the development of an interactive Power BI dashboard to generate business insights and support data-driven decision-making.

The repository documents each stage of the project, from the original raw datasets through to the final analytical outputs.

---

## Objectives

The objectives of this project are to:

- Assess and improve the quality of customer data.
- Prepare reliable datasets for customer analytics.
- Explore customer purchasing behaviour through exploratory data analysis.
- Perform customer segmentation using the RFM framework.
- Develop an interactive Power BI dashboard for business reporting.
- Generate actionable insights to support customer engagement and marketing strategies.

---

## Dataset

The project uses four datasets:

- **Transactions** – Customer purchase transactions.
- **CustomerDemographic** – Customer demographic information.
- **CustomerAddress** – Customer address information.
- **NewCustomerList** – Information about prospective customers.

Both the original datasets and cleaned datasets are included in this repository to document the complete data preparation process.

---

# Project Workflow

```
Raw Data
    ↓
Data Quality Assessment
    ↓
Data Cleaning
    ↓
SQL Analysis
    ↓
Exploratory Data Analysis (EDA)
    ↓
RFM Analysis
    ↓
Customer Segmentation
    ↓
Power BI Dashboard
    ↓
Business Insights
```

---

# 1. Data Quality Assessment and Data Cleaning

Each dataset was individually assessed before cleaning. Data quality issues were identified and addressed to improve consistency, accuracy, and usability for customer segmentation analysis.

## CustomerDemographic

The following data preparation steps were completed:

- Removed variables that were not relevant to the customer segmentation analysis:
  - `first_name`
  - `last_name`
  - `DOB`
  - `deceased_indicator`
  - `default`
- Created a new **age** variable from the `DOB` column and removed the original `DOB` field.
- Standardised inconsistent values in the `gender` column:
  - `F` → `Female`
  - `Femal` → `Female`
  - `M` → `Male`
  - `U` → `Unknown`
- Removed records containing missing values where appropriate.
- Verified that no duplicate records were present.
- Retained only the variables relevant to customer segmentation:
  - `customer_id`
  - `gender`
  - `past_3_years_bike_related_purchases`
  - `job_title`
  - `job_industry_category`
  - `wealth_segment`
  - `owns_car`
  - `tenure`
  - `age`

---

## NewCustomerList

The following data preparation steps were completed:

- Removed variables that were not required for the analysis:
  - `first_name`
  - `last_name`
  - `DOB`
  - `deceased_indicator`
  - `address`
  - `Rank`
  - `Value`
- Created a new **age** variable from the `DOB` column and removed the original `DOB` field.
- Standardised inconsistent values in the `gender` column by converting `U` to `Unknown`.
- Removed records containing missing values where appropriate.
- Verified that no duplicate records were present.
- Retained variables relevant to customer demographics and customer location.

---

## Transactions

The following data preparation steps were completed:

- Removed unnecessary empty columns from the original dataset.
- Converted the `product_first_sold_date` column from integer format to a datetime format.
- Removed records containing missing values where appropriate.
- Verified that no duplicate records were present.
- Retained the variables required for transaction analysis.

---

## CustomerAddress

The following data preparation steps were completed:

- Removed the `country` column as it was not required for the analysis.
- Standardised inconsistent values in the `state` column:
  - `New South Wales` → `NSW`
  - `Victoria` → `VIC`
- Removed records containing missing values where appropriate.
- Verified that no duplicate records were present.
- Retained the variables required for customer location analysis:
  - `customer_id`
  - `address`
  - `postcode`
  - `state`
  - `property_valuation`

---

# 2. SQL Analysis

SQL was used to support data exploration, validation, and data preparation throughout the project. Queries were developed to demonstrate fundamental SQL skills and to assist with preparing the cleaned datasets for subsequent analysis and visualisation in Power BI.

The SQL analysis included activities such as:

- Retrieving and exploring customer and transaction data.
- Filtering and summarising records using aggregate functions.
- Joining multiple tables to create integrated datasets for analysis.
- Validating data consistency after the data cleaning process.
- Preparing structured datasets for exploratory analysis, RFM analysis, customer segmentation, and dashboard development.

The SQL scripts in this project demonstrate practical data manipulation and querying techniques commonly used in data analytics workflows.

---

# 3. Exploratory Data Analysis (EDA)

Exploratory Data Analysis (EDA) was conducted on each cleaned dataset to understand customer characteristics, purchasing behaviour, and geographical distribution before performing customer segmentation. The analysis combined descriptive statistics with data visualisation to identify patterns, assess variable distributions, and provide business context for the subsequent RFM analysis.

The EDA covered four datasets:

### Transactions
The transaction dataset was analysed to understand purchasing behaviour and sales activity. The analysis included:

- Transaction volume over time
- Monthly transaction distribution
- Day-of-week purchasing patterns
- Product pricing and profit distributions
- Product and brand frequency analysis

### Customer Demographic
The customer demographic dataset was explored to understand the characteristics of existing customers. The analysis included:

- Gender distribution
- Age distribution
- Past three years of bike-related purchases
- Customer tenure
- Wealth segment distribution
- Vehicle ownership
- Job industry categories
- Most common job titles

### Customer Address
The customer address dataset was analysed to examine customer location characteristics. The analysis included:

- Customer distribution by state
- Property valuation distribution
- Most common customer postcodes

### New Customer List
The prospective customer dataset was explored to understand the characteristics of potential customers. The analysis included:

- Gender distribution
- Age distribution
- Past three years of bike-related purchases
- Customer tenure
- Wealth segment distribution
- Vehicle ownership
- Job industry categories
- Job title distribution
- Geographic distribution by state and postcode
- Property valuation
- Correlation analysis between numerical variables

### Key Outcome

The exploratory data analysis provided a comprehensive understanding of customer demographics, purchasing behaviour, and geographic characteristics. These insights validated the quality of the cleaned datasets, highlighted important customer patterns, and established the analytical foundation for the RFM analysis, customer segmentation, and Power BI dashboard developed in the later stages of the project.
---

# 4. RFM Analysis

*This section will document the Recency, Frequency, and Monetary (RFM) analysis used to evaluate customer value and purchasing behaviour.*

---

# 5. Customer Segmentation

*This section will present the customer segmentation methodology and describe the characteristics of each customer segment.*

---

# 6. Power BI Dashboard

*This section will showcase the interactive Power BI dashboard developed to visualise customer insights and business performance.*

---

# 7. Business Insights

*This section will summarise the key analytical findings and business recommendations derived from the project.*

---

## Repository Structure

```
customer-segmentation-analysis/
│
├── data/
│   ├── raw/
│   │   └── Customer_Segmentation_Data.xlsx
│   │
│   └── cleaned/
│       ├── Customer_Segmentation_Data_Cleaned.xlsx
│       ├── Transactions_Cleaned.xlsx
│       ├── CustomerDemographic_Cleaned.xlsx
│       ├── CustomerAddress_Cleaned.xlsx
│       └── NewCustomerList_Cleaned.xlsx
│
├── README.md
├── LICENSE
└── .gitignore
```

---

## Tools and Technologies

- Microsoft Excel
- Python
- SQL
- Power BI
- Git
- GitHub
