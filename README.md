# 🏥 Hospital Emergency Patients Analysis Dashboard

> An end-to-end Excel Data Analytics project built using **Power Query**, **Power Pivot**, **DAX**, Pivot Tables, and Interactive Dashboards to analyze hospital emergency room operations and support data-driven decision making.

---

# 📌 Project Overview

Healthcare organizations generate thousands of patient records every day. Without proper analysis, it becomes difficult for hospital management to monitor patient flow, identify operational bottlenecks, and improve service quality.

This project transforms raw emergency room patient data into an interactive Excel dashboard that enables stakeholders to monitor KPIs such as patient volume, average waiting time, patient satisfaction, admissions, referrals, and demographic trends.

The project follows a complete Business Intelligence workflow—from understanding business requirements to delivering actionable insights.

---

# 🎯 Business Objective

Develop an interactive Emergency Room Analysis Dashboard that helps hospital management:

- Monitor daily patient visits
- Track average waiting time
- Measure patient satisfaction
- Analyze admissions and referrals
- Understand patient demographics
- Improve operational efficiency through data-driven insights

---

# 🛠 Tech Stack

- Microsoft Excel
- Power Query
- Power Pivot
- DAX
- Pivot Tables
- Pivot Charts
- Excel Dashboard
- Data Modeling

---

# 🚀 Project Journey

## 1. Business Requirement Gathering

The project started by understanding the reporting requirements from hospital stakeholders.

The primary objective was to answer questions such as:

- How many patients visit every day?
- How long do patients wait?
- Which departments receive the highest referrals?
- Which age groups visit most frequently?
- How satisfied are patients with emergency services?

These business questions became the foundation for the dashboard KPIs.

---

## 2. Data Understanding

Before performing any transformations, the dataset was explored to understand:

- Available columns
- Data types
- Missing values
- Duplicate records
- Inconsistent categorical values
- Relationships between attributes

Understanding the dataset helped identify necessary cleaning and modeling steps.

---

## 3. Data Import using Power Query

The raw hospital dataset was imported into Power Query.

Power Query was used because it provides a repeatable ETL process where every transformation is automatically recorded and can be refreshed whenever new data arrives.

---

## 4. Data Cleaning & Transformation

Several data quality issues were identified and resolved.

### Date & Time Transformation

- Split Patient Admission DateTime into:
  - Admission Date
  - Admission Time

---

### Name Standardization

Merged:

- First Name
- Last Name

into a single

```
Patient Name
```

column.

---

### Gender Standardization

Low-cardinality values were standardized.

```
M      → Male
Male   → Male
F      → Female
Female → Female
```

This ensures consistent reporting across visualizations.

---

### Admission Status Cleaning

Converted Boolean values into meaningful business labels.

```
True  → Admitted
False → Not Admitted
```

---

### Duplicate Column Removal

Removed repeated Admission Flag column to eliminate redundancy.

---

### Data Loading Optimization

Instead of loading the entire dataset into worksheets, data was loaded as **Connection Only** and into the Data Model.

This approach:

- reduces workbook size
- improves refresh performance
- avoids unnecessary memory consumption

---

# 📅 Calendar Table Creation

A dedicated Date Table was created to support time intelligence.

Benefits include:

- Continuous date hierarchy
- Monthly analysis
- Year-over-Year reporting
- Better Pivot filtering
- Cleaner relationships

---

# 🔗 Data Modeling

A star schema style relationship was created.

```
Date Table
      │
      │
      ▼
Hospital Emergency Room Data
```

Relationship:

```
Date (1)
      │
      │
      ▼
Hospital Data (Many)
```

This enables efficient filtering and DAX calculations.

---

# 📐 Feature Engineering using DAX

Additional business-friendly columns were created.

### Age Group

Patients were grouped into:

- 00–10
- 11–20
- 21–30
- 31–40
- 41–50
- 51–60
- 61–70
- 71–80

---

### Patient Attendance Status

Business rule:

```
Wait Time > 30 minutes
        ↓
Delay

Wait Time ≤ 30 minutes
        ↓
On-Time
```

This simplified operational performance analysis.

---

# 📊 Dashboard KPIs

The dashboard tracks:

- Total Patients
- Average Waiting Time
- Patient Satisfaction Score
- Admission vs Non-Admission
- Timeliness (Seen within 30 minutes)
- Department Referrals
- Age Distribution
- Gender Distribution

---

# 📈 Dashboard Visualizations

The final dashboard includes:

- KPI Cards
- Pivot Charts
- Trend Analysis
- Admission Status Analysis
- Age Distribution
- Gender Analysis
- Department Referral Analysis
- Timeliness Monitoring
- Interactive Filters & Slicers

---

# 💡 Key Business Insights

Analysis of the emergency room data revealed several operational insights:

### 1. Emergency wait time remains efficient

The average waiting time is approximately **30 minutes**, which is lower than the typical **40–50 minute** waiting time observed in many general outpatient departments.

---

### 2. Most patients are treated within Emergency

A significant proportion of patients were not referred to specialized departments, indicating that many cases were successfully managed within the emergency unit itself.

---

### 3. Patient demographics become easier to understand

Grouping patients into age bands makes it easier to identify which age groups utilize emergency services most frequently.

---

### 4. Standardized data improves reporting

Cleaning inconsistent values such as Gender and Admission Status ensures accurate Pivot Tables, charts, and business reports.

---

### 5. Data modeling improves scalability

Using Power Pivot relationships instead of worksheet formulas creates a more scalable and maintainable reporting solution.

---

# 📚 Key Learnings

Throughout this project, I gained practical experience in:

- Business Requirement Analysis
- Data Cleaning using Power Query
- ETL workflow in Excel
- Data Quality Validation
- Feature Engineering using DAX
- Creating Date Dimensions
- Data Modeling with Power Pivot
- Building Interactive Dashboards
- KPI Design
- Storytelling with Data
- Dashboard Layout & Formatting

---

# ⚡ Challenges Faced

- Cleaning inconsistent categorical values
- Creating reusable Power Query transformations
- Building an optimized Data Model
- Designing a responsive dashboard layout in Excel
- Managing Pivot relationships and DAX calculations
- Dashboard formatting, which required significantly more manual effort compared to Power BI

---

# 📂 Project Workflow

```
Business Requirement Gathering
            │
            ▼
Understanding the Data
            │
            ▼
Import Data using Power Query
            │
            ▼
Data Cleaning & Transformation
            │
            ▼
Create Date Table
            │
            ▼
Data Modeling (Power Pivot)
            │
            ▼
DAX Calculations
            │
            ▼
Pivot Tables & Charts
            │
            ▼
Interactive Dashboard
            │
            ▼
Business Insights
```

---

# 🎯 Conclusion

This project demonstrates a complete Business Intelligence workflow using Microsoft Excel. It showcases how Power Query, Power Pivot, DAX, and interactive dashboards can transform raw healthcare data into meaningful insights that support operational monitoring and informed decision-making.

The techniques used in this project are directly applicable to real-world reporting and analytics scenarios across healthcare and other data-driven industries.
