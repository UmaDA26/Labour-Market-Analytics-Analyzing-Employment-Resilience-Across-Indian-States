# 📊 Labour Market Analytics: Employment Resilience Across Indian States

## 📌 Project Overview

This project analyzes India's labour market using data from the **Periodic Labour Force Survey (PLFS)** to understand how employment indicators changed across Indian states before, during, and after the COVID-19 pandemic.

Using Python for data cleaning, exploratory data analysis (EDA), and statistical analysis, four PLFS datasets were merged into a single analysis-ready dataset. Power BI was then used to develop interactive dashboards to explore labour market trends, state-wise unemployment shocks, recovery patterns, gender disparities, and sector-wise employment distribution.

The analysis covers **2019–2024**, with a particular focus on three phases:

* **Pre-COVID:** 2019
* **Pandemic:** 2020
* **Recovery:** 2022

This is a descriptive and diagnostic analytics project that uses statistical analysis and transparent, rule-based comparisons rather than machine learning.

## 🎯 Project Objectives

* Integrate four PLFS datasets covering LFPR, UR, WPR, and sector-wise employment.
* Analyze labour market trends across Indian states, genders, age groups, and years.
* Evaluate the impact of COVID-19 on unemployment and labour force participation.
* Identify states that experienced the largest unemployment shocks.
* Compare state-wise unemployment recovery by 2022.
* Examine gender disparities in labour force participation and unemployment.
* Analyze employment distribution across agriculture, secondary, and tertiary sectors.
* Develop interactive Power BI dashboards to communicate findings and support data-driven recommendations.

## 📂 Data Sources

**Primary Source:** Periodic Labour Force Survey (PLFS), published by the Ministry of Statistics and Programme Implementation (MoSPI).

**Data Access:** India Data Portal.

Source: https://indiadataportal.com/p/employment

### Datasets Used

Four CSV datasets were used:

1. Labour Force Participation Rate (LFPR)
2. Unemployment Rate (UR)
3. Worker Population Ratio (WPR)
4. Sector-wise Employment

### Dataset Summary

| Attribute             | Details                                      |
| --------------------- | -------------------------------------------- |
| Data source           | Periodic Labour Force Survey (PLFS)          |
| Analysis period       | 2019–2024                                    |
| Geographic coverage   | 22 Indian states and the All-India aggregate |
| Data frequency        | Quarterly                                    |
| Raw datasets          | 4 CSV files                                  |
| Merged dataset        | 4,347 rows × 12 columns                      |
| Final cleaned dataset | 4,347 rows × 17 columns                      |
| File format           | CSV                                          |

## 🛠️ Technology Used

| Technology       | Purpose                                                                               |
| ---------------- | ------------------------------------------------------------------------------------- |
| Python           | Data loading, cleaning, transformation, EDA, and statistical analysis                 |
| Pandas           | Data manipulation, merging, grouping, and missing-value checks                        |
| NumPy            | Numerical operations and statistical calculations                                     |
| Matplotlib       | Data visualization and customized charts                                              |
| Seaborn          | Statistical visualization, including heatmaps and boxplots                            |
| Power BI Desktop | Interactive dashboard development and data visualization                              |
| Power Query      | Data transformation and preparation                                                   |
| DAX              | Measures, phase-wise comparisons, unemployment shock calculations, and state rankings |
| Google Colab     | Python notebook development and analysis                                              |
| GitHub           | Project documentation and portfolio presentation                                      |

## 🔄 Project Workflow

The project followed a structured data analytics workflow:

1. **Data Collection:** Imported four PLFS datasets in CSV format.
2. **Data Understanding:** Examined dataset dimensions, column names, data types, missing values, and duplicate records.
3. **Data Cleaning:** Removed unwanted columns, addressed duplicate records, checked missing values, and validated the datasets.
4. **Data Integration:** Merged the four datasets using appropriate state, year, quarter, gender, and age-group keys.
5. **Feature Engineering:** Created additional columns for quarter number, period, phase, and log-transformed variables.
6. **Exploratory Data Analysis:** Examined distributions, outliers, correlations, trends, and differences across states and demographic groups.
7. **Statistical Analysis:** Compared labour market indicators across pre-COVID, pandemic, and recovery phases.
8. **Power BI Development:** Created DAX measures, organized the data model, and developed interactive dashboards.
9. **Insight Generation:** Identified major unemployment shocks, recovery patterns, gender disparities, and sectoral differences.
10. **Recommendations:** Translated the findings into actionable recommendations for employment analysis and policy discussion.

## 🧹 Data Cleaning and Preprocessing

The four source datasets were cleaned and integrated using Python.

### Key Activities

