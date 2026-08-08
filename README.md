# HR Data Analytics Dashboard

This project is a Power BI dashboard created to analyse employee attrition and workforce data.

The dashboard focuses on understanding employee attrition across departments, job roles, age groups, salary slabs, overtime status, and job levels. Power Query was used for data preparation and DAX was used to create the required measures and KPIs.
## Dashboard

![HR Analytics Dashboard](images/dashboard.png)
## Tools Used

- Power BI
- Power Query
- DAX
- Microsoft Excel
## What I Analysed

The dashboard covers:

- Total employees
- Total employee attrition
- Overall attrition rate
- Average employee age
- Attrition by department
- Attrition by job role
- Attrition by age group
- Attrition by salary slab
- Attrition by overtime
- Attrition by job level

The dashboard also includes slicers for:

- Department
- Job Role
- Gender
- Overtime

These slicers allow users to explore employee attrition from different perspectives.
## Data Preparation

Power Query was used to prepare the HR dataset before creating the dashboard.

The main steps included:

- Loading the HR dataset into Power BI
- Checking and correcting data types
- Checking the dataset for missing values
- Reviewing categorical and numerical fields
- Preparing the data for analysis and visualization
## Key Findings

Some of the main observations from the dashboard are:

- The overall employee attrition rate is 16.1%.
- The 26-35 age group has the highest employee attrition.
- Laboratory Technicians have the highest attrition among the job roles.
- Employees in the 6-10 LPA salary slab have the highest attrition.
- Job Level 1 has the highest attrition.
- Employees who work overtime show higher attrition than employees who do not work overtime.
## DAX Measures

Some of the measures used in the dashboard include:

```DAX
Total Employees = DISTINCTCOUNT('HR Data'[EmpID])

Total Attrition =
CALCULATE(
    DISTINCTCOUNT('HR Data'[EmpID]),
    'HR Data'[Attrition] = "Yes"
)

Attrition Rate =
DIVIDE(
    [Total Attrition],
    [Total Employees],
    0
)

Average Age =
AVERAGE('HR Data'[Age])
```

## Project Structure

```text
HR_Data_Analytics/
│
├── dashboard/
│   └── HR_Analytics.pbix
│
├── dataset/
│   └── HR_Analytics_dataset.csv
│
├── Images/
│   └── dashboard.png
│
└── README.md
```
## How to Use

Download the repository and open the `HR_Analytics.pbix` file from the `dashboard` folder using Power BI Desktop.

Use the slicers on the dashboard to filter the employee data by department, job role, gender, and overtime status.
## Dataset

The project uses an HR employee dataset containing information about employee demographics, departments, job roles, salary slabs, overtime status, and attrition.

The dataset is included in the `Dataset` folder.

## Author

**Yaswitha**

Power BI | DAX | Power Query | Data Analysis
