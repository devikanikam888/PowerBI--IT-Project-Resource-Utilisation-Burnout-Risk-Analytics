# 📊 IT Project Resource Utilisation & Burnout Risk Analytics (Power BI)

## 📌 Project Overview

This project addresses a **real-world IT project management challenge**:  
the lack of visibility into **resource workload, capacity constraints, and burnout risk**, which often results in delayed deliveries, reduced team performance, and reactive decision-making.

Using **Power BI and DAX**, I built an end-to-end analytics solution that transforms raw timesheet and capacity data into **actionable insights** for executives, project managers, and delivery leads.

The dashboard is designed to answer not only **“what happened”**, but more importantly:  
**“what is going wrong and where immediate action is required.”**

---

## 🎯 Business Problem Statement

In many IT organisations:

- Resource workload is tracked in Excel but **not analytically evaluated**
- Managers identify overload and burnout **after delivery issues occur**
- Project-level impact of overutilisation is unclear
- There is no unified view connecting **hours worked, capacity, risk, and trends**

### Key business questions addressed:
- Are resources working beyond their available capacity?
- Which projects are creating the highest workload risk?
- Which resources are at burnout risk?
- Are utilisation risks increasing week-over-week?
- Where should managers intervene first?

---

## 🧩 Data Used

### 1️⃣ Timesheets Table
- Resource Name  
- Project  
- Actual Hours  
- WeekNumber  

### 2️⃣ Resource Capacity Table
- Resource Name  
- Weekly Capacity  
- Team  

### 3️⃣ Project Mapping Table
- Project Name  
- (Optional attributes such as project priority or risk category)

---

## 🔗 Data Modeling Approach

- Created **one-to-many relationships**:
  - Resources → Timesheets (Resource Name)
  - Projects → Timesheets (Project)
- Enforced **single-direction filtering** to maintain predictable DAX behavior
- Validated the model before implementing calculations

**Why this matters:**  
Correct data modeling ensures DAX measures respond accurately to slicers, filters, and visual interactions.

---

## 📊 Dashboards Created

### 📄 Page 1: Executive Summary
- Total actual hours
- Overall utilisation vs capacity
- Number of high-risk resources
- Utilisation by team and by individual resource

**Audience:** Executives / PMO

---

### 📄 Page 2: Project Impact & Manager Action View
- Actual hours by project
- Critical projects identification
- Project risk and deadline indicators
- Overloaded projects
- Burnout-prone resources
- Project workload by duration (WeekNumber-based timeline)

**Audience:** Project Managers / Delivery Leads

---

## 📈 Key Insights Derived

- Multiple resources consistently exceeded **100% utilisation**
- Certain projects consumed **disproportionate capacity**
- Burnout risk increased **gradually over time**, not suddenly
- Overload was often concentrated within specific teams
- Sustained overutilisation trends could **predict project delivery risk**

---

## 🧠 What I Learned (Technical Focus)

- Clear distinction between **row context vs filter context**
- When to use **calculated columns vs measures**
- Writing DAX measures that respond correctly to slicers
- Debugging common Power BI issues (filter misuse, PLACEHOLDER errors)
- Implementing **rolling calculations** without a date table
- Translating operational project data into analytical business logic

---

## 🚀 Business Value of the Dashboard

- Enables **proactive workload and capacity management**
- Helps reduce burnout and delivery risk
- Improves project planning and forecasting accuracy
- Acts as a **single source of truth** for utilisation analytics
- Supports data-driven managerial and executive decision-making

---

## 🔮 Future Enhancements

- Add a dedicated **date dimension**
- Integrate real-time data from **Jira or Azure DevOps**
- Forecast utilisation using historical trends
- Automate refresh using **Power BI Service**
- Add drill-through views for individual resources and projects

---

## 🛠 Tools & Technologies

- **Power BI Desktop**
- **DAX**
- **Excel** (timesheets and capacity data)
