
# HR Analytics Dashboard

### Dashboard Link : https://app.powerbi.com/groups/me/reports/4c514784-16fa-46ea-a43f-d9eaa0f3a11c/ReportSection?experience=power-bi

## Problem Statement

This dashboard serves as a tool for HR,
Assisting in the identification of patterns and trends,
Specifically in employees attrition.
It enables the team to analyze data,
And make informed decisions,
To mitigate attrition risks effectively.


### Steps followed 

- Step 1 : Load data into Power BI Desktop, dataset is a csv file.
- Step 2 : Open power query editor & in view tab under Data preview section, check "column distribution", "column quality" & "column profile" options.
- Step 3 : Performing an ETL (Extract, Transform, Load) process and executing DAX (Data Analysis Expressions) queries involves several steps.
- Step 4 : Calculated column was created in which, employees were grouped into various age groups.

for creating new column following DAX expression was written;
       
    let

        age =[Age],
        AgeGroup = 
        if age>= 18 and age<=25 then "18-25"
        else if age >= 26 and age<= 35 then "26-35"
        else if age>=36 and age<= 45 then "36-45"
        else if age>=46 and age<= 55 then "46-55"
        else "55+"
    in 
        AgeGroup
        
Snap of new calculated column ,.
![ageGroup](https://github.com/kaushalsingh0410/HR_Analytics/assets/161219395/31bd8354-126c-4646-a3b9-7e529cdd9f1e)
- Step 5 : Calculated column was created in which, salary of employees were grouped into various salary groups.

for creating new column following DAX expression was written;
       
    let 
        salary = [MonthlyIncome],
        salarySlab1 =
        if salary<5000 then "LessThan 5K"
        else if salary>=5000 and salary<10000 then "5-10k"
        else if salary>=10000 and salary<15000 then "10-15k"
        else "15k+"
    in 
        salarySlab



Snap of new calculated column.
![salatySlab](https://github.com/kaushalsingh0410/HR_Analytics/assets/161219395/47476d31-d552-4137-ab12-a59ac8468ec9)

- Step 6 : Make some KPI card visuals: Total Employees, Total Attrition, Attrition Rate, Average Age of Employee, Average Salary of Employee, Average Years of Employee in the Company.

Snap of new calculated column.
![KPI](https://github.com/kaushalsingh0410/HR_Analytics/assets/161219395/8f6c32ba-e279-482a-9b41-fa46a759431f)

- Step 7 : Add more visuals to analyze the Attrition by Education, Age, Job Role, Salary, Job Satisfaction, Years at Company. 
 
 - Step 8 : The report was then published to Power BI Service.
 
 


# Snapshot of Dashboard (Power BI Service)

![Dash](https://github.com/kaushalsingh0410/HR_Analytics/assets/161219395/833ece24-0f47-4257-a939-cd6f6fdea994)

 
 # Report Snapshot (Power BI DESKTOP)

 
![report](https://github.com/kaushalsingh0410/HR_Analytics/assets/161219395/4d6edf2b-6ca9-4a55-94e4-060d460c026e)


# Insights

A single page report was created on Power BI Desktop & it was then published to Power BI Service.

Following inferences can be drawn from the dashboard;

### 1 Years At  Company

  Attrition rate is highest in 1st year (57), 2nd year (26), 3rd year (20).

 Employee leave company when they complete 5 or 10 years at the company.
           
### 2 Salary

Employees who have salary less than 5K (which is less than the average salary of 7K) leave the job (158)

Attrition rate is also high between the salary range of 5 to 10K (48).  
  
  ### 3 Education 
  
Most of the employees from the background of Education in 'Life Sciences' (88) and 'Medical' (57) leave the company.

 ### 4 Age
 
 Employees of age group 26 to 35 years have the highest attrition rate (111)


