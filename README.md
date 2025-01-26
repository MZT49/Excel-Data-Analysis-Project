# Excel-Data-Analysis-Project
An Excel-based data analysis project completed from Luke Barousse's Excel course, showcasing practical data analysis and visualization skills.
# Excel Salary Dashboard

![Screenshot 2025-01-24 160130](https://github.com/user-attachments/assets/ae77c787-8d04-42bb-8842-9b7b4a2e216b)

## Introduction

This salary dashboard project is my customized take on the original project provided in Luke Barousse's Excel course. It serves as a tool for job seekers to explore salary trends across various roles in data-related fields. This dashboard showcases salaries based on job titles, locations, and job types, enabling users to make informed career decisions.

### Dashboard File

My final dashboard file: [**Excel\_Data\_Analysis\_Project.xlsx**](Excel_Data_Analysis_Project.xlsx).

---

### Excel Skills Highlighted

In creating this project, I applied several core Excel skills, including:

- **📊 Data Visualization**: Charts and graphs to convey insights clearly.
- **🧮 Advanced Formulas**: Multi-condition filtering, aggregations, and dynamic calculations.
- **✔️ Data Validation**: Ensuring consistent and accurate data inputs.

---

## About the Dataset

This dataset comprises real-world job market data for data-related roles in 2023. It includes details such as:

- **💼 Job Titles**
- **💰 Salaries**
- **🌍 Locations**
- **🛠️ Key Skills**

The original dataset was part of the course, but I made modifications for this dashboard to better suit my analysis.

---

## Dashboard Components

### 📈 Visualizations

#### Job Salaries by Role (Bar Chart)

- **Objective**: Highlight salary variations across job roles.
- **Implementation**: A horizontal bar chart sorted by descending salaries for intuitive comparison.
- **Insights**: Senior roles like engineers and managers offer significantly higher pay compared to analyst roles.

#### Median Salaries by Country (Map Chart)

- **Objective**: Understand global salary trends.
- **Implementation**: A map chart with color gradients indicating salary ranges.
- **Insights**: Clear disparities between regions, with countries like the US offering higher median salaries.

---

### 🧮 Advanced Formulas

#### Median Salary Calculation by Role

**Formula Example:**

```
=MEDIAN(
IF(
    (jobs[job_title_short]=A2)*
    (jobs[job_country]=country)*
    (ISNUMBER(SEARCH(type,jobs[job_schedule_type]))) *
    (jobs[salary_year_avg]<>0),
    jobs[salary_year_avg]
)
)
```

- **Purpose**: Calculate median salary based on multiple criteria (role, location, job type).
- **Dynamic Filtering**: Ensures only relevant data is used for accurate results.

#### Unique Job Types List

**Formula Example:**

```
=FILTER(J2#, (NOT(ISNUMBER(SEARCH("and", J2#)) + ISNUMBER(SEARCH(",", J2#)))) * (J2#<>""))
```

- **Purpose**: Generate a clean list of unique job types for filtering.
- **Application**: Used in dropdowns for user input validation.

---

### ✅ Data Validation

To enhance usability, I implemented data validation rules for:

- **Job Titles**
  
![Screenshot 2025-01-26 160003](https://github.com/user-attachments/assets/f59883db-a69d-480c-aa26-08d101d44d1a)

- **Countries**

  ![Screenshot 2025-01-26 160029](https://github.com/user-attachments/assets/eac86a0b-c76e-44d5-9050-18aa7926a53d)

- **Job Types**

  ![Screenshot 2025-01-26 160055](https://github.com/user-attachments/assets/ee84a71f-9691-41d9-8382-d786d2cc3962)


This ensures consistent input and eliminates errors caused by invalid entries.

---

## Insights and Takeaways

- Senior-level roles and specialized positions tend to command higher salaries.
- Geographic location significantly influences salary ranges, with notable disparities between countries.
- Data validation and advanced formulas make the dashboard user-friendly and efficient for exploring the dataset.

---

## Personal Reflection

This project allowed me to refine my Excel skills and apply them to solve real-world data analysis problems. It showcases my ability to handle data, draw meaningful insights, and present them in an accessible way.

Feel free to check out the project and share your feedback. Connect with me on [**LinkedIn**](https://www.linkedin.com/in/maruffuzzman-tanvir) to discuss this project or any collaboration opportunities.

