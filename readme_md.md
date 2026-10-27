# 🚗 Car Sales & Gallery Management System (MS Access)

A comprehensive **Microsoft Access** relational database system designed to manage car dealership operations, sales tracking, customer records, and inventory analytics.

---

## 📌 Overview
This database project simplifies dealership management by organizing key business entities—including inventory (Cars), buyers (Customers), deals (Sales), and staff (Salesmen). It also features predefined Access Queries for generating business reports and insights.

---

## 🗄️ Database Schema

The database consists of the following primary tables and relationships:

### 1. **`Cars` Table**
* `Car ID` (Primary Key) – Unique identifier for each vehicle.
* `Manufacturer` – Vehicle brand/maker.
* `Model` – Vehicle model.
* `Year` – Production year.
* `Color` – Exterior color.
* `Price` – Listing price.
* `Status` – Availability status (`True` = Available, `False` = Sold).
* `Salesman ID` (Foreign Key) – Assigned sales representative.
* `Supplier ID` (Foreign Key) – Vehicle supplier reference.

### 2. **`Customers` Table**
* `Customer ID` (Primary Key) – Unique client ID.
* `Name` – Full customer name.
* `Phone Number` – Primary contact number.
* `E-mail Address` – Email contact.
* `National ID` – National identification/Passport number.
* `Address` – Physical address.

### 3. **`Sales` Table**
* `Sale ID` (Primary Key) – Transaction reference number.
* `Car ID` (Foreign Key) – Reference to the sold car.
* `Customer ID` (Foreign Key) – Reference to the buyer.
* `Salesman ID` (Foreign Key) – Reference to the representative who completed the sale.
* `Sale Date` – Date of purchase.
* `Payment Method` – Payment technique (Cash, Installment, Card, etc.).
* `Payment Status` – Status of transaction completion.

### 4. **`Salesman` Table**
* `Salesman ID` (Primary Key) – Unique staff ID.
* `Name` – Sales representative name.

---

## 🔍 Pre-configured Queries

This system contains built-in Access queries for quick reporting:

* **`Available Cars`**: Filters and displays all cars currently in stock (`Status = True`).
* **`Customer sales details`**: Generates detailed sales receipts showing customer info, purchased vehicle details, price, and transaction date.
* **`more than one Purchase`**: Identifies repeat customers who have purchased more than one vehicle (`Count(Sales.[Sale ID]) > 1`).
* **`Search Salesman`**: Enables parameterized searching for sales records by specific sales representatives or customers.

---

## 📁 Repository Structure

```text
.
├── README.md
├── .gitignore
└── database/
    └── Car_Sales_DB.accdb
```

---

## 🚀 How to Run

1. Clone this repository:
   ```bash
   git clone https://github.com/your-username/Car-Sales-Management-System.git
   ```
2. Open the `.accdb` file inside the `database/` directory using **Microsoft Access 2016** or newer.