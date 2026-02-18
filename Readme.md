**HOSPITAL INPATIENT COST &**

**LENGTH OF STAY INTELLIGENCE**

*Final Project Report --- Data & Visual Analytics Capstone*

**Newton School of Technology**

Sector: Healthcare / Hospital Inpatient Services

Dataset: New York State Inpatient Discharge Data (SPARCS), 2022

Tool: Google Sheets (Analysis, Pivot Tables & Dashboard)

**Team Details**

Ankit \| Kartik Madaan \| Riya Yadav

Pragya Kashyap \| Prateek Shukla \| Soumen Dass

**Section B \| Group G-11**

**February 2026**

**1. Executive Summary**

This report presents a comprehensive data analytics study of hospital inpatient cost and length of stay (LOS) patterns, conducted using New York State Inpatient Discharge data from 2022. The dataset contains 11,999 records (11,835 after cleaning) across 15 analytical variables spanning patient demographics, clinical severity, admission types, diagnoses, payment types, and financial outcomes.

**Problem**

Hospital inpatient costs represent a significant financial burden on both healthcare systems and patients. Without clear intelligence on which factors --- illness severity, admission type, patient age, or payer type --- drive cost and length of stay, healthcare administrators cannot make evidence-based resource allocation or cost-reduction decisions.

**Approach**

The team sourced publicly available New York State hospital discharge data, cleaned and standardized it in Google Sheets through 9 structured cleaning steps, engineered key performance indicators (KPIs), and built 6 pivot tables and an interactive dashboard to surface actionable insights.

**Key Insights**

- Extreme severity cases cost 4.7x more than minor cases (\$59,238 vs. \$12,690 avg.) and stay 3.7x longer.

- Trauma admissions are the costliest and longest (\$59,957, 15.33 days avg.) --- driven by case complexity.

- Patients aged 50 and above cost 50% more than patients aged 0-29, indicating age-driven resource intensity.

- Fungal infections are the single highest-cost diagnosis at \$340,911 avg., followed by Encephalitis at \$214,350.

- Surgical cases are billed 75% higher than medical cases (\$126,280 vs. \$72,221 avg. total charges).

- Medicaid accounts for the largest patient volume (4,890 cases) while Managed Care shows the highest average cost.

- Life expectancy (survival rate) is 96.20%, reflecting generally good care quality outcomes.

- 8,109 patients --- the majority --- were discharged to home or self-care, followed by 1,394 to home with health services.

**Key Recommendations**

- Implement dedicated triage and resource pathways for extreme and major severity patients to contain cost escalation.

- Develop multi-disciplinary trauma care teams to reduce the disproportionately long trauma admission LOS.

- Introduce geriatric care optimization protocols for the 50+ age group to improve efficiency and reduce LOS.

- Create clinical stewardship programs targeting high-cost diagnoses such as fungal infections and encephalitis.

- Renegotiate Managed Care contracts to address the highest average costs among payer categories.

**2. Sector & Business Context**

**2.1 Sector Overview**

The healthcare sector --- specifically hospital inpatient services --- is one of the most data-intensive and financially complex industries globally. In the United States, inpatient hospital care accounts for a substantial proportion of total healthcare expenditure. The New York State Statewide Planning and Research Cooperative System (SPARCS) collects detailed patient-level discharge data from all licensed hospitals, creating one of the richest publicly available hospital datasets in the world.

Hospital costs are driven by a complex interaction of clinical, demographic, and operational factors. Illness severity, length of stay, admission type, patient age, diagnosis category, and payer type all play significant roles in determining the total cost of an inpatient episode.

**2.2 Current Challenges**

- Rising inpatient costs with insufficient data-driven cost management protocols.

- Unequal resource distribution across severity levels, age groups, and admission types.

- High-cost diagnoses (e.g., fungal infections, encephalitis) lack early intervention pathways.

- Payer mix imbalances --- with Medicaid accounting for the majority of volume --- create reimbursement pressures.

- Discharge planning gaps leading to potential re-admissions and extended stays.

**2.3 Why This Problem Was Chosen**

Hospital cost intelligence is a critical enabler for healthcare administrators to make resource allocation, staffing, and financial planning decisions. By analysing inpatient cost and LOS data, healthcare systems can identify cost drivers, optimise pathways, and improve patient outcomes. This project directly addresses the need for structured, data-backed visibility into inpatient cost and efficiency patterns.

**3. Problem Statement & Objectives**

**3.1 Formal Problem Definition**

*To analyze hospitalisation patterns in order to identify the key clinical, demographic, and operational variables driving variability in inpatient costs and length of stay --- and to provide data-driven recommendations that enable healthcare administrators to optimize resource allocation, reduce avoidable cost, and improve patient care efficiency.*

**3.2 Project Scope**

- Dataset: New York State inpatient discharge data, discharge year 2022.

- Analysis focus: Cost (Total Costs), length of stay, severity, admission type, age, diagnosis, and payer type.

- Tool: Google Sheets for all cleaning, analysis, pivot tables, KPI calculations, and dashboard.

- Exclusions: Clinical treatment protocols, geographic drill-down below hospital service area level, and predictive modelling.

**3.3 Success Criteria**

- Build a clean, analysis-ready dataset from the raw SPARCS extract.

