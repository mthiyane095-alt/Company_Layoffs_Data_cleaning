# Layoffs Data Cleaning Project

## 📌 Project Overview
This project focuses on cleaning a raw dataset of global tech layoffs using MySQL. The goal was to take messy, raw data and transform it into a clean, standardized dataset ready for exploratory data analysis (EDA).

## 📂 Dataset
- Source: Alex The Analyst
- Raw Data: Raw data was cleaned an transformed in MYSQL Workbench
- Cleaned Data: cleaned_layoffs_data.csv 

## 🛠️ Tools Used
- **MySQL Workbench** (for data cleaning and transformation)

## 🧹 Data Cleaning Steps Taken
Here is a summary of the steps I took to clean the data:
1. **Removed Duplicates**: Created a staging table and used `ROW_NUMBER()` to identify and remove duplicate rows.
2. **Standardized Data:** 
   - Trimmed whitespace from company names.
   -  - Standardized the `industry` column (e.g., changing "Crypto Currency" to "Crypto").
   - Converted the `date` column from text to a proper `DATE` format.
3. **Handled Null/Blank Values:** 
   - Populated missing industry data by joining the table to itself based on company name.
   - Removed rows where both `total_laid_off` and `percentage_laid_off` were null.
4. **Removed Unnecessary Columns:** Dropped the temporary `row_num` column used to find duplicates.

## 📊 Final Result
The final cleaned table (`layoffs_staging2`) was exported as a CSV file to be used for further data visualization and analysis. 

## 🚀 How to Use
1. Download the `cleaned_layoffs_data.csv` file.
2. Open it in Excel, Tableau, Power BI, or Python for further analysis.
