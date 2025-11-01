# Hospital-emergency-room-dashboard-excel-project

I have created dashboard to find out meaningful insights on Hospital Emergency Room data

<img width="1531" height="560" alt="Screenshot Hospital Emergency Room" src="https://github.com/user-attachments/assets/07ad89d4-ac59-4e17-a002-80002c845388" />



Project Overview

This project demonstrates an **End-to-End Dashboard** built in **Microsoft Excel** for analyzing **Hospital Emergency Room performance**.
The goal is to improve efficiency and support better decision-making by tracking patient flow, timeliness, and departmental insights.


Purpose of the Project

To create a **Hospital Emergency Room Analysis Dashboard** that:

* Monitors patient admission status
* Evaluates wait times and timeliness
* Identifies age and gender distributions
* Highlights top-referred departments

This dashboard provides stakeholders with **actionable insights** to manage resources and improve patient services.


KPIs & Metrics

The dashboard tracks the following **Key Performance Indicators (KPIs):**

* **Patient Admission Status** – Admitted vs. Not Admitted
* **Patient Age Distribution** – Groups patients by age bracket
* **Timeliness** – % of patients seen within 30 minutes
* **Gender Analysis** – Male vs. Female patient ratio
* **Department Referrals** – Most frequent referral departments


Visuals / Charts Created

1. **Patient Admission Status** (Pie Chart)
2. **Patient Age Distribution** (Bar Chart)
3. **Timeliness Analysis** (% within 30 mins vs delayed)
4. **Gender Distribution** (Donut or Column Chart)
5. **Department Referrals** (Horizontal Bar Chart)
6. **Slicers:** Year, Month, and Department


Power Query and DAX Logic

Calendar Table Formula**

```m
= List.Dates(#date(2023,01,01),731,#duration(1,0,0,0))
```

### **DAX / Calculated Column Examples**

```DAX
-- Age Group Classification
= IF([Patient Age]>=70,"70-79",
   IF([Patient Age]>=60,"60-69",
   IF([Patient Age]>=45,"45-59",
   IF([Patient Age]>=30,"30-44",
   IF([Patient Age]>=15,"15-29",
   IF([Patient Age]>=5,"05-14","0-4"))))))
```

```DAX
-- Patient Attend Status
= IF([Patient Waittime]<30,"Within Time","Delay")
```


Tools & Features Used

* **Microsoft Excel**

  * Power Query for data transformation
  * Pivot Tables for aggregation
  * Slicers for interactivity
  * Charts for visual insights
* **Calendar Table** for time intelligence
* **Custom formatting** and **transparent slicer design** for dashboard aesthetics


Insights Gained

* Most patients are seen within target time limits.
* Certain departments have higher referral rates.
* Wait times correlate with peak admission hours.
* Younger and middle-aged patients form the majority of ER visits.


Files Included

* `Hospital Emergency Room.xlsx` — Excel dashboard file
* `END TO END DASHBOARD PROJECT IN EXCEL.pptx` — Project documentation and workflow presentation


How to Use

1. Clone or download the repository.
2. Open `Hospital Emergency Room.xlsx` in Excel (Desktop version recommended).
3. Use slicers (Year, Month, Department) to interact with the visuals.


Future Enhancements

* Add trend lines for multi-year analysis
* Include department-level KPIs
* Integrate external datasets (staffing, weather, etc.)