- Define and calculate at least 3 KPIs mapped to hospital cost and efficiency.

- Create a minimum of 6 structured pivot analyses covering all key dimensions.

- Develop an interactive Google Sheets dashboard with filters and multiple chart types.

- Generate 8-12 evidence-based insights and at least 6 actionable recommendations.

**4. Data Description**

**4.1 Dataset Source**

Source: New York State Department of Health --- SPARCS (Statewide Planning and Research Cooperative System)

Dataset: Hospital Inpatient Discharges (SPARCS De-Identified) --- 2022

Access: Publicly available via New York State Open Data portal. The dataset was downloaded, formatted as a Google Sheets workbook, and is maintained across four tabs: Raw_Dataset, Cleaned_Dataset, Data_dictionary_and_logs, and Calculations_and_pivot_table.

**4.2 Data Structure & Size**

- Raw dataset: 11,999 records, 32 columns.

- Cleaned dataset: 11,835 records (after removing 153 duplicates and blank rows), 15 analytical columns.

- All cleaning and transformation work was completed in Google Sheets.

**4.3 Column Explanations (Data Dictionary)**

|                                         |                    |               |                                            |
|-----------------------------------------|--------------------|---------------|--------------------------------------------|
| **Column Name**                         | **Data Type**      | **Unit**      | **Description**                            |
| **Hospital Service Area**               | Text (Categorical) | NA            | Regional service area of the hospital      |
| **Hospital County**                     | Text (Categorical) | NA            | County where hospital is located           |
| **Age Group**                           | Text (Categorical) | NA            | Patient age category                       |
| **Gender**                              | Text (Categorical) | NA            | Patient gender                             |
| **Length of Stay**                      | Integer            | Days          | Number of days patient was admitted        |
| **Type of Admission**                   | Text (Categorical) | NA            | Admission type (Emergency, Elective, etc.) |
| **Patient Disposition**                 | Text (Categorical) | NA            | Patient discharge outcome                  |
| **CCSR Diagnosis Description**          | Text (Categorical) | NA            | Diagnosis classification category          |
| **APR Severity of Illness Description** | Text (Categorical) | NA            | Severity level of illness                  |
| **APR Risk of Mortality**               | Text (Categorical) | NA            | Mortality risk classification              |
| **APR Medical Surgical Description**    | Text (Categorical) | NA            | Indicates medical or surgical case         |
| **Payment Typology 1**                  | Text (Categorical) | NA            | Primary insurance / payment type           |
| **Emergency Department Indicator**      | Text (Categorical) | NA            | Indicates if case originated in ED         |
| **Total Charges**                       | Integer            | Currency (\$) | Total amount billed by hospital            |
| **Total Costs**                         | Integer            | Currency (\$) | Actual hospital treatment cost             |

**4.4 Data Limitations**

- Dataset covers discharge year 2022 only --- longitudinal trends cannot be assessed.

- De-identified data prevents patient-level tracking across multiple admissions.

- Certain columns (e.g., Payment Typology 2 & 3, Birth Weight) had significant sparsity and were excluded from the cleaned dataset.

- Total Charges represents billed amounts and may not reflect actual reimbursement received.

- Geographical analysis is limited to Hospital Service Area (regional) level --- facility-level benchmarking is not available.

**5. Data Cleaning & Preparation**

All data cleaning and preparation steps were executed directly in Google Sheets, as required by the capstone project guidelines. The following 9-step cleaning protocol was applied, documented in the Data_dictionary_and_logs tab of the working spreadsheet.

|          |                                                                          |                                                                                                                                                                                                                        |                                                                                                      |
|----------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| **Step** | **Issue Identified**                                                     | **Column Affected**                                                                                                                                                                                                    | **Action Taken**                                                                                     |
| **1**    | Raw dataset imported                                                     | All columns                                                                                                                                                                                                            | Copied data from raw original dataset                                                                |
| **2**    | Presence of non-analytical, identifier, technical, and redundant columns | Operating Certificate Number, Permanent Facility Id, Facility Name, CCSR Diagnosis Code, CCSR Procedure Code, APR DRG Code, APR MDC Code, APR Severity Code, Payment Typology 2 & 3, Zip Code - 3 digits, Birth Weight | Removed irrelevant columns to align dataset strictly with cost and length of stay analysis objective |
| **3**    | Blank values                                                             | All columns                                                                                                                                                                                                            | Removed blank rows from Cleaned_Dataset                                                              |
| **4**    | Leading/trailing spaces and case inconsistencies                         | All categorical columns                                                                                                                                                                                                | Applied TRIM() and PROPER() to standardize formatting                                                |
| **5**    | Numeric values stored as text / comma formatting                         | Total Charges, Total Costs                                                                                                                                                                                             | Converted and standardized numeric format                                                            |
| **6**    | Duplicate record validation                                              | All columns                                                                                                                                                                                                            | 153 duplicates were found and then removed                                                           |
| **7**    | Outlier validation required                                              | Length of Stay, Total Costs                                                                                                                                                                                            | Reviewed extreme values and retained realistic clinical cases                                        |
| **8**    | Numeric columns stored as text and inconsistent decimal precision        | Capacity, Daily Requirement, Domestic Stock, Imported Stock, Normative Stock                                                                                                                                           | Converted to numeric using VALUE(TRIM()) and standardized to 2 decimal format                        |
| **9**    | Need for analytical KPI preparation                                      | Dataset (Derived Column)                                                                                                                                                                                               | Created Cost Per Day column (Total Cost / Length of Stay) etc.                                       |

