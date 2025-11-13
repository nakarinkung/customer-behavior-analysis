# Data Analytics Project: Customer Behavior Analysis
## Overview
This comprehensive data analytics project analyzes customer shopping behavior to uncover patterns in purchasing habits, subscription adoption, and customer preferences. The project follows a complete data pipeline from initial data loading and cleaning in Python, through SQL analysis in Microsoft SQL Server, to final visualization in Power BI. The goal was to identify key drivers of customer value and provide actionable insights for marketing strategy and customer retention.

## Dataset
**Source:** Customer Behavior Dataset

Description: Contains 3,900 customer transactions with detailed demographic, behavioral, and purchase information

Key Features: Customer demographics, purchase history, subscription status, product categories, review ratings, and shopping preferences

Initial Size: 3,900 rows × 18 columns

## Tools & Technologies
Programming Language: Python (Pandas for data manipulation and cleaning)

Database & Querying: Microsoft SQL Server, SQLAlchemy, pyodbc

Data Visualization: Microsoft Power BI

Key Libraries: Pandas, SQLAlchemy

## Project Steps

### 1. Data Loading & Initial Inspection (Python)
Loaded the customer shopping behavior dataset (customer_shopping_behavior.csv) into a Pandas DataFrame

Performed initial data exploration using .head() and .describe() to understand data structure and distributions

Identified data quality issues including 37 missing values in the review_rating column

---

### 2. Data Cleaning & Feature Engineering (Python)
Handled Missing Values: Imputed missing review ratings using median values grouped by product category

Standardized Column Names: Converted column names to lowercase and replaced spaces with underscores for consistency

Feature Engineering:

Created age_group feature using quantile-based binning (Young Adult, Adult, Middle-aged, Senior)

Created frequency_of_purchases_days by mapping categorical frequency values to numerical day equivalents

Data Validation: Identified and removed redundant column (promo_code_used) as it was identical to discount_applied

---

### 3. Database Integration
Established connection to Microsoft SQL Server Express using SQLAlchemy and pyodbc

Successfully loaded the cleaned DataFrame into SQL Server as customer_behavior table

Enabled seamless transition from Python analysis to SQL querying for deeper business intelligence

---

### 4. SQL Data Analysis
The SQL analysis (as shown in the separate SQL file) answered critical business questions including:

Revenue comparison between gender segments

Customer segmentation based on purchase history (New, Returning, Loyal)

Product performance analysis including top-rated items and discount effectiveness

Subscription behavior patterns and correlation with repeat purchases

Age group contribution to overall revenue

---

### 5. Power BI Dashboard
Developed interactive dashboard visualizing key customer behavior metrics

Included subscription analytics, demographic breakdowns, and product performance

Enabled dynamic filtering for stakeholder exploration and decision-making

--- 

## Key Components:

**Subscription Analytics:** 73% non-subscribers vs. 27% subscribers with 3.9K total customers

**Financial Metrics:** $59.76 average purchase amount and 3.75 average review rating

**Demographic Breakdown:** Gender distribution and age group analysis (Young Adult, Middle-aged, Adult, Senior)

**Product Performance:** Revenue and sales breakdown across Clothing, Accessories, Footwear, and Outerwear

**Shipping Preferences:** Distribution across 2-Day, Express, Free, Next Day Air, Standard, and Store Pickup

---

## Results & Insights
**Key Findings:**
Subscription Opportunity: Only 27% of customers are subscribed, indicating significant growth potential for subscription programs

Revenue Distribution: Clothing category generates the highest revenue, while Accessories show strong performance relative to sales volume

Customer Loyalty: Analysis reveals that repeat buyers (more than 5 previous purchases) are significantly more likely to subscribe to services

Shipping Preferences: Express and Standard shipping methods show correlation with higher average purchase amounts

Age Group Performance: Middle-aged and Young Adult segments contribute most significantly to both revenue and sales volume

---

**Business Recommendations:**
Targeted Subscription Campaigns: Focus on Loyal and Returning customer segments who show higher subscription conversion rates

Product Strategy: Leverage high-rated products in Accessories category to drive cross-selling opportunities

Shipping Incentives: Use Express shipping as a premium option to increase average order value

Age-Specific Marketing: Develop tailored campaigns for Middle-aged and Young Adult demographics who demonstrate highest purchasing power
