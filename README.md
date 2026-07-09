# End-to-End-Data-Cleaning-in-MySQL
**Project Overview**

Real-world datasets are rarely clean. Missing values, duplicate records, inconsistent formatting, and incorrect data types can affect the accuracy of any analysis. This project focuses on cleaning a global layoffs dataset using SQL by following a structured data cleaning workflow before performing any exploratory data analysis.
The objective was to transform the raw dataset into a reliable, analysis-ready dataset by identifying duplicate records, standardizing values, handling missing data, correcting formatting inconsistencies, and removing unnecessary records.
This project was inspired by Alex The Analyst's SQL Data Cleaning tutorial, and I implemented the complete workflow while understanding the purpose behind each transformation.
- - - 
**Dataset**

The dataset contains information about layoffs across companies worldwide, including:
•	Company  

•	Industry 

•	Location 

•	Total Employees Laid Off 

•	Percentage Laid Off 

•	Date 

•	Funding Stage 

•	Country 

•	Funds Raised (Millions) 
- - -
**Tools Used**

•	MySQL 

•	SQL 

•	Window Functions 

•	Common Table Expressions (CTEs) 

•	Data Cleaning Techniques 
- - -
**Data Cleaning Process**
Created a Staging Table:

To preserve the original dataset, I first created a staging table and performed all cleaning operations on the copied data.

Removed Duplicate Records:

Used the ROW_NUMBER() window function to identify duplicate rows based on multiple business-related columns.
Duplicate entries were isolated and removed while ensuring legitimate repeated layoffs were retained.

Concepts Used:

•	Window Functions 

•	ROW_NUMBER() 

•	PARTITION BY 

•	Staging Tables 

Standardized Data:

Improved data consistency by:

•	Filling missing industry values using self joins 

•	Converting blank values to NULL 

•	Standardizing different industry names 

•	Removing unnecessary punctuation from country names 

•	Formatting date values into SQL DATE format 

•	Converting incorrect data types 

Handled Missing Values:

Reviewed NULL values across the dataset and retained meaningful NULLs that could provide useful information during future analysis instead of replacing them with arbitrary values.

Removed Unnecessary Records:

Deleted rows where both total layoffs and layoff percentages were unavailable since they provided no analytical value.
Temporary helper columns created during cleaning were also removed to produce the final cleaned dataset.
- - -
**SQL Concepts Demonstrated**

•	Data Cleaning Workflow 

•	Window Functions 

•	ROW_NUMBER() 

•	PARTITION BY 

•	Self Joins 

•	UPDATE Statements 

•	DELETE Operations 

•	ALTER TABLE 

•	Data Type Conversion 

•	STR_TO_DATE() 

•	TRIM() 

•	NULL Handling 

•	Data Standardization 

•	Staging Tables 
- - -
**Key Learning Outcomes:**

Through this project, I strengthened my understanding of how SQL is used for real-world data preparation before analysis. Instead of simply removing duplicates or correcting formatting, I learned the importance of preserving raw data, validating records before deletion, handling missing values thoughtfully, and creating consistent datasets that improve the reliability of downstream analytics.This project also improved my confidence in using window functions, joins, update operations, and data transformation techniques commonly used by data analysts in production environments.
- - - 

**Visualisation:**
<img width="1878" height="950" alt="Screenshot 2026-07-09 173653" src="https://github.com/user-attachments/assets/7e429552-3ef7-4883-9e4d-642d124e4c76" />
