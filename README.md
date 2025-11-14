# 📄 README -- Persons Database Dump

## 📌 Overview

This repository contains a MySQL database dump for a simple database
named **`persons`**.\
The dump includes the schema for a single table: **`person`**, which
stores basic information such as a person's name and birth year.

The dump was generated using **MySQL 8.0.44** on Windows (x86_64).

------------------------------------------------------------------------

## 🗂️ Database Details

### **Database Name**

`persons`

### **Table Included**

#### **`person`**

  Column    Type            Description
  --------- --------------- -------------------------------------------------
  `name`    `VARCHAR(30)`   Name of the person
  `BDATE`   `INT`           Numeric birth date value (likely year of birth)

No records are included in the dump---only the table structure.

------------------------------------------------------------------------

## 📥 How to Import This Dump

### **MySQL Command Line**

``` bash
mysql -u your_username -p persons < persons_person.sql
```

### **Using phpMyAdmin**

1.  Create a new database named **persons** (if it does not exist).
2.  Open the database.
3.  Go to the **Import** tab.
4.  Upload `persons_person.sql`.
5.  Click **Go**.

------------------------------------------------------------------------

## 🔧 Table Creation Script (Included in Dump)

``` sql
CREATE TABLE `person` (
  `name` varchar(30) DEFAULT NULL,
  `BDATE` int DEFAULT NULL
) ENGINE=InnoDB DEFAULT CHARSET=utf8mb4 COLLATE=utf8mb4_0900_ai_ci;
```

------------------------------------------------------------------------

## 📅 Dump Metadata

-   **Dump created on:** 2025-11-14\
-   **MySQL Version:** 8.0.44\
-   **Engine:** InnoDB\
-   **Character Set:** utf8mb4

------------------------------------------------------------------------

## 📚 Notes

-   The `BDATE` column stores an `INT`, which may represent a year
    (e.g., 1999). You may want to convert this into a proper `DATE` type
    if needed.
-   No sample data is included. Populate using:

``` sql
INSERT INTO person (name, BDATE) VALUES ('John Doe', 1990);
```
