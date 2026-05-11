

**🚗 Car Data Analysis using Pandas**

**📌 Project Overview**

This project focuses on performing data analysis and data cleaning operations on a car dataset using Python and Pandas in Jupyter Notebook. The dataset contains information about different car models including their make, origin, engine specifications, mileage, weight, and other automobile-related attributes.

The main objective of this project is to understand how Pandas functions can be used for:

Data cleaning
Filtering
Value counting
Removing unwanted records
Applying functions on columns
Handling missing values

This project demonstrates practical implementation of Exploratory Data Analysis (EDA) techniques using Pandas.

**📂 Dataset Description**

The dataset contains details about various cars and includes the following features:

Make
Model
Type
Origin
DriveTrain
MSRP
Invoice
EngineSize
Cylinders
Horsepower
MPG_City
MPG_Highway
Weight
Wheelbase
Length

Each row represents information about a specific car model.

**🛠️ Technologies Used**
Python 🐍

Used as the programming language for performing data analysis.

Pandas 📊

**Used for:**

Data cleaning
Data manipulation
Filtering records
Statistical analysis
Jupyter Notebook

Used to execute Python code interactively and visualize outputs.

🔍 Pandas Functions Used
🔹 import pandas as pd

Used to import the Pandas library.

import pandas as pd
🔹 pd.read_csv()

Used to load the CSV dataset into the notebook.

df = pd.read_csv("Car Data.csv")
🔹 head()

Displays the first 5 rows of the dataset.

df.head()
🔹 shape

Shows the total number of rows and columns.

df.shape
🔹 isnull().sum()

Checks for missing values in each column.

df.isnull().sum()
🔹 fillna()

Used to replace missing values.

df['Cylinders'] = df['Cylinders'].fillna(df['Cylinders'].mean())
🔹 value_counts()

Shows unique values along with their occurrence count.

df['Make'].value_counts()
🔹 isin()

Filters records containing specific values.

df[df['Origin'].isin(['Asia','Europe'])]
🔹 apply()

Applies a function on dataframe columns.

df['MPG_City'] = df['MPG_City'].apply(lambda x:x+3)
📊 Tasks Performed in the Project

**✅ Q1) Data Cleaning**
Find all Null Values in the dataset and fill them with the mean value of that column.
Code Used:
df.isnull().sum()

df['Cylinders'] = df['Cylinders'].fillna(df['Cylinders'].mean())
Explanation:
Missing values were identified using isnull().sum()
Null values in numerical columns were replaced with the mean value
This improves dataset quality and prevents errors during analysis

**📊 Q2) Value Counts Analysis**
Check different types of car Make and count their occurrences.
Code Used:
df['Make'].value_counts()
Explanation:
Displays all unique car manufacturers
Shows how many times each make appears in the dataset
Helps identify the most common car brands

**📊 Q3) Filtering Records**
Show all records where Origin is Asia or Europe.
Code Used:
df[df['Origin'].isin(['Asia','Europe'])]
Explanation:
Filters the dataset based on specific regions
Displays only cars manufactured in Asia or Europe

**📊 Q4) Removing Unwanted Records**
Remove all records where Weight is above 4000.
Code Used:
df = df[df['Weight'] <= 4000]
Explanation:
Removes heavy vehicles from the dataset
Keeps only cars with weight less than or equal to 4000

**📊 Q5) Applying Function on Column**
Increase all values of MPG_City column by 3.
Code Used:
df['MPG_City'] = df['MPG_City'].apply(lambda x:x+3)

Explanation:
apply() function is used to modify column values
Increased city mileage values by 3 for all records
📌 Key Insights
✔️ Missing values can be handled effectively using Pandas.
✔️ Value counting helps analyze the frequency of different car brands.
✔️ Filtering operations simplify region-based analysis.
✔️ Unwanted records can be removed easily using conditional filtering.
✔️ Functions can be applied efficiently on dataframe columns using apply().

📁 Project Structure
├── Car Data Analysis.ipynb
├── Car Data.csv
├── README.md
🎯 Conclusion

This project demonstrates how Pandas can be used for real-world automobile data analysis and preprocessing. Various operations such as handling missing values, filtering records, removing unnecessary data, counting occurrences, and modifying column values were successfully performed.

The project helped in gaining practical knowledge of

Data Cleaning
Exploratory Data Analysis (EDA)
Data Manipulation using Pandas
Working with real-world datasets

Overall, this project provides a strong foundation in data analytics using Python and Pandas.
