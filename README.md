# Employee-Attrition-Analysis

## Dataset
The project uses the IBM HR Analytics Attrition & Performance dataset.
The dataset contains employee-related information, including demographic characteristics, job roles, compensation, job satisfaction, working conditions and employee attrition.

## Dataset Inspection

When first opening the dataset I have found 0 missing values and 0 duplicate records.

##Data Structure

The dataset contains both numerical and categorical variables.
Examples:
- Numerical: Age, MonthlyIncome, YearsAtCompany
- Categorical: Department, Gender, Attrition, OverTime

## Assessment

As of the first inspection there are no missing values or duplicate records to be found.
Further data quality checks and preparation will be conducted before the analytical phase.

<img width="1910" height="925" alt="image" src="https://github.com/user-attachments/assets/12aed2d4-e831-4be6-9fe3-10579bf8c383" />

# Data Cleaning & Preparation

## 1. Initial Data Quality Assessment

The original dataset contains 1470 employee records and 35 columns.
The initial data quality assessment identified:
- No missing values
- No duplicate records
- 26 numerical columns
- 9 text-based columns

## 2. Data Preparation

The original dataset was duplicated to preserve the raw data.
All cleaning operations are performed on a separate working copy.

## 3. Removal of Redundant Columns

Three columns were identified as redundant:
EmployeeCount, Over18, StandardHours
They all had a constant value across all records and provide no additional analytical value.

## 4. Identifier Handling

EmployeeNumber is retained as a unique employee identifier.
It will not be used as an analytcal measure.

## 5. Data Type Considerations

Variables such as Education, JobLevel and JobSatisfaction contain numerical codes representing ordinal categories.
These variables will be treated according to their analytical meaning rather than automatically as continuous numerical measures.

## 6. Next Steps

- Validate the cleaned dataset
- Review categorical variables
- Prepare  the dataset for exploratory analysis and Power BI

# Exploratory Data Analysis

## 1. Overall Employee Attrition

The first analysis examines the overall employee attrition within the dataset.

### Key Metrics

Total Employees 1470
Employees Who Left 237
Employees Who Stayed 1233
Attrition Rate 16.12%

### Initial Observation

Approximately 16.12% of employees in the dataset have left the company. This metric provides an initial overview of employee turnover and serves as the baseline for further analysis.
Further investigations will examine potential relationships between attrition and demographic characteristics, departments, working conditions and employee satisfaction.

## 2. Attrition by Age Group

### Objective
Analyze whether employee attrition differs across age groups.

### Methodology
Employees were divided into five age groups:
- 18.25
- 26-35
- 36-45
- 46-55
- 56+

Attrition rates were calculated for each group.

### Results

| Age Group | Attrition Rate |
|---|---:|
| 18.25 | 35.77% |
| 26-35 | 19.14% |
| 36-45 | 9.1% |
| 46-55 | 11.50% |
| 56+ | 17.02% |

### Key Finding
The highest attrition rate was observed among employees aged 18-25 (35.77%).
The lowest rate was observed among employees aged 36-45 (9.19%).

### Interpretation
The results indicate differences in employee attrition across age groups.
However, age alone does not explain employee turnover. Further analysis of job satisfaction, tenure, compensation and working conditions is required.

## 3. Attrition by Department

### Objective
Analyze employee attrition across different organizational departments.

### Methodology
Employees were grouped by department.
The attrition rate was calculated by dividing the number of employees who left by the total number of employees in each department.

### Results

| Department | Employees | Employees Left | Attrition Rate |
|---|---:|---:|---:|
| Human Resources | 63 | 12 | 19.05% |
| Research & Development | 961 | 133 | 13.84% |
| Sales | 446 | 92 | 20.63% |

### Key Findings
- Sales has the highest attrition rate at 20.63%.
- Research & Development has the lowest attriton rate at 13.84%.
- Human Resources has an attrition rate of 19. 05%.

### Interpretation
Employee attrition differs across organizational departments.
Sales shows the highest attrition rate, including that this department may require further investigation.
The results do not establish causal relationships. Additional analysis of working conditions, compensation and job satisfaction is necessary.

## 4. Attrition by Overtime

### Objective
Investigate the relationship between overtime work and employee attrition.

### Methodology
Employees were divided into two groups:
- Employees working overtime
- Employees not working overtime

The attrition rate was calculated for each group.

### Results
| Overtime | Employees | Employees Left | Attrition Rate |
|---|---:|---:|---:|
| No | 1,054 | 110 | 10.44% |
| Yes | 416 | 127 | 30.53% |

### Key Finding
Employees working overtime have a substantially higher attrition rate (30.53%) compared to employees who do not work overtime (10.44%).
The attrition rate is almost three times higher among employees working overtime.

### Interpretation
The results indicate a strong asssociation between overtime work and employee attrition.
This may suggest that workload and working conditions are relevant factors for employee retention.
However, the analysis does not establish causation. Other variables, such as job role, department and job satisfaction, may also influence this relationship.

## 5. Attrition by Tenure

### Objective
Analyze the relationship between employee tenure and attrition.

### Methodology
Employees were grouped according to their years at the company:
- 0-1 years
- 2-5 years
- 6-10 years
- 11-20 years
- 21+ years

The attrition rate was calculated for each group.

### Results

