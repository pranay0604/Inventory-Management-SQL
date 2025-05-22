# 📦 Inventory Management System Database

## 📘 Project Description

This project implements a simple Inventory Management System database using SQL. It is designed to manage products, suppliers, and inventory transactions, enabling users to perform basic **CRUD** (Create, Read, Update, Delete) operations efficiently. The system provides functionality to track inventory levels, product details, and supplier information.

---

## 🧱 Database Structure

### 1. **Products Table**
Stores information about products including name, description, price, and quantity.

| Column Name     | Data Type      | Description                   |
|-----------------|----------------|-------------------------------|
| product_id      | INT (PK)       | Unique product identifier     |
| name            | VARCHAR(100)   | Name of the product           |
| description     | TEXT           | Description of the product    |
| price           | DECIMAL(10,2)  | Price of the product          |
| quantity        | INT            | Available quantity in stock   |

---

### 2. **Suppliers Table**
Contains information about suppliers such as name and contact details.

| Column Name     | Data Type      | Description                   |
|-----------------|----------------|-------------------------------|
| supplier_id     | INT (PK)       | Unique supplier identifier    |
| name            | VARCHAR(100)   | Supplier name                 |
| contact_info    | VARCHAR(150)   | Email or phone                |

---

### 3. **Inventory Transactions Table**
Tracks inventory movements (purchases or sales).

| Column Name     | Data Type      | Description                           |
|-----------------|----------------|---------------------------------------|
| transaction_id  | INT (PK)       | Unique transaction ID                 |
| product_id      | INT (FK)       | Linked product ID                     |
| transaction_type| VARCHAR(10)    | 'purchase' or 'sale'                  |
| quantity        | INT            | Quantity moved                        |
| transaction_date| DATE           | Date of transaction                   |

---

## 🛠️ SQL Tasks Performed

- ✅ Created tables with relationships and constraints
- ✅ Inserted sample records for products, suppliers, and transactions
- ✅ Performed **CRUD** operations with SQL queries
- ✅ Implemented **filters and sorting** on queries (e.g., by price, date)
- ✅ Joined tables to retrieve detailed inventory information

---

## 🔍 Sample SQL Queries

### Insert a new product:
```sql
INSERT INTO Products (name, description, price, quantity)
VALUES ('Wireless Mouse', 'Ergonomic design with USB receiver', 599.99, 100);
