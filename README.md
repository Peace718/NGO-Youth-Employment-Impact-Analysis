# Measuring the Impact of Digital Skills Training on Youth Employment Outcomes in Nigeria

### An NGO Monitoring and Evaluation Dashboard for Tracking Training Participation, Engagement, and Employment Outcomes

## Table of Contents
- [Project Overview](#project-overview)
- [Business Problem](#business-problem)
- [Project Objectives](#project-objectives)
- [Dataset Overview](#dataset-overview)
- [Tools and Technologies](#tools-and-technologies)
- [Data Preparation and Cleaning](#data-preparation-and-cleaning)
- [Data Modeling](#data-modeling)
- [DAX Measures and KPIs](#dax-measures-and-kpis)
- [Dashboard Design](#dashboard-design)
- [Key Insights and Findings](#key-insights-and-findings)
- [Recommendations](#recommendations)
- [Conclusion](#conclusion)
- [Project Files](#project-files)

## Project Overview
This project analyzes the effectiveness of digital skills training programs delivered by a nonprofit organization across Nigeria.
The objective is to evaluate participant engagement, training completion, and employment outcomes while identifying opportunities to improve program effectiveness and social impact.
An interactive Power BI dashboard was developed to support evidence-based decision-making for NGO leadership, program managers, and donors.

## Business Problem
A nonprofit organization providing digital skills training across Nigeria struggles to evaluate whether its programs are improving youth employment outcomes and participant engagement across different regions.
As a result:
- Leadership cannot identify which programs drive the strongest employment outcomes.
- Management cannot determine factors influencing training completion.
- Donors lack visibility into regional program impact.
- The organization cannot effectively allocate resources to underserved areas.
The NGO requires a centralized analytics solution to evaluate program performance and support data-driven decision-making.

## Project Objectives
The dashboard was designed to:
- Monitor participant enrollment and engagement.
- Evaluate training completion performance.
- Identify factors contributing to participant dropout.
- Measure employment outcomes across training programs.
- Compare regional program impact.
- Support resource allocation and strategic planning.

## Dataset Overview
### Dataset Type
Synthetic dataset created for portfolio and educational purposes using realistic assumptions based on publicly available information relating to youth employment, digital skills development, and labour market trends in Nigeria.
### Main Tables
- Participants
- Programs
- Employment Outcomes
- Mentorship
- Social Indicators

The Mentorship and Social Indicators tables are included in the data model for future analysis but were not a primary focus of the current study.

### Total Participants
- 3,000

## Tools and Technologies
- Power BI Desktop
- Power Query
- DAX
- Microsoft Excel

## Data Preparation and Cleaning
The following data quality checks and transformations were performed:
- Verified data types for all columns.
- Converted date fields into the proper date format.
- Promoted headers where necessary.
- Reviewed null and missing values.
- Validated primary keys and relationships.
- Created Salary_Midpoint for salary analysis.
- Checked for duplicate records.

## Data Modeling
A star-schema data model was implemented to support efficient analysis and reporting.
### Data Model
![Data Model](images/data_model.png)

## DAX Measures and KPIs
Key performance indicators created include:
- Total Participants
- Completion Rate
- Dropout Rate
- Employment Rate
- Average Attendance
- Average Salary

### Completion Rate
```DAX
Completion Rate =
DIVIDE(
    CALCULATE(
        COUNTROWS(Participants),
        Participants[Completion_Status] = "Completed"
    ),
    [Total Participants]
)
```

### Employment Rate
```DAX
Employment Rate =
DIVIDE(
    CALCULATE(
        COUNTROWS(Employment_Outcomes),
        Employment_Outcomes[Employment_Status] = "Employed"
    ),
    [Total Participants]
)
```

## Dashboard Design
### Executive Overview and Program Performance
![Executive Overview Dashboard](images/dashboard_page1.png)
### Employment Outcomes and Regional Impact
![Employment Outcomes Dashboard](images/dashboard_page2.png)

## Key Insights and Findings

### Nearly Half of Participants Secured Employment After Training
Out of 3,000 enrolled participants:
- 71.23% completed training.
- 48.73% secured employment.
- Average salary among employed participants was approximately ₦267,000.
### Digital Marketing and Cloud Computing Produced the Strongest Employment Outcomes
These programs consistently recorded the highest employment rates among participants.
### Family Commitments Were the Leading Cause of Dropout
Dropout analysis revealed that personal and family responsibilities significantly affected participant retention.
### South East Achieved the Strongest Employment Outcomes
Despite lower participant enrollment, the South East region recorded the highest employment rate.
### Web Development and Cybersecurity Delivered the Highest Salary Outcomes
Although employment rates were lower, employed graduates from these programs earned the highest average salaries.

## Recommendations
- Expand Digital Marketing and Cloud Computing programs to maximize employment outcomes.
- Provide flexible learning options to reduce dropout caused by family commitments.
- Increase support and outreach in underserved regions.
- Strengthen employer partnerships to improve job placement outcomes.
- Continue using data-driven monitoring to evaluate program effectiveness.

## Conclusion
The analysis demonstrates that digital skills training contributes positively to youth employment outcomes across Nigeria.
While employment outcomes vary by program and region, the findings highlight opportunities to improve participant retention, strengthen regional impact, and maximize employment opportunities through targeted program improvements and evidence-based decision-making.

## Project Files
- ![Power BI Report (.pbix)]( youth_employment_impact_dashboard.pbix)
- ![Project Report(pdf)]( project_report.pdf)
- ![ Dataset (.xlsx)]( youth_skills_employment_impact_dataset.xlsx)









