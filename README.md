# SQL Retail & Sales Analysis — Data Technician Bootcamp

## Project Overview
This repository contains SQL practical work completed during **Week 3 of a Data Technician Bootcamp: Databases and SQL**. The project focused on designing a simple relational database and writing SQL queries to analyse retail and sales data using the **Northwind Traders** database in **Supabase**.

The work demonstrates how SQL can be used to retrieve, filter, sort, aggregate, and join data from related tables to answer real business questions about customers, products, orders, suppliers, categories, and employees.

## Tools & Technologies
- **SQL**
- **PostgreSQL / Supabase**
- **Northwind Traders** retail and sales dataset
- **World** database for additional SQL practice
- Relational database design concepts

## Skills Demonstrated

### Querying and Filtering
- `SELECT` to retrieve all columns or specific columns
- `WHERE` with comparison operators
- `IN`, `BETWEEN`, and `LIKE`
- `DISTINCT` to remove duplicate values
- Column aliases for readable output

### Sorting and Limiting Results
- `ORDER BY` ascending and descending
- `LIMIT` and `OFFSET` for paginated results

### Aggregation and Grouping
- `GROUP BY` to summarise data
- `COUNT`, `SUM`, `MIN`, and `MAX`
- Aggregated reports by category, product, country, and population

### Joining Tables
- `INNER JOIN` / `JOIN` to combine related tables
- Understanding of `LEFT`, `RIGHT`, `FULL`, and `CROSS` JOIN concepts
- Multi-table joins across products, categories, suppliers, orders, customers, and employees

### Relational Database Design
- Identified primary keys and foreign keys
- Designed tables for learners, courses, instructors, and enrolments
- Compared relational and non-relational database use cases

## Retail and Sales Analysis Highlights
Using the Northwind retail dataset, queries were written to:

- Retrieve full customer data and targeted customer names and cities for marketing
- Identify unique cities for delivery network expansion
- Filter high-value and mid-range products by price
- Analyse recent orders and 1996 order activity
- Join products with suppliers and categories to classify inventory
- Produce complete order overviews with customer and employee details
- Count products per category
- Calculate sales volume by product and price
- Build supply chain reports showing product, category, and supplier information

<img width="608" height="691" alt="image" src="https://github.com/user-attachments/assets/c98b0a3e-3f63-4a39-a87a-fafa43fbe06e" />


## Example Query
```sql
SELECT p.productname,
       p.price,
       SUM(od.quantity) AS total_quantity
FROM order_details od
JOIN products p ON od.productid = p.productid
GROUP BY p.productname, p.price
ORDER BY total_quantity DESC;
```

This query demonstrates `JOIN`, `GROUP BY`, `SUM`, aliases, and `ORDER BY` to analyse product sales volume.

## Key Insights Supported
- Customer distribution by city and country for marketing and logistics
- Product pricing tiers for inventory and promotional planning
- Category and supplier product coverage
- Order activity by customer, employee, and date
- Sales volume by product and price
- Product counts by category for range management

## Additional Practice
The project also included SQL practice against the **World** database, using filters, `LIKE`, `ORDER BY`, `LIMIT/OFFSET`, and aggregate functions to analyse cities, countries, populations, and capital cities.

## Learning Outcomes
- Wrote SQL queries to answer real-world business questions
- Applied `SELECT`, `WHERE`, `ORDER BY`, `GROUP BY`, and `JOIN` to retail and sales data
- Understood how primary and foreign keys link related tables
- Practised running queries in Supabase and interpreting results
- Built confidence in using SQL for reporting and data analysis
