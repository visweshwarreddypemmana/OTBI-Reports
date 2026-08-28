# OTBI – Employee Workforce Details Report

## 📊 Report Overview

**Employee Workforce Details Report** is an Oracle Fusion OTBI report developed to provide the HR team with a clear view of the current employee workforce and basic employment information.

The report is designed based on the Bussiness requirement to allow HR users to view, search, filter, and sort employee information using key employee and organizational attributes.

The report displays only **active employee assignments** based on the required assignment status criteria.

---

## 📌 Business Requirement

> **“The HR team wants to see the current employee population and basic employment information. The report should allow HR users to filter the data based on key employee and organizational attributes.”**

### Report Name

**Employee Workforce Details Report**

---

## 🎯 Business Objective

The objective of this report is to provide HR users with a simple and interactive workforce report containing current employee assignment information.

The report enables HR users to:

* View the current employee population
* Review basic employee and employment information
* Filter employees based on organizational attributes
* Search employee records easily
* Sort employees based on Hire Date and Department
* View results in a clean table format
* Restrict the report to active employee assignments

---

## 🛠️ OTBI Configuration

### Subject Area

**Workforce Management – Worker Assignment Real Time**

The report was developed using the **Workforce Management – Worker Assignment Real Time** subject area.

---

## 📋 Report Columns

The following columns were selected based on the client requirements:

| #  | Column            |
| -- | ----------------- |
| 1  | Employee Number   |
| 2  | Employee Name     |
| 3  | Work Email        |
| 4  | Person Type       |
| 5  | Hire Date         |
| 6  | Assignment Status |
| 7  | Job               |
| 8  | Department        |
| 9  | Business Unit     |
| 10 | Legal Employer    |
| 11 | Location          |
| 12 | Manager Name      |

---

## 🔎 Filters & Prompts

The report provides filtering capability for the following attributes:

* Business Unit
* Department
* Legal Employer
* Job
* Assignment Status
* Location

### Prompt Configuration

Prompts were created for the required filter attributes.

The prompts allow HR users to dynamically select the required values when running the report.

The default value for the required prompts was configured as:

**All Column Values**

This allows the report to initially display all applicable records while still providing users with the ability to narrow down the results.

---

## 👥 Active Employee Assignment Requirement

An important Business requirement was that the report should display **only active employee assignments**.

For **Assignment Status**, the following specific values were selected:

* Active – Payroll Eligible
* Active – No Payroll

This configuration ensures that the report focuses on currently active employee assignments and excludes inactive assignment statuses.

---

## 🔐 Security Configuration

The report was validated with the following HR roles:

* **HR Specialist View All**
* **HR Manager View All**
* **HR Analyst View All**

The required **data roles were refreshed** after the role configuration to ensure the latest security assignments were available for testing.

### Security Objective

The security configuration was considered to ensure that authorized HR users can access the report according to their assigned Fusion HCM security roles and data access.

---

## 📊 Report Layout

The report uses a **Table View** to present employee workforce information.

The table format was selected because it provides a simple and readable representation of employee records and supports:

* Easy searching
* Filtering
* Sorting
* Row-by-row employee information
* Clear presentation of organizational attributes

---

## ↕️ Sorting

The report supports sorting employee records based on:

* **Hire Date**
* **Department**

Hire Date sorting can be used to identify employees based on their joining date, while Department sorting allows HR users to organize the workforce by organizational structure.

---

## 🔄 Report Development Process

The report was developed using the following process:

```text
Client Requirement
        ↓
Requirement Analysis
        ↓
Subject Area Selection
        ↓
Column Selection
        ↓
Analysis Creation
        ↓
Filter Configuration
        ↓
Prompt Configuration
        ↓
Active Assignment Filter
        ↓
Table Layout Configuration
        ↓
Sorting Configuration
        ↓
Security Validation
        ↓
Data Role Refresh
        ↓
Report Testing & Validation
        ↓
Catalog Export
        ↓
Final Report
```

---

## 📝 Key Configuration Steps

### 1. Analyze Business Requirement

Reviewed the business requirement and identified:

* Required employee attributes
* Required organizational attributes
* Required filters/prompts
* Active employee requirement
* Sorting requirements
* Security requirements
* Expected report layout

### 2. Select Subject Area

Selected:

**Workforce Management – Worker Assignment Real Time**

### 3. Select Required Columns

Required columns were identified from the subject area and added to the analysis using drag-and-drop.

### 4. Configure Filters

Filters were added for the required employee and organizational attributes.

The required filter attributes were configured as prompted filters where applicable.

### 5. Configure Prompts

Prompts were created for:

* Business Unit
* Department
* Legal Employer
* Job
* Assignment Status
* Location

Default prompt values were configured to show **All Column Values**.

### 6. Configure Active Assignment Filter

Assignment Status was restricted to:

```text
Active – Payroll Eligible
Active – No Payroll
```

This was done to satisfy the requirement to display only current/active employee assignments.

### 7. Configure Report Layout

The report was configured using a clean **Table View**.

### 8. Configure Sorting

Sorting was configured to support:

* Hire Date
* Department

### 9. Configure Security

The following roles were considered for report access and validation:

```text
HR Specialist View All
HR Manager View All
HR Analyst View All
```

### 10. Refresh Data Roles

Data roles were refreshed after the security configuration to ensure the updated role/data access was available during testing.

### 11. Validate Report

The report was tested against the client requirements to verify:

* Required columns are displayed
* Required prompts are available
* Active assignment restriction works
* Sorting works
* Table layout is readable
* Authorized HR roles can access the required data
* Report results are consistent with the expected data

### 12. Export Report Artifacts

The completed OTBI report artifacts were exported and maintained in the repository.

---

## 🧪 Validation & Testing

The following scenarios should be validated before considering the report complete:

| Test Case                            | Expected Result                                                              |
| ------------------------------------ | ---------------------------------------------------------------------------- |
| Run report without selecting prompts | All applicable active assignments are displayed                              |
| Filter by Business Unit              | Employees belonging to selected BU are displayed                             |
| Filter by Department                 | Employees belonging to selected department are displayed                     |
| Filter by Legal Employer             | Employees belonging to selected legal employer are displayed                 |
| Filter by Job                        | Employees with selected job are displayed                                    |
| Filter by Location                   | Employees at selected location are displayed                                 |
| Filter by Assignment Status          | Selected assignment status records are displayed                             |
| Active Assignment Validation         | Only Active – Payroll Eligible and Active – No Payroll records are displayed |
| Sort by Hire Date                    | Records are sorted according to Hire Date                                    |
| Sort by Department                   | Records are organized by Department                                          |
| HR Specialist access                 | Authorized report/data access is available                                   |
| HR Manager access                    | Authorized report/data access is available                                   |
| HR Analyst access                    | Authorized report/data access is available                                   |
| Table validation                     | Data is displayed in a clean table format                                    |

---

## 📁 Repository Structure

```text
otbi-employee-workforce-details-report/
│
├── README.md
│
├── requirements/
│   └── Business-requirement.md
│
├── otbi-report/
│   ├── Employee Workforce Details Report.catalog
│   └── Employee Workforce Details Report.xlsx
│
├── documentation/
│   ├── report-design.md
│   ├── report-creation-steps.md
│   ├── filters-and-prompts.md
│   └── validation-testing.md
│
└── screenshots/
    ├── 01-subject-area.png
    ├── 02-selected-columns.png
    ├── 03-filters.png
    ├── 04-prompts.png
    ├── 05-active-assignment-filter.png
    └── 06-final-report.png
```

---
