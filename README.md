# GA4 User Intent Prediction System

## Overview
End-to-end analytics and machine learning project using GA4 data exported to BigQuery to identify high-intent user behaviour and predict conversion likelihood.

This project moves beyond traditional reporting by turning behavioural data into actionable signals that can drive real-time product and marketing decisions.

* Note: This project is based on anonymised / simulated GA4 data for demonstration purposes.*

---

## Problem
In B2B environments, users rarely convert immediately. The challenge is identifying high-intent sessions early, before users reach the contact stage.

---

## Approach

### Data & Processing
- Cleaned and validated GA4 event data in BigQuery
- Resolved schema inconsistencies and null handling
- Structured session-level features for analysis and modelling

### Analysis (SQL)
- Session behaviour and engagement baseline
- Scroll depth as a proxy for intent
- Traffic source segmentation (Direct vs Organic)
- Device behaviour analysis
- User journey mapping

### Key Behavioural Signals
- High scroll depth (>80%)
- Longer engagement time
- Multi-page journeys (especially demo interactions)
- Direct traffic patterns

---

## Key Insights

- Direct traffic converts ~3x higher than organic
- High scroll depth strongly correlates with intent
- Conversion journeys are multi-step, not immediate
- Desktop users show deeper engagement in B2B contexts

---

## Visual Insights

### Engagement by Traffic Source
![Traffic](visuals/avg_engagement_by_source.png)

### Scroll Depth by Page
![Scroll](visuals/avg_scroll_by_page.png)

### Device Engagement
![Device](visuals/device_engagement.png)

### User Segmentation
![Segmentation](visuals/engagement_segmentation.png)

---

## Machine Learning Use Case

### Objective
Predict high-intent sessions before conversion.

### Model
- Logistic Regression (prototype)
- Features:
  - Engagement time
  - Scroll depth
  - Event count
  - Traffic source
  - Device type

### Outcome
- Identified engagement time as strongest predictor
- Demonstrated feasibility of real-time intent scoring

---

## Business Impact

- Enables real-time identification of high-intent users
- Supports personalised CTAs and on-site experiences
- Improves lead scoring and marketing efficiency
- Shifts analytics from reporting → prediction → action

---

## Tech Stack

- Python
- BigQuery SQL
- GA4
- Scikit-learn
- Jupyter Notebook

---

## Project Structure

- `/data` → cleaned dataset
- `/queries` → BigQuery SQL
- `/models` → ML prototype
- `/visuals` → charts
- `main.ipynb` → analysis
- `report.pdf` → full write-up

---

## Next Steps

- Real-time scoring pipeline (streaming / API)
- Advanced models (XGBoost / classification ensembles)
- Integration with marketing automation tools

---

## Summary

This project demonstrates how behavioural data can be transformed into predictive systems that drive real-world decisions.

It reflects a shift from analysing what happened → predicting what will happen → acting on it.
