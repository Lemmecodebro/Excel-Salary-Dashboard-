# 📊 Excel Salary Dashboard

![Salary_Dashboard_Final_Dashboard](https://github.com/user-attachments/assets/0fbef0ad-ca37-4d5e-be70-c86723dec275)


---

## 🧠 Overview
The **Excel Salary Dashboard** visualizes salary data across various data-related job titles, helping job seekers understand salary trends, evaluate compensation fairness, and identify high-paying roles by region and job type.

This project uses real-world 2023 data from data-related positions, covering **job titles, salaries, countries, and essential skills**.  
It was built entirely using **Microsoft Excel**, demonstrating data analysis, visualization, and interactivity skills.

---

## 📁 Project Files
- 📄 **Final Dashboard File:** [`Final_Salary_Dashboard.xlsx`](Final_Salary_Dashboard.xlsx)

---

## 💡 Excel Skills Utilized
- 📉 **Charts & Data Visualization**
- 🧮 **Formulas & Functions**
- ❎ **Data Validation & User Input Controls**

---

## 🧩 Dataset Information
The dataset includes real-world job data from 2023 with information on:

- 👨‍💼 Job Titles  
- 💰 Salaries  
- 📍 Locations  
- 🛠️ Key Skills  

---

## 🛠️ Dashboard Build Process

### 1️⃣ Charts

#### 📊 Data Science Job Salaries – Bar Chart
<img width="797" height="498" alt="image" src="https://github.com/user-attachments/assets/8a4f801d-a548-45ef-af28-104da59909ba" />


**Excel Features Used:**
- Created a **horizontal bar chart** with formatted salary values  
- Sorted job titles in descending salary order  
- Designed a minimal layout for better readability  

**Insights:**
Senior roles and Engineering positions generally pay higher than Analyst roles.

---

#### 🗺️ Country Median Salaries – Map Chart
![1_Salary_Dashboard_Country_Map](https://github.com/user-attachments/assets/9d89205a-374b-46c4-9e7b-71e4be03fb08)



**Excel Features Used:**
- Used Excel’s **map chart** to display salary distribution by country  
- Applied color-coding to differentiate salary ranges  
- Optimized readability for global comparison  

**Insights:**
Helps identify high and low median salary regions worldwide.

---

### 2️⃣ Formulas and Functions

#### 💰 Median Salary by Job Title

```excel
=MEDIAN(
IF(
    (jobs[job_title_short]=A2)*
    (jobs[job_country]=country)*
    (ISNUMBER(SEARCH(type,jobs[job_schedule_type])))*
    (jobs[salary_year_avg]<>0),
    jobs[salary_year_avg]
)
)
```

**Purpose:**
Calculates the median salary filtered by job title, country, and schedule type while excluding blank salary entries.

**Background Table**
<img width="265" height="220" alt="image" src="https://github.com/user-attachments/assets/bab8d694-7f83-4f1c-a4d0-c6fb0733bb38" />

**Dashboard Implementation**
<img width="484" height="520" alt="image" src="https://github.com/user-attachments/assets/dc6815b8-04dc-4df9-8760-c11ce79258dc" />

```excel
**⏰ Count of Job Schedule Type**
=FILTER(J2#,(NOT(ISNUMBER(SEARCH("and",J2#))+ISNUMBER(SEARCH(",",J2#))))*(J2#<>0))
```
**Purpose:**
Generates a list of unique job schedule types by filtering out duplicates, invalid entries, and zero values.

**Background Table**

<img width="195" height="119" alt="image" src="https://github.com/user-attachments/assets/fdcf29fb-00a5-412b-af87-b48647dc37e6" />

**Dashboard Implementation**

<img width="484" height="520" alt="image" src="https://github.com/user-attachments/assets/a58169b5-a4e8-4611-b7cb-3c7044e0b07d" />

**3️⃣ Data Validation**

<img width="524" height="502" alt="image" src="https://github.com/user-attachments/assets/18ffdb10-6730-4d0b-aa22-2eac04fe4bef" />


**Implementation Details:**

- Applied data validation to dropdown filters for Job Title, Country, and Type

- Ensures consistent and correct user input

- Prevents typing errors or invalid entries

Benefits:

- 🎯 Cleaner and validated user data

- 🚫 Eliminates inconsistent entries

- 👥 Enhances usability of the dashboard


**✅ Conclusion**

This Excel dashboard provides a clear, interactive way to explore salary trends across data-related roles worldwide.
It combines visualization, formulas, and interactivity to help users:

- Understand how job title and location influence compensation

- Identify salary patterns in data science roles

- Make more informed career and negotiation decisions
