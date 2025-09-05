# gtc-ml-project1--hotel-bookings
This project focuses on data cleaning, preprocessing, and feature engineering
Hotel Booking Demand Analysis
•	 Project Overview
This project analyzes the Hotel Booking Dataset to understand booking behaviors, detect data quality issues, and prepare the dataset for machine learning models. The main focus is on cleaning, exploring, and engineering features to create a high-quality dataset suitable for predictive modeling.

•	Objectives
1.	Understand the Data: Load, inspect, and summarize the dataset.
2.	Data Cleaning: Handle missing values, duplicates, and outliers.
3.	Feature Engineering: Create new informative variables (e.g., total_guests, total_nights, is_family).
4.	Exploratory Analysis: Visualize relationships and data distributions.
5.	Data Preparation for ML: Encode categorical variables, fix data types, and split into train/test sets.

•	Steps Performed
1. Data Inspection
•	Used .info() and .describe() for summary statistics.
•	Identified missing values and duplicate rows.
•	Visualized missing data using heatmaps.
2. Handling Missing Data
•	Company & Agent → replaced with "None" or 0.
•	Country → imputed with the mode or "Unknown".
•	Children → imputed with median/mode.
3. Outlier Detection & Handling
•	Detected outliers in adr (average daily rate) and lead_time using boxplots & IQR.
•	Capped extreme ADR values at 1000 to reduce skew.
4. Feature Engineering
•	total_guests = adults + children + babies.
•	total_nights = stays_in_weekend_nights + stays_in_week_nights.
•	is_family = flag if booking includes children or babies.
5. Encoding & Data Types
•	Applied One-Hot Encoding for low-cardinality categorical features (e.g., meal, market_segment).
•	Grouped infrequent countries into "Other".
•	Converted date columns to proper datetime format.
6. Removing Data Leakage
•	Dropped reservation_status and reservation_status_date (not available at prediction time).
7. Final Dataset Preparation
•	Dropped exact duplicate rows.
•	Split into train/test sets with test_size=0.2, random_state=42.


•	Tools & Libraries
o	Python
o	Pandas, NumPy → Data wrangling
o	Matplotlib, Seaborn → Visualization
o	Scikit-learn → Preprocessing & splitting

