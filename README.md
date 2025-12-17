# NYC Yellow Taxi Data Analysis & Visualization (2015)

## Project Overview
Every taxi ride tells a story — of time, distance, money, and movement.

This project analyzes over **one million NYC Yellow Taxi trips from 2015**, transforming raw trip-level data into a complete **data analytics and visualization journey**. From preprocessing and feature engineering to clustering, regression, and time-series analysis, the project uncovers meaningful patterns behind **pickup hotspots, peak travel hours, fare behavior, and customer mobility trends**.

By combining **Python-based analysis**, **KNIME workflows**, and **interactive dashboards built using Tableau and Power BI**, the project demonstrates how large-scale urban transportation data can be converted into actionable insights for operational and business decision-making.


---

## Dataset Information
- **Dataset Name:** NYC Yellow Taxi Trip Data
- **Year Used:** 2015
- **Source:** Kaggle  
- **Dataset Link:**  
  https://www.kaggle.com/datasets/elemento/nyc-yellow-taxi-trip-data
  
### Final Dataset Used
https://docs.google.com/spreadsheets/d/1h9fRKx9_PxuGk1PytCXSCwvTGnO-VUlu/edit?usp=drive_link&ouid=104901862408898418589&rtpof=true&sd=true


### Key Columns
- **Trip Details:** `trip_distance`, `trip_duration_min`, `passenger_count`
- **Time Features:** `hour`, `day`, `month`, `day_of_week`, `is_weekend`
- **Fare & Payment:** `fare_amount`, `tip_amount`, `tolls_amount`, `total_amount`
- **Location:** `pickup_latitude`, `pickup_longitude`, `dropoff_latitude`, `dropoff_longitude`
- **Engineered Features:**  
  `haversine_km`, `avg_speed_kmph`, `fare_per_km`, `fare_per_min`, `tip_rate`

---

## Tools & Technologies
- **Python:** Pandas, NumPy, Matplotlib, Seaborn, Scikit-learn
- **KNIME Analytics Platform**
- **Tableau Public**
- **Microsoft Power BI**
- **GitHub** (Version Control & Documentation)

---

## Project Workflow
1. Data Cleaning & Validation  
2. Feature Engineering  
3. Outlier Detection & Treatment  
4. Exploratory Data Analysis (EDA)  
5. Clustering (K-Means)  
6. Regression Modeling  
7. Time Series Analysis  
8. Dashboard Creation  
9. Reporting & Documentation  

---

## Repository Structure

<pre>
NYC-YELLOW-TAXI-DAV/
│
├── Images/
│ ├── KNIME Workflow.png
│ ├── PowerBI Dashboard 1.png
│ ├── PowerBI Dashboard 2.png
│ ├── Tableau Dashboard 1.png
│ └── Tableau Dashboard 2.png
│
├── Source/
│ ├── Original Source Link.txt
│ └── Used Data Source Link.txt
│
├── KNIME_Workflow.knwf
├── Power_BI_Dashboards.txt
├── Tableau_Dashboards.txt
├── Project_Code.ipynb
├── Project_Report.docx
└── README.md
</pre>

---

## Analysis Performed

### 🔹 Exploratory Data Analysis
- Distribution of trip distance, duration, fare, and tips
- Correlation heatmaps
- Hourly and daily trip patterns

### 🔹 Clustering (K-Means)
- Segmentation based on:
  - Trip distance
  - Duration
  - Fare amount
  - Speed
- Identified **short**, **medium**, and **long-distance trip clusters**

### 🔹 Regression Analysis
- Target variable: `total_amount`
- Models used:
  - Linear Regression
  - Random Forest Regression
- Evaluation metrics:
  - RMSE
  - MAE
  - R² Score

### 🔹 Time Series Analysis
- Daily and hourly trip trends
- Weekly seasonality
- Moving averages and trend analysis

**Python Code Location**
/Project_Code.ipynb

---

## Dashboards

### Dashboard 1: Operations Overview
**Purpose:** Operational monitoring

**KPIs:**
- Total Trips
- Average Trip Duration (minutes)
- Average Trip Distance (miles)
- Average Speed (km/h)
- Mean Fare Amount ($)
- Average Tip Rate

**Visuals:**
- Trips by Hour (Line Chart)
- Trips by Day of Week (Bar Chart)
- Pickup Hotspots (Map)
- Fare vs Tip (Scatter Plot)

**Filters:**
- Hour
- Day of Week
- Payment Type

**Dashboard Preview:**  
![Tableau Dashboard 1](Images/Tableau%20Dashboard%201.png)

