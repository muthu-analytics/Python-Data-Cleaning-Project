# Sales Data Cleaning Project

## Project Overview

This project demonstrates a complete data cleaning workflow using Python and Pandas. The goal was to identify data quality issues in a raw sales dataset and transform it into a clean, validated dataset suitable for analysis.

## Dataset

- Raw sales dataset
- 4,000 records
- 13 columns

## Problems Identified

- ✔ Duplicate rows
- ✔ Duplicate Transaction IDs
- ✔ Missing values
- ✔ Inconsistent category names
- ✔ Placeholder values like `"-"`, `"N/A"`, `"?"`
- ✔ Currency stored as text
- ✔ Incorrect data types
- ✔ Revenue mismatches
- ✔ Negative values
- ✔ Outliers
- ✔ Inconsistent date formats

## Data Cleaning Steps

1. Loaded and inspected the dataset
2. Standardized column names
3. Removed duplicate rows
4. Resolved duplicate Transaction IDs
5. Standardized text formatting
6. Corrected inconsistent category labels
7. Replaced placeholder values with nulls
8. Handled missing values
9. Converted numeric columns
10. Imputed missing numeric values using group medians
11. Standardized date formats
12. Removed negative values
13. Treated outliers using the IQR method
14. Recalculated Total Revenue
15. Validated all cleaned data
16. Exported the cleaned dataset

## Before → After

| Metric | Before | After |
|---|---|---|
| Rows | 4,000 raw | 3,786 validated |
| Duplicates | 59 exact + ID dupes | 0 |
| Category typos | "Cloths", "Cc", ... | Standardized |
| Junk placeholders | "-", "N/A", "Nan" | Converted to null |
| Unit_Price dtype | Text ("$1,250") | float64 |
| Missing Units/Price | 262 rows | 0 (0 fabricated) |
| Revenue mismatches | 402 unflagged | Reconciled |

## Tools Used

- Python
- Pandas
- NumPy
- Regular Expressions (`re`)
- Jupyter Notebook

## Project Outcome

- Started with 4,000 raw records.
- Removed duplicate records and resolved duplicate transaction IDs.
- Corrected inconsistent categories and data types.
- Recalculated 402 revenue mismatches.
- Produced a clean dataset with 3,786 validated records ready for analysis.

## Repository Structure

```
sales-data-cleaning/
├── README.md
├── data/
│   ├── raw/unclaimed_business_performance_dataset.csv
│   └── cleaned/cleaned_business_performance_dataset1.csv
├── notebook/
│   └── data_cleaning.ipynb
└── requirements.txt
```

## How to Run

1. Clone this repository
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
3. Open `notebook/data_cleaning.ipynb` in Jupyter Notebook or JupyterLab
4. Run all cells to reproduce the cleaning process

## requirements.txt

```
pandas
numpy
```
