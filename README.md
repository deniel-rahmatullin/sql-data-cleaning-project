# World Layoffs: SQL Data Cleaning & Exploratory Analysis

MySQL project: cleaning a raw dataset of global company layoffs and
exploring it to find patterns by company, industry and country.

## Dataset
World layoffs data from the Alex The Analyst MySQL course.
564 raw rows, 480 rows after cleaning.
Covers layoffs from 6 Dec 2022 to 6 Mar 2023.

## Part 1: Data cleaning (`data_cleaning2.sql`)
1. Created a staging table so the raw data stays untouched
2. Removed duplicate rows using `ROW_NUMBER() OVER (PARTITION BY ...)` in a CTE
3. Standardised values, e.g. changed "United States." to "United States"
4. Converted `date` from text to DATE type
5. Handled NULL / blank values (2 rows with missing industry)
6. Removed rows with no layoff data and dropped helper columns

Result: 84 rows removed in total (564 raw rows, 480 after cleaning).

## Part 2: Exploratory analysis (`eda_project.sql`)
- Total layoffs by company, industry, country and year
- Rankings and rolling totals using CTEs and window functions

## Key findings
- Largest layoffs by company: Google (12,000), Microsoft (10,000),
  Ericsson (8,500), Salesforce (8,000), Amazon (8,000)
- Top industries: Other (28,767), Consumer (16,518), Retail (14,202)
- The United States dominates by country (94,985 laid off), far ahead of
  Sweden (9,100) and the Netherlands (7,650)
- The dataset covers only about three months (6 Dec 2022 to 6 Mar 2023),
  so 2022 (8,633) is not comparable to 2023 (125,677)

## Skills
SQL (MySQL), data cleaning, CTEs, window functions, exploratory data analysis
