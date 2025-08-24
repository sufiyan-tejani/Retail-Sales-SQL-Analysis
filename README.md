# Retail Sales & Customer Analysis (SQL Project)

## Project Overview
This project demonstrates SQL skills by analyzing a **retail/bookstore database**.  
It includes multiple tables (Customers, Orders, Books, Employees) to answer real-world business queries.

---

## Tools Used
- SQL (MySQL / PostgreSQL / SQL Server)
- CSV Datasets (Books, Customers, Orders, Employees)

---

## Project Files
- `Books.csv` → Book details  
- `Customers.csv` → Customer information  
- `Orders.csv` → Orders placed by customers  
- `Employee_data.csv` → Employee records  
- `Retail_Sales_Analysis.sql` → SQL queries for analysis  

---

## Key Analysis Performed
- Retrieve **top-selling books** and categories  
- Find **total revenue per customer**  
- Identify **high-value orders** and repeat customers  
- Analyze **employee sales performance**  
- Check **monthly/weekly sales trends**  

---

## Sample Queries
```sql
-- Total revenue by customer
SELECT c.customer_name, SUM(o.amount) AS total_spent
FROM Customers c
JOIN Orders o ON c.customer_id = o.customer_id
GROUP BY c.customer_name
ORDER BY total_spent DESC;
