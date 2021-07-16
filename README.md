# SQL_Basics

This is a short brief for SQL Basics. 

SQL is a standard language for accessing and manipulating databases.


SQL can execute queries against a database
SQL can retrieve data from a database
SQL can insert records in a database
SQL can update records in a database
SQL can delete records from a database
SQL can create new databases
SQL can create new tables in a database
SQL can create stored procedures in a database
SQL can create views in a database
SQL can set permissions on tables, procedures, and views


# RDBMS
RDBMS stands for Relational Database Management System.

RDBMS is the basis for SQL, and for all modern database systems such as MS SQL Server, IBM DB2, Oracle, MySQL, and Microsoft Access.

The data in RDBMS is stored in database objects called tables. A table is a collection of related data entries and it consists of columns and rows.


# SQL Statements

Most of the actions you need to perform on a database are done with SQL statements.

SELECT * FROM Customers;

The SELECT statement is used to select data from a database.

The data returned is stored in a result table, called the result-set.

### SELECT Column Example

SELECT CustomerName, City FROM Customers;

### The SQL SELECT DISTINCT Statement

The SELECT DISTINCT statement is used to return only distinct (different) values.

The following SQL statement selects only the DISTINCT values from the "Country" column in the "Customers" table:
SELECT DISTINCT Country FROM Customers;

The following SQL statement lists the number of different (distinct) customer countries (Here is the workaround for MS Access):
SELECT Count(*) AS DistinctCountries
FROM (SELECT DISTINCT Country FROM Customers);

###The SQL WHERE Clause
The WHERE clause is used to filter records.

It is used to extract only those records that fulfill a specified condition.

SELECT * FROM Customers
WHERE Country='Mexico';

SELECT * FROM Customers
WHERE CustomerID=1;

Select all records where the City column has the value "Berlin":
SELECT * FROM Customers
WHERE City  = "Berlin";

###The SQL AND, OR and NOT Operators

The WHERE clause can be combined with AND, OR, and NOT operators.

The AND and OR operators are used to filter records based on more than one condition:

The AND operator displays a record if all the conditions separated by AND are TRUE.
The OR operator displays a record if any of the conditions separated by OR is TRUE.
The NOT operator displays a record if the condition(s) is NOT TRUE.

Examples:

SELECT * FROM Customers
WHERE Country='Germany' AND City='Berlin';

SELECT * FROM Customers
WHERE Country='Germany' OR Country='Spain';

SELECT * FROM Customers
WHERE NOT Country='Germany';

Combining AND, OR, NOT:

SELECT * FROM Customers
WHERE Country='Germany' AND (City='Berlin' OR City='München');

SELECT * FROM Customers
WHERE NOT Country='Germany' AND NOT Country='USA';

###The SQL ORDER BY Keyword

The ORDER BY keyword is used to sort the result-set in ascending or descending order.

The ORDER BY keyword sorts the records in ascending order by default. To sort the records in descending order, use the DESC keyword.

SELECT * FROM Customers
ORDER BY Country;

SELECT * FROM Customers
ORDER BY Country DESC;


###The SQL INSERT INTO Statement

The INSERT INTO statement is used to insert new records in a table.

INSERT INTO Customers (CustomerName, ContactName, Address, City, PostalCode, Country)
VALUES ('Cardinal', 'Tom B. Erichsen', 'Skagen 21', 'Stavanger', '4006', 'Norway');

###The SQL UPDATE Statement

The UPDATE statement is used to modify the existing records in a table.

--*--

Inside a table, a column often contains many duplicate values; and sometimes you only want to list the different (distinct) values.

### Some of The Most Important SQL Commands

SELECT - extracts data from a database
UPDATE - updates data in a database
DELETE - deletes data from a database
INSERT INTO - inserts new data into a database
CREATE DATABASE - creates a new database
ALTER DATABASE - modifies a database
CREATE TABLE - creates a new table
ALTER TABLE - modifies a table
DROP TABLE - deletes a table
CREATE INDEX - creates an index (search key)
DROP INDEX - deletes an index

