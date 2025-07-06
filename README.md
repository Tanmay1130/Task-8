# 📦 Task 8: Stored Procedures and Functions

This task demonstrates how to create **reusable SQL blocks** using **stored procedures** and **user-defined functions** in MySQL.

---

## 🎯 Objective

- Modularize SQL logic
- Reuse logic across queries
- Improve maintainability and consistency

---

## 🛠️ Tools

- ✅ MySQL Workbench (recommended)
- ❌ SQLite (limited support)

---

## 📋 Deliverables

- [x] One `CREATE PROCEDURE`: `BorrowBook`
- [x] One `CREATE FUNCTION`: `CalculateFine`
- [x] One additional procedure: `ListOverdueBooks`
- [x] Sample usage for all

---

## 🧠 Hints / Guide

- Use parameters, `DECLARE`, `IF`, and `SELECT INTO`
- Use `CALL procedure()` or apply function in `SELECT` or `INSERT`
- For overdue books: check if `due_date < CURDATE()` and no matching return

---

## 🧪 Sample Usage

```sql
-- 1. Borrow a book
CALL BorrowBook(1, 2, '2024-07-05', '2024-07-15');

-- 2. Calculate fine
SELECT CalculateFine('2024-07-10', '2024-07-14');

-- 3. List overdue books
CALL ListOverdueBooks();
