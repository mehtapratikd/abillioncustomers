# A Billion Customers
Design a system for information retrieval using REST APIs, consisting of a billion customers.

#### Customers Data Schema
The schema is for a relational database management system

```mermaid
---
config:
  theme: neutral
---
erDiagram
    direction LR
    customers {
        unsignedbigint customer_id PK
        varchar(100) full_name
        varchar(100) email
        varchar(15) mobile_number
        datetime registration_date
    }
    addresses {
        unsignedbigint address_id PK
        unsignedbigint customer_id FK
        varchar(100) full_name
        varchar(50) address_line_1 "Building name & Flat no. | House name"
        varchar(200) address_line_2 "Road or Street name & Area"
        int pincode
        varchar(50) city
        smallint state_code_of_india
    }
    customers only one..zero or more addresses : have
```
