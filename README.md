#  📊 Comparison-of-SQL-and-Python-Pandas-

#SQL vs Python (Pandas) – Data Analysis Comparison

This project demonstrates how to perform common data analysis operations using both **SQL** and **Python (Pandas)**. The goal is to understand the similarities and differences in syntax and logic when working with structured datasets.

---

## 📁 Dataset Used

The analysis was performed on a sample dataset `dataset_1.csv` containing information such as:
- `passenger`
- `destination`
- `weather`
- `temperature`
- `coupon`
- `occupation`
- `time`

Additional dataframes `df1` and `df2` were used for UNION and JOIN operations.

---

## 🔍 Objective

To compare **commonly used SQL operations** with their **Python Pandas equivalents**, including:
- Selection
- Filtering
- Sorting
- Aggregation
- Grouping
- Joining
- Text matching (LIKE)
- Range filtering (BETWEEN, IN)

---

## 🛠️ Technologies Used

- **Python 3.x**
- **Pandas**
- **Jupyter Notebook / VS Code**
- **SQL (conceptual reference)**

---

## ✅ SQL vs Python (Pandas) Comparison Table

| Operation                  | SQL Query Example                                             | Python (Pandas) Equivalent                             |
|---------------------------|---------------------------------------------------------------|--------------------------------------------------------|
| Select All Rows           | `SELECT * FROM dataset_1`                                     | `df` or `df.head()`                                    |
| Select Specific Columns   | `SELECT weather, temperature FROM dataset_1`                  | `df[['weather', 'temperature']]`                       |
| Unique Values             | `SELECT DISTINCT passenger FROM dataset_1`                    | `df['passenger'].unique()`                             |
| Filtering Rows (WHERE)    | `WHERE destination = 'Home'`                                  | `df[df['destination'] == 'Home']`                      |
| Sorting (ORDER BY)        | `ORDER BY coupon`                                             | `df.sort_values('coupon')`                             |
| Rename Columns (AS)       | `SELECT destination AS Destination`                           | `df.rename(columns={'destination': 'Destination'})`    |
| Group By & Aggregation    | `GROUP BY weather, AVG(temperature)`                          | `df.groupby('weather')['temperature'].mean()`          |
| Count                     | `COUNT(*)`                                                    | `df['column'].count()` or `df.groupby(...).size()`     |
| Sum, Min, Max             | `SUM(column)`                                                 | `.sum()`, `.min()`, `.max()`                           |
| Count Distinct            | `COUNT(DISTINCT column)`                                      | `.nunique()`                                           |
| HAVING Clause             | `HAVING occupation = 'Student'`                               | `groupby().filter(lambda x: x['occupation'].iloc[0]=='Student')` |
| UNION                     | `UNION ALL / DISTINCT`                                        | `pd.concat([df1, df2]).drop_duplicates()`              |
| JOIN                      | `INNER JOIN ON a.time = b.time`                               | `pd.merge(df, df2, on='time', how='inner')`            |
| LIKE                      | `WHERE weather LIKE 'Sun%'`                                   | `df[df['weather'].str.startswith('Sun')]`              |
| BETWEEN                   | `WHERE temperature BETWEEN 29 AND 75`                         | `df[(df['temperature'] >= 29) & (df['temperature'] <= 75)]` |
| IN Clause                 | `WHERE occupation IN ('Sales', 'Management')`                 | `df[df['occupation'].isin(['Sales', 'Management'])]`   |

---

## 📌 Key Takeaways

- Most SQL queries have **direct equivalents** in Pandas.
- Pandas syntax is often more **flexible** for complex chaining and analysis.
- This project helps understand **how SQL logic translates into Python code**, which is essential for Data Analysts working across multiple tools.

---


---

## 📚 Skills Gained

- Data filtering, aggregation, and transformation in both SQL & Pandas
- Data joining and merging
- Writing efficient and readable data manipulation code in Python
- Understanding SQL logic for real-world datasets

---


