# Mini Project #3 — Stablecoin (PYUSD) | KNIME + MongoDB + Dune

## Overview
This project analyzes **PYUSD transaction activity in 2024** by merging quarterly datasets and transforming them in **KNIME** to answer one core question:

> **Which month in 2024 had the most PYUSD transactions?**

## Data Sources
- **Dune Analytics** query results (daily transaction count + total transferred volume)
- Quarterly datasets (Q1–Q4 2024) imported into **MongoDB Atlas**

## Tools Used
- **MongoDB Atlas** (storage)
- **Dune API** (data extraction)
- **Python (pandas, requests, pymongo)** for API → MongoDB loading
- **KNIME Analytics Platform** for merge + transformation + visualization

## Workflow Summary (KNIME)
Steps performed:
1. Read Q1–Q4 datasets from MongoDB
2. **Concatenate** into a single annual dataset
3. Convert date fields (String → Date/Time)
4. Remove duplicates (Duplicate Row Filter)
5. Create month field from date (Date&Time Part Extractor)
6. Aggregate monthly totals (GroupBy)
7. Rank months by transaction count (Sorter + Top K)
8. Visualize results (Line Plot, Pie Chart, Bar Chart)

## Key Visualizations
- **Daily trend over 2024** (Line Plot)
- **Monthly distribution** (Pie Chart)
- **Top 3 months** by transaction count (Bar Chart)

## Outputs
- KNIME workflow: `workflows/Project3_Team8.knwf`
- Slides: `slides/Project3_Stablecoin_Slides.pdf`
- Screenshots of workflow + charts: `screenshots/`

## Dune Query
Add your query link here:
https://dune.com/prattkk/dai-dashboard-story?utm_source=share&utm_medium=copy&utm_campaign=dashboard

## How to Run (Optional)
1. Open KNIME
2. Import workflow: `Project3_Team8.knwf`
3. Configure MongoDB Connector with your Atlas credentials
4. Execute nodes from left → right

## Author
Prateek Verma
