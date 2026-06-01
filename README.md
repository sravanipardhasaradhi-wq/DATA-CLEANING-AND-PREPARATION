# TASK 2: DATA CLEANING AND PREPARATION

## PROJECT OVERVIEW
This project focuses on cleaning and preprocessing the Sample Superstore dataset using Python and the Pandas library. The objective was to identify missing values, remove duplicate records, convert data types, and export a cleaned dataset for further analysis.

---

## OBJECTIVE

* Load the dataset into a Python environment.
* Identify missing values.
* Remove duplicate records.
* Convert date columns into proper datetime format.
* Export the cleaned dataset into a new CSV file.

---

## DATASET USED
**Sample Superstore Dataset**
The dataset contains sales transactions including:
* Order ID
* Order Date
* Ship Date
* Customer Information
* Product Information
* Sales
* Quantity
* Discount
* Profit

Number of Columns: 21

---

## TOOLS AND TECHNOLOGIES

* Python
* Pandas
* Google Colab
* CSV Dataset

---

## DATA CLEANING STEPS

### 1. Loaded Dataset
Used Pandas to load the Sample Superstore dataset.

### 2. Missing Value Analysis
Checked all columns for missing values using:

```python
df.isnull().sum()
```

### 3. Duplicate Removal
Removed duplicate rows using:

```python
df.drop_duplicates()
```

### 4. Data Type Conversion
Converted Order Date and Ship Date columns from string format to datetime format.

### 5. Export Cleaned Dataset
Saved the cleaned dataset as:

```text
Cleaned_Superstore.csv
```

---

## PYTHON CODE

```python
import pandas as pd

df = pd.read_csv('Sample - Superstore.csv', encoding='latin1')

print(df.head())

print("\nMissing Values:")
print(df.isnull().sum())

df = df.drop_duplicates()

df['Order Date'] = pd.to_datetime(df['Order Date'], errors='coerce')
df['Ship Date'] = pd.to_datetime(df['Ship Date'], errors='coerce')

print("\nData Types:")
print(df.dtypes)

df.to_csv('Cleaned_Superstore.csv', index=False)

print("\nCleaned dataset saved successfully!")
```

---

## RESULTS

* Missing values identified successfully.
* Duplicate records removed.
* Date columns converted to datetime format.
* Cleaned dataset exported successfully.

---

## LEARNING OUTCOMES

* Data Cleaning using Pandas
* Handling Missing Values
* Removing Duplicate Records
* Data Type Conversion
* Exporting Cleaned Data

---

## AUTHOR

Lakshmi Sravani


