# AI-Based Groundwater Potential Mapping – El Kebab

This project applies machine learning techniques and geospatial analysis to assess groundwater potential in **El Kebab**, using a combination of global and local datasets. It is a continuation of the earlier AI Water Management Project, with a more comprehensive inclusion of raster layers and an improved hybrid workflow involving Google Earth Engine and QGIS.

---

## 📍 Study Area
- **Location**: El Kebab, Morocco
- **Projection**: UTM Zone 30N (EPSG:32630)
- **Purpose**: Generate a data-driven map of groundwater potential zones

---

## 🧠 Objectives
- Collect, process, and analyze relevant environmental and climatic factors influencing groundwater occurrence
- Train a machine learning model (Random Forest) to predict groundwater potential
- Produce maps and metrics to guide sustainable water resource planning in El Kebab

---

## 🛠️ Tools & Technologies
- **QGIS** (terrain analysis, hydrological modeling, styling)
- **Google Earth Engine (GEE)** (climate and vegetation raster extraction)
- **R** (data processing, machine learning modeling)

---

## 🗂️ Folder Structure
```
AI_Water_El_Kebab/
├── data/
│   ├── gee_exports/         # Output from GEE (NDVI, LST, etc.)
│   ├── qgis_outputs/        # Hydrological and terrain layers
│   ├── soil_and_veg/        # SoilGrids and vegetation
│   └── shapefiles/          # Boundaries and vector data
├── scripts/                 # R and GEE code
├── outputs/                 # Final maps and figures
├── docs/                    # Report and documentation
└── README.md
```

---

## 🔄 Workflow Overview

### Phase 0 – Project Setup
- Define tools, goals, and structure

### Phase 1 – Study Area Definition
- Obtain and reproject El Kebab boundary

### Phase 2A – GEE Preprocessing
- Extract:
  - MODIS NDVI
  - MODIS LST
  - CHIRPS Precipitation
  - MODIS ET
  - Land Cover (ESA/WorldCover)
- Export GeoTIFFs clipped to El Kebab

### Phase 2B – QGIS Preprocessing
- DEM-based terrain analysis:
  - Slope, Aspect, Curvature
  - Flow Accumulation & Drainage Network
- Reprojection and clipping of soil and vegetation layers

### Phase 3 – Raster to Point Conversion
- Convert all rasters to points
- Join into a single dataset for modeling

### Phase 4 – Machine Learning
- Build a Random Forest model in R
- Predict groundwater potential map

### Phase 5 – Evaluation
- Accuracy metrics (e.g., RMSE, AUC)
- Spatial validation if possible

### Phase 6 – Documentation
- README and final report

---

## ⚠️ Data Limitation
- **Piezometric data** (groundwater depth) might not be available.
  - Alternatives include: spring/well points, expert zones, unsupervised clustering, or index-based methods.

---

## 📊 Final Output
- Raster map of groundwater potential
- CSV with feature values and predictions
- Accuracy and feature importance metrics
- PDF report

---

## 👤 Author
**Naim Ayoub**  
Hydraulic Technician & Environmental Engineering Student  
Morocco

---

## 📅 Project Timeline
- **Start Date**: June 2025
- **Estimated Completion**: Flexible (all phases will be completed thoroughly without deadline constraints)

---

## 📬 Contact
For questions or collaboration, please contact: ayoubnaim833@gmail.com
