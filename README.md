# E-Commerce Product Funnel Analysis
### Python | Power BI | Zerve | Kaggle

---

## 📌 Project Summary

Analyzed 42 million behavioral events from a real-world e-commerce platform to identify where and why customers drop off throughout the purchase journey. Built an end-to-end data pipeline from raw data cleaning to interactive dashboard and business recommendations.

---

## 🎯 Problem Statement

E-commerce businesses lose a significant portion of potential revenue when users abandon their journey before completing a purchase. This project answers:
- Where exactly in the funnel are users dropping off?
- Which product categories convert best and worst?
- When during the day and week do users convert most?
- What should the business do about it?

---

## 📦 Dataset

| Detail | Info |
|---|---|
| Source | REES46 E-Commerce Dataset (Kaggle) |
| Size | 42 million rows |
| Period | October 2019 |
| Key Variables | event_type, user_id, user_session, category_code, price, event_time |

**Dataset link:** https://www.kaggle.com/datasets/mkechinov/ecommerce-behavior-data-from-multi-category-store

---

## ⚙️ Workflow

1. **Data Loading** — Chunked reading from zip file for memory efficiency
2. **Data Cleaning** — Removed nulls, duplicates, invalid prices, parsed timestamps
3. **Funnel Construction** — Unique user counts at view → cart → purchase stages
4. **Segmentation** — Conversion rates by product category, hour of day, day of week
5. **Cohort Analysis** — Single-session vs multi-session user comparison
6. **Visualization** — Matplotlib charts + Power BI interactive dashboard
7. **Export** — Aggregated CSVs for Power BI import

---

## 📊 Dashboard Preview
<img width="713" height="395" alt="image" src="https://github.com/user-attachments/assets/a23a52e4-0c47-48d2-8434-84db9614840f" />


---

## 🔍 Key Findings

| Metric | Value |
|---|---|
| View → Cart Conversion | ~2.27% |
| Cart → Purchase Conversion | ~37.46% |
| Overall Conversion Rate | ~0.85% |
| Biggest Drop-off | View → Cart stage |
| Best Converting Day | Sunday |
| Peak Purchase Hours | 7AM – 10AM UTC |

---

## 💡 Business Recommendations

**1. Reduce Cart Abandonment**
The cart → purchase drop-off is the highest-impact opportunity. Automated email sequences at 1h, 24h, and 72h post-cart with a time-limited discount can recover 5–15% of abandoned carts.

**2. Target Peak Conversion Windows**
Concentrate paid ad spend during identified peak conversion hours. Scale back overnight when conversion rates are lowest.

**3. Prioritize High-Converting Categories**
Electronics and computers show strong conversion. Increase inventory depth and homepage placement for top-performing categories while auditing UX friction in low-converting ones.

**4. Retarget Single-Session Users**
Single-session users convert at a far lower rate than returning users. Personalized retargeting campaigns on social platforms for users who viewed but didn't return represent significant untapped revenue.

---

## 🛠️ Tools Used

| Tool | Purpose |
|---|---|
| Python 3 | Data cleaning, analysis, visualization |
| Pandas | Data manipulation and aggregation |
| Matplotlib | Chart generation |
| Power BI | Interactive dashboard |
| Zerve | Cloud-based notebook execution |
| Kaggle | Dataset source |

---

## 📁 Repository Structure

```
ecommerce-funnel-analysis/
│
├── ecommerce_product_funnel.py   ← Main Python analysis script
├── powerbi_funnel.csv            ← Funnel stage data for Power BI
├── powerbi_category_funnel.csv   ← Category conversion data
├── powerbi_dow.csv               ← Day of week conversion data
├── powerbi_hourly.csv            ← Hourly conversion data
├── dashboard.png                 ← Power BI dashboard screenshot
└── README.md                     ← This file
```

---

## 🚀 How to Run

1. Download `2019-Oct.csv` from the Kaggle link above
2. Place it in the same folder as the script
3. Install dependencies:
```bash
pip install pandas numpy matplotlib
```
4. Run the script:
```bash
python ecommerce_product_funnel.py
```
5. Import the generated `powerbi_*.csv` files into Power BI Desktop

---

*Project completed as part of a Data Analyst application — June 2025*