**5.1 Derived Column: Cost Per Day**

A derived column, Cost Per Day, was engineered using the formula: Total Costs / Length of Stay. This KPI enables daily cost benchmarking across severity groups, age groups, and admission types --- a metric not present in the raw data but essential for financial efficiency analysis.

**5.2 Assumptions**

- Outliers in Length of Stay and Total Costs were reviewed clinically --- extreme values consistent with documented conditions (e.g., trauma, extreme severity) were retained as valid data points.

- Cases with blank values in key analysis columns were removed to maintain analytical integrity.

- Total Costs is used as the primary cost measure throughout this report (reflecting actual treatment cost vs. Total Charges, which is the billed amount).

**6. KPI & Metric Framework**

The following five Key Performance Indicators were defined to measure hospital cost efficiency, patient throughput, and care quality outcomes. Each KPI is directly mapped to the project objectives.

|                              |                                       |             |                                                                                |
|------------------------------|---------------------------------------|-------------|--------------------------------------------------------------------------------|
| **KPI**                      | **Formula**                           | **Value**   | **Business Purpose**                                                           |
| **Average Length of Stay**   | SUM(Length of Stay) / COUNT(Cases)    | 5.87 days   | Measures operational efficiency; longer stays = higher cost burden             |
| **Average Cost to Hospital** | SUM(Total Costs) / COUNT(Cases)       | \$25,576.29 | Actual treatment cost incurred by hospital per inpatient episode               |
| **Average Cost to Patient**  | SUM(Total Charges) / COUNT(Cases)     | \$30,358.98 | Average amount billed to the patient side; reveals charge-to-cost gap          |
| **Cost Per Day**             | Total Costs / Length of Stay          | \$4,508.25  | Identifies daily resource consumption; drives staffing and resource allocation |
| **Life Expectancy Rate**     | (Surviving Cases / Total Cases) × 100 | 96.20%      | Patient outcome quality indicator; reflects care effectiveness                 |

**6.1 KPI Mapping to Objectives**

- Average Length of Stay (5.87 days) --- Operational efficiency: directly impacts bed availability and cost per episode.

- Average Cost to Hospital (\$25,576.29) --- Financial performance: actual treatment cost incurred by the hospital per inpatient case.

- Average Cost to Patient (\$30,358.98) --- Patient financial burden: the average amount billed/charged to the patient side per episode.

- Cost Per Day (\$4,508.25) --- Resource intensity: enables daily cost comparison across admission and severity categories.

- Life Expectancy Rate (96.20%) --- Clinical outcome quality: measures whether cost management is achieved without compromising patient safety.

**7. Exploratory Data Analysis (EDA)**

**7.1 Impact of Illness Severity on Cost & LOS (Pivot Table 1)**

The most striking pattern in the dataset is the exponential relationship between APR Severity of Illness and both cost and length of stay.

|                  |                           |                                |
|------------------|---------------------------|--------------------------------|
| **APR Severity** | **Avg. Total Costs (\$)** | **Avg. Length of Stay (Days)** |
| **Extreme**      | 59,238.31                 | 11.08                          |
| **Major**        | 28,042.51                 | 6.62                           |
| **Moderate**     | 21,464.86                 | 5.29                           |
| **Minor**        | 12,690.26                 | 2.97                           |

*Insight: Extreme severity cases are nearly 5x more expensive than minor cases and stay nearly 4x longer. This direct, proportional relationship confirms that clinical severity is the single strongest driver of both cost and LOS. The data shows a clear linear escalation from Minor to Extreme, underscoring the need for early severity-based intervention protocols.*

**7.2 Admission Type Analysis (Pivot Table 2)**

Emergency, Trauma, and Urgent admissions represent the highest-cost and longest admission categories.

|                       |                           |                                |
|-----------------------|---------------------------|--------------------------------|
| **Type of Admission** | **Avg. Total Costs (\$)** | **Avg. Length of Stay (Days)** |
| **Elective**          | 29,366.00                 | 4.80                           |
| **Emergency**         | 27,393.27                 | 6.33                           |
| **Newborn**           | 15,723.55                 | 4.09                           |
| **Trauma**            | 59,957.20                 | 15.33                          |
| **Urgent**            | 49,123.02                 | 9.68                           |

*Insight: Trauma admissions are the costliest (\$59,957) with an exceptional LOS of 15.33 days, more than double that of Emergency admissions (6.33 days). Urgent cases, while fewer in volume, also carry high costs (\$49,123). Elective cases, despite having the highest average cost among planned admissions (\$29,366), have shorter LOS (4.8 days), suggesting efficient elective pathway management. Newborn admissions have the shortest LOS and lowest costs, consistent with typical delivery patterns.*

**7.3 Age Group Cost & LOS Analysis (Pivot Table 6)**

Cost and LOS increase significantly with patient age, particularly for patients aged 50 and above.

