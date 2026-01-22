# 🦠 State-Level Drivers of COVID-19 Mortality in the United States (2021)

## 📌 Project Overview
This project analyzes **state-level variation in COVID-19 mortality across the United States in 2021**, with the goal of identifying how **vaccination coverage, testing intensity, and public-health policy stringency** contributed to differences in death rates.

Using publicly available COVID-19 data, the analysis combines **exploratory data analysis, regression modeling, classification, clustering, spatial visualization, and machine learning** to provide a comprehensive view of pandemic outcomes at the state level.

The project emphasizes **reproducibility, interpretability, and clear communication**, aligning with real-world data science workflows.

---

## 🎯 Research Questions
- How strongly is **vaccination coverage** associated with COVID-19 mortality across states?
- Do **testing intensity** and **policy stringency** independently explain mortality differences?
- Can states be **clustered** into meaningful groups based on pandemic characteristics?
- How well can we **classify high-mortality vs low-mortality states** using statistical models?

---

## 📊 Data Source
- **COVID19 R Package**  
  Aggregated state-level COVID-19 data including:
  - Daily deaths
  - Testing counts
  - Vaccination coverage
  - Policy stringency index
  - Population estimates

The analysis focuses on **January 1, 2021 – December 31, 2021**, capturing vaccine rollout and multiple pandemic waves.

---

## 🛠 Methods & Techniques
The project follows an **end-to-end data science pipeline**:

- **Data Cleaning & Feature Engineering**
  - Aggregation to state-level metrics
  - Handling missing and infinite values
  - Outlier detection using IQR rules

- **Exploratory Data Analysis (EDA)**
  - Distributional analysis
  - Bivariate relationships
  - Correlation analysis

- **Statistical Modeling**
  - Multiple linear regression
  - Interaction effects
  - Multicollinearity diagnostics (VIF)

- **Classification**
  - Logistic regression
  - ROC curve and AUC evaluation

- **Unsupervised Learning**
  - K-means clustering to identify state-level patterns

- **Machine Learning**
  - Random forest modeling
  - Variable importance analysis

- **Spatial & Temporal Analysis**
  - US state-level choropleth maps
  - National mortality time trends (7-day rolling averages)

---

## 🔑 Key Findings
- **Vaccination coverage** is the strongest and most consistent predictor of lower COVID-19 mortality.
- States with **higher vaccination rates** experienced substantially fewer deaths per 100,000 people.
- **Testing intensity** and **policy stringency** show weaker independent effects after accounting for vaccination.
- Clustering reveals distinct groups of states:
  - Low vaccination / high mortality
  - High vaccination / moderate mortality
  - High vaccination / low mortality
- Results are consistent across **regression, classification, clustering, and random forest models**.

---

## 📁 Repository Structure

state-level-covid19-mortality/
│
├── code/
│ └── covid19_mortality_analysis.Rmd
│
├── report/
│ ├── covid19_mortality_report.html
│ └── covid19_mortality_report.pdf
│
├── README.md

### Folder Description
- **code/** – Reproducible RMarkdown analysis (data cleaning → modeling → visualization)
- **report/** – Final rendered project reports (HTML and PDF)
- **README.md** – Project documentation and summary

---

## ▶️ How to Reproduce the Analysis
1. Open `covid19_mortality_analysis.Rmd` in **RStudio**
2. Install required packages:
   ```r
   install.packages(c(
     "COVID19", "dplyr", "ggplot2", "lubridate", "janitor",
     "randomForest", "pROC", "corrplot", "zoo", "usmap", "car"
   ))
3. Knit the RMarkdown file to HTML or PDF

📚 Academic Context
Course: DATA 607 – Communication in Data Science and Analytics

Institution: University of Maryland

Author: Pravalika Sure
