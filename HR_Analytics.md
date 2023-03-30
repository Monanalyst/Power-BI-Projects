# Dashboard

![HR Analytics](https://user-images.githubusercontent.com/123024674/228867564-abdd1230-1e3e-4c1f-9fd0-5ea19ed177b3.png)


## Objectives

1. What is the highest attrition by gender?
2. What is the highest attrition by education?
3. What is the highest attrition by age?
4. What is the highest attrition rate salary slab?
5. What is the highest attrition rate job role?
6. What is the highest attrition by years at company?
7. Which job role has the highest number of employees who gave a score of 1 (lowest satisfaction)?

## Data Cleaning

I loaded a CSV dataset into Power BI and transformed the data using Power Query. To check for null values efficiently, I enabled the ‘Column quality’ option in the ‘View’ tab. This showed an overview of the total null values as a percentage under the ‘Empty’ area.

One column had null values but was not needed, so I removed it completely. If I had needed this column, I would have sorted it in ascending order and identified the starting and ending row numbers containing null values. Then, I would have clicked on ‘Remove Rows’ and ‘Remove Top Rows’ to enter the total number of rows to remove.

I checked the primary key column ‘EmpId’ for duplicates by clicking on ‘Group By’ and using the count function. A count of 1 meant that the EmpId was unique, while anything greater than 1 indicated a duplicate. I identified 10 duplicates where the EmpId was repeated twice. This method was used for checking purposes only, so I removed this step from ‘Applied Steps’ once I established the total number of duplicates.

To remove duplicates from the entire dataset, I selected every column and row using CTRL + A, then right-clicked and removed duplicates. In the ‘BusinessTravel’ column, there were two separate string values that should have been one. To fix this, I replaced the value ‘TravelRarely’ with ‘Travel_Rarely’ to match the value convention format used across other text values.

I created a new column by clicking on ‘Conditional Column’ and naming it ‘AttritionCount’. If the ‘Attrition’ column was equal to ‘Yes’, the output was 1; otherwise, it was 0. This method was used because the ‘Attrition’ column only contained ‘Yes’ and ‘No’ values. The new column will be used to create a metric card in the visualisation.

Finally, I selected all columns and clicked on ‘Detect Data Type’ to ensure that all columns were in the correct format.

## Findings

The Research & Development department is facing some challenges with employee retention. A significant number of employees are leaving, particularly those with a background in Life Sciences or Medical and those in the 26-35 age range. It’s interesting to note that Laboratory Technicians seem to have lower job satisfaction scores compared to other roles where the low salary could be a key factor. Also, the spike in attrition among employees in their first year at the company is the highest.

In the Sales department a significant number of employees are also leaving, particularly those aged 26-35 and those with a background in Marketing or Life Sciences. Salary also seems to be a factor in their decision to leave. The low job satisfaction among Sales Executives could be contributing to their high attrition rate. There is a spike in attrition among employees in their first year at the company in the Sales department as well. 

The Human Resources department has a total of 63 employees and 12 have left. Despite being a smaller department compared to others in the company, it is still important to address any challenges with employee retention and job satisfaction. This department also has 26-35 years old being the majority leaving with low salary being a potential key factor in their decision.

## Key Points

- All three departments are facing challenges with employee retention.
- The age group with the highest attrition rate in all three departments is 26-35 years old.
- Salary seems to be a factor in the decision to leave for employees in all three departments.
- There is a spike in attrition among employees in their first year at the company in both the Research & Development and Sales departments.
- The company’s staff is made up of 60% male and 40% female. When it comes to employees leaving, more males left than females.

## Recommendations

- Conduct exit interviews with employees who leave to better understand their reasons for leaving and identify areas for improvement.
- Explore opportunities for career growth or development to help retain employees, particularly those aged 26-35.
- Review salary and compensation packages to ensure they are competitive with industry standards.
- Look into issues with new employees fitting in and consider measures to improve their experience and retention.



