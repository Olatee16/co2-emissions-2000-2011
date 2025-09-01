# 🌍 CO₂ Emissions per Capita (2000–2011): Country Comparison Dashboard

**Objective:** Enable year-by-year comparison of countries' **CO₂ emissions per capita** with context on **population, GDP, and energy use** for policy analysis.

[▶️ View the Interactive Dashboard](https://public.tableau.com/app/profile/oluwatosin.olaniyan/viz/C02Dataset1/Sheet1)  

![Preview of the CO2 per capita map](./assets/preview.file:///C:/Users/HP-PC/Downloads/Sheet%201%20(1).pdf)

---

## Why this matters
Policy makers need to compare **per-capita emissions** across countries and over time. By pairing emissions with **population**, **GDP**, and **energy use**, this dashboard helps reveal whether changes stem from demographics, economic growth, or energy intensity.

---

## Data Sources
- **CO₂ emissions per capita** (1960–2011) – original dataset provided.
- **Population, GDP (current USD), Energy use** – collected from an official government website.
- For this project, the analysis focuses on **2000–2011** to avoid older missing values.

> Note: Source files live in `/data/raw`. Cleaned/merged tables are in `/data/prepared`.

---

## Methodology (condensed)
1. **Scope filter:** Keep years **2000–2011** only.
2. **Keys:** Join/relate on **Country** (prefer ISO3) + **Year**.
3. **Cleaning:** Standardize country names; handle nulls (drop or impute where safe).
4. **Modeling in Tableau:**
   - Relationship across tables by **Country–Year**.
   - **Map view:** Country geometry + Color = *CO₂ per capita*.
   - **Tooltips:** Show *Population*, *GDP*, *Energy use* for the selected Year.
   - **Year control:** Parameter/slider to animate from 2000 → 2011.

---

## Reproducing Locally
1. Clone the repo and open `/tableau/co2_emissions_2000_2011.twbx` in Tableau.
2. Ensure relative paths to `/data/prepared/` are intact (or relink).
3. Interact with the **Year slider** and map to explore countries.

---

## Findings (examples)
- Countries with rapid GDP growth sometimes show **diverging** per-capita emissions depending on **energy intensity** and **fuel mix**.
- Regions with similar GDP per capita can have **different emissions** if **energy use per capita** differs markedly.

---

## Limitations
- Some country-year combinations may be missing in earlier decades; restricting to **2000–2011** minimizes gaps.
- Cross-country comparisons can be sensitive to **definition changes** and **data revisions**.

---

## Files
- `/assets/CO2_per_capita_map.pdf` – static export of the map (Mapbox/OSM basemap; 0–62 mt/person scale in this export).  
- `/tableau/co2_emissions_2000_2011.twbx` – Tableau workbook.  
- `/data/` – raw and prepared tables.  
- `/notebooks/01_prepare_data.ipynb` – optional data cleaning/merge.

---

## License
MIT © Your Name
