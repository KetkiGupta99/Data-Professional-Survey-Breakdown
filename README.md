# 📊 Data Professional Survey Analysis Dashboard (Power BI)

## 📌 Project Overview

This project analyzes a global survey of data professionals using Power BI. The dashboard provides insights into salary trends, career satisfaction, demographic distributions, programming language preferences, and factors influencing career decisions.

The project demonstrates end-to-end Business Intelligence development, including ETL processes, data modeling, DAX calculations, dashboard design, and security implementation.

---

# 🚀 Project Workflow

## Phase 1: Data Extraction & Transformation (ETL)

### Data Ingestion

* Connected Power BI Desktop to the raw **Data Professional Survey** Excel dataset.

### Data Cleaning

* Promoted headers using Power Query.
* Removed empty rows and unnecessary records.
* Standardized text values by:

  * Trimming whitespace
  * Fixing capitalization inconsistencies
  * Ensuring uniform data formatting

### Error Handling

* Resolved `DataSource.NotFound` connection issues.
* Re-mapped broken file paths through Data Source Settings.

---

## Phase 2: Advanced Data Modeling (Star Schema)

### Dimension Table Creation

Created dedicated dimension tables:

* **Dim_Country**
* **Dim_Job**

### Data Normalization

* Removed duplicate values from dimension tables.
* Generated unique records for each category.

### Primary Key Generation

Created index-based primary keys:

* `Country_ID`
* `Job_ID`

### Fact Table Optimization

* Merged dimension tables with the fact table.
* Replaced repetitive text fields with numeric IDs.
* Removed redundant columns to reduce model size and improve performance.

### Relationship Mapping

Established one-to-many relationships:

* Dim_Country → Fact Table
* Dim_Job → Fact Table

This created a clean and scalable **Star Schema Architecture**.

---

## Phase 3: DAX & Analytical Engineering

### Timestamp Conversion

Converted duration values (e.g., `00:03:00`) into total minutes using DAX:

```DAX
Total Minutes =
MINUTE([Time_Taken]) + SECOND([Time_Taken]) / 60
```

### Aggregation Optimization

Corrected default Power BI aggregations:

* Salary → Average
* Time-based Metrics → Average

instead of the default Sum aggregation.

### Accurate Record Counting

Implemented counting logic using categorical fields to ensure reporting accuracy across visuals.

---

## Phase 4: UI/UX & Enterprise Formatting

### Multi-Page Navigation

Built an interactive dashboard navigation system with dedicated pages:

* Overview
* Salary Analysis
* Happiness Insights
* Person Insights

### Executive KPI Layout

Designed a management-friendly landing page featuring:

* Total Survey Respondents
* Average Salary
* Key Business Metrics

### Business-Friendly Naming

Converted technical field names into user-friendly labels.

**Example:**

* "Most Important Factors When Seeking a New Job"

### Data Formatting

Applied consistent formatting:

* Currency symbols
* Decimal precision
* Removed unnecessary display units (K/M) where appropriate

---

## Phase 5: Governance & Security (Row-Level Security)

### Role Creation

Implemented Row-Level Security (RLS) roles for controlled data access.

### Geographic Security

Example:

```DAX
[Country] = "United States"
```

### Department-Level Security

Example:

```DAX
[Current_Role] = "Data Scientist"
```

### Security Validation

Used the **View As Role** feature to verify and test access restrictions before deployment.

---

## Phase 6: Visualization Design & Architecture

### KPI Cards

Used for:

* Total Survey Takers
* Average Salary
* Key Performance Metrics

### Horizontal Bar Charts

Ideal for ranking categories with long labels:

* Job Titles
* Programming Languages
* Job-Seeking Factors

### Donut & Pie Charts

Used for demographic analysis:

* Gender Distribution
* Education Levels

### Treemap

Used for:

* Average Salary by Country

Provides an efficient visual comparison of geographical salary differences.

### Gauge Charts

Used for happiness metrics:

* Salary Satisfaction
* Work-Life Balance
* Coworker Satisfaction

### Column Charts

Used for direct comparisons such as:

* Difficulty of Breaking into Data Careers

---

# 📈 Key Business Insights

## Global Overview

* Total Survey Respondents: **452**
* Average Salary: **$54,479**

---

## Role-Based Compensation

| Job Role       | Average Salary |
| -------------- | -------------- |
| Data Scientist | $103K          |
| Data Engineer  | $64K           |
| Data Analyst   | $55K           |

**Insight:** Data Scientists earn the highest average compensation among surveyed professionals.

---

## Geographic Salary Analysis

| Country       | Average Salary |
| ------------- | -------------- |
| United States | $78,901        |
| Canada        | $59,450        |
| India         | $32,010        |

**Insight:** Significant salary disparities exist across regions, with the United States leading in compensation.

---

## Gender Salary Comparison

| Gender | Average Salary |
| ------ | -------------- |
| Male   | $54,497        |
| Female | $54,433        |

**Insight:** The survey indicates near salary parity between male and female respondents.

---

## Career Satisfaction

| Metric                    | Score (/10) |
| ------------------------- | ----------- |
| Happiness with Co-workers | 5.90        |
| Happiness with Salary     | 4.25        |

**Insight:** Salary satisfaction is the lowest-rated aspect of respondents' careers.

---

## Programming Language Popularity

| Language | Respondents |
| -------- | ----------- |
| Python   | 300         |

**Insight:** Python dominates as the preferred programming language among data professionals.

---

## Career Transition Trends

* Better salary is the most important factor when considering a new opportunity.
* Most respondents reported that transitioning into the data field is difficult.

| Response      | Count |
| ------------- | ----- |
| Difficult     | 265   |
| Not Difficult | 187   |

---

# 🛠️ Tools & Technologies

* Power BI Desktop
* Power Query
* DAX (Data Analysis Expressions)
* Star Schema Data Modeling
* Row-Level Security (RLS)
* Excel

---

# 🎯 Skills Demonstrated

* ETL & Data Cleaning
* Data Modeling (Star Schema)
* DAX Development
* Dashboard Design
* Data Visualization
* Business Intelligence Reporting
* Row-Level Security (RLS)
* Analytical Storytelling
* Performance Optimization

---

# 📷 Dashboard Preview

> Attached pdf file of dashboard.

---

# 📌 Conclusion

This project showcases a complete Business Intelligence workflow from raw data ingestion to secure, interactive reporting. The dashboard delivers actionable insights into compensation trends, career satisfaction, demographic patterns, and technology adoption within the global data professional community.


Note: This dataset I have taken from YouTube channel - 'Alex the Analyst' 
