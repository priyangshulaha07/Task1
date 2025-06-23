# 📚 Library Management Database System

This project is a simple SQL-based Library Management System. It helps manage books, library members, and the issue-return process of books using a relational database.

---

## 📌 Project Features

- Manage Members (Name, Email, Join Date)
- Manage Books (Title, Author, ISBN, Quantity)
- Track which member has borrowed which book
- Maintain issue and return dates

---

## 🛠 Tech Stack

- *Database*: MySQL
- *Tool*: MySQL Workbench
- *Diagram*: EER Diagram (generated from MySQL Workbench)

---

## 🗂 Tables Overview

### 1. Members
| Column     | Type        | Description          |
|------------|-------------|----------------------|
| MemberID   | INT (PK)    | Unique member ID     |
| Name       | VARCHAR(100)| Member's full name   |
| Email      | VARCHAR(100)| Member's email       |
| JoinDate   | DATE        | Membership start date|

### 2. Books
| Column     | Type        | Description         |
|------------|-------------|---------------------|
| BookID     | INT (PK)    | Unique book ID      |
| Title      | VARCHAR(100)| Book title          |
| Author     | VARCHAR(100)| Author name         |
| ISBN       | VARCHAR(20) | ISBN number         |
| Publisher  | VARCHAR(100)| Publisher name      |
| Quantity   | INT         | Available copies    |

### 3. IssuedBooks
| Column     | Type        | Description                  |
|------------|-------------|------------------------------|
| IssueID    | INT (PK)    | Unique issue ID              |
| MemberID   | INT (FK)    | Linked to Members(MemberID)  |
| BookID     | INT (FK)    | Linked to Books(BookID)      |
| IssueDate  | DATE        | Date when book was issued    |
| ReturnDate | DATE        | Date when book was returned  |

---

## 🖼 ER Diagram

The EER Diagram (ERD) visually represents table relationships and keys.  
📎 File: Library_ER_Diagram.png

---

## 📜 SQL Schema

The SQL file contains table definitions with primary keys, foreign keys, and constraints.  
📎 File: create_schema.sql

---

## 🚀 How to Run

1. Open *MySQL Workbench*
2. Connect to your local MySQL server
3. Open create_schema.sql
4. Execute the script to create the database and tables
5. Use the diagram or queries to start inserting and managing data

---

## 🔗 Submission

This project is submitted as part of the *SQL Developer Internship Task 1*.
