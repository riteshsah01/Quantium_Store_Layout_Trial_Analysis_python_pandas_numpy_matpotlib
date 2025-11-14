# Quantium – Store Layout Trial Analysis

## 📑 Table of Contents
- [Brief Summary](#brief-summary)
- [Overview](#overview)
- [Problem Statement](#problem-statement)
- [Dataset Description](#dataset-description)
- [Tools & Technologies](#tools--technologies)
- [Methodology](#methodology)
- [Key Insights](#key-insights)
- [Model Output](#model-output)
- [How to Run](#how-to-run)
- [Results & Conclusion](#results--conclusion)
- [Author & Contact](#author--contact)

---

## Brief Summary
This project was completed during my internship with **Quantium**, a leading data analytics consultancy.  
The objective was to evaluate the impact of a **new store layout trial** conducted in three stores (77, 86, 88).  
Using transactional and customer behavior data, I performed **customer analytics, control store selection, normalization, and uplift testing** to determine whether the trial stores experienced significant performance improvements.  

The project demonstrates skills in **data wrangling, feature engineering, statistical testing, and business storytelling**, with outputs designed for both technical reproducibility and executive decision-making.

---

## Overview
Quantium’s client, Julia (Category Manager), wanted to understand whether new store layouts improved chip sales and customer engagement.  

The project involved three major components:
1. **Customer Analytics** – analyzing purchasing behavior across customer segments, brands, and pack sizes.  
2. **Experimentation & Uplift Testing** – comparing trial stores against matched control stores to measure impact.  
3. **Presentation** – synthesizing findings into a clear recommendation for rollout decisions.  

This case study highlights how **data-driven experimentation** can guide strategic retail decisions.

---

## Problem Statement
The business problem was twofold:
- **Customer Analytics**: Identify which customer segments, brands, and pack sizes drive chip purchases, and understand purchasing trends.  
- **Experimentation**: Evaluate whether trial stores with new layouts showed significant uplift compared to control stores, and diagnose whether changes were driven by more customers or more transactions per customer.  

The ultimate objective was to provide Julia with a **strategic recommendation** for the upcoming category review.

---

## Dataset Description
Two datasets were provided:
- **QVI Transaction Data**  
  - Transaction-level records: `DATE`, `STORE_NBR`, `LYLTY_CARD_NBR`, `PROD_NAME`, `PROD_QTY`, `TOT_SALES`.  
  - Granularity: one row per purchase.  
  - Includes product details (brand, pack size) and customer IDs.  

- **QVI Purchase Behaviour**  
  - Customer-level demographics: `LYLTY_CARD_NBR`, `LIFESTAGE`, `PREMIUM`.  
  - Provides segmentation attributes for customer profiling.  

**Derived Features**:
- **Brand**: extracted from product name.  
- **Pack Size (grams)**: parsed from product name and bucketed into ranges.  
- **Segment KPIs**: spend, transactions, units, revenue share.  
- **Time Trends**: monthly revenue and customer counts.  

---

## Tools & Technologies
- **Languages**: Python (primary), R (template provided by Quantium).  
- **Libraries**:  
  - Data wrangling: `pandas`, `numpy`  
  - Visualization: `matplotlib`, `seaborn`  
  - Statistical testing: `scipy.stats`  
- **Tools**: Jupyter Notebook for reproducible workflows, GitHub for documentation, Excel for quick validation.  

---

## Methodology
1. **Data Preparation**  
   - Cleaned duplicates, standardized date formats, removed outliers in `TOT_SALES`.  
   - Engineered features: brand extraction, pack size parsing, standardized brand names.  
   - Integrated customer demographics with transaction data.  

2. **Customer Analytics**  
   - Built customer-level metrics (total spend, transaction count, units per transaction).  
   - Built segment-level KPIs (revenue share, penetration, average basket size).  
   - Analyzed product mix (top brands, pack sizes, price-per-gram).  
   - Conducted time-series analysis (monthly revenue trends).  

3. **Experimentation & Uplift Testing**  
   - Aggregated monthly metrics: revenue, customers, transactions per customer.  
   - Selected control stores using Pearson correlation and magnitude distance.  
   - Normalized control store baselines to trial stores.  
   - Created indexed performance metrics (Trial ÷ Normalized Control).  
   - Conducted t-tests to assess statistical significance.  
   - Diagnosed drivers of uplift (customers vs transactions).  

4. **Presentation**  
   - Synthesized findings into a stakeholder-ready slide deck.  
   - Highlighted actionable recommendations for rollout decisions.  

---

## Key Insights
- **Customer Analytics**  
  - Premium segments contributed disproportionately to revenue.  
  - Mid-size pack sizes (200–400g) were most popular across demographics.  
  - Top brands (Smiths, Doritos, Kettle) dominated category share.  
  - Seasonal spikes in chip purchases observed in certain months.  

- **Experimentation**  
  - Store 86 showed statistically significant uplift during trial period.  
  - Stores 77 and 88 did not show consistent or significant uplift.  
  - Uplift in Store 86 was driven by **more purchasing customers**, not increased frequency.  

---

## Model Output
- **Control Store Selection**:  
  - Trial Store 77 → Control Store 233  
  - Trial Store 86 → Control Store 155  
  - Trial Store 88 → Control Store 237  

- **Indexed Performance Metrics**:  
  - Revenue Index, Customer Index, Transactions per Customer Index.  
  - Pre-trial indices ≈ 1 (alignment confirmed).  
  - Trial period indices diverged for Store 86.  

- **Statistical Test Outputs**:  
  - Store 86: p-values < 0.05 for revenue and customers → significant uplift.  
  - Stores 77 & 88: p-values > 0.05 → no significant uplift.  

---

## How to Run
1. Clone this repository.  
2. Navigate to `Task1/` and `Task2/` folders for code and documentation.  
3. Run Jupyter notebooks with Python 3.x and required libraries installed.  
4. Review outputs in notebooks and plots.  
5. Refer to `README.md` and `PPT/` for recruiter-facing summaries and presentation slides.  

---

## Results & Conclusion
- **Store 86**: Significant uplift observed → rollout recommended.  
- **Stores 77 & 88**: No significant uplift → further testing required.  
- **Customer Analytics**: Premium segments and mid-size packs are key drivers of revenue.  
- **Strategic Recommendation**: Roll out new layout selectively, focusing on stores with similar profiles to Store 86, and align promotions with premium segments and seasonal demand.  

---

## Author & Contact
**Author**: Ritesh Gupta  
📞 Phone: 8010211665  
📧 Email: riteshshahofficial1@gmail.com  