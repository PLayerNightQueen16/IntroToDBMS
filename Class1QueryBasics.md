# Query Basics
## 📊 Why Structured Data Management Matters

### 🧩 The Problem with Flat Files (Excel/CSV)

When handling data from sources like **social media** or **delivery systems**, it’s common to store everything in Excel sheets or CSV files. While this works for small-scale use, it quickly becomes inefficient as data grows.

### 🚧 Key Challenges

* **Scalability Issues**
  Large datasets become slow and hard to manage

* **Data Inconsistency**
  Duplicate or mismatched data across files

* **Poor Data Integrity**
  No relationships or constraints between data

* **Collaboration Problems**
  Difficult for multiple users to work simultaneously

---

## 💡 The Need for Structured Data Management

A **DBMS (Database Management System)** helps organize, store, and retrieve data efficiently.

### ✅ Benefits

* Structured storage using tables and relationships
* Data consistency through constraints
* Fast querying using SQL
* Handles large-scale data easily
* Supports multiple users

---

## 🗂️ When & Why Different DBMS Are Used

* **Relational DBMS (MySQL, PostgreSQL)**
  Used when data is structured and relationships matter
  👉 Example: users, orders, transactions

* **NoSQL DBMS (MongoDB, Firebase)**
  Used for flexible or semi-structured data
  👉 Example: social media posts, real-time apps

* **In-Memory DB (Redis)**
  Used when speed is critical (caching, sessions)

### 🚀 Conclusion

Excel/CSV works for small tasks, but for real-world applications, a DBMS is essential for **scalability, consistency, and performance**.

---
## 🧠 Memory Hierarchy

Computers don’t treat all memory equally. Data flows through a **hierarchy of storage layers**, each designed to balance **speed, cost, and capacity**.

### ⚙️ How It Works

* **Hard Disk / SSD (Secondary Storage)**
  This is where all data is stored permanently.
  👉 Largest capacity, but **slowest access speed**

* **Main Memory (RAM)**
  Data and programs currently in use are loaded here from disk.
  👉 Faster than disk, but **temporary (volatile)**

* **CPU (Processing Unit)**
  All instructions are executed inside the CPU using tiny electronic components (transistors).
  👉 Extremely fast processing, handling roughly **10⁸–10⁹ operations per second**

### ⚡️ Key Idea

As we move **closer to the CPU**:

* Speed increases 🚀
* Size decreases 📉
* Cost per unit increases 💰

### 🧩 Why This Hierarchy Exists

If we stored everything in ultra-fast memory, it would be **too expensive**.
If we only used slow storage, performance would collapse.

So systems use a layered approach to get the **best of both worlds**.

### 🧠 In One Line

> Frequently used data stays closer to the CPU for speed, while bulk data stays farther away for cost efficiency.

---

## 🧪 Example Case: Managing Student Data

Let’s say we’re building a small app for **SST students**.

### 📌 Required Data

* Student ID
* Name
* Email ID
* Batch
* Contact Number

### 📈 How Data Storage Evolves

* **👥 10 Students**
  A simple notebook works fine
  👉 Easy to read and manage manually

* **📄 500 Students**
  Move to an Excel/CSV file
  👉 Better organization, basic sorting/filtering

* **🧠 10,000+ Students**
  Flat files start breaking down
  👉 Slow, messy, and hard to maintain

### 🚧 Challenges at Scale

At large scale, we need a system where:

* **🔍 Data is searchable**
  Quickly find any student record

* **🤝 Data is shareable**
  Multiple users can access and update simultaneously

* **✅ Data is consistent**
  No duplicates or conflicting entries

* **🔒 Data is secure**
  Access control for sensitive information

* **⚡️ Data is efficient**
  Fast retrieval and updates

* **🧩 Data is structured**
  Clear relationships and organization

### 💡 The Solution: DBMS

This is where a **Database Management System (DBMS)** comes in.

A DBMS allows us to:

* Store large amounts of data efficiently
* Enforce rules for accuracy and consistency
* Query data quickly using structured languages (like SQL)
* Support multiple users without conflicts

### 🚀 Conclusion

As data grows, simple storage methods stop being practical.
A DBMS becomes essential to ensure **performance, reliability, and scalability**.

---
## 🗂️ Types of DBMS

In this course, we focus on **SQL databases**, which are among the most widely used data management systems.

### 🧱 Common SQL Databases

* MySQL
* PostgreSQL
* Oracle Database

### ❓ What is a SQL Database?

A **SQL (Structured Query Language) database** is used to store and manage data using a structured format.

These databases are also called **Relational Databases (RDBMS)**.

### 🔗 Why “Relational”?

In a relational database:

* Data is stored in **tables** (rows and columns)
* Each table represents an **entity**
* Tables can be **connected (related)** to each other using keys

👉 Example:

* A `Students` table can be linked to a `Courses` table
* Relationships help avoid duplication and keep data organized

### 🧩 Attributes and Values

* **Attributes (Columns)**
  These define the properties of an entity and store values of the same type for every record (homogenous).
  👉 Example: `StudentID`, `Name`, `Email`, `Batch`

* **Values (Cell Data)**
  These are the actual data entries for each attribute
  👉 Example: `101`, `Shreya`, `shreya@email.com`, `2026`

