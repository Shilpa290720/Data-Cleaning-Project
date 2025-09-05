# 🧹 SQL Data Cleaning Project - Layoffs 2022 Dataset

This project focuses on cleaning and preparing the **Layoffs 2022** dataset using SQL for further analysis and visualization. The dataset, sourced from [Kaggle](https://www.kaggle.com/datasets/swaptr/layoffs-2022), contains records of tech layoffs from companies around the world, including information such as the number of employees laid off, the percentage of the workforce affected, industry type, and more.

---

## 📌 Project Goals

- Create a staging environment for safe data cleaning
- Identify and remove duplicate records
- Standardize inconsistent data entries
- Handle and impute missing values where appropriate
- Remove unnecessary or unusable records
- Prepare the dataset for accurate and insightful analysis

---

## 📁 Dataset Overview

- **Source**: [Kaggle - Layoffs 2022](https://www.kaggle.com/datasets/swaptr/layoffs-2022)
- **Fields Include**:
  - Company name
  - Location
  - Industry
  - Number of employees laid off
  - Percentage laid off
  - Stage of the company (e.g. Series A, Series B)
  - Funds raised
  - Country
  - Date of layoff

---

## 🧼 Cleaning Process Overview

1. **Created a Staging Table**: To protect the original raw data and allow experimentation safely.
2. **Removed Duplicates**: Identified exact and near-exact duplicate rows using SQL window functions.
3. **Standardized Data**:
   - Cleaned up inconsistencies in country and industry names
   - Converted textual date values into SQL `DATE` format
   - Unified different representations of the same category (e.g., “CryptoCurrency” → “Crypto”)
4. **Handled Null Values**:
   - Filled missing `industry` data where possible using company name matching
   - Kept relevant NULLs for analytical flexibility
   - Removed rows with no useful data (e.g., both `total_laid_off` and `percentage_laid_off` missing)
5. **Final Cleanup**:
   - Dropped temporary columns (e.g., `row_num`)
   - Verified dataset integrity

---

## ✅ Outcome

The cleaned dataset is stored in a new staging table (`layoffs_staging2`) and is now ready for:

- Exploratory Data Analysis (EDA)
- Visualizations
- Reporting
- Predictive modeling (if desired)

---

## 🧠 Skills & Concepts Used

- SQL window functions (`ROW_NUMBER()`)
- CTEs (Common Table Expressions)
- Data normalization and standardization
- NULL handling and conditional updates
- Date formatting and conversion
- Good data governance practices (e.g., staging tables)

---

## 📊 Next Steps

- Build dashboards using tools like Tableau or Power BI
- Perform trend analysis (layoffs by industry, country, date)
- Forecast potential future layoffs using historical trends

---

## 📬 Contact

Feel free to fork the project, open issues, or reach out with questions or suggestions.

---
