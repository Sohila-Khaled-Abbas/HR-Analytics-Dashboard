# HR Analytics Power BI Dashboard  

🚀 **An interactive and insightful Power BI Dashboard for HR analytics, featuring employee attendance and leave management insights.**  

## Table of Contents  
- [Project Overview](#project-overview)  
- [Features](#features)  
- [Getting Started](#getting-started)  
  - [Prerequisites](#prerequisites)  
  - [Installation](#installation)  
- [Data Insights](#data-insights)  
  - [Attendance Insights Page](#attendance-insights-page)  
  - [Leave Insights Page](#leave-insights-page)  
- [DAX Measures](#dax-measures)  
- [Design Inspiration](#design-inspiration)  
- [Resources](#resources)  
- [License](#license)  

---

## Project Overview  
This dashboard was created using **Power BI** to streamline HR analytics. It visualizes employee attendance and leave data, enabling HR teams to make data-driven decisions.  

🔗 **[Live Dashboard](https://app.powerbi.com/groups/808869fc-e1b7-4ff5-87ed-b9dcaaf02f4e/reports/b1482fb6-65c8-4257-bcfa-491d319dae89?ctid=27a388d0-1a33-462f-a48b-52c5342daf56&pbi_source=linkShare)**  

### Pages Included:
1. **Attendance Insights**:  
   - 📊 **Cards**:  
     - Presence %  
     - Work From Home %  
     - Sick Leave %  
   - 📋 **Tables**:  
     - Employee Attendance Overview  
     - Daily Attendance Logs  
   - 📈 **Area Charts**: Trends over time for Presence %, WFH %, Sick Leave %.  
   - 📅 **Tables for Trends** by Day of Week.

2. **Leave Insights**:  
   - 📊 **Cards**:  
     - Total Sick Leave  
     - Total Paid Leave  
     - Total Unpaid Leave  
     - Special Leave Summary  
   - 📊 **Visuals**:  
     - Bar Chart (Leave Types by Employee)  
     - Column Chart (Frequent Absentees, Top 5 Employees)  
     - Donut Chart (Unpaid Leave Proportion)  

3. **Bonus**:  
   - **Interactive Q&A** for dynamic user queries.  

### Dynamic Filters:
- **Month Slicer**: Choose specific months for a focused view.  
- **Search Bar Slicer**: Filter by Employee Name or ID.  

---

## Getting Started  


### Prerequisites  
- **Power BI Desktop** for viewing or editing `.pbix` files.  
- Basic understanding of Power BI dashboards.  

### Installation  
1. Clone the repository:  
   ```bash  
   git clone https://github.com/yourusername/HR-Analytics-Dashboard.git
   ```
2. Open the `.pbix` file in Power BI Desktop.
3. Review the data and visuals, or modify it to suit your needs.

---

## Data Insights
### Attendance Insights Page
- Key Metrics: Presence %, Work From Home %, Sick Leave %.
- Visualizations:
  - Employee Attendance Overview (Table).
  - Daily Attendance Logs (Table).
  - Area charts for trends.
  - Tables for each metric by day of the week.

### Leave Insights Page
- Key Metrics: Total Sick Leave, Paid Leave, Unpaid Leave, Special Leave Summary.
- Visualizations:
  - Leave Types by Employee (Bar Chart).
  - Frequent Absentees (Top 5 employees).
  - Unpaid Leave Proportion (Donut Chart).

---

## DAX Measures
Here are the key **DAX measures** used in the dashboard:

**1. Day of Week**
```dax
Day of Week = FORMAT('Attendance'[Date], "dddd")  
```

**2. Month**
```dax
Month = FORMAT('Attendance'[Date], "MMMM")  
```

**3. SL Count**
```dax
SL Count = COUNTROWS(FILTER('Attendance', 'Attendance'[Key] IN {"SL", "HSL"}))  
```

**4. WFH Count**
```dax
WFH Count = COUNTROWS(FILTER('Attendance', 'Attendance'[Key] IN {"WFH", "HWFH"}))  
```
These measures provide actionable insights into attendance and leave patterns.

---

## Design Inspiration
This dashboard's theme colors and layout were inspired by the [Relink HR Management Dashboard](https://dribbble.com/shots/23681998-Relink-HR-Management-Dashboard) on Dribbble.

---
## Resources
### Tutorial Inspiration
This project implements the tutorial series: [Data Analyst Project For Beginners | HR Analytics](https://www.youtube.com/playlist?list=PLeo1K3hjS3uuVQccZa7yFwK3ltoGQOWbM) from **Codebasics**.

### Blog for Data Combination
Combining multiple Excel worksheets using Power BI: [Chris Webb's Blog](https://blog.crossjoin.co.uk/2018/07/09/power-bi-combine-multiple-excel-worksheets/)

---

## Visual Previews

### Attendance Insights  
![Attendance Insights](src/Attendance%20Insights.png)

### Leave Insights  
![Leave Insights](src/Leave%20Insights.png)

---

## License

This project is licensed under the MIT License. Feel free to modify and use it in your projects.

---

## Connect

For questions, reach out via [LinkedIn](https://www.linkedin.com/in/sohilakhaledabbas/) or contribute to this repository.





