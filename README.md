Google Fiber — Exploring Repeat Calls

> **Business Intelligence Project** | BigQuery SQL · Tableau · ETL
> **Analyst:** Seth-Ayodele OluwaTomiwa | **Year:** 2026 | **Client:** Google Fiber

---

## 📌 Project Overview

Google Fiber wanted to understand **why customers were calling customer support more than once** after their first inquiry. Repeat calls signal unresolved issues, hurt customer satisfaction, and inflate operational costs.

As the BI Analyst on this project, I was tasked with:
- Identifying which **problem types** drive the most repeat calls
- Finding which **market cities** have the highest repeat call rates
- Designing a **Tableau dashboard** that lets leadership explore trends by week, month, quarter, and year

---

## 🧩 Business Problem

> *"The business problem Google Fiber is trying to solve is the problem of repeat calls. They want to know why customers are having to call more than once so that they can improve the overall customer experience."*

**Key questions this project answers:**
- How often does a customer call after their first inquiry?
- Which problem types generate the most repeat calls?
- Which market cities have the worst repeat call patterns?
- How do repeat calls trend across days, weeks, months, and quarters?

---

## 🗂️ Project Files

| File | Description |
|------|-------------|
| `Google_Fiber_Data.csv` | Cleaned master dataset (merged from 3 markets) |
| `market_1.csv` | Raw data — Market 1 |
| `market_2.csv` | Raw data — Market 2 |
| `market_3.csv` | Raw data — Market 3 |
| `SQL_Query_for_Table_merging.sql` | BigQuery SQL used to merge the three market tables |
| `Customer_Data_dashboard.twbx` | Tableau packaged workbook (final dashboard) |
| `Dashboard_1.pdf` | PDF export of the Tableau dashboard |
| `Planning_Documents_for_google_Fiber_.docx` | Stakeholder, Project & Strategy requirements docs |

---

## 🗃️ Dataset

- **Records:** ~1,350 support call entries
- **Markets:** 3 cities (market_1, market_2, market_3)
- **Time period:** 2022 (Q1 focus)

| Field | Description |
|-------|-------------|
| `date_created` | Date of first customer contact |
| `contacts_n` | Number of calls on first contact day |
| `contacts_n_1` to `contacts_n_7` | Repeat calls on days 1–7 after first contact |
| `new_type` | Problem category (Type 1–5) |
| `new_market` | Market city identifier |

### Problem Type Key

| Code | Problem Type |
|------|-------------|
| Type 1 | Account Management |
| Type 2 | Technician Troubleshooting |
| Type 3 | Scheduling |
| Type 4 | Construction |
| Type 5 | Internet & Wifi |

---

## 🔧 Methodology

### Step 1 — Requirements Gathering
Produced three planning documents:
- **Stakeholder Requirements Doc** — captured what stakeholders needed to see
- **Project Requirements Doc** — defined purpose, dependencies, and deliverables
- **Strategy Doc** — outlined roll-out plan and success criteria

### Step 2 — ETL: SQL Table Merging (BigQuery)

Three separate market tables were merged into one unified dataset using `UNION ALL`:

```sql
SELECT *
FROM `continual-works-490313-h3.490313.Fiber`
UNION ALL
SELECT *
FROM `continual-works-490313-h3.490313.Fiber 2`
UNION ALL
SELECT *
FROM `continual-works-490313-h3.490313.fiber 3`
```

### Step 3 — Data Exploration
Explored repeat call behaviour across all 7 contact days per customer, segmented by market and problem type.

### Step 4 — Tableau Dashboard
Built an accessible, interactive dashboard with **6 chart views**:

- Repeat calls by **month**
- Repeat calls by **market**
- Repeat calls by **problem type**
- Repeat calls by **week**
- Repeat calls by **quarter**
- Repeat calls by **year**

---

## 📊 Key Findings

1. **Most repeat calls happen immediately** — the highest volume of callbacks occurred within the same day or day 1, suggesting customers gave up and called back quickly when issues weren't resolved.

2. **Internet & Wifi (Type 5) and Technician Troubleshooting (Type 2) generated the most repeat calls** — pointing to resolution quality gaps in technical support.

3. **Repeat call behaviour varied across all three market cities** — indicating that some problems may be city-specific (infrastructure, staffing, or service coverage).

4. **Q1 2022 showed elevated repeat call volumes** — with over 64,939 contacts recorded in the first contact bucket alone.

---

## 📈 Dashboard Preview

> Open `Customer_Data_dashboard.twbx` in **Tableau Desktop** or **Tableau Public** to explore the full interactive dashboard.
> A static PDF export is available in `Dashboard_1.pdf`.

---

## 🎯 Business Impact

By identifying the specific problem types and market cities that generate the most repeat calls, this dashboard enables Google Fiber leadership to:

- **Target training** for technicians handling internet and wifi issues
- **Prioritise resources** in high-repeat-call markets
- **Measure improvement** over time as interventions are made
- **Reduce call volume** by solving problems right the first time

---

## ✅ Success Criteria

| Criteria | Type |
|----------|------|
| Reduce call volume by increasing customer satisfaction | Strategic |
| Improve operational optimisation | Strategic |
| Dashboard showing repeat caller volumes by market and problem type | Measurable |
| Identify the problem type that brings in the most calls | Measurable |
| Identify the market city that brings the most calls | Analytical |

---

## 🛠️ Tools Used

- **BigQuery (SQL)** — data merging and preparation
- **Tableau Desktop** — dashboard design and visualisation
- **Google Sheets / CSV** — raw data management
- **Microsoft Word** — planning and stakeholder documentation

---

##  About the Analyst

**Seth-Ayodele OluwaTomiwa**
Business Intelligence Analyst
Signed off: 17 April 2026

---

*This project was completed as part of a BI portfolio demonstrating skills in stakeholder management, SQL-based ETL, and Tableau dashboard design.*
