# 🧬 DBMS Complete Repository | Case Studies + Lab Manual + Project with GUI 💉

Welcome to the **Database Management System (DBMS)** comprehensive repository.

This repository serves as an academic portfolio and complete documentation of:
- 🧠 Real-world case study exercises
- 🔍 DBMS lab practicals (SQL, PL/SQL, DDL/DML, TCL, Python integration)
- 💻 Full-fledged GUI project: **Blood Bank Management System** using MySQL + Python (Tkinter)

---

## 📁 Repository Contents

| File / Folder                     | Description |
|----------------------------------|-------------|
| `DBMS_CASE_STUDIES_PDF.pdf`      | Complete case study with ER modeling, relational schema, SQL design and 30+ complex queries |
| `DBMS_LAB_PRACTICAL.pdf`         | Full lab manual with step-by-step SQL, PL/SQL, W3Schools exercises, triggers, and DB connectivity |
| `Project_PDF.pdf`                | Blood Bank Management System – complete ERD, schema, data, security, and backend structure |
| `Project_PPT.pptx`               | Final project presentation (overview, need, implementation, live demo summary) |
| `Project_Python_code_PDF.pdf`    | Full backend GUI application logic in Python using Tkinter and MySQL |

---

## 📘 DBMS Case Study 

**📄 File:** `DBMS_CASE_STUDIES_PDF.pdf`

### 🧾 Description
A university exam management system designed using:
- Entity-Relationship diagrams
- Table creation scripts
- Data insertion
- More than 30 practice queries

### 🏗️ ERD Entities:
- **Exam**
- **Course**
- **Room**
- **Section**

### 🔐 Constraints:
- Primary Keys: `C_name`, `S_number`, `R_number`
- Foreign Keys: Proper references across tables

### 🧠 Example Queries:
```sql
-- List all rooms with capacity greater than 30 and in Building B
SELECT R_number FROM room WHERE Capacity > 30 AND Building = 'Building B';

-- Count total sections
SELECT COUNT(*) AS Total_Sections FROM section;

-- Update exam time
UPDATE exam SET time = '08:00:00' WHERE C_name = 'Operating System';
```
### 📊 Covered Topics

- ER Modeling  
- Table Normalization  
- Join Queries  
- Aggregates (SUM, COUNT, AVG)  
- Subqueries  
- LIKE, IN, BETWEEN  

---

# 🧪 DBMS Lab Manual (SQL + PL/SQL + MySQL Workbench)  
📄 **File:** `DBMS_LAB_PRACTICAL.pdf`  
This file is a complete hands-on guide to the DBMS syllabus, including **12 full lab exercises** with output screenshots and live code execution.

---

### 🔍 Labs Covered

| Lab No. | Topic                                     |
|--------:|-------------------------------------------|
| 1       | MySQL Server, Client, Workbench Setup     |
| 2       | Basic SQL Commands                        |
| 3       | DDL & DML (CREATE, INSERT)                |
| 4       | Data Manipulation & Aggregation           |
| 5       | W3Schools SQL Practice                    |
| 6       | Table Creation from W3 reference          |
| 7       | Complex Query Practice                    |
| 8       | Advanced SQL (GROUP BY, HAVING)           |
| 9       | PL/SQL Control Structures                 |
| 10      | Loops in PL/SQL                           |
| 11      | Transaction Control Language (TCL)        |
| 12      | Connecting Python + MySQL                 |

---

### 📌 Sample Code

```sql
-- Create Table
CREATE TABLE CUSTOMERS (
  CNAME VARCHAR2(19),
  CITY VARCHAR2(18)
);

-- Aggregate Query
SELECT COUNT(*) FROM CUSTOMERS;

-- PL/SQL Example
DECLARE
  counter NUMBER := 1;
BEGIN
  WHILE counter <= 10 LOOP
    DBMS_OUTPUT.PUT_LINE(counter);
    counter := counter + 1;
  END LOOP;
END;
```

# 💉 Major Project: Blood Bank Management System (End-Semester)

### 📄 Files

- `Project_PDF.pdf` – Complete backend structure and DB schema  
- `Project_PPT.pptx` – Project presentation  
- `Project_Python_code_PDF.pdf` – Python GUI application code  

---

### 🌐 Objective

Design and implement a complete **Blood Bank Management System** that:

- Tracks donors and patients  
- Connects hospitals and blood banks  
- Manages blood group inventory in real time  
- Provides secure user login and GUI  

---

### 🧬 Entities in ER Diagram

- **Donor**  
- **Patient**  
- **Blood_Bank**  
- **Hospital**  
- **Manager**  
- **Registration_Team**  
- **Blood_Bank_Available**  

---

### 🔗 Relationships

- **One-to-Many**:  
  - `Registration_Team → Donor`  
  - `Donor → Blood_Bank`  

- **Many-to-One**:  
  - `Patient → Hospital`  
  - `Donor → Registration_Team`  

- **Composite Primary Key**:  
  - `Blood_Bank_Available (b_id, blood_group)`  

---

### 🧾 Sample SQL Tables

```sql
CREATE TABLE Blood_Bank (
  b_id INT PRIMARY KEY,
  b_name VARCHAR(255),
  h_id INT,
  FOREIGN KEY (h_id) REFERENCES Hospital(h_id)
);

CREATE TABLE login (
  id INT PRIMARY KEY,
  username VARCHAR(50) UNIQUE NOT NULL,
  password VARCHAR(100) NOT NULL
);
```
# 🐍 Python GUI Integration (Tkinter + MySQL)

### 🔐 Key Features

- Login authentication (admin/user)  
- Display all tables from DB  
- Dynamic insert, delete, update, and view options  
- Automatic blood inventory adjustment  
- Real-time database connectivity  

---

### 📁 Highlights from `Project_Python_code_PDF.pdf`

```python
# Connect to MySQL
connection = mysql.connector.connect(
    host="localhost",
    user="root",
    password="*****",
    database="dbms_project"
)

# Insert into Donor table
def insert_record(...):
    query = "INSERT INTO Donor (...) VALUES (%s, ...)"
    cursor.execute(query, values)
    update_blood_bank_available(...)
```
### 🎨 GUI Features

- Full-screen main menu  
- Dropdowns for table selection  
- Separate windows for each CRUD operation  
- Easy-to-use interface for staff and users  

---

### 📽️ Presentation Summary

📊 `Project_PPT.pptx` includes:

- Purpose of DBMS-based blood bank  
- Public health significance  
- State-level use cases and dynamic stock tracking  
- Live demo screenshots of the GUI  
- Backend table samples with sample queries  

---

### 👩‍💻 Authors

> 👨‍💻 **Kaushal Ramoliya**  
> 🎓 B.Tech in Computer Science & Engineering  
> 📧 Email: [kaushalramoliya17@gmail.com](mailto:kaushalramoliya17@gmail.com)  
> 🌐 LinkedIn: [linkedin.com/in/kaushalramoliya](https://www.linkedin.com/in/kaushalramoliya)  
> 💻 GitHub: [github.com/kaushalramoliya](https://github.com/Kaushalramoliya)