|                 |                           |                                |
|-----------------|---------------------------|--------------------------------|
| **Age Group**   | **Avg. Total Costs (\$)** | **Avg. Length of Stay (Days)** |
| **0 to 17**     | 21,516.35                 | 4.61                           |
| **18 to 29**    | 21,907.75                 | 5.34                           |
| **30 to 49**    | 23,128.68                 | 5.30                           |
| **50 to 69**    | 32,583.94                 | 7.06                           |
| **70 or Older** | 32,150.56                 | 7.04                           |

*Insight: Patients aged 50-69 and 70+ incur average costs of \$32,584 and \$32,151 respectively, compared to \$21,516 for the 0-17 age group. Length of stay similarly escalates to over 7 days for the 50+ groups. This pattern reflects the higher comorbidity burden and care complexity of older patient populations. The near-identical costs and LOS of the 50-69 and 70+ groups suggests that cost escalation plateaus beyond age 50, but remains significantly elevated.*

**7.4 Payment Type Analysis (Pivot Table 5)**

Payer mix reveals both volume concentration in public programmes and cost variation across private and public insurers.

|                               |                           |                    |
|-------------------------------|---------------------------|--------------------|
| **Payment Type**              | **Avg. Total Costs (\$)** | **Count of Cases** |
| **Medicaid**                  | 25,576.29                 | 4,890              |
| **Medicare**                  | 33,192.87                 | 4,475              |
| **Private Health Insurance**  | 22,601.78                 | 1,985              |
| **Blue Cross/Blue Shield**    | 23,384.99                 | 441                |
| **Self-Pay**                  | 25,009.15                 | 104                |
| **Miscellaneous/Other**       | 34,078.77                 | 24                 |
| **Dept. of Corrections**      | 28,618.93                 | 8                  |
| **Federal/State/Local/VA**    | 13,498.89                 | 13                 |
| **Managed Care, Unspecified** | 35,670.78                 | 10                 |

*Insight: Medicaid (4,890 cases) and Medicare (4,475 cases) dominate patient volume, together representing over 78% of all inpatient cases. This heavy reliance on public payers creates reimbursement risk, as public programme rates are typically lower than private rates. Managed Care (Unspecified) has the highest average cost at \$35,671, followed by Medicare at \$33,193. Self-Pay patients have notably lower average costs (\$25,009), which may reflect early discharge or limited resource utilisation.*

**7.5 High-Cost Diagnoses (Pivot Table 3)**

Certain diagnoses drive disproportionately high costs relative to the system average of \$27,861.

|                                                       |                           |
|-------------------------------------------------------|---------------------------|
| **CCSR Diagnosis**                                    | **Avg. Total Costs (\$)** |
| **Fungal infections**                                 | 340,911.30                |
| **Encephalitis**                                      | 214,349.50                |
| **Endocarditis and endocardial diseases**             | 195,881.64                |
| **Noninfectious hepatitis**                           | 195,150.81                |
| **Disruptive, impulse-control and conduct disorders** | 186,422.12                |
| **Postprocedural or postoperative circulatory**       | 159,883.73                |
| **Respiratory congenital malformations**              | 138,807.54                |
| **Diseases of white blood cells**                     | 137,157.29                |
| **Anal and rectal conditions**                        | 125,140.09                |
| **Leukemia - acute myeloid leukemia**                 | 117,220.72                |

*Insight: Fungal infections have an extraordinary average cost of \$340,911 --- more than 12x the system average --- reflecting the intensive treatment, long ICU stays, and specialist care required. Encephalitis (\$214,350) and Endocarditis (\$195,882) similarly represent extreme cost outliers. These diagnoses are rare but exert significant financial pressure. Targeted clinical protocols and early detection programmes for these diagnoses could significantly reduce system-wide costs.*

**7.6 Medical vs. Surgical Cases (Pivot Table 4)**

|               |                             |                                |
|---------------|-----------------------------|--------------------------------|
| **Case Type** | **Avg. Total Charges (\$)** | **Avg. Length of Stay (Days)** |
| **Surgical**  | 126,279.86                  | 6.51                           |
| **Medical**   | 72,221.23                   | 6.12                           |

*Insight: Surgical cases are billed at \$126,280 in average total charges --- 75% more than medical cases at \$72,221. LOS is also marginally longer for surgical cases (6.51 vs. 6.12 days). This reflects the higher procedural costs, theatre time, anaesthesia, implants, and post-operative care associated with surgical pathways. Medical cases, while lower in charges, still carry significant care costs, suggesting that non-surgical complexity is also a major cost contributor.*

**8. Advanced Analysis**

**8.1 Segmentation Analysis**

Severity-Age Interaction: The combination of older age (50+) and high severity (Extreme/Major) creates the highest-cost patient segments in the dataset. These patients simultaneously trigger the longest LOS and highest daily resource consumption. This compound risk factor underscores the importance of integrated geriatric and severity-based care pathways.

**8.2 Cost Distribution Analysis**

The distribution of Total Costs across the dataset is right-skewed, with the majority of cases clustering below \$40,000 and a small number of extreme outliers (e.g., fungal infections, Encephalitis, trauma cases) pulling the mean significantly above the median. This skew is expected in healthcare cost data, where rare but extremely high-cost cases disproportionately impact system finances.

**8.3 Patient Disposition Pattern (Pivot Table --- Count Analysis)**

