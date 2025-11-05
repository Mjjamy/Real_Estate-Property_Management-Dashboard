# Real Estate and Property Management Analysis

## Table Of Contents

- Project Overview
- Data Sources
- Tools
- Data Cleaning/Data Preparation
- Exploratory Data Analysis
- Data Analysis
- Results/Findings
- Recommendations
- Limitations

### Project Overview

---

A Power BI project for Real Estate and Property Management showcasing insights on property conditions, renovations, waterfront status, and construction year. Interactive dashboard enable filtering by year and location, helping stakeholders analyze property performance, occupancy trends, and maintenance priorities efficiently.

<img width="890" height="505" alt="RealEstate_Property_Mngnt_Dashboard_Overview" src="https://github.com/user-attachments/assets/f3f8a4b5-ad86-4189-ad21-e017e6f4d7e5" />





<img width="892" height="504" alt="RealEstate_Property_Mngnt_Dashboard_Details" src="https://github.com/user-attachments/assets/b5e6b1bd-c201-4c72-86eb-0aee1f293823" />



### Data Sources

Housing Dataset:The primary dataset used for this analysis is the "Housing Dataset.xlsx",which contains the detailed information about the properties.

### Tools

- POWER BI (Data Cleaning, Data Analysis, Creating Reports)

### Data Cleaning/Data Preparation

In the initial data preparation phase, we performed the following tasks:

1.Data loading and inspection.

2.Handling missing values.

3.Removing duplicates.

4.Checking and fixing the data types.

5.Creating calculated columns.

6.Data Modelling.

### Exploratory Data Analysis

EDA involved exploring the Housing Dataset to answer key questions, such as:

- How many properties are in very good, good, or bad condition?

- Does renovating a property help improve its value or occupancy?

- How do the number of bedrooms and floors differ across properties?

- How has property construction changed over the years?

- Do waterfront properties perform better than non-waterfront ones?

### Data Analysis

Worked with some DAX queries:
- Total Properties = COUNTROWS('Fact Table')
- Very Good Condition = CALCULATE([Total Properties],FILTER('Dim_Condition Status','Dim_Condition Status'[Condition Status]="Very Good"))
- Renovated = CALCULATE([Total Properties],FILTER('Dim_Renovated Status','Dim_Renovated Status'[Renovated Status]="Renovated"))
- Not Renovated = CALCULATE([Total Properties],FILTER('Dim_Renovated Status','Dim_Renovated Status'[Renovated Status]="Not Renovated"))
- Have Waterfront = CALCULATE([Total Properties],FILTER('Dim_Waterfront Status','Dim_Waterfront Status'[Waterfront Status]="Yes"))
- No Waterfront = CALCULATE([Total Properties],FILTER('Dim_Waterfront Status','Dim_Waterfront Status'[Waterfront Status]="No"))
- Good Condition = CALCULATE([Total Properties],FILTER('Dim_Condition Status','Dim_Condition Status'[Condition Status]="Good"))
- Bad Condition = CALCULATE([Total Properties],FILTER('Dim_Condition Status','Dim_Condition Status'[Condition Status]="Bad"))
- % of waterfront status yes = DIVIDE([Have Waterfront],[Total Properties],0)
- % of waterfront status no = DIVIDE([No Waterfront],[Total Properties],0)


### Results/Findings

The analysis results are summarized as follows:

1. Most properties are in good condition, showing overall stable maintenance levels.

2. Renovated properties tend to have better value.

3. 1- and 2-bedroom properties with 1–2 floors are the most common.

4. Property development peaked in earlier years and has slowed recently.

5. Waterfront properties are rare but tend to have higher potential value.

### Recommendations

Based on the analysis we recommend the following actions:

- Focus on Renovations: Invest in renovating older or poorly rated properties to improve overall value and attract more tenants.

- Promote Waterfront Properties: Highlight and market the limited waterfront properties for premium pricing opportunities.

- Monitor Property Conditions: Regularly track property conditions through dashboards to plan maintenance and reduce future repair costs.

### Limitations

The analysis is based on available property data, which may have missing or outdated records; therefore, insights might not fully represent real-time market conditions.



  