* **Rows (Records/Tuples)**
  A complete set of values for one entity
  👉 One row = one student

### ⚡️ Key Features of SQL Databases

* **Structured Data** → Data follows a fixed schema
* **Relationships** → Tables are connected logically
* **Querying with SQL** → Easy to retrieve and manipulate data
* **Data Integrity** → Constraints ensure accuracy

### 🧠 In Simple Terms

> A SQL (relational) database organizes data into tables and links them together, making large datasets easy to manage, query, and maintain.

---
## 🧩 Schema

A **schema** defines the structure of a table in a database.

It specifies:

* **Columns (Attributes)**
  What fields exist in the table

* **Data Types**
  What kind of data each column can store (e.g., INT, VARCHAR, DATE)

* **Constraints (Rules)**
  Conditions applied to data to ensure accuracy and integrity

### 🔑 Common Constraints in a Schema

* **PRIMARY KEY**
  Uniquely identifies each row in a table
  👉 Cannot be NULL or duplicate

* **FOREIGN KEY**
  Creates a relationship between two tables
  👉 References a PRIMARY KEY in another table

* **NOT NULL**
  Ensures a column must have a value

* **UNIQUE**
  Prevents duplicate values in a column

* **DEFAULT**
  Assigns a default value if none is provided

* **CHECK**
  Ensures values satisfy a specific condition

* **AUTO INCREMENT**
  Automatically generates sequential values (commonly for IDs)


### 🧠 In Simple Terms

> A schema is the blueprint of a table that defines its columns, data types, and rules (like keys and constraints) to keep data organized and reliable.

---

## 🗄️ SQL Basics Cheat Sheet

A quick reference for the most commonly used SQL commands in this course.

### 🧭 Database Operations

#### 🔍 Show all databases

```sql
SHOW DATABASES;
```

#### ➕ Create a database

```sql
CREATE DATABASE database_name;
```

#### 📂 Use a database

```sql
USE database_name;
```

#### ❌ Delete a database

```sql
DROP DATABASE database_name;
```

### 🧱 Table Operations

#### 📋 Show all tables

```sql
SHOW TABLES;
```

#### 🏗️ Create a table

```sql
CREATE TABLE table_name (
    column1 datatype constraints,
    column2 datatype constraints,
    ...
);
```

#### 🔎 Describe table structure

```sql
DESC table_name;
```

#### ❌ Delete a table

```sql
DROP TABLE table_name;
```

### 📥 Insert Data

#### ➕ Insert values into table

```sql
INSERT INTO table_name (column1, column2, ...)
VALUES (value1, value2, ...);
```

### 🔍 Retrieve Data

#### 📄 Select all data

```sql
SELECT * FROM table_name;
```

#### 🎯 Select specific columns

```sql
SELECT column1, column2 FROM table_name;
```

### 🔎 WHERE Clause (Filtering Data)

Used to filter records based on conditions.

#### 📌 Basic syntax

```sql
SELECT * FROM table_name
WHERE condition;
```

#### 🔸 Examples

```sql
-- exact match
SELECT * FROM students
WHERE batch = 'B';

-- multiple conditions
SELECT * FROM students
WHERE batch = 'B' AND id > 10;

-- using OR
SELECT * FROM students
WHERE batch = 'A' OR batch = 'B';
```

#### 🔸 Common Operators

* `=` equal to
* `!=` or `<>` not equal to
* `>` greater than
* `<` less than
* `>=` greater than or equal
* `<=` less than or equal

#### ⚡️ Conditions inside WHERE

#### 🔹 BETWEEN (range)

```sql
SELECT * FROM students
WHERE id BETWEEN 10 AND 20;
```

#### 🔹 LIKE (pattern matching)

```sql
-- starts with 'S'
SELECT * FROM students
WHERE name LIKE 'S%';

-- ends with 'a'
SELECT * FROM students
WHERE name LIKE '%a';

-- contains 'rey'
SELECT * FROM students
WHERE name LIKE '%rey%';
```

#### 🔹 IN (multiple values)

```sql
SELECT * FROM students
WHERE batch IN ('A', 'B', 'C');
```

#### 🔹 AND / OR

```sql
SELECT * FROM students
WHERE batch = 'B' AND id > 10;

SELECT * FROM students
WHERE batch = 'A' OR batch = 'C';
```

### ✏️ Update Data

#### 🔄 Update existing records

```sql
UPDATE table_name
SET column1 = value1
WHERE condition;
```

### ❌ Delete Data

#### 🗑️ Delete specific records

```sql
DELETE FROM table_name
WHERE condition;
```

### ⚡️ Useful Extras

#### 🔑 Create table with primary key

```sql
CREATE TABLE students (
    id INT PRIMARY KEY,
    name VARCHAR(100) NOT NULL
);
```

#### 🔁 Auto increment ID

```sql
id INT AUTO_INCREMENT PRIMARY KEY
```

### 🧠 Quick Tips

* SQL keywords are **case-insensitive** (`SELECT` = `select`)
* Always end statements with `;`
* Use `WHERE` to avoid updating/deleting all rows
* Avoid trailing commas in queries

### 🚀 In One Line

> SQL lets you create, manage, and query structured data efficiently using simple, readable commands.

---