Patient Disposition provides insight into discharge outcomes and downstream care requirements.

|                                                   |           |
|---------------------------------------------------|-----------|
| **Patient Disposition**                           | **Count** |
| Home or Self Care                                 | 8,109     |
| Home w/ Home Health Services                      | 1,394     |
| Skilled Nursing Home                              | 888       |
| Expired                                           | 455       |
| Left Against Medical Advice                       | 433       |
| Inpatient Rehabilitation Facility                 | 186       |
| Short-term Hospital                               | 218       |
| Psychiatric Hospital or Unit of Hospital          | 55        |
| Hospice - Home                                    | 63        |
| Other (including Court/Law, Cancer Centers, etc.) | 162       |

*Insight: The majority of patients (8,109) are discharged to home or self-care, which is the most cost-effective disposition. However, 1,394 patients require home health services, and 888 are discharged to skilled nursing homes, suggesting a significant post-acute care burden. The 455 expired cases (3.8% of total) are consistent with the 96.20% life expectancy rate. The 433 patients who left against medical advice represent a potential quality of care and re-admission risk.*

**8.4 Risk Analysis: High-LOS Outliers**

Cases with Length of Stay exceeding 15 days represent a small but disproportionately costly segment. Trauma admissions (avg. LOS 15.33 days) and Extreme severity cases (avg. LOS 11.08 days) are the primary contributors to high-LOS outliers. These cases require dedicated monitoring, structured discharge planning, and multi-disciplinary case management to prevent unnecessary bed days.

**9. Dashboard Design**

**9.1 Dashboard Overview**

The interactive dashboard --- titled \'Hospital Cost & Operational Performance Dashboard\' --- was built in Google Sheets using pivot tables, dynamic formulas (AVERAGEIF, COUNTIF, SUMIF), chart visualisations, and slicer-style dropdown filters. The dashboard is housed in the Dashboards tab of the working spreadsheet.

**9.2 Dashboard Structure**

- Header: Title banner --- \'Hospital Cost & Operational Performance Dashboard\' on a teal background.

- KPI Cards (Row 1): Total Number of Cases (11,965) \| Avg. Length of Stay (5.87) \| Average Cost to Hospital (\$25,576.29) \| Average Cost to Patient (\$30,358.98) \| Life Expectancy (96.20%).

- Chart 1 --- Length of Stay by Age Group: Horizontal bar chart showing average LOS across five age groups (0 to 17, 18 to 29, 30 to 49, 50 to 69, 70 or Older).

- Chart 2 --- Patient Distribution by Payment Type: Donut chart showing proportional patient volumes across all payer types (Medicare, Medicaid, Blue Cross/Blue Shield, Private Health Insurance, Self-Pay, etc.).

- Chart 3 --- Impact of Illness Severity on Cost & LOS: Clustered bar chart (Avg. Total Costs by severity) overlaid with a line chart (Avg. LOS), clearly showing the cost-severity escalation from Minor to Extreme.

- Chart 4 --- Count of Patients with Their Age Groups: Line chart showing patient volume distribution across the five age groups.

- Chart 5 --- Count of Cases in Each Payment Type: Line chart showing case volume by payer category.

- Chart 6 --- Avg. Charges as Per Treatment Type: Pie chart showing charge split between Surgical and Medical case types.

- Chart 7 --- Cost by Admission Type: Area chart showing average total costs across Elective, Emergency, Newborn, Trauma, and Urgent admission types.

**9.3 Interactive Filters (Slicers)**

The dashboard includes two interactive dropdown slicers, allowing users to filter all charts and KPIs simultaneously by:

- Age Group

- Payment Typology 1

**9.4 Dashboard Design Principles**

- Color palette: Teal/gold palette consistent with healthcare analytics standards --- dark teal for headers, gold/amber for primary data bars, red line for LOS trend.

- All charts are dynamic and update in response to slicer selections.

- KPI scorecard format with large, bold figures for immediate executive readability.

- Charts selected to match data type: bar for comparison, donut for distribution, area for trend, horizontal bar for ranking.

**10. Insights Summary**

The following 10 evidence-based insights are derived from the EDA and pivot table analyses. Each insight is expressed in decision-ready language for hospital administrators and healthcare executives.

|        |                                                                                                  |                                                                                                                         |
|--------|--------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| **\#** | **Insight**                                                                                      | **Decision Implication**                                                                                                |
| **1**  | Extreme severity drives 4.7x higher costs --- \$59,238 vs. \$12,690 for minor severity cases.    | Prioritise fast-track pathways and dedicated resources for extreme/major severity patients to prevent cost escalation.  |
| **2**  | Trauma admissions carry the longest LOS at 15.33 days and highest costs at \$59,957.             | Invest in multi-disciplinary trauma teams and early discharge planning protocols.                                       |
| **3**  | Patients aged 50+ cost 50% more than younger patients --- avg. \$32,584 vs. \~\$21,500.          | Implement geriatric care protocols and community-based post-discharge support programmes.                               |
| **4**  | Fungal infections cost \$340,911 on average --- more than 12x the system average.                | Develop infection control and antifungal stewardship programmes for early detection and intervention.                   |
| **5**  | Surgical cases are billed 75% higher than medical cases --- \$126,280 vs. \$72,221.              | Apply surgical cost containment strategies: implant standardisation, pre-surgical optimisation, and theatre efficiency. |
| **6**  | Medicaid and Medicare together account for 78%+ of all inpatient cases.                          | Plan for payer mix risk and ensure care pathways are optimised for high-volume public payer populations.                |
| **7**  | Managed Care (Unspecified) has the highest average cost at \$35,671 among payer types.           | Review and renegotiate Managed Care contracts; align care protocols to managed care specifications.                     |
| **8**  | Life expectancy rate is 96.20%, indicating good care quality outcomes.                           | Maintain current care quality standards while pursuing cost efficiency improvements.                                    |
| **9**  | 8,109 patients (68%+) were discharged to home or self-care --- the largest disposition category. | Strengthen post-discharge community support and home health services to reduce re-admission risk.                       |
| **10** | 433 patients left against medical advice --- a significant care gap and re-admission risk.       | Investigate reasons for self-discharge and implement patient engagement and care satisfaction initiatives.              |