---

### Dashboard 2: Customer & Revenue Insights
**Purpose:** Business and customer behavior analysis

**Visuals:**
- Revenue trends
- Trip efficiency metrics
- Cluster-based customer segmentation
- Time-based demand analysis

**Dashboard Preview:**  
![Tableau Dashboard 2](Images/Tableau%20Dashboard%202.png)

---

## Key Insights
- **Peak pickup times:** 8–10 AM and 5–8 PM
- **Pickup hotspots:** Manhattan and Downtown NYC
- **Longer trips → higher fares and tips**
- **Weekends show higher average trip distance**
- **Strong positive correlation between distance and total fare**
- **Cluster analysis reveals distinct trip behavior patterns**

---

## KNIME Workflow

The project includes a complete **KNIME Analytics Platform workflow** that demonstrates the end-to-end analytics process in a low-code environment.

### 🔹 Workflow Overview
The KNIME workflow performs the following steps:

1. **Data Ingestion**
   - Data loaded using the *Excel Reader* node.

2. **Data Cleaning**
   - Detection and removal of numerical outliers using IQR-based filtering.
   - Handling missing values for numerical and categorical fields.
   - Column filtering to retain only relevant features.

3. **Data Preparation**
   - Normalization of numerical features using Min-Max scaling.
   - Optional row sampling for performance optimization.

4. **Exploratory Analysis**
   - Histograms and box plots for distribution analysis.
   - Correlation heatmap to identify relationships between features.
   - Scatter plots for fare, distance, and tip analysis.

5. **Clustering**
   - K-Means clustering applied on normalized numerical features.
   - Visual inspection of clusters using scatter plots.
   - Identification of distinct trip behavior patterns.

6. **Regression Modeling**
   - Linear Regression model to predict `total_amount`.
   - Train–test split using Table Partitioner.
   - Model evaluation using RMSE, MAE, and R² metrics.
   - Actual vs Predicted visualization using scatter plots.

**Workflow File:**  
/KNIME_Workflow.knwf


**Workflow Snapshot:**  
![KNIME Workflow](Images/KNIME%20Workflow.png)

---

## Power BI Dashboards

Power BI is used to create **interactive, business-focused dashboards** that provide actionable insights from the cleaned dataset.

### Dashboard 1 – Operations Overview
**Focus:** Taxi operations and demand monitoring

**KPIs Included:**
- Total Trips
- Average Trip Duration (minutes)
- Average Trip Distance (miles)
- Average Speed (km/h)
- Mean Fare Amount
- Average Tip Rate

**Visualizations:**
- Trips by Hour (Line Chart)
- Trips by Day of Week (Bar Chart)
- Pickup Hotspots (Map)
- Fare vs Tip Relationship (Scatter Plot)

**Interactive Filters:**
- Hour
- Day of Week
- Payment Type

**Dashboard Preview:**  
![Power BI Dashboard 1](Images/PowerBI%20Dashboard%201.png)

---

### Dashboard 2 – Revenue & Customer Insights
**Focus:** Business performance and customer behavior

**Visualizations:**
- Revenue trends across time
- Trip efficiency metrics
- Customer segmentation using clusters
- Time-based travel patterns

**Insights Provided:**
- Revenue contribution by trip type
- High-value customer behavior
- Peak revenue periods

**Dashboard Preview:**  
![Power BI Dashboard 2](Images/PowerBI%20Dashboard%202.png)

---

## Value of Multi-Tool Approach
This project demonstrates the same dataset analyzed through **multiple analytics platforms**, showcasing:

- Python for flexible data science workflows
- KNIME for visual and reproducible analytics
- Tableau and Power BI for stakeholder-ready dashboards

This highlights adaptability across tools and real-world analytics practices.

---

## Project Report
A detailed report including:
- Methodology
- Visualizations
- KNIME workflow explanation
- Dashboard screenshots
- Insights & conclusions

Location:
/Project_Report.docx

---

## How to Use This Project
- **Python:** Open `.ipynb` files using Jupyter Notebook
- **Tableau:** Open `.twbx` files in Tableau Public
- **Power BI:** Open `.pbix` file in Power BI Desktop
- **KNIME:** Import `.knwf` file into KNIME Analytics Platform

---

## Author
**Tapasya Patel**  
**Varun Patel**  

Data Analytics & Visualization Project

---

## Acknowledgements
- NYC Taxi & Limousine Commission
- Kaggle Dataset Contributors
- Folium for spatial visualizations


