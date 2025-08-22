# Coffee Quality Analysis — Power BI Project

> **Status:** Production-ready • **Last updated:** 2025-08-22

This repository/documentation explains a Power BI report that analyzes coffee quality using **sensory attributes**, **processing methods**, **origin countries**, and **defect counts** to understand their impact on **Total Cup Points**. It is written to be copy‑paste ready for a `README.md` on GitHub.

---

## 📌 Business Goal

Provide a decision-support dashboard for coffee buyers and Q-graders to:
- Identify the **drivers of Total Cup Points** (aroma, flavor, acidity, body, etc.).
- See how **processing methods** and **country of origin** influence quality.
- Track the **relationship between defects and cup score**.
- Compare **grades** (Basic, Standard, Premium) across all dimensions.

---

## 🧰 Tech Stack & Power BI Features

- **Power BI Desktop** (recent version).
- Data preparation with **Power Query (M)**: data types, trimming/cleaning, null handling.
- **Modeling** with a simple **star schema** (fact table with measures + supporting dimensions).
- **DAX** measures for KPIs and visual aggregations.
- **Visuals**: Card, Matrix, Clustered Bar/Column, Line/Area, Scatter with **Analytics trendline**, **Map (Bing)** / Filled Map, Slicers.
- **Interactions**: cross-filtering, **Sync Slicers** for Grade across pages.
- **Formatting**: custom theme, data labels, titles, tooltips.
- **Performance**: hide unused columns, summarize by measures, avoid row-by-row calculated columns when possible.

> RLS/What‑If parameters/Bookmarks are **not required** for this solution; you can add them later if you need segmented access or scenario planning.

---

## 📊 Report Pages & What They Show

### 0) Overview — *Coffee Quality Analysis*
![Overview](‘https://image2url.com/images/1755840822354-63c4849b-e3a5-4ba7-b9b0-ffa2d8899950.png’)
Imgsrc:-
 ‘https://image2url.com/images/1755840822354-63c4849b-e3a5-4ba7-b9b0-ffa2d8899950.png’

- KPI Cards: **Avg Total Cups ~83.69**, **Avg Aroma ~7.72**, **Avg Acidity ~7.64**, **Avg Flavor ~7.74** (driven by DAX).
- **Slicers**: Grade, Processing Method, Country of Origin.
- **Clustered Column**: Sensory Attributes (Aroma, Flavor, Acidity) by **Grade**.
- **Map (Bing)**: geographic distribution by **Grade**.
- **Scatter**: **Defects vs Total Cup Points** with **trendline** (negative correlation).
- **Bar chart**: *Interaction of Variables on Total Cup Points* — attribute contribution view.

### 1) Interaction of Variables Influencing Total Cup Points
![Interaction Variables](/coffee_quality_assets/01_interaction_variables.png)
https://image2url.com/images/1755841434064-fb3d9021-0a05-4a7d-b4c1-82800f8e931a.png
- **Matrix**: Grade × Processing Method with **Sum of Total Cup Points** and **Sum of Total Defects**.
- **Map**: Sum of Cup Points & Defects by **Country** and **Grade**.
- **Scatter**: Cup Points vs Defects with an **Analytics** dotted reference line.

### 2) Sensory Attribute vs Grade (with Geography)
![Sensory vs Grade Map](/coffee_quality_assets/02_sensory_vs_grade_map.png)
‘https://image2url.com/images/1755841141725-352b89cc-6285-4791-b16f-f6fb706cd4c0.png’
- **Filled Map**: Country shading segmented by **Grade**.
- **Clustered Bar & Column**: Comparative averages for **Acidity, Aftertaste, Aroma, Balance** by **Grade**.

### 3) Trends in Defect Occurrences and Their Effect on Coffee
![Defects Trends](/coffee_quality_assets/03_defects_trends.png)
https://image2url.com/images/1755841221230-0b26b53d-25aa-4189-bbac-d8f9f7ea9bc7.png
- **Bar**: *Total Defects by Average Cup Points* (reverse insight).
- **Area/Line**: *Defect by Grade & Total Cups* (distribution shape).
- **Column**: **Average of Total Defects by Grade** → **Basic ≈ 6.5**, **Standard ≈ 2.3**, **Premium ≈ 1.1**.
- **Column**: *Defect by Grade & Total Cups* (count distribution).

### 4) Impact of Processing Methods & Origin Regions on Coffee
![Processing & Region](/coffee_quality_assets/04_processing_methods_region.png)
https://image2url.com/images/1755841272243-aecea291-006a-4418-b062-f9ccfaf1b6f3.png
- **Table**: **Premium counts by Country** (e.g., Taiwan leads in sample counts).
- **Map**: Premium distribution by country.
- **Column**: **Average Total Cup Points by Processing Method** — *Double Anaerobic Washed* leads (~89), others ≈ 86–87.

### 5) Key Determinants of Coffee Quality — Sensory Attribute Analysis (Bar)
![Key Determinants Bar](/coffee_quality_assets/05_key_determinants_bar.png)
https://image2url.com/images/1755841310650-bc27881e-80d4-4c8c-b4d0-d2bf26c00cae.png
- **Multi-category Column** showing averaged sensory attributes: CleanCup, Sweetness, Uniformity often at **10.0**, others around **7.6–7.7**.

### 6) Key Determinants — Aroma vs Flavor by Country + Grade Lines
![Key Determinants Scatter/Line](/coffee_quality_assets/06_key_determinants_scatter_line.png)
https://image2url.com/images/1755841351161-77ca43d8-d02c-41ec-a1e6-89c2eabae2e5.png
- **Scatter**: *Avg_Aroma vs Avg_Flavor* by **Country** — positive correlation.
- **Line Chart**: *Cup Quality vs Key Determinants* by **Grade** (Premium → Standard → Basic downward trend).

> All visuals are **interactive**: click a bar/point to filter other visuals on the page. Use the **Grade slicer** to contrast segments.  

---



