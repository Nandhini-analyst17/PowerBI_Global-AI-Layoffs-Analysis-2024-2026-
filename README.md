# PowerBI_Global-AI-Layoffs-Analysis-2024-2026
This study analyses global AI-related layoffs across industries and countries from 2024 to 2026. A Power BI dashboard was developed to vizualise employment trends by comparing AI and non-AI-related layoffs across different industries and countries.

# Global AI Layoffs & Employment Trends (SDG 8)

## 1. Project Overview

This project focuses on **UN Sustainable Development Goal 8 (SDG 8): Decent Work and Economic Growth**, specifically **Target 8.5**, which aims to achieve full and productive employment and decent work for all by 2030.

Using the **Global AI Layoffs and Job Market (2020–Present)** dataset from Kaggle, this project explores employee layoffs, companies, industries, countries, and AI-related workforce reductions.

The growth of artificial intelligence has created a significant impact on the workforce and may contribute to job displacement and affect employment stability. This study investigates layoffs related to AI and non-AI organisations across industries and countries to identify patterns in workforce reduction and consider how these patterns may affect decent and productive employment.

The central question is whether AI adoption is causing layoffs indirectly, or whether other factors are contributing to workforce reductions.

## 2. Data Source

**Dataset:** Global AI Layoffs and Job Market (2020–Present)  
**Platform:** Kaggle  
**Dataset link:** [Global AI Layoffs and Job Market (2020–Present)](https://www.kaggle.com/datasets/belbino/global-ai-layoffs-and-job-market-2020-present)

The dataset includes information about employee layoffs, companies, industries, countries, and AI-related job workforce reductions.

The project uses four CSV datasets loaded into Power BI. The Python EDA notebook uses two cleaned CSV files:

- `global_labor_indicators_clean.csv`
- `layoffs_events_clean.csv`

## 3. Project Workflow and Analysis Periods

The project contains two complementary analysis components: exploratory data analysis (EDA) using Python and an interactive dashboard developed in Power BI.

The two components use different analysis periods for different purposes:

| Component | Analysis period | Purpose |
|---|---|---|
| Python EDA | 2020–2025 | Provides a broader historical overview of layoff events, AI vs non-AI layoff events, labour market indicators, industries, countries, and layoff-count statistics. |
| Power BI dashboard | 2024–2026 | Focuses on more recent AI and non-AI layoff patterns across industries and countries. The 2026 records represent January–April only. |

The Python EDA provides historical context for the more recent period examined in the Power BI dashboard. The analysis periods are intentionally documented separately and are not presented as identical.

## 4. Data Preprocessing

The datasets were preprocessed before analysis.

The preprocessing steps included:

- Screening for missing values and duplicates.
- Standardising inconsistent country names. Different variations of country names, such as **United Kingdom** and **United States**, were standardised into consistent country labels using the Value Replacement and Fill functions in Power Query for the `Global_Labor_Data` dataset.
- Reviewing entries classified as **Other** in the `Layoff_Data` dataset and assigning them to Technology, Software, and Other categories depending on their nature of business.
- Creating a Calendar table to support time-based analysis and comparisons across years.
- Filtering the data for the relevant analysis period.

### Dataset files used in Python EDA

- `global_labor_indicators_clean.csv`
- `layoffs_events_clean.csv`

### Power BI data preparation

Four CSV datasets were loaded into Power BI. The Power Query preparation and modelling process described for the dashboard includes the cleaning and standardisation steps above, as well as the creation of a Calendar table.

## 5. Exploratory Data Analysis (Python)

The exploratory data analysis was conducted using Python in Jupyter Notebook. The notebook is named `EDA_analysis.ipynb` and uses Pandas, NumPy, and Matplotlib to analyse the cleaned datasets and generate visualisations.

### Libraries Used

- **Pandas:** Loading, filtering, grouping, and analysing the datasets.
- **NumPy:** Calculating statistical measures, including the mean, median, and standard deviation.
- **Matplotlib:** Creating graphs and visualisations.

### EDA analysis and visualisations

The notebook filters both datasets to include records from **2020 to 2025** and generates the following visualisations and statistical calculations:

| No. | Visualisation / Analysis | Description |
|---|---|---|
| 1 | Layoff Events by Year (2020–2025) | Shows the number of layoff events by year. |
| 2 | AI vs Non-AI Layoff Events (2020–2025) | Compares yearly layoff event counts between AI and non-AI companies. |
| 3 | Labour Market Trends (2020–2025) | Shows average overall unemployment, youth unemployment, and employment-to-population percentages by year. |
| 4 | Top 10 Industries by Layoff Events | Displays the ten industries with the highest number of layoff events. |
| 5 | Top 10 Countries by Layoff Events | Displays the ten countries with the highest number of layoff events. |
| 6 | Layoff Count Statistical Analysis | Calculates the average, median, and standard deviation of layoff counts using NumPy. |

These EDA outputs provide historical context and supporting analysis for the more recent trends explored in the Power BI dashboard.

## 6. Power BI Dashboard Analysis

The Power BI dashboard focuses mainly on the period **2024–2026** and analyses AI and non-AI layoffs across industries and countries.

### Graph 1: AI vs Non-AI Layoffs by Industry (Top 5)

**Pattern:**
- Retail has the highest AI layoffs, at approximately 32K, similar to Hardware, which is the second highest.
- Technology shows the opposite pattern, with approximately 40K non-AI layoffs compared with only a small AI share.
- Transportation and Consumer show almost no AI-linked layoffs.

**Interpretation:**

This may indicate that AI has different impacts on employment across industries. The impact of technological advances on the job market is not uniform.

### Graph 2: Average Workforce Affected by Industry (Top 10)

**Pattern:**
- Transportation loses the largest share of staff per event, at approximately 36%.
- Sales follows at approximately 33%, and Retail at approximately 32%.
- Real Estate and Travel are much lower.

**Interpretation:**

The total number of laid-off workers may not correctly reflect employment disruption. This measure can be used to identify industries with a larger impact by estimating the average layoffs workforce relative to workforce size.

## 7. Key Insights

- **AI-related layoffs:** AI accounts for around 30.4% of layoffs. Out of 231K layoffs, approximately 70K are AI-related and 161K are non-AI-related. AI is already a significant contributor to job losses, although most layoffs have other reasons.
- **Industry differences:** Retail and Hardware are mostly AI-driven, while Technology's layoffs are largely non-AI. Finance and Retail lead in total layoffs. Consumer, Finance, and Retail rank highest by total layoffs.
- **Workforce impact:** Transportation, Sales, and Retail have the highest percentage of workforce affected per occurrence, indicating higher risk.
- **Geographical distribution:** Layoffs are geographically concentrated, with the United States dominating. Therefore, the impact on employment is not uniformly shared around the globe.

## 8. Research Questions

**RQ1:** What are the global trends and patterns in layoffs within AI-related organisations from 2024 to 2026?

**RQ2:** In between 2024 and 2026, which were the industries records the most layoffs in concern with AI-related organisations?

**RQ3:** What are the variations in layoff trends among AI-related organisations across various countries and regions from 2024 to 2026?

**RQ4:** How effectively can machine learning models predict layoff counts and detect patterns related to layoffs of AI-related companies using historical company-level and aggregated data?

**RQ5:** How much are global layoff trends of AI-related businesses linked with AI developments and other contributing factors such as organizational changes, business restructuring and economic conditions?

## 9. Recommendations

### Government & Organization

Since AI-related layoffs account for 30.4% of workforce layoffs, developing essential computing skills may help people adapt to new job demands and retain employability. Hence, reskilling and skills programmes should be strengthened.

### Employers

Businesses should explore options such as job redesign and collaboration between humans and AI. It is advisable to retrain employees for new roles instead of firing them.

### Predictive Analysis

Develop a machine learning model to analyse this trend and identify the most affected groups. This information can help policymakers take appropriate action.

## 10. Project Files

The repository analysis materials include:

| File | Description |
|---|---|
| `EDA_analysis.ipynb` | Python notebook for exploratory data analysis. |
| `global_labor_indicators_clean.csv` | Cleaned labour indicators dataset used in the EDA notebook. |
| `layoffs_events_clean.csv` | Cleaned layoffs events dataset used in the EDA notebook. |

The Power BI project uses four CSV datasets, as described in the data preprocessing section. The two CSV filenames listed above are the files referenced by the Python EDA notebook.

## 11. How to Run the Python EDA Notebook

1. Clone or download this repository.
2. Ensure `global_labor_indicators_clean.csv` and `layoffs_events_clean.csv` are available in the same working directory as the notebook, or update the file paths in the notebook to match their locations.
3. Open `EDA_analysis.ipynb` in Jupyter Notebook or JupyterLab.
4. Install the required Python libraries, if they are not already installed.
5. Run the notebook cells to load the datasets, filter the analysis period, generate the graphs, and calculate the layoff statistics.

Install the required libraries using:

```bash
pip install pandas numpy matplotlib
```

## 12. Project Objective

This project aims to investigate global AI and non-AI layoff patterns, examine differences across industries and countries, and consider the implications for employment stability and decent work in relation to **UN SDG 8, Target 8.5**.

The Python EDA contributes a broader historical perspective (2020–2025), while the Power BI dashboard provides a focused view of recent layoff trends (2024–2026). Together, these components support the project's investigation of AI-related workforce changes and employment trends.
