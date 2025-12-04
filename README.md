# Zomato Bangalore Data Cleaning Project: End-to-End Pipeline

##  Project Overview
This project focuses on **cleaning and preprocessing** the Zomato Bangalore Restaurants dataset. The raw data contained redundant columns, inconsistent data types, null values, and formatting issues. 

Using **Python and Pandas**, I built a cleaning pipeline to transform this raw data into a clean, structured dataset ready for Exploratory Data Analysis (EDA) and Machine Learning models.

---

##  Key Data Cleaning Steps performed

## 1️. Column Optimization
* **Dimensionality Reduction:** Removed 7 redundant columns (e.g., `url`, `phone`, `reviews_list`) that were not useful for analysis.
* **Renaming:** Standardized column names for better readability (e.g., `approx_cost(for two people)` → `cost_for_two`, `listed_in(city)` → `location`).

## 2️. Data Integrity Checks
* **Duplicate Removal:** Identified and dropped **124 duplicate rows** to ensure data uniqueness.
* **Handling Nulls:** Removed rows with missing critical information in `rest_type` and `cuisines`.

## 3️. Data Type & Format Standardization
* **Rating Cleaning:** * Handled non-numeric values like "NEW" by converting them to `NaN`.
    * Cleaned formats like "4.1/5" to pure numeric float "4.1".
* **Cost Formatting:** Removed formatting characters (commas in "1,200") and converted the column to **Integer** type for arithmetic operations.

## 4️. Statistical Imputation
* **Correlation Check:** Performed a Pearson correlation test between `votes` and `rating`.
* **Imputation:** Validated that there was no strong correlation, so missing `rating` values were imputed using the **Mean Imputation** method.

---

##  Final Outcome
* The dataset was successfully cleaned and exported as `cleaned_df.csv`.
* The final data is free of nulls, duplicates, and formatting errors, making it ready for immediate visualization or modeling.

---

##  Tech Stack
* **Python**
* **Pandas** (Data Manipulation)
* **NumPy** (Numerical Operations)
* **Seaborn / Matplotlib** (Correlation Heatmap)
