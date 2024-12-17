# SQL
SQL Basics for Beginners: Must-Know Concepts

## What is SQL?  
   SQL (Structured Query Language) is a standard language used to communicate with databases. It allows you to query, update, and manage relational databases by writing simple or complex queries.

## SQL Syntax  
   SQL is written using statements, which consist of keywords like SELECT, FROM, WHERE, etc., to perform operations on the data.
   - SQL keywords are not case-sensitive, but it's common to write them in uppercase (e.g., SELECT, FROM).

## SQL Data Types  
   Databases store data in different formats. The most common data types are:
   - INT (Integer): For whole numbers.
   - VARCHAR(n) or TEXT: For storing text data.
   - DATE: For dates.
   - DECIMAL: For precise decimal values, often used in financial calculations.

## Basic SQL Queries  
   Here are some fundamental SQL operations:

   - SELECT Statement: Used to retrieve data from a database.
    
  Example
     SELECT column1, column2 FROM table_name;
     
   - WHERE Clause: Filters data based on conditions.

Example
     SELECT * FROM table_name WHERE condition;
     
   - ORDER BY: Sorts data in ascending (ASC) or descending (DESC) order.
    
Example
      SELECT column1, column2 FROM table_name ORDER BY column1 ASC;
     
   - LIMIT: Limits the number of rows returned.
    
 Example
     SELECT * FROM table_name LIMIT 5;
     
## Filtering Data with WHERE Clause  
   The WHERE clause helps you filter data based on a condition:
  
Example

   SELECT * FROM employees WHERE salary > 50000;
   
   You can use comparison operators like:
   - =: Equal to
   - >: Greater than
   - <: Less than
   - LIKE: For pattern matching

## Aggregating Data  
   SQL provides functions to summarize or aggregate data:
   - COUNT(): Counts the number of rows.

Example

     SELECT COUNT(*) FROM table_name;
     
   - SUM(): Adds up values in a column.
    
Example
    SELECT SUM(salary) FROM employees;
     
   - AVG(): Calculates the average value.
    
Example
     SELECT AVG(salary) FROM employees;
     
   - GROUP BY: Groups rows that have the same values into summary rows.
    
Example
     SELECT department, AVG(salary) FROM employees GROUP BY department;
     
## Joins in SQL  
   Joins combine data from two or more tables:
   - INNER JOIN: Retrieves records with matching values in both tables.
    
Example
     SELECT employees.name, departments.department
     FROM employees
     INNER JOIN departments
     ON employees.department_id = departments.id;
     
   - LEFT JOIN: Retrieves all records from the left table and matched records from the right table.

Example
     SELECT employees.name, departments.department
     FROM employees
     LEFT JOIN departments
     ON employees.department_id = departments.id;
     
## Inserting Data
   To add new data to a table, you use the INSERT INTO statement:
  
Example
   INSERT INTO employees (name, position, salary) VALUES ('John Doe', 'Analyst', 60000);
   
## Updating Data
   You can update existing data in a table using the UPDATE statement:
  
   UPDATE employees SET salary = 65000 WHERE name = 'John Doe';
   
## Deleting Data
    To remove data from a table, use the DELETE statement:
   
    DELETE FROM employees WHERE name = 'John Doe';
    
