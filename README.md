# 🚢 Titanic Data Analysis using Python

## 📌 Project Overview

This project focuses on analyzing the Titanic dataset using Python. The objective was to perform data exploration, data cleaning, and data visualization to gain meaningful insights from the dataset.

---

## 🎯 Task Objectives

* Analyze a given CSV dataset.
* Perform basic data exploration and preprocessing.
* Create and present 3 meaningful visualizations with insights.

---

## 📂 Dataset

**Dataset Used:** Titanic.csv

The Titanic dataset contains passenger information such as age, gender, passenger class, fare, and survival status.

---

## 🛠️ Tools & Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Jupyter Notebook

---

## 🔍 Data Exploration

The dataset was loaded using Pandas and explored to understand its structure.

### Steps Performed

```python
import pandas as pd

df = pd.read_csv("Titanic.csv")

print(df.head())
print(df.info())
print(df.describe())
print(df.isnull().sum())
```

The following checks were performed:

* Number of rows and columns
* Data types of columns
* Missing values
* Basic statistical summary

---

## 🧹 Data Cleaning & Preprocessing

### Handling Missing Values

```python
df["Age"].fillna(df["Age"].median(), inplace=True)

df["Embarked"].fillna(df["Embarked"].mode()[0], inplace=True)
```

### Removing Duplicate Records

```python
df.drop_duplicates(inplace=True)
```

### Verifying Missing Values

```python
print(df.isnull().sum())
```

---

## 📊 Data Visualizations

### 1️⃣ Survival Distribution

```python
import matplotlib.pyplot as plt
import seaborn as sns

sns.countplot(x="Survived", data=df)
plt.title("Survival Distribution")
plt.show()
```

### Insight

* More passengers died than survived.
* Survival rate was lower than the mortality rate.

---

### 2️⃣ Gender Distribution

```python
sns.countplot(x="Sex", data=df)
plt.title("Gender Distribution")
plt.show()
```

### Insight

* Male passengers were more than female passengers.
* The dataset shows a noticeable gender imbalance.

---

### 3️⃣ Passenger Class Distribution

```python
sns.countplot(x="Pclass", data=df)
plt.title("Passenger Class Distribution")
plt.show()
```

### Insight

* Most passengers traveled in Third Class.
* First Class had the smallest number of passengers.

---

## 📈 Key Findings

* The majority of passengers did not survive.
* Male passengers outnumbered female passengers.
* Third Class contained the highest number of passengers.
* Data cleaning improved dataset quality for analysis.

---

## 🎓 What I Learned

Through this project, I learned:

* How to load CSV datasets using Pandas.
* How to explore and understand datasets.
* How to identify and handle missing values.
* How to remove duplicate records.
* How to create visualizations using Matplotlib and Seaborn.
* How to derive meaningful insights from data.

---

## 📁 Project Structure

```text
Titanic-Data-Analysis/
│
├── Titanic.csv
├── task 1 completed.ipynb
├── README.md
├── survival_distribution.png
├── gender_distribution.png
└── passenger_class_distribution.png
```

---

## 📷 Visualization Outputs

### Survival Distribution

![Survival Distribution](survival_distribution.png)

### Gender Distribution

![Gender Distribution](gender_distribution.png)

### Passenger Class Distribution

![Passenger Class Distribution](passenger_class_distribution.png)

---

## ✅ Conclusion

This project provided hands-on experience with the complete data analysis workflow, including data exploration, preprocessing, and visualization. It strengthened my understanding of Python-based data analysis and helped me gain practical experience working with real-world datasets.

---

## 👨‍💻 Author

**Deep Dnath**

BBA Student | Aspiring Data Analyst

Currently Learning:

* Python
* SQL
* Power BI
* Data Analytics
