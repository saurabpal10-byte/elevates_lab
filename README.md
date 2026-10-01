# Elevate Labs - Data Analyst Internship

## Task 1: Data Cleaning and Preprocessing

### Objective

The objective of this task was to clean and preprocess a raw customer dataset by identifying and handling missing values, duplicate records, inconsistent formatting, incorrect data types, invalid values, and potential outliers.

## Dataset

**Dataset:** Customer Personality Analysis

**File:** `marketing_campaign_raw.csv`

The dataset contains customer demographic information, purchasing behavior, campaign responses, and other customer-related attributes.

## Tools Used

- Python
- Pandas
- NumPy
- Google Colab
- GitHub

## Data Cleaning Steps

The following steps were performed:

1. Loaded the raw dataset using Pandas.
2. Inspected the dataset structure, dimensions, and data types.
3. Checked for missing values.
4. Identified 24 missing values in the `Income` column.
5. Filled missing `Income` values using the median value of `51,381.5`.
6. Checked for duplicate rows.
7. Checked for duplicate customer IDs.
8. Standardized column names using lowercase letters and underscores.
9. Removed unnecessary whitespace from text fields.
10. Inspected categorical variables such as `Education` and `Marital_Status`.
11. Converted `Dt_Customer` to the `datetime64[ns]` data type.
12. Validated numerical columns.
13. Checked for invalid negative values.
14. Identified potential `Income` outliers using the IQR method.
15. Investigated unusually old birth-year values.
16. Performed final data-quality validation.

## Data Quality Results

| Metric | Result |
|---|---:|
| Initial Rows | 2,240 |
| Initial Columns | 29 |
| Missing Income Values | 24 |
| Missing Values After Cleaning | 0 |
| Duplicate Rows | 0 |
| Duplicate Customer IDs | 0 |
| Invalid Dates | 0 |
| Final Rows | 2,240 |
| Final Columns | 29 |

## Outlier Check

Potential Income outliers were identified using the Interquartile Range (IQR) method.

The potential outliers were not automatically removed because an unusual value does not necessarily represent a data-entry error. Additional business context would be required before modifying or removing such observations.

## Birth Year Validation

The `Year_Birth` column was inspected for potentially unusual values. Some very old birth years were identified and investigated.

These records were retained because the dataset alone did not provide sufficient evidence to confirm that they were data-entry errors.

## Deliverables

- Google Colab notebook
- Raw dataset
- Cleaned dataset
- Screenshots
- Data-cleaning documentation

## Conclusion

The raw customer dataset was successfully cleaned and validated using Python and Pandas. Missing values, duplicates, formatting issues, date types, numerical data types, invalid values, potential outliers, and unusual birth-year values were investigated.

The resulting dataset contains **2,240 rows and 29 columns** and is ready for further analysis.
