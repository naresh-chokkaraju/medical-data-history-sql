# Medical Data History Analysis (SQL / MySQL)

## Overview
A set of 34 MySQL queries on a medical database, practising filters, joins, grouping, conditional counts, and calculated measures.

## Database
Database: `project_medical_data_history`

| Table | Contents |
|---|---|
| patients | Patient details, allergies, height, weight, birth date, province_id |
| admissions | Diagnoses, admission dates, attending_doctor_id |
| doctors | Doctor names and specialties |
| province_names | Full province names |

Joins used:
- `patients.patient_id = admissions.patient_id`
- `admissions.attending_doctor_id = doctors.doctor_id`
- `patients.province_id = province_names.province_id`

## SQL Concepts Covered
- Filtering: WHERE, LIKE, BETWEEN, IS NULL
- Text and date functions: CONCAT, date and time-part extraction
- Joins across multiple tables
- Aggregation: COUNT, GROUP BY, HAVING
- Conditional counts with CASE (for example male vs. female patients)
- Calculated measure: BMI-based obesity flag

## Notes from the Script Review
- Task 5 is an UPDATE that changes stored allergy values (NULL to 'NKA'), so run it deliberately.
- Task 9 can miss tied patients; a MAX(height) subquery returns all ties.
- Task 34 can repeat a patient; DISTINCT returns one row per patient.
- Task 33 should guard against zero or missing height before dividing.

## Tools
MySQL, SQL

## Files
- `MEDICAL_DATA_HISTORY.sql`: all 34 queries
- `Medical_Data_History_SQL_Script_Report.docx`: script review report
- `presentation.pptx`: project presentation
