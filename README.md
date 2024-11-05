# Healthcare Analytics Dashboard

This repository contains a Power BI dashboard designed to analyze and visualize healthcare data, providing actionable insights into patient demographics, length of stay, operational efficiency, and financial performance across healthcare facilities.

## Overview

The **Healthcare Analytics Dashboard** enables healthcare administrators and analysts to monitor and evaluate performance metrics for hospital discharges, length of stay, patient demographics, and financial information. This dashboard is tailored to support data-driven decisions aimed at optimizing patient care, reducing costs, and enhancing operational efficiency.

### Key Files

1. **Healthcare Analytics.pbix** - Power BI dashboard file containing all report pages and visuals.
2. **hospital_inpatient_discharges_totalhipreplacement.csv** - Dataset on hospital inpatient discharges, specifically focusing on total hip replacement procedures.
3. **Metadata - Case Study: Analyzing Healthcare Data in Power BI.pdf** - Metadata document providing details about the dataset's columns and data types.

   
## Dashboard Pages and Visuals

### 1. Patient Demographics and Admissions

This page provides insights into the demographic distribution of patients, including age groups, gender, race, and ethnicity. Key visuals include:

- **Age Group Distribution**: Bar chart showcasing the age range of patients discharged.
- **Gender and Ethnicity Breakdown**: Pie charts showing gender distribution and ethnicity.
- **Admission Type**: Pie chart to show admission sources, such as emergency or elective.

### 2. Length of Stay Analysis
This section allows users to analyze the average **Length of Stay (LOS)** for patients, helping identify trends and compare hospital LOS to state averages. Key metrics include:

- **Var Average Cost per Discharge  and % Var Average LOS Days**calculated with a DAX formula:
  DAX
 ``` % Var Average Cost per Discharge = 
DIVIDE(
    ([Average Cost per Discharge]-[Average Cost per Discharge ALL]),
    [Average Cost per Discharge ALL]
)
 % Var Average LOS Days = 
DIVIDE(
    ([Average LOS Days]-[Average LOS Days ALL]),
    [Average LOS Days ALL]
)
```

- **Patient LOS Distribution**: Histogram of patient stay lengths.
- **Trend Analysis**: Line graph displaying LOS trends over time by admission type.

### 3. Financial Overview

This page provides financial insights, including **total charges** and **total costs**. Key visuals include:

- **Total Charges vs. Total Costs**: A stacked bar chart comparing expenses and charges across facilities.
- **Revenue Streams and Expense Categories**: Breakdown of revenue by category and analysis of key expense areas.
- **Profitability Metrics**: Calculation of net income, total charges, and total costs to assess financial health.

### 4. Quality and Compliance Metrics

The quality and compliance section offers insights into the hospital's performance in maintaining healthcare standards:

- **Compliance with Standards**: A compliance gauge chart showing adherence to healthcare standards.
- **Patient Satisfaction Scores**: Bar charts representing satisfaction and discharge status.
- **Mortality Risk and Severity Levels**: Visuals segmented by **Severity of Illness (SOI)** and **Risk of Mortality (ROM)** to show patient outcomes.

---

## Technical Details

- **Data Model**: Integrates fields including `facility_name`, `length_of_stay`, `total_charges`, `total_costs`, `patient_disposition`, and more, facilitating comprehensive analysis of patient and hospital data.
- **Interactive Filters**: Users can filter by age group, admission type, hospital name, and county to customize their view.
- **Custom Visuals**: Utilizes Power BI’s custom visuals for presenting complex healthcare metrics in an accessible format.

## Getting Started

### Prerequisites

- **Power BI Desktop**: Download and install [Power BI Desktop](https://powerbi.microsoft.com/desktop/) to open and modify the dashboard.
- **Data Import**: Ensure you have the `hospital_inpatient_discharges_totalhipreplacement.csv` file to load data into the dashboard.

### Installation

1. Clone this repository
2. Open the `.pbix` file in Power BI Desktop.
3. Refresh the dataset connections to ensure the latest data is displayed.

### Usage

1. **Open Healthcare Analytics.pbix** in Power BI Desktop.
2. **Navigate Through Pages**: Explore each page to view insights into patient demographics, LOS, financial data, and compliance metrics.
3. **Use Slicers and Filters** to customize views and drill down into specific metrics.
4. **Export Data**: Power BI allows exporting data from visuals for deeper analysis.

