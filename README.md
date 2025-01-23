# Database Design and Implementation Project

This repository showcases my work on designing and implementing a relational database system for a New York-based coffee shop chain. The goal was to streamline operations and support data-driven decision-making as the company expands nationally. Below is a step-by-step overview of the tasks I performed during this project.

## Scenario
I was tasked with centralizing data from disparate sources such as accounting software, supplier databases, POS systems, and spreadsheets into a cohesive database. This effort involved designing, normalizing, and implementing a relational database system to enhance operational efficiency.

## Software Used
- PostgreSQL Database
- IBM Db2 Database
- MySQL

## Data Sources
- Staff information from HQ spreadsheets
- Sales outlet data from HQ spreadsheets
- Sales data from POS system CSVs
- Customer data from a CRM system CSV
- Product information from supplier spreadsheets

---

## Objectives
By the end of the project, I accomplished the following:
- Identified entities and attributes
- Created and normalized tables in an Entity Relationship Diagram (ERD)
- Defined keys and relationships between tables
- Created database objects using SQL scripts
- Exported and imported data across PostgreSQL, Db2, and MySQL databases
- Created views and materialized views for specific data subsets

---

### Task 1: Identifying Entities
I reviewed existing data and identified key entities for the central database:
- Staff
- Sales Transactions
- Customers
- Products
- Sales Outlets

### Task 2: Identifying Attributes
I analyzed the data and determined attributes for each entity. For instance, the Sales Transactions entity includes attributes such as transaction ID, product ID, quantity, and transaction timestamp.

### Task 3: Creating an ERD
Using **pgAdmin**, I:
- Created an ERD for the COFFEE database.
- Added tables for the `sales_transactions` and `products` entities, defining appropriate data types.
- Captured screenshots of the ERD for documentation.

### Task 4: Normalizing Tables
I ensured the database conformed to the second normal form (2NF):
- Created a `sales_detail` table to eliminate redundancy in `sales_transactions`.
- Designed a `product_type` table to reduce redundancy in the `products` table.
- Updated relationships and documented changes with screenshots.

### Task 5: Defining Keys and Relationships
I assigned primary keys to each table and established relationships:
- Connected `sales_detail` to `sales_transactions` and `products`.
- Linked `products` to `product_type`.
- Documented the updated ERD with relationships.

### Task 6: Creating Database Objects
- Generated SQL scripts from the ERD to create database objects.
- Executed the scripts in **pgAdmin** to create tables.
- Loaded sample data into the database and validated the results.

### Task 7: Creating a View
I created a view named `staff_locations_view` to meet the payroll company’s request for staff location data:
- Excluded the CEO and CFO from the results.
- Exported the data to a CSV file.

### Task 8: Creating a Materialized View
To support a marketing campaign, I created a materialized view `product_info_m-view`:
- Combined data from the `products` and `product_type` tables.
- Exported the data to a CSV file.

### Task 9: Importing Data into Db2
I uploaded the `staff_locations_view.csv` file into an IBM Db2 database:
- Used the Load Data feature to create a `STAFF_LOCATIONS` table.
- Verified the data in the new table.

### Task 10: Importing Data into MySQL
I imported product information into a MySQL database:
- Created a new database named `coffee_shop_products`.
- Imported the `product_info_m-view.csv` data into a new table.
- Validated the data in the MySQL database.

---

## Screenshots
Screenshots for all tasks, including ERDs, views, and imported data, are saved in the `screenshots/` folder.

## Conclusion
This project demonstrates my expertise in designing, normalizing, and implementing relational databases across multiple RDBMS platforms. It also showcases my ability to manipulate and export data efficiently for diverse business needs.
