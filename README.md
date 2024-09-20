# Business-Analysis-Project
https://docs.google.com/spreadsheets/d/1O8XSHDluWkMelZKTjDxRsJ3AcqNLdI4vQLHdLiMmH_U/edit?usp=sharing
Above is te project link

## Project Overview
This project aims to analyze user activity data from the company's website to understand conversion rates and user retention. The analysis focuses on creating a conversion funnel and conducting cohort analysis.

## Data Description
The dataset contains user activities on the company's website with the following columns:
- `user_id`: Unique customer IDs
- `event_type`: Type of activity (e.g., page view, add to cart, purchase)
- `category_code`: Category of the product
- `brand`: Company that makes the product
- `price`: Price of the product in USD
- `event_date`: Date of the user activity in YYYY-MM-DD format

## Part 1: Build a Conversion Funnel

1. **Create Conversion Funnel Sheet:**
    - Create a new sheet named "conversion_funnel".
    - Insert a pivot table from the "raw_user_activity" sheet.
    - Add `event_type` to Rows and `user_id` to Values (set to count unique users).
    - Calculate total conversion rates and conversion rates to the next step using formulas.

## Part 2: Prepare Data for Cohort Analysis

1. **Filter Purchases:**
    - Create a new sheet named "purchase_activity".
    - Filter `event_type` in "raw_user_activity" to select only purchases.
    - Copy the filtered data to "purchase_activity".

2. **Calculate First Purchase Dates:**
    - Create a pivot table in a new sheet named "first_purchase" to find the minimum `event_date` for each `user_id`.
    - Add a `first_purchase_date` column in "purchase_activity" and use `VLOOKUP` to populate it.

3. **Set Up Monthly Data:**
    - Add `event_month`, `first_purchase_month`, and `cohort_age` columns in "purchase_activity".
    - Use the `TEXT` function to format months and the `DATEDIF` function to calculate `cohort_age`.

## Part 3: Calculate Retention Rates

1. **Group Data into Cohorts:**
    - Insert a pivot table in a new sheet named "cohort_analysis".
    - Group data by `first_purchase_month` and count unique users for each `cohort_age`.

2. **Calculate Retention Rates:**
    - Create a new sheet named "retention_rates".
    - Add rows for each cohort and columns for cohort ages from 1 to 4 months.
    - Use formulas to calculate retention rates based on starting cohort sizes.

## Part 4: Organize and Document Your Spreadsheet

1. **Executive Summary:**
    - Fill in results and analysis descriptions in the "Executive Summary" sheet.
    - Summarize results from "conversion_funnel" and "retention_rates".

2. **Reorder Sheets:**
    - Organize sheets with "Table of Contents" and "Executive Summary" first, followed by analytical results, calculations, and raw data sheets.

3. **Format for Readability:**
    - Format numbers and dates, add borders, use bold fonts for headers, freeze rows, and highlight cells with calculations.

## Conclusion
This project provides insights into user conversion and retention, helping the executive team make data-driven decisions to improve business performance.
