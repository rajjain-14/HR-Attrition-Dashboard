# HR-Attrition-Dashboard

Title : HR_ATTRITION_DASHBOARD

Objective :
The main aim of this dashboard is to study the Employee attrition (people leaving the company) and understand which factors affect it the most. The dashboard helps to identify patterns and causes of attrition using data visualization.

Data Source : 
This dataset contains detailed employee records from an organization, including departments, job roles, income, satisfaction, and attrition status.
It is used to analyze the key factors influencing employee turnover and workforce trends. 
Dataset - HR-Employee-Attrition
Source - Kaggle

Data Cleaning :
Removed unnecessary columns.
Checked and handled null values.
Remove the duplicate values.
Check the datatypes.

DAX Measures Created :

1.	Attritioncount - The total number of employees who left the company.
Formula :IF(Employees_Data[Attrition]="Yes",1,0)



2.	Attrition rate - The percentage of employees who left the company
Formula : SUM(Employees_Data[Attritioncount])/SUM(Employees_Data[EmployeeCount])



3.	Male Employees - This gives the count of all male employees in the company.
Formula :  CALCULATE(
    											COUNT(Employees_Data[EmployeeNumber]),
                  Employees_Data[Gender] = "Male"
                                )



4.	Female Employees - This gives the count of all female employees in the company.
Formula : CALCULATE(
                  COUNT(Employees_Data[EmployeeNumber]),
                  Employees_Data[Gender] = "Female"
                  )


Visuals used in the Dashboard :


1. KPI Cards - Top Cards
 Description : These cards display important summary metrics such as:

Count of Employees - The total employees in the company.

Attrition - It represents the number of employees who have left the company.

Average Age - The average age of employees in the company.

Average Salary - The mean value of monthly income of all employees.

Average Years - The average tenure of employees in the company.


 2. Donut Chart – Attrition by Education
 Description : Shows the percentage of attrition based on employees’ education fields (Life Sciences, Medical, Technical, etc.).
 									   It helps identify which educational background has the highest turnover.

3. Column Chart – Attrition by Age 
Description : Shows how attrition changes across different age ranges.

4. Line Chart – Attrition by Years at Company
Description : Shows the trend of attrition based on how long employees have worked in the company.
 
5. Bar Chart – Attrition by Salary
 Description : Shows the number of employees leaving the company based on their income levels 
 
6. Matrix Table – Attrition by Rating
 Description : Displays attrition counts categorized by job role and performance rating. It identifies specific job roles ( like Sales   Executive or Lab Technician) with  high attrition.

7. Treemap – Gender
 Description : Visualizes total attrition split by gender.

8. Slicers – Department
 Description : Interactive filters that allow users to select a particular department to view related visuals.


Key Insights :

Cards : Shows Total employees (1470), Attrition (237), Avg age (37), Avg salary (7K), and Avg years (7).

Attrition by Education : Highest in Life Sciences (38%) and Medical (27%).

Attrition by Age : Mostly between 26–35 years.

Attrition by Salary : Most employees leaving earn below 5K

Attrition by Years at Company : Highest in early service years (1–2 years).

Attrition by Rating : Sales Executives and Lab Technicians show the highest attrition.

Screenshot of the Dashbord : 
