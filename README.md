# Library-Application
# Project Overview
This project involves building a backend SQLite database for a Library application using Python. It manages core entities such as Users, Addresses, Books, Checkouts, Reviews, and Logs. The system utilizes Python’s sqlite3 library for database operations and pandas for data analysis and manipulation. The project demonstrates complete database functionality-schema creation, data insertion, query execution, and automated logging via SQL triggers.

---

### 🧩 Description of the Operation of Program’s Module

The operation of my program module involves several steps interacting with an SQLite database and using Python with the `sqlite3` and `pandas` libraries to perform tasks related to a library database system. Here's a breakdown:


#### 🔗 SQLite Database Connection  
🔹 The program starts by connecting to the SQLite database (`LibraryDatabase.db`)  
🔹 It queries the database to check the existing tables  

---

#### 🗂️ Database Table Creation  
🔹 If the tables exist, they are dropped  
🔹 The program creates new tables (`Users`, `Addresses`, `Books`, `Checkouts`, `Reviews`, `Logs`) if they don't already exist  
🔹 Each table is defined with specific columns and relationships, using foreign keys to link the tables  

---

#### 📝 Inserting Data  
🔹 Data is inserted into the tables: `Users`, `Addresses`, `Books`, `Checkouts`, and `Reviews`  
🔹 This data is manually defined in the program and inserted using `executemany()` for bulk inserts  

---

#### 📌 Logging and Triggers  
🔹 The `Logs` table is created to track checkout operations  
🔹 A trigger (`log_checkout`) is created to automatically insert a record into the `Logs` table after each new checkout  
🔹 After a test checkout is added, the program retrieves and displays all records from the `Logs` table  

---

#### 🔍 SQL Queries  
🔹 📚 Books checked out by 'John Smith'  
🔹 🧑‍💼 Reviewers for a specific book ('My Third SQL book')  
🔹 🚫 Users who have not checked out any books  
🔹 🧾 Records in the `Logs` table  

---

#### 📊 Using Pandas  
🔹 The program uses `pandas` to load the `Logs` table data into a DataFrame using `pd.read_sql_query()`  
🔹 This provides an easy-to-read output of the records in the `Logs` table  
