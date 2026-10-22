# The Adult Dental Atlas: Epidemiological Trajectories of Lifetime Tooth Retention

**A Clinical & Epidemiological Study on Permanent Dentition Preservation across U.S. Demographics**  
*Lead Data Architect & Epidemiological Visualizer: Rama Wijaya*  
*Dataset: U.S. Centers for Disease Control and Prevention (CDC) — National Health and Nutrition Examination Survey (NHANES) 2009–2014*  
*Sample Size: 24,625 clinical respondents | 788,000 tooth crown assessments | 1,430,000 periodontal probing sites*

---

## Executive Overview

Healthy natural dentition is essential for masticatory function, nutritional absorption, and systemic well-being. Adult humans possess 28 functional permanent teeth (excluding third molars). While tooth loss is historically dismissed as an inevitable consequence of aging, empirical epidemiological microdata reveals a starkly different reality: **tooth loss is primarily driven by cumulative periodontal disease, access to routine preventive hygiene, and socioeconomic capital.**

This project presents a publication-grade, long-form vertical scrollytelling visual analytics architecture built in **Tableau Desktop (`.twbx`)** and complemented by an **interactive web companion**.

---

## Key Clinical Findings

1. **The Age-40 Divergence:**  
   Natural tooth retention remains relatively uniform through age 39 (median 28 teeth). Beginning in the fifth decade (ages 40–59), the interquartile range widens precipitously. By age 80+, the national median drops to 7 retained teeth, yet the upper quartile preserves 20+ functional natural teeth.
2. **Preventive Prophylaxis vs. Emergency Care:**  
   Cohorts scheduling annual routine cleanings preserve on average 4.8 more natural teeth by age 70 compared to those who only visit the dentist during acute symptoms or pain.
3. **The Oral Health Wealth Gap:**  
   Household income and educational attainment are powerful longitudinal determinants of tooth retention. Over 74% of high-income households visit dentists proactively for routine prophylaxis, whereas lower-income cohorts predominantly present for emergency extraction due to cost and insurance barriers.

---

## Technical Architecture & Tableau Implementation

* **Dual-Axis Anatomical Arch:** Dual-axis polygon projection mapping normalized $(X, Y)$ coordinates for all 32 permanent teeth with central real-time age parameter filtering.
* **Horizontal Small Multiples Strip:** Single-worksheet horizontal projection mapping decade cohorts ($10\text{s}$ through $80\text{s}$) with median retained teeth displayed inside each dental arch.
* **Organic Jitter Dispersion:** Respondent-level microdata points ($n=24,625$) with subtle sizing (`0.25`) and high transparency (`14%`) layered behind median reference bands.
* **Triple-Axis Multi-Panel Trajectories:** Unified multi-panel continuous regression curves comparing flossing frequency, visit recency, and visit rationale side-by-side.
* **100% Horizontal Stacked Bar:** Stratified breakdown of visit purpose across 6 income tiers with in-bar percentage labels.

---

## Production Files

* `NHANES_Dental_Longevity_Atlas_Production.twbx`: Production Tableau workbook with embedded `.hyper` extract, 1200×4700 px scrollytelling canvas, and zero external dependencies.
* `index.html`: Standalone interactive web companion rendering the full analytical flow.

---

*Data Source: U.S. Centers for Disease Control and Prevention (CDC) National Center for Health Statistics (NCHS).*