* Removed unwanted ID columns before merging.
* Excluded 2018 records because LFPR and WPR contained conflicting duplicate records for the same state, period, age group, and gender.
* Identified and resolved duplicate keys in the sector-wise employment dataset.
* Checked missing values and handled missing agriculture-sector shares after validating the other sector shares.
* Merged LFPR, UR, and WPR using the appropriate combination of state, year, quarter, age group, and gender.
* Merged sector-wise employment using a reduced set of keys because the sector dataset did not contain an age-group field.
* Detected outliers using the Interquartile Range (IQR) method.
* Examined skewness and applied logarithmic transformations to highly skewed variables.
* Standardized column names and checked data types.
* Created derived features for quarter number, period, and analytical phase.

### Feature Engineering

| Feature      | Description                                                                  |
| ------------ | ---------------------------------------------------------------------------- |
| `Quarter_no` | Numerical representation of the survey quarter                               |
| `Period`     | Combined year and quarter label, such as 2019 Q2                             |
| `Phase`      | Categorizes observations into Pre-COVID, Pandemic, Recovery, and Other Years |
| `UR_log`     | Log-transformed unemployment rate                                            |
| `Agri_log`   | Log-transformed agriculture employment share                                 |

### Data Quality Results

* Final dataset: **4,347 records and 17 columns**
* Missing values after final validation: **0**
* Duplicate keys after final validation: **0**

The cleaned dataset was saved as `Cleaned_labour_market_data.csv`.

## 🔍 Exploratory Data Analysis (EDA)

Python was used to perform univariate, bivariate, and multivariate analysis.

### 1. Univariate Analysis

* Examined record distributions across years and genders.
* Analyzed the distributions of LFPR, UR, and agriculture employment.
* Used boxplots to examine variation and potential outliers in labour market indicators.

### 2. Bivariate Analysis

* Compared average unemployment rates across states.
* Examined average LFPR by gender.
* Compared unemployment across analytical phases.
* Analyzed the relationship between LFPR and WPR.
* Investigated unemployment and tertiary-sector employment relationships.
* Examined correlations among labour market indicators.

### 3. Multivariate Analysis

* Created pair plots to compare LFPR, UR, and WPR across genders.
* Analyzed labour market changes by phase and gender.
* Developed a state-wise unemployment heatmap across years.
* Created a bubble scatter plot comparing LFPR and UR, with agriculture and tertiary-sector employment used as additional visual dimensions.

These analyses helped identify important trends, state-level disparities, and potential relationships between employment indicators.

## 📊 Power BI Dashboard Development

An interactive, two-page Power BI dashboard was developed to present the findings.

### Dashboard 1: Labour Market Overview

**Objective:** Understand India's overall labour market trends and differences across states and demographic groups.

**Key Performance Indicators (KPIs)**

* Average Labour Force Participation Rate (LFPR)
* Average Unemployment Rate (UR)
* Average Worker Population Ratio (WPR)
* Average Agriculture Employment Share

**Visualizations**

* LFPR trend from 2019 to 2024
* Unemployment Rate trend
* Worker Population Ratio trend
* Employment share by sector
* Male versus female labour market comparison
* State-wise Labour Force Participation Rate

**Interactive Features**

* Gender slicer
* Age-group slicer
* State slicer
* Interactive charts and cross-filtering
* Key insights displayed alongside the visualizations

**Purpose:** Provide an overview of labour market performance and highlight trends, gender disparities, and differences across states.
<img width="1338" height="732" alt="Screenshot 2026-10-24 195644" src="https://github.com/user-attachments/assets/221e821b-28c5-4a6c-abc1-591c0d896913" />


### Dashboard 2: Labour Market Resilience

**Objective:** Assess the severity of pandemic-related unemployment shocks and compare recovery across Indian states.

**Key Performance Indicators (KPIs)**

* Pre-COVID Unemployment Rate
* Pandemic Unemployment Rate
* Recovery Unemployment Rate
* Increase in Unemployment Rate during the pandemic

**Visualizations**

* State-wise unemployment increase during 2020
* State-wise unemployment recovery by 2022
* Relationship between unemployment shock and recovery
* LFPR comparison across pre-COVID, pandemic, and recovery phases
* Treemap showing where unemployment peaked
* State Resilience Ranking table
* Unemployment Rate by State and Year heatmap

**Interactive Features**

* Age-group slicer
* State slicer
* Interactive state comparisons
* Conditional formatting for state rankings and recovery indicators
* Key insights explaining the impact and recovery patterns

**Purpose:** Identify states that experienced severe unemployment shocks, compare recovery performance, and distinguish states that returned to or remained above their pre-COVID unemployment levels.
<img width="1381" height="730" alt="Screenshot 2026-10-24 195718" src="https://github.com/user-attachments/assets/fbb74507-0805-4a91-9a32-beaf47fa940c" />


## 📐 DAX Measures and Data Modeling

A dedicated `Labour_Measures` table was created to organize DAX measures separately from the `Fact_Labour` table.

### Key Measures