**11. Recommendations**

Each recommendation below is directly mapped to a data-driven insight and includes estimated business impact and feasibility assessment.

|        |                                          |                                                                                                                                                                                                     |            |                 |
|--------|------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------|-----------------|
| **\#** | **Recommendation**                       | **Rationale & Action**                                                                                                                                                                              | **Impact** | **Feasibility** |
| **R1** | **High-severity early triage**           | Extreme severity cases cost 4.7x more than minor cases. Implement fast-track triage and dedicated resource pathways for extreme and major severity patients to reduce escalation risk.              | High       | High            |
| **R2** | **Trauma & urgent pathway optimization** | Trauma admissions average 15.33 days and \$59,957 - the highest of all admission types. Dedicated multi-disciplinary trauma teams and care coordination can reduce unnecessary bed days.            | High       | Medium          |
| **R3** | **Elderly patient management program**   | Patients aged 50-69 and 70+ have significantly higher costs (\$32,584 and \$32,151) and LOS (7+ days). Implement geriatric care protocols, early discharge planning, and post-acute support.        | High       | High            |
| **R4** | **Surgical cost containment strategy**   | Surgical cases generate \$126,280 in avg. charges vs. \$72,221 for medical. Pre-surgical optimization checklists and implant/supply cost standardization can reduce surgical costs.                 | High       | Medium          |
| **R5** | **Managed Care cost review**             | Managed Care (Unspecified) shows the highest avg. cost among payer types (\$35,671). Renegotiate contracts and align care protocols to managed care expectations.                                   | Medium     | High            |
| **R6** | **High-cost diagnosis management**       | Fungal infections (\$340,911 avg.) and Encephalitis (\$214,350 avg.) are top-cost diagnoses. Develop clinical protocols for early detection, infection control, and antifungal stewardship.         | High       | Medium          |
| **R7** | **Emergency-to-elective channel shift**  | While emergency admissions are common, elective admissions are significantly cheaper (\$29,366 vs \$27,393 emergency). Where clinically feasible, redirect suitable cases to planned care pathways. | Medium     | Medium          |
| **R8** | **Discharge planning enhancement**       | 8,109 patients discharged to Home or Self-Care and 1,394 to Home with Health Services. Strengthening discharge planning and community-based support can reduce re-admission risk.                   | Medium     | High            |

**12. Impact Estimation**

The following impact estimates are derived from the data findings. All figures are approximate and based on observed cost differentials and industry benchmarks.

**12.1 Cost Savings**

- Severity triage optimisation: If even 5% of Extreme severity cases are caught earlier (reducing costs by 15%), this could save approximately \$1.7M across the dataset\'s 11,835 cases.

- Trauma LOS reduction: Reducing average trauma LOS from 15.33 to 13 days (a conservative 2-day reduction per trauma case) could yield significant bed-day savings.

- Surgical cost containment: Standardising surgical supply chains and optimising theatre efficiency could reduce surgical avg. charges by 10-15%.

**12.2 Efficiency Improvements**

- Discharge planning: Improving discharge planning for home-care-bound patients (8,109 cases) could reduce average LOS by 0.5 days, significantly improving bed utilisation.

- Geriatric protocols: Structured geriatric care pathways could reduce LOS for 50+ patients by 1 day, improving throughput and reducing cost per case by approximately \$4,500.

**12.3 Service Quality Improvements**

- Reducing the 433 \'left against medical advice\' cases through improved patient engagement could reduce re-admission rates and associated costs.

- Early detection programmes for fungal infections and encephalitis could reduce diagnosis-specific costs by 20-30% through earlier intervention.

**12.4 Risk Reduction**

- Payer mix diversification strategies could reduce over-reliance on Medicaid/Medicare (78% of volume) and improve revenue stability.

- Managed Care contract optimisation could reduce the avg. cost premium of \$35,671 for this payer segment.

**13. Limitations**

**13.1 Data Limitations**

- Single year of data (2022 only): Trend analysis across multiple years is not possible, limiting the ability to assess improvement or deterioration over time.

- De-identified data: Patient-level tracking across multiple admissions is not possible, preventing readmission analysis.

- Sparse columns: Payment Typology 2 & 3 and Birth Weight had significant missing data and were excluded, potentially limiting analysis of secondary payer patterns.

