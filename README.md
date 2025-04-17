TASK 7: Get Basic Sales Summary from a Tiny SQLite Database using Python

Objective
The objective of this task is to extract basic sales information such as total quantity sold and total revenue from a simple SQLite database using SQL within Python. The results are displayed using print statements and a basic bar chart.

Tools Used
Python with sqlite3, pandas, and matplotlib
SQLite (no installation required, built-in with Python)
Jupyter Notebook 

Dataset
A small SQLite database file named sales_data.db is created. It contains a single table named sales with sample records for product sales.

Task Workflow

Connect to the SQLite database using Python

Run simple SQL queries to summarize sales data

Load query results into a pandas DataFrame

Display summary output using print statements

Create a basic bar chart for revenue by product

Save the bar chart as an image if required

Key Code Snippets
Connect to database
import sqlite3
conn = sqlite3.connect("sales_data.db")

Run SQL query
query = "SELECT product, SUM(quantity) AS total_qty, SUM(quantity * price) AS revenue FROM sales GROUP BY product"

Load into pandas
import pandas as pd
df = pd.read_sql_query(query, conn)

Display and plot
print(df)
df.plot(kind='bar', x='product', y='revenue')

Save the chart
plt.savefig("sales_chart.png")

Outcome
This task helps in understanding how to use basic SQL inside Python, retrieve and analyze data, and create visual summaries using bar charts. It also reinforces working with pandas and matplotlib for data presentation