| Tenure Group | Employees | Employees Left | Attrition Rate |
|---|---:|---:|---:|
| 0–1 | 215 | 75 | 34.88% |
| 2–5 | 561 | 87 | 15.51% |
| 6–10 | 448 | 55 | 12.28% |
| 11–20 | 180 | 12 | 6.67% |
| 21+ | 66 | 8 | 12.12% |

### Key Findings
Employees with 0-1 years of tenure show the highest attrition rate at 34.88%.
The lowest attrition rate was observed among employees with 11-20 years of tenure (6.67%).

### Interpretation
The results indicate that employees with shorter tenure are more likely to leave the company.
This suggests that onoarding, early employee engagement and retention strategies may deserve further investigation.
The findings indicate an association, not a causal relationship.

## 6. Attrition by Job Satisfaction

### Objective
Investigate the relationship between employee job satisfaction and attrition.

### Methodology
Employees were grouped according to their job satisfaction scores, ranging from 1 (Low) to 4 (Very High).
The attrition rate was calculated for each satisfaction level.

### Results

| Job Satisfaction | Employees | Employees Left | Attrition Rate |
|---|---:|---:|---:|
| 1 - Low | 289 | 66 | 22.84% |
| 2 - Medium | 280 | 46 | 16.43% |
| 3 - High | 442 | 73 | 16.52% |
| 4 - Very High | 459 | 52 | 11.33% |

### Key Findings
Employees with low job satisfaction show the highest attrition rate (22.84%).
Employees with very high job satisfaction show the lowest attrition rate (11.33%).

### Interpretation
The results indicate an association between job satisfaction and employee attrition.
This suggests that employee satisfaction monitoring and engagement initiatives may support retention efforts.
However, the analysis does not establish causation.

## 7. Summary of Key Findings

The exploratory data analysis revealed several patterns associated with employee attrition.

### Main Findings
- Overall Attrition: 237 out of 1470 employees left the company, resulting in an overall attrition rate of 16.12%.
- Age: Employees aged 18-25 showed the highest attrition rate (35.77%).
- Department: The Sales department had the highest attrition rate (20.63%).
- Overtime: Employees working overtime had an attriton rate of 30.53%, compared to 10.44% for employees without overtime.
- Tenure: Employees with 0-1 years of compan tenure had the highest attrition rate (34.88%).
- Job Satisfaction: Employees with low job satisfaction had a higher attrition rate (22.84%) than employees with very high job satisfaction (11.33%).

### Overall Interpretation
The analysis indicates that attrition is not equally distributed across employee groups. Younger employees, employees with short company tenure, employees working overtime, and employees in the Sales department show comparatively high attrition rates.
These findings provide starting points for further investiagtion and potential HR interventions.

Limitation:
The analysis identifies statistical associations, not causal relationships. Further analysis would be required to determine the underlying reasons for employee attrition.
<img width="435" height="286" alt="image" src="https://github.com/user-attachments/assets/0eeb4ffd-fa64-43e7-95d0-8015c355e1bb" />

## Power BI Dashboard

<img width="1457" height="796" alt="Screenshot 2026-11-25 111954" src="https://github.com/user-attachments/assets/e9fb9ffc-bba1-4c18-bf52-ab4bdf0c4d15" />

<img width="1442" height="812" alt="Screenshot 2026-11-25 112031" src="https://github.com/user-attachments/assets/dd4b1e80-8135-4c75-9d83-12189fb1be92" />

# HR Recommendations

Based on the exploratory data analysis and Power BI dashboard, several potential areas for improvement were identified.

## 1. Improve Employee Onboarding

Employees with 0-1 years of company tenure showed the highest attrition rate (34.88%).

### Recommendation:
- Introduce structured onboarding programs
- Establish mentoring and buddy systems
- Conduct regular check-ins during the first year

## 2. Review Overtime and Workload

Employees working overtime had an attrition rate of 30.53%, compared to 10.44% among employees without overtime.

Recommendation:
- Monitor overtime frequency
- Review workload distribution
- Evaluate work-life balance initiatives

## 3. Strengthen Sales Employee Retention

The Sales department showed an attrition rate of 20.63%. Sales Representatives had an especially high rate of 39.76%.

Recommendation:
- Investigate job-specific challenges
- Review performance expectations and workload
- Evaluate compensation and carreer development opportunities

## 4. Improve Employee Satisfaction

Employees with low job satisfaction showed an attrition rate of 22.84%, compared to 11.33% among employees with very high satisfaction.

Recommendation:
- Conduct regular employee satisfaction surveys
- Improve employee feedback processes
- Support leadership and management development

# Conlcusion

The analysis highlights several workforce segments that may require additional attention. Targeted HR initiatives could help improve employee retention and reduce turnover.

Limitation: These recommendation are based on observed statistical associations. The analysis does not establish causal relationships.

# Skills Development & Learning Process

Throughout this project, I focused on improving my practical skills in Excel and Power BI, particularly in data cleaning, data modeling and DAX. I also placed greater emphasis on data quality, selecting appropriate metrics, interpreting results correctly, and translating analytical findings into meaningful business insights.
Additionally, I learned to use AI tools more effectively as part of my workflow. I used AI to support problem-solving, improve workflow efficiency, structure tasks, and create more professional and consistent project documentation.
Overall the project helped me develop a more structured approach to data analysis while combining technical skills, AI-assisted workflows, and business-oriented thinking.




