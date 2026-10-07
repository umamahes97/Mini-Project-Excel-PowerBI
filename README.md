# MINI PROJECT- EXCEL & POWERBI

## PROJECT TITLE

## STUDENT PERFORMANCE ANALYSIS

## Project Overview:
  This project involves cleaning, transforming, and analysing raw data using Excel and creating an interactive Power BI dashboard to derive meaningful business insights.
  
## Objective:
  To evaluate student performance across different departments, identify the best-performing department, and analyse key factors such as attendance, study hours, and internal scores that influence final exam outcomes. The main objective is to demonstrate data pre-processing techniques using Excel and an interactive Power BI dashboard visualization to make informed decisions.
  
## Data Source:
• Source Description and Timeline: Google Dataset Search and 2024-2025.
• Domain: Education

## Problem Statement:

•	To Find the Missing Values and to impute the missing values by using aggregation functions.
•	To Analyse the duplicate Values in this data set.
•	To Analyse the Correlation between attendance and exam scores.
•	To Evaluate the Impact of study hours on performance levels.
•	To Analyse the Department-wise performance comparison.
•	To Identification of top-performing students and departments.

## Attribute (Column /Features) Details: 
## Attribute Name	Data Type	Description
  Student ID	Integer / String	Unique identifier for each Student
  Student Name	String (Text)	Name of the Student
  Gender	String (Text)	Female / Male 
  Age	Numeric Integer	Age of the employee in years
  Department	String (Text)	Types of the departments as CIVIL,MECH,ECE,EEE,CSE,IT
  Attendance	Numeric Integer	Attendance of the each student
  Study Hours	Numeric Integer	Number of hours studying for each student
  Internal Score	Numeric Integer	Internal Score of the Each Student
  Final Exam Score	Numeric Integer	Final exam Score of the Each Student
  Performance	String (Text)	Based on the final exam score of the each student.
## Four Types:
  Excellent, Good, Average, Poor

## Tools & Technologies:
●	Excel: Data cleaning, transformation, and Pivot Tables.
●	Power BI: Data modelling, DAX calculations, visualization, and interactive dashboard creation.

## Data Pre-Processing (Excel):

## Tasks Performed:

  ●	Data Cleaning & Transformation: Removed duplicates, handled missing values, standardized formats, and created calculated fields.
  •	Standardized department names and performance categories
  •	Converted numeric columns to proper data types
  •	Verified ranges for attendance and scores
  ●	Filtering & Sorting: Organized data to focus on relevant records.
  ●	Pivot Tables: Generated Pivot Tables for data summarisation and initial insights.

## Data Modelling and DAX (Power BI) :

 ## Data Modelling:
  In Power BI, the dataset was structured into a star schema for efficient analysis.
  
## Fact Tables:
  o	Raw Data Set / Cleaned Data → Contains student-level metrics (Attendance %, Study Hours, Internal Score, Final Exam Score, Performance).
  o	Imputed Data → Used for handling missing or inconsistent values.

## Dimension Tables:
o	Department → CSE, ECE, EEE, MECH, CIVIL, IT.
o	Student → Student_ID, Name, Gender, Age.
o	Performance Category → Excellent, Good, Average, Poor.

## Relationships:
o	Student_ID links fact tables with student details.
o	Department connects student records to departmental analysis.
o	Performance dimension enables grouping and visualization.
This model allows slicing data by Department, Age, Gender, Attendance, and Performance.

## DAX Measures:

## Attendance Metrics:
•	Total Attendance = SUM('Imputed Data'[Attendance_%])
•	Average Attendance = AVERAGE('Imputed Data'[Attendance_%])
•	Min Attendance = MIN('Imputed Data'[Attendance_%])
•	Max Attendance = MAX('Imputed Data'[Attendance_%])

