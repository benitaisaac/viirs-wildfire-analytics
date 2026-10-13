# 🔥 VIIRS Wildfire Analytics
### Large-Scale Satellite Data Analysis & Machine Learning

**Python | NVIDIA RAPIDS | cuDF | Scikit-learn | Plotly | Tableau | Power BI | Streamlit**

Analyzing approximately **22 million NASA VIIRS satellite records** to investigate global wildfire patterns, build predictive models, and develop interactive visualizations.

*Graduate group project | San José State University*

---

## Interactive Wildfire Dashboard

https://github.com/user-attachments/assets/012caf4e-f1d3-4aea-b486-f1598b91de72




Developed with Plotly Dash to visualize temporal wildfire trends, geographic detection density, and fire intensity patterns. Users can filter observations by confidence level, FRP range, and season.


---

## Project Overview

Wildfires pose significant environmental and public safety challenges. Satellite imagery provides valuable data for understanding when and where fires occur, but analyzing millions of observations requires efficient data processing and careful modeling.

This project explores global wildfire activity using NASA's Visible Infrared Imaging Radiometer Suite (VIIRS) data from 2024–2025.

We developed an analytical workflow combining:

- **Large-scale data engineering:** Processing millions of satellite observations with NVIDIA RAPIDS.
- **Exploratory data analysis:** Investigating geographic distributions, temporal patterns, and fire intensity.
- **Machine learning:** Comparing baseline and enhanced models to understand wildfire-related patterns and predict fire radiative power (FRP).
- **Data visualization:** Developing interactive dashboards to communicate findings.

### Research Question

What spatial and temporal patterns can be identified from VIIRS satellite data, and how effectively can machine learning models capture relationships in wildfire observations?

## Project at a Glance

| Category | Details |
|---|---|
| Dataset | NASA VIIRS satellite fire detections |
| Scale | Approximately 22 million records |
| Period | 2024–2025 |
| Processing | NVIDIA RAPIDS, cuDF, Python |
| Modeling | Regression, tree-based models, PCA, hyperparameter tuning |
| Visualization | Plotly Dash, Tableau, Power BI, Streamlit |

---

## My Contributions

As part of a four-person graduate team at San José State University, I was responsible for three core components of the wildfire analytics pipeline:

### GPU-Accelerated Data Processing | NVIDIA RAPIDS
- Implemented GPU-accelerated data processing workflows using NVIDIA RAPIDS and cuDF to support analysis of a large-scale satellite dataset.
- Applied GPU-based transformations and aggregations to prepare wildfire detection data for downstream analysis and visualization.

### Machine Learning | Enhanced Models
- Developed and evaluated enhanced machine learning models for predicting Fire Radiative Power (FRP).
- Explored feature engineering, data transformations, and hyperparameter tuning to improve predictive performance beyond baseline approaches.
- Analyzed model performance to understand how different preprocessing and modeling decisions affected predictive accuracy.

### Interactive Data Visualization | Plotly Dash
- Developed an interactive wildfire analytics dashboard using Plotly Dash to explore global fire activity and geographic distributions.
- Implemented filters for confidence level, FRP range, and season, enabling interactive exploration of wildfire observations.
- Created time-series visualizations, geospatial heatmaps, and summary metrics to communicate wildfire activity patterns.

**Collaboration:** This project was completed with three teammates who contributed to baseline modeling, data cleaning, exploratory analysis, and additional dashboards in Tableau, Streamlit, and Power BI.

---

## Technical Approach

### 1. Data Processing & Engineering

The dataset contained approximately 22 million observations, making efficient processing an important consideration.

We used **NVIDIA RAPIDS and cuDF** to perform GPU-accelerated transformations and aggregations.

Key processing steps included:

- Filtering low-confidence fire detections.
- Converting and standardizing date fields.
- Engineering temporal features such as month and seasonal period.
- Aggregating geographic observations into latitude/longitude bins.
- Managing conversions between GPU and CPU DataFrames.

**Technical challenges:** Working with large datasets introduced memory constraints and required careful handling of data transformations.

### 2. Exploratory Data Analysis

We investigated wildfire activity across geography, time, and fire intensity.

Our analyses included:

- Global wildfire hotspot distributions.
- Daily and seasonal detection patterns.
- Fire radiative power (FRP) distributions.
- Spatial density maps.
- Relationships among satellite measurements and wildfire characteristics.

**Key findings:**

- Daily aggregation revealed meaningful variation that broader monthly summaries obscured.
- Weak linear correlations between features and FRP suggested that more complex relationships may be present.
- Outliers and variability in fire measurements presented challenges for predictive modeling.

### 3. Machine Learning

We evaluated multiple modeling approaches to understand the influence of feature engineering and model complexity.

Our workflow included:

- Establishing baseline models.
- Engineering temporal and categorical features.
- Applying logarithmic transformations to highly skewed FRP values.
- Comparing linear and tree-based methods.
- Exploring principal component analysis (PCA).
- Using grid search for hyperparameter tuning.

**Key finding:** Log-transforming FRP improved model performance, particularly for simpler linear approaches.

**[ADD MODEL RESULTS]**

Include a table comparing the strongest models and their evaluation metrics, such as MAE, RMSE, and R², once verified from the notebooks.

### 4. Interactive Data Visualization

To make the analysis accessible, the team developed dashboards using four visualization tools.

| Tool | Purpose |
|---|---|
| Tableau | Visual exploration of wildfire distributions and correlations |
| Plotly Dash | Interactive spatial and temporal analysis |
| Power BI | Summary reporting and analytical dashboards |
| Streamlit | Interactive exploration application |

**[ADD SCREENSHOTS HERE]**

Include screenshots of your strongest dashboard, geographic visualization, and model results.

---

## Project Structure

```text
viirs-wildfire-analytics/
├── EDA Notebooks/        # Exploratory data analysis
├── PCA/                  # Principal component analysis
├── baseline/             # Baseline ML models
├── enhanced_models/      # Feature engineering and tuned models
├── dashboards/           # Interactive visualizations
├── data/                 # Data files
├── cleaning_overview.py  # Data cleaning workflow
├── smaller_dataset.py    # Dataset preparation
└── README.md
```

## Data & Reproducibility

**Data source:** NASA VIIRS satellite fire detection data, 2024–2025.

Due to the size of the original dataset, intermediate data files are stored separately.

[Access the project dataset](https://drive.google.com/file/d/17lHVkabbMYZ8FH9FFHpUXV9TBRMjlCPW/view?usp=sharing)

To explore the code:

1. Clone this repository.
2. Download the required dataset.
3. Place the appropriate files in the `data/` directory.
4. Open the relevant analysis or modeling notebooks.

*Environment-specific dependencies and execution instructions can be added for each component.*

---

## Lessons Learned

This project demonstrated the importance of combining efficient data infrastructure with thoughtful statistical analysis.

Major takeaways included:

- **Scalability:** Large datasets benefit from GPU-accelerated processing, but memory management remains important.
- **Feature engineering:** Transformations and feature selection can meaningfully affect model performance.
- **Data granularity:** The choice of aggregation level influences which patterns become visible.
- **Communication:** Interactive dashboards help translate complex datasets into understandable findings.

---

## Team & Acknowledgments

Originally developed as a collaborative graduate project at San José State University.

[View the original team repository](https://github.com/svtlys/viirs-wildfire-analytics)

All original contributors are acknowledged through the shared repository and preserved Git commit history.

This fork contains additional documentation and improvements for my individual project portfolio.
