# Elevate-Labs-Intern
Data cleaning and Data Processing 


1) Data Cleaning Guide (Python + Google Colab)

Basic data cleaning tasks using Python and Pandas in Google Colab.
The steps include handling missing values, removing duplicates, standardizing text, formatting dates, renaming columns, and fixing data types.


2) SETUP INSTRUCTIONS

1. Open Google Colab.
2. Upload Diabetes dataset (CSV or Excel).


3) DATA CLEANING

Identify the missing values by using
df.isnull().sum()


4) DATA HANDLING (REMOVE DUPLICATES)

print(df.isnull().sum())
df = df.dropna()
df['Glucose'] = df['Glucose'].fillna(df['Glucose'].mean())
df = df.drop_duplicates()


5) RENAME COLUMN HEADERS

df.rename(columns={'BMI': 'Brain_Medicine_Injury'}, inplace=True)


6) CHECK AND FIX DATA TYPES

print(df.dtypes)

df['Glucose'] = df['Glucose'].astype(int)
df['BMI'] = df['BMI'].astype(float)


7) SAVE THE CLEANED DATA SET

save as a cleaned_data.csv
