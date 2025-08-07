# Tokyo Olympic Data Engineering Project 🏅
This project is a personal data engineering and analytics exercise using Python and Pandas. This project aims to recreate the @darshilparmar Tokyo Olympic Data Engineering project using Pandas instead of PySpark.  
The goal is to transform, clean, and analyse the Tokyo 2020 Olympic datasets to generate meaningful insights on medal distribution, gender participation, and national performance.

## 🧠 Objectives

- Practice data cleaning, merging, filtering, and aggregation in Pandas.
- Extract insights from Olympic data such as athlete distribution, medal efficiency, and gender disparities.
- Use best practices for structuring data projects.

 ## 📁 Dataset Overview

Five datasets were used, each representing a dimension of Olympic participation:

| Table         | Description                                         |
|---------------|-----------------------------------------------------|
| `Athletes`    | (PersonName, Country, Discipline)                   |
| `Coaches`     | (Name, Country, Discipline, Event)                  |
| `EntriesGender` | (Discipline, Female, Male, Total)                |
| `Medals`      | (Rank, TeamCountry, Gold, Silver, Bronze, Total, Rank by Total) |
| `Teams`       | (TeamName, Discipline, Country, Event)              |


## 🛠️ Key Tasks Completed

1. Load and inspect all datasets.
2. Clean and normalise column names and values.
3. Join tables using multiple columns (`merge` on `Country` and `Discipline`).
4. Calculate the medal-per-athlete ratio by country.
5. Rank countries based on total medals.
6. Analyse gender ratios and disparities in disciplines.

## 🧮 Key Steps & Logic

- 🔹 **Loaded all 5 datasets** into Pandas from CSV files using appropriate encoding (`ISO-8859-1`).
- 🔹 **Checked for missing values and duplicate records** using `.isnull().sum()` and `.duplicated().sum()` to ensure data integrity.
- 🔹 **Queried subsets** of data using the `.query()` method for clear and readable filtering.
- 🔹 **Performed joins** across multiple tables (e.g., matching Athletes with Teams or Countries) using `.merge()` on shared keys like `Country` and `Discipline`.
- 🔹 **Calculated participation ratios**, such as Female-to-Male ratios per sport, and used `.round(2)` to limit results to 2 decimal places.
- 🔹 **Created ranking columns** using `.rank(method='min')` to sort countries based on medal tallies.


## 📦 Technologies Used
- Python 3.10+
- Pandas
- Jupyter Notebook

  

