# Titanic Survival Analysis – SQL Data Analytics

## 📌 Project Overview

This project focuses on analyzing the Titanic passenger dataset using SQL to identify meaningful patterns in passenger survival, passenger class, gender, age, fare, and journey details.

As part of the SkillAudit.ai Data Analytics Internship – Week 3 SQL Analysis task, the cleaned Titanic dataset was loaded into MySQL and analyzed using SQL queries involving JOINs, aggregations, GROUP BY, HAVING clauses, and subqueries.

The objective was to transform passenger-level data into meaningful analytical insights that can support data-driven conclusions.

---

## 🎯 Project Objective

The main objectives of this project were to:

- Analyze passenger survival patterns.
- Compare survival across passenger classes.
- Analyze survival by gender.
- Calculate survival rates.
- Analyze average passenger age by class.
- Compare average fares across passenger classes.
- Use JOIN operations to combine related datasets.
- Apply subqueries for advanced analysis.
- Identify groups with significant passenger counts.
- Generate meaningful insights from SQL analysis.

---

## 🛠️ Technologies Used

- MySQL 8.0
- SQL
- MySQL Workbench
- CSV Dataset
- GitHub

---

## 📂 Dataset

The Titanic dataset contains passenger-level information including:

- Passenger ID
- Survival Status
- Passenger Class
- Passenger Name
- Gender
- Age
- Siblings/Spouses
- Parents/Children
- Ticket
- Fare
- Embarkation Port

### Dataset Statistics

- Total Records: **891**
- Original Columns: **12**
- Cleaned Columns: **11**
- Duplicate Records: **0**
- Missing Values After Cleaning: **0**

The `Cabin` column was removed during data preparation because it contained a large number of missing values.

---

## 🗄️ Database Structure

The cleaned Titanic dataset was loaded into the MySQL database:

**Database:** `netflix_analysis`

**Main Table:** `krish_data`

Two analytical tables were also created:

### passengers

Contains passenger-related information:

- PassengerId
- Name
- Sex
- Age
- SibSp
- Parch

### journey_details

Contains journey and survival information:

- PassengerId
- Survived
- Pclass
- Ticket
- Fare
- Embarked

The `PassengerId` column was used to connect the tables.

---

## 🔍 SQL Analysis Performed

### Query 1 – Combine Passenger and Journey Details

Used an `INNER JOIN` to combine passenger information with journey and survival information.

**SQL Concepts:**
- INNER JOIN
- SELECT

---

### Query 2 – Survival Analysis by Passenger Class

Analyzed the number of survivors in each passenger class.

**SQL Concepts:**
- JOIN
- GROUP BY
- COUNT

---

### Query 3 – Survival Analysis by Gender

Compared the number of survivors between male and female passengers.

**SQL Concepts:**
- JOIN
- GROUP BY
- COUNT

---

### Query 4 – Survival Rate by Gender

Calculated the survival percentage for each gender.

**SQL Concepts:**
- JOIN
- GROUP BY
- Aggregate Functions
- Percentage Calculation

---

### Query 5 – Average Age by Passenger Class

Calculated the average passenger age for each class.

**SQL Concepts:**
- JOIN
- GROUP BY
- AVG

---

### Query 6 – Average Fare by Passenger Class

Compared average ticket fares across passenger classes.

**SQL Concepts:**
- JOIN
- GROUP BY
- AVG
- ROUND

---

### Query 7 – LEFT JOIN Analysis

Used a `LEFT JOIN` to retain all passenger records while combining journey details.

**SQL Concepts:**
- LEFT JOIN

---

### Query 8 – Passengers Paying Above-Average Fare

Used a subquery to identify passengers whose fare was higher than the overall average fare.

**SQL Concepts:**
- Subquery
- AVG
- WHERE

---

### Query 9 – Above-Average Fare Survivors

Identified passengers who both survived and paid a fare above the overall average.

**SQL Concepts:**
- JOIN
- Subquery
- WHERE
- AND

---

### Query 10 – Passenger Classes with More Than 100 Passengers

Identified passenger classes containing more than 100 passengers.

**SQL Concepts:**
- JOIN
- GROUP BY
- HAVING
- COUNT

---

## 📊 Key Findings

### Overall Survival

- Total passengers: **891**
- Survivors: **342**
- Non-survivors: **549**
- Overall survival rate: **38.38%**

### Survival by Gender

- Female survivors: **233**
- Male survivors: **109**
- Female survival rate: approximately **74.20%**
- Male survival rate: approximately **18.89%**

The analysis shows a strong difference in survival outcomes between male and female passengers.

### Survival by Passenger Class

| Passenger Class | Passengers | Survivors | Survival Rate |
|---|---:|---:|---:|
| Class 1 | 216 | 136 | 62.96% |
| Class 2 | 184 | 87 | 47.28% |
| Class 3 | 491 | 119 | 24.24% |

The analysis indicates that survival outcomes varied substantially across passenger classes.

### Average Fare

The overall average passenger fare was approximately:

**32.20**

The higher passenger classes generally had higher average fares and higher survival rates.

---

## 💡 Business / Analytical Insights

The SQL analysis identified several important patterns:

1. Survival outcomes were strongly associated with passenger gender.
2. Passenger class showed a clear survival gradient, with first-class passengers having the highest survival rate.
3. Third-class passengers represented the largest passenger group but had the lowest survival rate.
4. Higher-fare passengers could be isolated using subquery-based analysis.
5. SQL JOINs allowed passenger and journey information to be analyzed together.

These findings demonstrate how SQL can be used to move from raw transactional records to meaningful analytical insights.

---

## 📁 Project Structure

```text
Titanic-SQL-Analysis/
│
├── data/
│   └── titanic_cleaned.csv
│
├── sql/
│   ├── titanic_analysis.sql
│   └── sample_outputs.txt
│
└── README.md
