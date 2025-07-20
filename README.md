# Greater Sydney Resource Allocation Analysis

This project investigates the spatial distribution of resources across Statistical Area Level 2 (SA2) regions in Greater Sydney, using a custom scoring system built on standardized z-scores across multiple categories. The analysis aims to uncover disparities in resource allocation and explore how these relate to socioeconomic indicators like median income.

## 📊 Overview

We created a composite score for each SA2 region based on 8 categories:

- Retail business density
- Health service availability
- Public transport access
- Polling station coverage
- Educational catchment areas
- Emergency services presence
- Per capita government expenditure
- Homelessness rate (inverted as a penalty)

Each metric was standardized using z-scores and then aggregated and scaled using a sigmoid function to produce a final score per region. These scores reflect how “well-resourced” a region is relative to others.

## 🔍 Key Findings

- Strong spatial inequalities exist across Greater Sydney in terms of resource distribution.
- A **positive correlation** was observed between the resource score and **median income**, supporting the scoring method as a valid proxy for regional well-being.
- High-scoring areas tend to be inner-city regions with dense infrastructure, while some rural regions show inflated scores due to low population.
- The inclusion of homelessness and expenditure data offers insight into both current and future resource conditions.

## 🗺️ Visualizations

- 📌 **[Interactive Map](https://lewischao.com/greater-sydney-analysis/#result-map):** Explore the well-resourced score across SA2 regions.
- 🧮 **[Notebook.ipynb](https://github.com/lewiseng/greater-sydney-analysis/blob/main/Notebook.ipynb):** Full code, analysis, and plots.

## 🧰 Technologies Used

- **Python:** Data analysis and scoring logic (Pandas, GeoPandas, Shapely, Matplotlib)
- **SQL + PostGIS:** Geospatial joins and indexing
- **HTML/CSS + MathJax:** For report formatting and math rendering
- **GitHub Pages / Netlify:** For interactive map and report hosting

## 🧾 Data Sources

- Australian Bureau of Statistics (ABS)
- NSW Department of Education
- Transport NSW Open Data
- AURIN Data Catalogue
- NSW Spatial Data Portal
- NSW Government Open Data

## 👥 Authors

- Lewis Chao  
- Jake Laherty  
- Gabriel Timothy

## 📂 Project Structure
greater-sydney-analysis/
├── Notebook.ipynb # Main analysis and scoring notebook
├── index.html # Final report (for GitHub Pages)
├── /data/ # Cleaned and raw datasets
├── README.md # You're here
