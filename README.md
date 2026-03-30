# Data_cleaning_python_cheatsheet
---

## 🧹 Data Cleaning in Python – Cheat Sheet

This repository contains a quick and practical cheat sheet for **data cleaning using Pandas and NumPy**. It covers the most commonly used techniques required for preparing raw data for analysis and machine learning.

---

## 📌 Why Data Cleaning?

Real-world data is often:

* Incomplete
* Inconsistent
* Noisy

Data cleaning helps in:

* Improving data quality
* Ensuring accurate analysis
* Enhancing model performance

---

## 🔧 Key Steps Covered

### 1. Handling Missing Values

```python
df.isnull().sum()
df.fillna(method='ffill')
df.dropna()
```

---

### 2. Removing Duplicates

```python
df.drop_duplicates(inplace=True)
```

---

### 3. Renaming Columns

```python
df.columns = df.columns.str.lower().str.replace(" ", "_")
```

---

### 4. Changing Data Types

```python
df['date'] = pd.to_datetime(df['date'])
df['age'] = df['age'].astype(int)
```

---

### 5. Filtering Data

```python
df = df[df['age'] > 18]
```

---

### 6. Handling Outliers

```python
df = df[df['salary'] < df['salary'].quantile(0.95)]
```

---

### 7. Standardizing String Values

```python
df['name'] = df['name'].str.lower().str.strip()
```

---

### 8. Removing Unnecessary Columns

```python
df.drop(['unnamed: 0'], axis=1, inplace=True)
```

---

### 9. Value Replacement

```python
df['col'] = df['col'].replace({'A': 'Alpha'})
```

---

### 10. Resetting Index

```python
df.reset_index(drop=True, inplace=True)
```

---

## 🚀 Tools Used

* Python
* Pandas
* NumPy

---

## 📊 Use Cases

* Data Analysis
* Machine Learning Preprocessing
* Data Wrangling Tasks

---

## 💡 Conclusion

Data cleaning is a crucial step in any data workflow. A well-cleaned dataset leads to better insights and more reliable models.

---

## 🙌 Author

**Surya_Namburi**

---