- Total Charges vs. Total Costs: Charges represent billed amounts and may not reflect actual reimbursements or contracted rates.

- Geographic granularity: Analysis is limited to Hospital Service Area level --- facility-level benchmarking is not available.

**13.2 Assumption Risks**

- Extreme outliers in LOS and Total Costs were retained as clinically valid, but some may represent data quality issues in the original SPARCS extract.

- The \'Life Expectancy\' KPI in this context measures in-hospital survival rate (non-expired cases / total cases), which differs from population-level life expectancy.

- Impact estimates in Section 12 are indicative and based on proportional reasoning rather than formal econometric modelling.

**13.3 What Cannot Be Concluded**

- Causal relationships cannot be established --- e.g., we cannot conclude that higher severity causes higher cost independently of other confounding variables.

- Quality of care at a provider/facility level cannot be assessed from this dataset.

- Patient satisfaction and experience data are not available in this dataset.

- The analysis does not account for inflation or year-over-year cost trends, as only 2022 data is analysed.

**14. Future Scope**

**14.1 Additional Analyses**

- Multi-year trend analysis: Incorporating SPARCS data from 2018-2022 to identify cost trends, LOS improvements, and the impact of COVID-19 on inpatient volumes and costs.

- Predictive modelling: Building regression models to predict LOS and Total Costs based on admission characteristics (severity, age, diagnosis) at the point of admission --- enabling proactive resource planning.

- Re-admission analysis: Linking de-identified records longitudinally (if data permits) to calculate re-admission rates by diagnosis and severity group.

- Geographic benchmarking: Comparing cost and LOS across Hospital Service Areas (e.g., New York City vs. Hudson Valley vs. Finger Lakes) to identify regional performance variations.

- Payer mix optimisation modelling: Scenario analysis on how shifting payer mix (e.g., increasing private insurance volume) could impact total revenue.

**14.2 New Data Requirements**

- Multi-year SPARCS data (2018-2022) for longitudinal analysis.

- Patient-level re-admission data to enable readmission rate calculations.

- Staffing and resource utilisation data to model the relationship between resource inputs and LOS.

- Actual reimbursement rates by payer type (vs. billed charges) for accurate revenue analysis.

- Patient satisfaction scores (HCAHPS) to correlate care quality with cost and LOS data.

**15. Conclusion**

This project delivered a comprehensive, data-driven intelligence framework for understanding hospital inpatient cost and length of stay patterns using New York State SPARCS 2022 discharge data. Through structured data cleaning, KPI engineering, six pivot analyses, and an interactive Google Sheets dashboard, the team identified clear, actionable insights across clinical severity, admission type, patient demographics, diagnosis categories, and payer types.

The analysis conclusively demonstrates that illness severity is the primary driver of both cost and LOS, with extreme severity cases costing 4.7x more than minor cases. Trauma admissions, patients aged 50 and above, and specific high-cost diagnoses (particularly fungal infections and encephalitis) represent priority areas for targeted cost management intervention. The 96.20% life expectancy rate confirms that care quality is being maintained, providing a strong foundation from which to pursue cost efficiency improvements without compromising patient outcomes.

The eight recommendations provided --- spanning severity triage, trauma pathway optimisation, geriatric care protocols, surgical cost containment, high-cost diagnosis management, and payer strategy --- are directly grounded in the data findings and are designed to be practically implementable by hospital administrators and healthcare policy makers.

The dashboard created in Google Sheets provides a reusable, interactive intelligence tool that can be refreshed with updated discharge data to support ongoing monitoring and decision-making across hospital management teams.

**Appendix A: Data Dictionary**

Full data dictionary for the Cleaned_Dataset (15 analytical columns):

|                                         |                    |               |                                            |
|-----------------------------------------|--------------------|---------------|--------------------------------------------|
| **Column Name**                         | **Data Type**      | **Unit**      | **Description**                            |
| **Hospital Service Area**               | Text (Categorical) | NA            | Regional service area of the hospital      |
| **Hospital County**                     | Text (Categorical) | NA            | County where hospital is located           |
| **Age Group**                           | Text (Categorical) | NA            | Patient age category                       |
| **Gender**                              | Text (Categorical) | NA            | Patient gender                             |
| **Length of Stay**                      | Integer            | Days          | Number of days patient was admitted        |
| **Type of Admission**                   | Text (Categorical) | NA            | Admission type (Emergency, Elective, etc.) |
| **Patient Disposition**                 | Text (Categorical) | NA            | Patient discharge outcome                  |
| **CCSR Diagnosis Description**          | Text (Categorical) | NA            | Diagnosis classification category          |
| **APR Severity of Illness Description** | Text (Categorical) | NA            | Severity level of illness                  |
| **APR Risk of Mortality**               | Text (Categorical) | NA            | Mortality risk classification              |
| **APR Medical Surgical Description**    | Text (Categorical) | NA            | Indicates medical or surgical case         |
| **Payment Typology 1**                  | Text (Categorical) | NA            | Primary insurance / payment type           |
| **Emergency Department Indicator**      | Text (Categorical) | NA            | Indicates if case originated in ED         |
| **Total Charges**                       | Integer            | Currency (\$) | Total amount billed by hospital            |
| **Total Costs**                         | Integer            | Currency (\$) | Actual hospital treatment cost             |

