# JavaAssignment6
---

# Employee Payroll System (Java – OOP & Inheritance)

## Overview

This project is a **Java-based Employee Payroll System** designed to demonstrate core object-oriented programming concepts such as **inheritance, polymorphism, method overriding, and encapsulation**.

The system models different types of employees—**Permanent Employees, Contract Employees, and Managers**—each with distinct salary structures. It calculates gross salary, applies tax rules, and generates detailed payslips for each employee.

---

## Features

* Supports multiple employee types:

  * Permanent Employee
  * Contract Employee
  * Manager
* Calculates salary based on employee type
* Applies tax based on salary slabs
* Generates detailed payslips
* Demonstrates:

  * Single inheritance
  * Hierarchical inheritance
  * Multilevel inheritance
* Uses `ArrayList` to manage employees
* Implements polymorphism for unified processing

---

## Project Structure

### 1. Employee Class (Base Class)

Represents a generic employee.

#### Data Members

* `empId` – employee ID
* `empName` – employee name
* `basicSalary` – base salary

#### Methods

* `calculateGross()` – returns gross salary (default = basic)
* `printComponents()` – prints salary breakdown
* `printHeader()` – prints employee details
* `getEmployeeType()` – returns employee type

---

### 2. PermanentEmployee Class

Extends `Employee` (Single Inheritance).

#### Additional Components

* HRA (20% of basic salary)
* DA (15% of basic salary)

#### Features

* Overrides `calculateGross()` to include allowances
* Provides detailed salary breakdown

---

### 3. ContractEmployee Class

Extends `Employee` (Hierarchical Inheritance).

#### Additional Components

* `hoursWorked`
* `hourlyRate`

#### Features

* Salary calculated as:

  ```
  hoursWorked × hourlyRate
  ```
* No additional allowances

---

### 4. Manager Class

Extends `PermanentEmployee` (Multilevel Inheritance).

#### Additional Components

* Bonus
* Travel Allowance (10% of basic salary)

#### Features

* Overrides `calculateGross()` to include bonus and travel allowance
* Builds upon PermanentEmployee salary structure

---

### 5. EmployeePayrollSystem Class (Main Class)

Handles program execution.

Responsibilities:

* Creates employee objects
* Stores them in an `ArrayList`
* Calculates tax based on salary
* Generates payslips using a unified method
* Demonstrates polymorphism

---

## Salary Calculation Logic

### Permanent Employee

```
Gross = Basic + HRA (20%) + DA (15%)
```

### Contract Employee

```
Gross = Hours Worked × Hourly Rate
```

### Manager

```
Gross = Basic + HRA + DA + Bonus + Travel Allowance (10%)
```

---

## Tax Calculation

* Salary ≤ 20,000 → No tax
* 20,001 – 50,000 → 10% tax
* Above 50,000 → 20% tax

---

## Payslip Generation

Each employee receives a structured payslip containing:

* Employee details
* Salary breakdown
* Gross salary
* Tax deduction
* Net salary

---

## How to Run the Program

### Prerequisites

* Java Development Kit (JDK) installed
* Terminal or command prompt

### Steps

1. Compile the program:

```
javac EmployeePayrollSystem.java
```

2. Run the program:

```
java EmployeePayrollSystem
```

---

## Sample Output

```
====== PAYSLIP ======
EmpID           : 101
Name            : Priya Sharma
Type            : PERMANENT

---- Salary Breakdown ----
Basic           : INR 40000.00
HRA (20%)       : INR 8000.00
DA  (15%)       : INR 6000.00

---- Summary ----
Gross           : INR 54000.00
Tax             : INR 10800.00
NET             : INR 43200.00
```

---

## Concepts Used

* Object-Oriented Programming (OOP)
* Inheritance (Single, Hierarchical, Multilevel)
* Method Overriding
* Polymorphism
* Encapsulation
* Collections (`ArrayList`)
* Conditional Logic
* Modular Code Design

---



Tell me the number.
