# FMCG-RADAR
### Retail Market Intelligence & Territory Expansion System — Gujarat, India

FMCG-RADAR is an end-to-end data intelligence system that helps FMCG brands identify where to expand next. It scores all **33 districts of Gujarat** on market opportunity, demand forecast, expansion risk, and untapped "white space" — then generates a professional, decision-ready PDF report.

📄 **[View Sample Report — Gujarat 2025 (PDF)](reports/FMCG_RADAR_Gujarat_2025.pdf)**

---

## The Problem

When an FMCG brand plans territory expansion, the question is rarely *"where do we have the most customers?"* — it's *"where do we have the most customers we haven't already lost to competitors?"*

Most analyses stop at population and urbanization. FMCG-RADAR goes further — combining market opportunity, demand forecasting, entry risk, and **white space detection** to separate genuinely promising markets from already-saturated ones.

---

## What It Does

**1. Market Opportunity Scoring**
Every district is scored 0–100 using a weighted composite of population density, urbanization rate, literacy rate, market maturity (non-agricultural income share), and population size.

**2. Demand Forecasting (2025 Q1–Q4)**
District-level FMCG demand is projected forward using Gujarat's historical FMCG sector growth rates, adjusted by district-specific urbanization momentum and population growth differentials.

**3. Expansion Risk Scoring**
Each district is scored on market saturation risk, infrastructure/distribution risk, and market accessibility risk — quantifying how *difficult* it is to enter, not just how attractive it looks.

**4. White Space Detection**
The key differentiator: identifies districts with large addressable populations but **low existing competition** — markets that look unattractive by raw opportunity score but are genuine first-mover goldmines.

**5. Priority Matrix & Strategic Recommendations**
Combines all four pillars into a final classification — **Priority Expand, Strategic Entry, Monitor, Avoid** — with a complete ranked table across all 33 districts.

**6. Automated PDF Report**
A 7-page intelligence report generated entirely in Python — methodology, maps, rankings, and strategic recommendations, ready to share with stakeholders.

---

## Sample Output

| Opportunity Map | Expansion Priority Matrix |
|---|---|
| ![Opportunity](outputs/fmcg_opportunity_map.png) | ![Matrix](outputs/fmcg_expansion_matrix.png) |

| Demand Forecast | White Space Detection |
|---|---|
| ![Demand](outputs/fmcg_demand_forecast.png) | ![White Space](outputs/fmcg_whitespace_map.png) |

---

## Methodology & Data Sources

| Component | Source |
|---|---|
| District boundaries | OpenStreetMap (OSM), fetched live via OSMnx |
| Population base | Census of India 2011 |
| Population projection | CAGR methodology, Census 2001–2011 growth rates, projected to 2024 |
| FMCG sector growth | IBEF Gujarat Sector Reports, RBI State Finance Data |
| Urbanization & literacy | Census of India 2011 |

**A note on data honesty:** Population figures are projected from Census 2011 using compound growth rates — the same methodology used by government planning departments between census cycles. This is documented transparently in the report itself. For production deployment, this model would incorporate Census 2021 district data (pending public release), PLFS annual surveys, and satellite nightlight intensity as a real-time consumption proxy.

---

## Tech Stack

`Python` · `GeoPandas` · `OSMnx` · `Pandas` · `NumPy` · `Scikit-learn` · `Matplotlib` · `ReportLab`

---

## Project Structure

```
FMCG_RADAR/
├── notebooks/
│   ├── 01_data_collection.ipynb     # District data, scoring, forecasting
│   └── 02_report_generator.ipynb    # PDF report generation
├── data/
│   └── gujarat_districts_final.geojson
├── outputs/
│   ├── fmcg_opportunity_map.png
│   ├── fmcg_demand_forecast.png
│   ├── fmcg_expansion_matrix.png
│   └── fmcg_whitespace_map.png
├── reports/
│   └── FMCG_RADAR_Gujarat_2025.pdf
└── README.md
```

---

## Key Insight

The Opportunity Score alone would point every brand toward Ahmedabad, Surat, and Gandhinagar — Gujarat's largest, most urbanized districts. But these markets are also the most **saturated**. White Space Detection reveals districts like **Banaskantha** and **Dahod** — large populations, low urbanization, minimal existing FMCG penetration — as genuine first-mover opportunities that a pure opportunity-ranking model would overlook entirely.

---

## Author

**Yashkumar Joshi**
M.Sc. Applied Mathematics, Gujarat University
[LinkedIn](https://www.linkedin.com/in/yash-joshi-689a962b7/) · [GitHub](https://github.com/Yash1910-03)
