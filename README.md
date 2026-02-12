# 💼 Global Tech Layoffs (2020–2023) – SQL Data Cleaning & Exploratory Analysis

This project analyzes a real-world dataset of global tech layoffs between 2020 and 2023. The data was sourced from Kaggle and cleaned, transformed, and explored entirely using **MySQL**.

The objective was to simulate a real-world data workflow: starting with raw, messy data and transforming it into structured, analysis-ready insights using SQL.

---

## 🎯 Project Goals

- Clean and standardize raw layoff data using SQL  
- Detect and remove duplicate records  
- Handle missing and inconsistent values  
- Perform exploratory data analysis (EDA) to uncover trends across time, industries, and regions  
- Apply advanced SQL techniques such as window functions and CTEs  

---

## 🛠️ Technologies & Concepts Used

- **MySQL**
- **Common Table Expressions (CTEs)**
- **Window Functions** (`ROW_NUMBER()`, `DENSE_RANK()`)
- **Aggregate Functions**
- **Date Functions** (`STR_TO_DATE()`, `YEAR()`, `MONTH()`)
- **String Functions & Data Standardization**
- **Self JOINs**

---

## 🧹 Data Cleaning Process

To ensure data integrity and accuracy, the following cleaning steps were performed:

- Created a **staging table** to preserve the original dataset
- Identified and removed **150+ duplicate rows** using `ROW_NUMBER()` inside a CTE
- Standardized inconsistent text values (e.g., `"CryptoCurrency"` unified to `"Crypto"`)
- Cleaned formatting issues in country names (e.g., removing trailing periods like `"United States."`)
- Converted date fields from text format to proper `DATE` datatype using `STR_TO_DATE()`
- Filled missing `industry` values using a **self-join** based on matching company names
- Removed irrelevant or fully null records where necessary

This structured cleaning pipeline ensured the dataset was analysis-ready.

---

## 📊 Exploratory Data Analysis (EDA)

After cleaning, several analytical queries were written to identify trends and patterns:

### 🔹 Layoff Trends Over Time
- Total layoffs per year
- Monthly layoff trends
- Rolling cumulative layoffs using window functions

### 🔹 Company-Level Insights
- Companies with the highest total layoffs
- Companies that laid off **100% of their workforce**
- Year-wise ranking of top companies using `DENSE_RANK()`

### 🔹 Industry & Geographic Analysis
- Total layoffs by:
  - Industry
  - Country
  - Location
  - Funding stage
- Comparison of layoff impact across different sectors

---

## 📈 Key Insights

- **2022 recorded the highest number of layoffs**, significantly exceeding other years.
- Several well-funded startups that raised hundreds of millions still conducted full workforce layoffs.
- The **Crypto and Retail sectors** were among the most heavily impacted industries.
- The **United States accounted for the largest share** of total layoffs globally.
- Layoffs showed noticeable spikes during specific months, visible through rolling monthly totals.

---

## 📂 Project Structure

```
├── sql_data_cleaning.sql     # Complete SQL data cleaning process
├── sql_eda_analysis.sql      # Exploratory data analysis queries
├── README.md                 # Project documentation
```

---

## 📌 Dataset Source

Kaggle Dataset:  
https://www.kaggle.com/datasets/swaptr/layoffs-2022  

---

## 👨‍💻 Author

Developed by Ruwab Aziz


GitHub: https://github.com/ruwabaziz  

---

## 📚 Key Learnings

Through this project, I strengthened my ability to:

- Build a structured **SQL-based data cleaning workflow**
- Work with messy, real-world datasets
- Apply **window functions for advanced analysis**
- Perform trend analysis using time-series aggregation
- Write optimized, readable, and professional SQL queries


