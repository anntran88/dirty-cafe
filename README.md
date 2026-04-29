# dirty-cafe
Data cleaning and analysis project using Python, Pandas, and Jupyter

--------------------------------------
Dirty Café Sales
--------------------------------------
Dataset Overview

Source: dirty_café_sales.csv (Kaggle)

Purpose: 

The Dirty Cafe Sales dataset contains 10,000 rows of synthetic data representing sales transactions in a cafe. This dataset is intentionally "dirty," with missing values, inconsistent data, and errors introduced to provide a realistic scenario for data cleaning and exploratory data analysis (EDA). It can be used to practice cleaning techniques, data wrangling, and feature engineering.

--------------------------------------
This project demonstrates a full cleaning and EDA workflow on a messy real‑world‑style dataset.
It includes:
- Data cleaning
- Feature engineering
- Exploratory analysis
- Visual storytelling

--------------------------------------------------------------------------------------
Data Cleaning Workflow
--------------------------------------
Input: dirty_café_sales.csv  
Notebook: CLEAN_dirty_cafe.ipynb  
Output: cafe_sales.csv
--------------------------------------
Alterations Made:

I have a deliberated duplicated 2 records to this dataset making the total 10,002 rows.
These are later removed as part of my data cleaning process.

After cleaning:

35 rows dropped where 2+ fields among Total Spent, Quantity, Price Per Unit were missing.

Final cleaned dataset: 9,965 rows.

Remaining DK/NS Values:
Some fields still contain DK/NS ("UNKNOWNS", "ERROR", or blanks).

These were retained after review:
- Item              474   ( 4.76%)
- Payment Method    3164  (31.75%)
- Location          3951  (39.65%)
- Transaction Date  460   ( 4.62%)

These were kept intentionally for analysis rather than dropped.

--------------------------------------------------------------------------------------
Input: CLEAN_café_sales.csv  
Notebook: NUM_dirty_cafe.ipynb
--------------------------------------
Explores numeric fields:
- Price per unit
- Total spent

Includes:
- Statistical review to justify dropping DK/NS in numeric fields.  Total Sample: 9491
- Summary tables
- Bar charts
- Pie charts

--------------------------------------------------------------------------------------
Input: CLEAN_café_sales.csv  
Notebook: TIME_dirty_cafe.ipynb
--------------------------------------
Dropped 460 rows with NaT in Transaction Date.
Final sample size: 9,505 rows.

Focuses on time‑based analysis.

Created two new classification fields: Item Category and Item Sub‑Category.

Contains:
- Line graph 1: Total spend by month
- Line graph 2: Spend by category (Food vs Drink)
- Line graph 3: Spend by sub‑category (Hot Drink, Cold Drink, Meal, Treat)
These enable richer analysis and cleaner visualisations.

--------------------------------------------------------------------------------------
