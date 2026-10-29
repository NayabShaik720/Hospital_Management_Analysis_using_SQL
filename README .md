# 🏥 Hospital Management System — MySQL Project

This project showcases a comprehensive Hospital Management Database System designed using MySQL, focusing on efficient data modeling, relational integrity, and real-world operational use cases.

It is structured to reflect best practices in database schema design, data importation, and analytical querying, making it an ideal addition to a professional portfolio for roles in data engineering, backend development, or database administration.

---

## 📁 Project Structure

| Component              | Description                                                                                           |
|------------------------|-------------------------------------------------------------------------------------------------------|
| `CREATE DATABASE`      | Initializes the `Hospital` database and its relational structure                                      |
| `TABLE DEFINITIONS`    | Logical data modeling across core entities: Patients, Doctors, Appointments, Medical Records, Billing |
| `DATA IMPORT`          | CSV data ingestion using `LOAD DATA INFILE` with proper handling of nulls, delimiters, and headers    |
| `SQL QUERIES`          | Set of 20+ optimized SQL queries for insights, scheduling logic, and reporting                        |

---

## 🧱 Database Schema Overview

### 1. `patients`
Stores patient information including demographics and contact details.

### 2. `doctors`
Holds doctor profiles, specializations, and availability information.

### 3. `appointments`
Captures patient-doctor interactions with appointment type, timing, and status.

### 4. `medicalrecords`
Records diagnoses, prescriptions, and treatment plans.

### 5. `billing`
Manages invoices and tracks payment status per appointment.

> All tables follow **normalized design principles**, with primary keys, foreign key constraints (`ON DELETE CASCADE`), and relevant integrity checks.

---

## 📥 Data Loading

Data is imported from local CSV files using two methods:

- `LOAD DATA INFILE` for scripted bulk loading
- MySQL Workbench's **"Import Data"** option (right-click on table → Table Data Import Wizard) for manual uploads

| Table          | CSV Filename      | Method Used         | Notes                                             |
|----------------|-------------------|---------------------|---------------------------------------------------|
| `patients`     | `PatientID.csv`   | LOAD DATA INFILE    | Includes contact and demographic details          |
| `doctors`      | `DoctorID.csv`    | Import Data (GUI)   | Includes specialization and availability          |
| `appointments` | `Hospital.csv`    | LOAD DATA INFILE    | Appointment metadata and scheduling               |
| `billing`      | `Billing.csv`     | Import Data (GUI)   | Amount, payment date, and payment status fields   |

⚠️ **Note for `LOAD DATA INFILE`:** Ensure the files are located in the directory allowed by MySQL’s `secure_file_priv` configuration, typically:
`C:/ProgramData/MySQL/MySQL Server 8.0/Uploads/`
---

## 🔎 Key Features & Use Cases

### 🗓️ Scheduling Logic
- Book appointments with conflict checks
- Reschedule based on availability
- Cancel appointments with proper tracking

### 📊 Operational Queries
- Daily reports
- Revenue estimation
- Most loyal/inactive patients
- Popular appointment types

### 👨‍⚕️ Doctor Utilization
- Most booked doctors
- Doctors with no appointments today
- Appointment duration insights

### 🧾 Billing & Payments
- Invoice management
- Payment status tracking
- Total revenue reporting

---

## ✅ Technical Highlights

- Normalized schema with referential integrity
- Use of ENUMs, AUTO_INCREMENT, and CHECK constraints
- CSV ingestion via `LOAD DATA INFILE`
- Query logic using JOINS, AGGREGATION, TEMP TABLES, and SUBQUERIES
- Practical use cases for real-world hospital systems

---

## 🔧 Requirements

- MySQL Server 8.0+
- CSV files placed in allowed `secure_file_priv` path
- SQL client (MySQL Workbench, DBeaver, CLI, etc.)

---

## 🧭 Potential Enhancements

- Stored procedures for automation
- Views for dashboards
- Role-based access and user authentication

## 📌 Repository Contents

Hospital-management-system/
│
├── Hospital_Management.sql      # Full SQL script (schema + data load + queries)

├── PatientID.csv                # Sample patient data

├── DoctorID.csv                 # Sample doctor data

├── Hospital.csv                 # Appointment data

├── Billing.csv                  # Billing and payment data

├── MedicalRecords.csv           # Medical records data

└── README.md                    # Project documentation