| Measure               | Purpose                                                                                |
| --------------------- | -------------------------------------------------------------------------------------- |
| `Average_LFPR`        | Calculates average Labour Force Participation Rate                                     |
| `Average_UR`          | Calculates average Unemployment Rate                                                   |
| `Average_WPR`         | Calculates average Worker Population Ratio                                             |
| `Average_Agriculture` | Calculates average agriculture employment share                                        |
| `PreCOVID_UR`         | Calculates unemployment during 2019                                                    |
| `Pandemic_UR`         | Calculates unemployment during 2020                                                    |
| `Recovery_UR`         | Calculates unemployment during 2022                                                    |
| `PreCOVID_LFPR`       | Calculates LFPR during the pre-COVID phase                                             |
| `Pandemic_LFPR`       | Calculates LFPR during the pandemic phase                                              |
| `Recovery_LFPR`       | Calculates LFPR during the recovery phase                                              |
| `UR Rise`             | Measures the increase in unemployment from pre-COVID to the pandemic                   |
| `UR Recovery`         | Measures the decline in unemployment from the pandemic to recovery                     |
| `UR Gap`              | Measures the difference between recovery and pre-COVID unemployment                    |
| `Shock Rank`          | Ranks states by the increase in unemployment                                           |
| `Recovery Rank`       | Ranks states by the decline in unemployment                                            |
| `Recovery Ratio`      | Measures the proportion of the pandemic unemployment increase reversed during recovery |
| `Status`              | Identifies whether a state returned to or fell below its pre-COVID unemployment level  |
| `Recovery Level`      | Categorizes recovery using rule-based thresholds                                       |

The dashboards use these measures to compare labour market conditions and communicate state-level differences.

## 💡 Key Findings and Insights

### 1. COVID-19 Impact on Unemployment

* Average unemployment increased from approximately **9.52% before COVID-19 to 13.67% during the pandemic**.
* By the recovery phase in 2022, average unemployment had declined to approximately **8.79%**.
* Maharashtra experienced the largest unemployment increase, rising from 6.8% to 19.6%, an increase of **12.8 percentage points**.
* Jharkhand and Kerala also experienced substantial unemployment increases.

### 2. State-wise Recovery

* **15 of the 22 states** returned to or fell below their pre-COVID unemployment levels by 2022.
* Delhi recorded a decline of approximately 7.2 percentage points from its pandemic peak and ended about 6.0 points below its pre-COVID level.
* Seven states remained above their pre-COVID unemployment levels: Rajasthan, Chhattisgarh, Haryana, Jammu and Kashmir, Bihar, Himachal Pradesh, and Karnataka.
* The results demonstrate that recovery varied across states.

### 3. Gender Disparities

* Average male LFPR was approximately **57.1%**, compared with **16.9% for females**.
* Female unemployment was approximately **11.1%**, compared with **8.6% for males**.
* Female LFPR increased from approximately 15.6% to 20.3% during the analysis period.
* The findings highlight persistent differences in labour force participation and unemployment between men and women.

### 4. State-wise Labour Force Participation

* Himachal Pradesh recorded the highest average LFPR at approximately **43.51%**.
* Bihar recorded the lowest average LFPR at approximately **28.39%**.
* The difference between these states was approximately 15 percentage points.

### 5. Employment by Sector

* The tertiary or services sector accounted for the largest share of employment, with a median share of approximately 63%.
* The secondary or industrial sector followed at approximately 30%.
* Agriculture accounted for approximately 6%.

These findings provide a descriptive overview of employment distribution and regional differences in labour market conditions.

## 🧠 Analytical Approach

The project focuses on two main forms of analytics.

### Descriptive Analytics

* Summarized labour market indicators using averages and distributions.
* Compared employment indicators across years, states, genders, and age groups.
* Examined changes in unemployment and labour force participation.
* Analyzed employment shares across sectors.

### Diagnostic Analytics

* Investigated the relationship between sector structure and labour market outcomes.
* Examined correlations among LFPR, UR, and WPR.
* Identified states with severe unemployment shocks and stronger recovery.
* Compared recovery outcomes against pre-COVID unemployment levels.

**Note:** This project does not implement predictive machine learning models. Its conclusions are based on historical data, descriptive statistics, and rule-based comparisons.

## 📌 Recommendations

Based on the analysis, the following recommendations were identified:

1. **Support slow-recovering states:** Prioritize states that remained above their pre-COVID unemployment levels with sustained employment initiatives.
2. **Improve women's labour force participation:** Encourage access to employment opportunities, skill development, and childcare support.
3. **Address gender disparities:** Develop targeted training and placement programmes to address differences in unemployment.
4. **Expand non-farm employment:** Explore opportunities for industrial and service-sector employment, particularly in states with lower labour force participation.
5. **Learn from stronger recovery outcomes:** Examine the recovery patterns of states that returned below their pre-COVID unemployment levels.
6. **Monitor multiple indicators:** Track LFPR and WPR alongside unemployment to obtain a more complete picture of labour market recovery.