## Performance Counts:
•	Count Excellent = CALCULATE(COUNTROWS('Imputed Data'), ‘Imputed Data'[Performance] = "Excellent")
•	Count Good = CALCULATE(COUNTROWS(''Imputed Data'), 'Imputed Data'[Performance] = "Good")
•	Count Average = CALCULATE(COUNTROWS('Imputed Data’),Imputed Data'[Performance] = "Average")
•	Count Poor = CALCULATE(COUNTROWS('Imputed Data’),Imputed Data'[Performance] = "Poor")

## Count of Student ID:
•	Total count =count(‘Imputed Data’[Student ID])

## Age Metrics:
•	Total Age = SUM('Imputed Data'[Age])
•	Average Age = AVERAGE('Imputed Data'[Age])
•	Min Age = MIN('Imputed Data'[Age])
•	Max Age = MAX('Imputed Data'[Age]) 

## Analysis and Visualizations (Power BI):

  1. Bar Chart : To Visualize the Department Vs Performance ,And to count the students based on Performance (Average, Good, Excellent, Poor).ECE is the best Performance compared to another Departments.

  2. Pie Chart: To Visualize the Department Vs Performance and Sum of Final Exam Score.

  3. Column Chart: To Visualize the Gender Vs Sum of study hours. Gender (Female   and Male).Female Study Hours is more than Male Study Hours. To visualize the Gender vs Sum of Final exam Score.

  4. Line & Clustered Column Chart: To Visualize the Count of Student ID and Age Vs Department and Performance.

  5. Funnel Chart: To Visualize the Department vs Count of Final Exam Score. ECE Is High Score .To used the filters and slicers with drill -down function.
  
  6. Donut Chart : To Visualize the Performance Vs Department Count. It Indicates the No of students In Performance Levels.

## Key Insights:
  The dashboard integrates Raw Data, Cleaned Data, and Imputed Data to provide a comprehensive view of student performance. It allows interactive analysis by department, age, gender, attendance, and performance categories.
  
## Key Visuals in the Dashboard:

## Department vs Performance Count:
  o	Shows how many students fall into Excellent, Good, Average, Poor categories per department.
  o	Example: ECE has the highest proportion of Excellent performers, while MECH shows more Poor cases.
  
## Attendance Analysis (Min, Max, Average):

  o	Displays attendance statistics for each department.
  o	Example: CIVIL average attendance ~79.9%, CSE ~81%, ECE ~79.2%.
  o	Helps identify departments with strong attendance discipline.
  
## Age Distribution by Department:

  o	Minimum and maximum ages (18–22) are consistent across departments.
  o	Count of students per age group shows balanced enrollment.
  
## Performance vs Final Exam Score:

 o	A clustered chart showing how exam scores align with performance categories.
 o	Excellent students consistently have higher final exam scores.
 
## Gender vs Study Hours:

  o	Compares total study hours between male and female students.
  o	Useful for analysing study behaviour differences.
  
## Department & Performance vs Final Exam Score (Sum):

  o	Aggregates exam scores by department and performance category.
  o	Confirms ECE and CSE contribute significantly to high scores.
 
## Insights from Dashboard:

  •	ECE Department → Best performing overall (high “Excellent” count, strong attendance).
  •	CSE Department → Largest student population, mixed performance.
  •	MECH & IT → Higher “Poor” cases, need improvement strategies.
  •	Attendance & Internal Scores → Strong predictors of final exam success.
  •	Gender Analysis → Both male and female students contribute equally to study hours, but performance varies by department.

## Conclusion:
  The analysis of student performance across six departments — CSE, ECE, EEE, MECH, CIVIL, and IT — highlights clear academic patterns.
  •	ECE Department consistently emerges as the top performer, with the highest proportion of Excellent students supported by strong attendance and internal scores.
  •	CIVIL Department also shows steady performance with high attendance and balanced results.
  •	CSE Department, despite having the largest student population, displays mixed outcomes, with both high achievers and weak performers.
  •	MECH and IT Departments reveal significant challenges, with higher counts of Poor performers, indicating the need for targeted interventions in attendance and study engagement.
  •	EEE Department maintains moderate performance, with scope for improvement in study consistency.
    Finally I get the cleaned with transformation data from Excel and Power BI with Data Visualization.









