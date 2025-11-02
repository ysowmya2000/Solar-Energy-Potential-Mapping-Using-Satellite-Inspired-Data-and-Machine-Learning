# Solar-Energy-Potential-Mapping-Using-Satellite-Inspired-Data-and-Machine-Learning

## Overview
This project analyzes solar energy potential for **Austin, Texas** using **satellite-inspired environmental data** and **machine learning**.  
It demonstrates how data science and geospatial analytics can be combined to identify **Low**, **Medium**, and **High** solar potential zones for renewable energy planning.

The project integrates:
- Python data science workflow  
- Geospatial analysis (`geopandas`, `folium`)  
- Unsupervised learning (`K-Means clustering`)  
- Interactive visualization (Folium map)

## Objectives
- Collect and preprocess **solar irradiance** and **cloud cover** data using NASA’s POWER API.  
- Engineer synthetic features for **terrain** and **land use** (Elevation, NDVI, NDBI).  
- Build a **Solar Potential Score** combining environmental and geospatial factors.  
- Apply **machine learning clustering** to classify potential zones.  
- Visualize results on an **interactive map**.

## Project Workflow

### 1️Data Acquisition & Preprocessing
- **Source:** NASA POWER API (for solar irradiance & cloud fraction)  
- **Location:** Austin, Texas  
- **Additional Features:** Synthetic data simulating real satellite metrics (NDVI, NDBI, elevation)

### Feature Engineering
| Feature | Description |
|----------|-------------|
| Solar_Irradiance | Solar radiation (kWh/m²/day) |
| Cloud_Cover | Percent cloud cover |
| Elevation | Synthetic elevation data (m) |
| NDVI | Vegetation index |
| NDBI | Built-up index |
| Solar_Potential_Score | Combined score of irradiance, clouds & surface type |

### Machine Learning
- Used **K-Means clustering (k=3)** to categorize potential zones:
  - **Low**
  - **Medium**
  - **High**
- Normalized data using `StandardScaler` for balanced feature impact.

### Visualization
- Created an **interactive Folium map** showing solar potential zones.  
- Each point includes pop-ups with irradiance, NDVI, NDBI, and elevation details.
- Saved output map as: austin_solar_potential_map.html