**Appendix B: All Pivot Table Summaries**

**Pivot Table 1: Severity Impact on Cost & LOS**

|                  |                           |                                |
|------------------|---------------------------|--------------------------------|
| **APR Severity** | **Avg. Total Costs (\$)** | **Avg. Length of Stay (Days)** |
| **Extreme**      | 59,238.31                 | 11.08                          |
| **Major**        | 28,042.51                 | 6.62                           |
| **Moderate**     | 21,464.86                 | 5.29                           |
| **Minor**        | 12,690.26                 | 2.97                           |

**Pivot Table 2: Admission Type Analysis**

|                       |                           |                                |
|-----------------------|---------------------------|--------------------------------|
| **Type of Admission** | **Avg. Total Costs (\$)** | **Avg. Length of Stay (Days)** |
| **Elective**          | 29,366.00                 | 4.80                           |
| **Emergency**         | 27,393.27                 | 6.33                           |
| **Newborn**           | 15,723.55                 | 4.09                           |
| **Trauma**            | 59,957.20                 | 15.33                          |
| **Urgent**            | 49,123.02                 | 9.68                           |

**Pivot Table 3: Top 10 Highest-Cost Diagnoses**

|                                                       |                           |
|-------------------------------------------------------|---------------------------|
| **CCSR Diagnosis**                                    | **Avg. Total Costs (\$)** |
| **Fungal infections**                                 | 340,911.30                |
| **Encephalitis**                                      | 214,349.50                |
| **Endocarditis and endocardial diseases**             | 195,881.64                |
| **Noninfectious hepatitis**                           | 195,150.81                |
| **Disruptive, impulse-control and conduct disorders** | 186,422.12                |
| **Postprocedural or postoperative circulatory**       | 159,883.73                |
| **Respiratory congenital malformations**              | 138,807.54                |
| **Diseases of white blood cells**                     | 137,157.29                |
| **Anal and rectal conditions**                        | 125,140.09                |
| **Leukemia - acute myeloid leukemia**                 | 117,220.72                |

**Pivot Table 4: Medical vs. Surgical**

|               |                             |                                |
|---------------|-----------------------------|--------------------------------|
| **Case Type** | **Avg. Total Charges (\$)** | **Avg. Length of Stay (Days)** |
| **Surgical**  | 126,279.86                  | 6.51                           |
| **Medical**   | 72,221.23                   | 6.12                           |

**Pivot Table 5: Payment Type Analysis**

|                               |                           |                    |
|-------------------------------|---------------------------|--------------------|
| **Payment Type**              | **Avg. Total Costs (\$)** | **Count of Cases** |
| **Medicaid**                  | 25,576.29                 | 4,890              |
| **Medicare**                  | 33,192.87                 | 4,475              |
| **Private Health Insurance**  | 22,601.78                 | 1,985              |
| **Blue Cross/Blue Shield**    | 23,384.99                 | 441                |
| **Self-Pay**                  | 25,009.15                 | 104                |
| **Miscellaneous/Other**       | 34,078.77                 | 24                 |
| **Dept. of Corrections**      | 28,618.93                 | 8                  |
| **Federal/State/Local/VA**    | 13,498.89                 | 13                 |
| **Managed Care, Unspecified** | 35,670.78                 | 10                 |

**Pivot Table 6: Age Group Analysis**

|                 |                           |                                |
|-----------------|---------------------------|--------------------------------|
| **Age Group**   | **Avg. Total Costs (\$)** | **Avg. Length of Stay (Days)** |
| **0 to 17**     | 21,516.35                 | 4.61                           |
| **18 to 29**    | 21,907.75                 | 5.34                           |
| **30 to 49**    | 23,128.68                 | 5.30                           |
| **50 to 69**    | 32,583.94                 | 7.06                           |
| **70 or Older** | 32,150.56                 | 7.04                           |

**Appendix C: Contribution Matrix**

The following matrix documents the contribution of each team member across all project stages. Please update team member names and tick marks as applicable. Contribution claims must be verifiable through Google Sheets Version History.

|                    |                        |              |                    |               |                    |                                     |
|--------------------|------------------------|--------------|--------------------|---------------|--------------------|-------------------------------------|
| **Team Member**    | **Dataset & Sourcing** | **Cleaning** | **KPI & Analysis** | **Dashboard** | **Report Writing** | **Overall Role**                    |
| **Ankit**          | ✓                      | ✓            | ✓                  |               | ✓                  | Lead --- Data, Analysis & Dashboard |
| **Kartik Madaan**  | ✓                      |              | ✓                  | ✓             | ✓                  | Lead --- Analysis, Pivots & Report  |
| **Riya Yadav**     |                        | ✓            | ✓                  |               | ✓                  | Data Cleaning & Analysis            |
| **Pragya Kashyap** |                        | ✓            |                    | ✓             | ✓                  | Dashboard & Report Writing          |
| **Prateek Shukla** | ✓                      | ✓            | ✓                  |               |                    | Dataset Sourcing & Cleaning         |
| **Soumen Dass**    |                        |              | ✓                  | ✓             | ✓                  | Analysis & Visualisation            |

*Declaration: We confirm that the above contribution details are accurate and verifiable through version history and submitted artifacts.*

Team Signature Block: \_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_
