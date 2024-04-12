# BookShop Management System Database Schema

## DataBase Name : Management
## Tables

- Books
- Suppliers
- Purchases
- Employees
- Members
- Sales

### Books

Column names for the "Books" table:

```sql
id INT PRIMARY KEY,
name VARCHAR(255),
auth VARCHAR(255),
price INT,
qty INT
```
### suppliers

Column names for the "suppliers" table:

```sql
id INT PRIMARY KEY,
name VARCHAR(255),
phn BIGINT,
addr_line1 VARCHAR(255),
addr_line2 VARCHAR(255),
addr_city VARCHAR(255),
addr_state VARCHAR(255)
```

### purchases

Column names for the "purchases" table:

```sql
ord_id INT PRIMARY KEY,
book_id INT,
sup_id INT,
qty INT,
dt_ordered DATE,
eta INT,
received CHAR(1) CHECK (received IN ('T', 'C', 'F')),
inv INT
```

### employees

Column names for the "employees" table:

```sql
id INT PRIMARY KEY,
name VARCHAR(255),
addr_line1 VARCHAR(255),
addr_line2 VARCHAR(255),
addr_city VARCHAR(255),
addr_state VARCHAR(255),
phn BIGINT,
date_of_joining DATE,
salary BIGINT,
mgr_status CHAR(1) CHECK (mgr_status IN ('T', 'F'))
```

### members

Column names for the "members" table:

```sql
id INT PRIMARY KEY,
name VARCHAR(255),
addr_line1 VARCHAR(255),
addr_line2 VARCHAR(255),
addr_city VARCHAR(255),
addr_state VARCHAR(255),
phn BIGINT,
beg_date DATE,
end_date DATE,
valid VARCHAR(255)
```

### sales

Column names for the "sales" table:

```sql
invoice_id INT PRIMARY KEY,
member_id INT,
book_id INT,
qty INT,
amount INT,
date DATE
```
