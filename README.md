---
# 🧹 Using SQL String Functions to Clean Data
This notebook demonstrates how to use SQL string functions to clean up and standardize text data in a relational database — specifically focusing on entries in the `Country_name` column of the `Access_to_Basic_Services` table in the `united_nations` MySQL database.

| ⚠️ Important: This notebook is intended to run locally and not on Google Colab, as it requires a connection to a local MySQL database.
---
## 🎯 Objectives
By the end of this notebook, you will be able to:

  - Identify and remove unwanted characters from text fields.
  
  - Trim unnecessary white spaces from strings.
  
  - Extract meaningful substrings based on character positions.
  
  - Use string functions like `TRIM()`, `POSITION()`, and `LEFT()`.
---
## 🧰 Tools & Setup
  - Database Engine: MySQL
  
  - Client Interface: MySQL Workbench or Jupyter Notebook with SQLAlchemy and `pymysql`
  
  - Table Used: `Access_to_Basic_Services`
---
## 🧪 Data Cleaning Example
The `Country_name` column may contain entries like:
```sql
"Kenya (East Africa)"
```
Using string functions, we extract just:
`"Kenya"`
To do this, we use:
```
SUBSTRING(Country_name, 1, LOCATE('(', Country_name) - 2)
```
This trims off the region inside the brackets and any trailing space.
---
## 🔌 Database Connection
Make sure your notebook is running on the same machine as your MySQL installation. You’ll connect using a string like this:
```sql
'mysql+pymysql://root:yourpassword@localhost:3306/united_nations'
```
---
## 📝 Usage
  1. Clone or download the notebook and the required database.
  
  2. Ensure your MySQL server is running.
  
  3. Run the notebook in Jupyter or another supported IDE.
  
  4. Review and clean the Country_name column using the string functions demonstrated.
---
## 📦 Requirements
  - Python ≥ 3.8
  
  - sqlalchemy
  
  - pymysql
  
  - MySQL Workbench or any MySQL database setup
  
  - `united_nations` database with `Access_to_Basic_Services` table
---
👨‍💻 Author
Developed by ExploreAI Academy

Adapted and enhanced by Ibrahim Ambale
---




