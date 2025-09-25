# Urban Flood Risk Predictor

## Project Overview
This project builds a **machine learning classification model** using the **Urban Flood Risk Data: Global City Analysis 2025** dataset from Kaggle. The goal is to predict **flood risk levels** for urban areas—**High, Medium, or Low**—based on environmental and urban factors such as rainfall intensity, elevation, land use, soil type, drainage infrastructure, and more.  

The analysis helps identify the **key drivers of urban flood risk**, supporting city planners and policymakers in making **data-driven decisions** to allocate resources and implement mitigation strategies.

---

## Dataset
- **Source:** [Urban Flood Risk Data: Global City Analysis 2025 (Kaggle)](https://www.kaggle.com/datasets)  
- **Size:** 2,963 rows × 17 columns (after cleaning: 1,922 rows × 11 relevant columns)  
- **Key Features:**  
  - `elevation_m`: Segment elevation in meters  
  - `historical_rainfall_intensity_mm_hr`: Rainfall intensity  
  - `soil_group`: Hydrologic soil classification (A–D)  
  - `land_use`, `drainage_density_km_per_km2`, `storm_drain_proximity_m`, `storm_drain_type`  
  - `risk_labels`: Original multi-label flood risk indicators  

- **Target Variable:** `risk_level` (**High, Medium, Low**) derived from risk labels:  
  - High: `low_lying`, `ponding_hotspot`  
  - Medium: `sparse_drainage`, `extreme_rain_history`  
  - Low: none of the above  

---

## Data Cleaning & EDA
- Removed rows with missing critical values (`elevation_m`, `soil_group`)  
- Filtered risk labels to meaningful categories: `low_lying`, `ponding_hotspot`, `sparse_drainage`, `extreme_rain_history`  
- Created **binary flags** for each risk label (`is_low_lying`, `is_ponding_hotspot`, etc.)  
- Explored patterns via visualizations:  
  - Scatter plot of **Elevation vs Historical Rainfall**  
  - Bar chart of **risk label frequencies**  
  - Stacked bar chart of **risk labels by soil type**  

---

## Methodology
1. **Feature Selection:** Environmental (elevation, rainfall, soil), urban (land use, drainage density, storm drains)  
2. **Target Creation:** Assign `risk_level` based on binary risk flags  
3. **Exploratory Analysis:** Identify patterns between risk labels and features  
4. **Model Training:** Build classification models to predict high, medium, low flood risk  

---

## Visualizations
- **Elevation vs Rainfall:** Identify potential flood-prone low-lying areas  
- **Risk Label Frequency:** Understand the prevalence of each flood risk type  
- **Soil Type vs Risk Labels:** Examine which soil types correlate with higher flood risks  

---

## Outcome
- Provides a predictive framework for **urban flood risk**  
- Highlights **key environmental and infrastructure factors** contributing to risk  
- Supports **data-driven urban planning** and **resource allocation**

