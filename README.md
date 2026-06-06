# Data Analytics

## Task 1: Data Cleaning

### Overview
This task focuses on loading, inspecting, and cleaning the sales dataset ("Dataset for Data Analytics.xlsx") to prepare it for analysis.

### Steps 

#### 1. Load & Inspect the Dataset
- Loaded the dataset using "pandas" and "openpyxl".
- Checked the shape and previewed the first 10 rows.
- Used "df.info()" to examine column data types and non-null counts.

#### 2. Handle Missing Values
- Ran "df.isnull().sum()" to identify columns with null values.
- Found 309 missing values in the "CouponCode" column (25.75% of the dataset).
- Since coupon usage is optional, missing values were assumed as transactions where no coupon was applied.
- Missing values were filled with "No Coupon" to preserve all transaction records.

#### 3. Check for Duplicates
- Checked for full-row duplicates using "df.duplicated().sum()".
- Checked for duplicate "OrderID" values specifically.
- No duplicate records were found — no removal was required.

#### 4. Save Cleaned Dataset
- Exported the cleaned dataset to "cleaned_dataset.xlsx" (index excluded).

#### 5. Validation
- Re-confirmed zero null values across all columns.
- Re-confirmed zero duplicate "OrderID" values.
- Verified "Date" column format.
- Confirmed "CouponCode" missing count = 0.


### Output
cleaned_dataset.xlsx  Cleaned version of the original dataset |


### Key Findings
- The only column with missing data was "CouponCode" (25.75% missing).
- No duplicate rows or order IDs were present in the raw data.
- The dataset was clean and ready for analysis after filling the coupon nulls.
