# Premier League Analytics Dashboard

A comprehensive Power BI solution that transforms 12,000+ Premier League matches across 25 seasons into interactive, broadcast-quality dashboards. This repository includes the full ETL pipeline (SSIS), star schema data model, DAX measures, and the Power BI report.

---

## 🔍 Overview

This project delivers end-to-end business intelligence for Premier League data, including:

- Automated ETL with SQL Server Integration Services (SSIS)
- Star schema data model (FactMatchResults + DimTeam, DimSeason, DimReferee)
- Interactive Power BI dashboards covering:
  - League-wide overview
  - Season-level trends
  - Referee behavior
  - Team performance comparisons
  - Club-specific deep dives (e.g., Arsenal 2024–25)

---

## ✨ Key Features

- **Automated ETL Pipeline**  
  Extract raw match CSVs, transform into cleaned tables, load into CSVs .

- **Star Schema Data Model**  
  Central fact table (`FactMatchResults`) with conformed dimension tables (`DimTeam`, `DimSeason`, `DimReferee`, `DimDate`, `DimTime`).

- **Power BI Dashboards**  
  Sleek, consistent theme (burgundy headers, cream cards, navy text) with:
  - KPI cards for goals, cards, wins/losses
  - Time series, bar, donut, and line charts
  - Dynamic slicers and navigation buttons

- **Advanced DAX Measures**  
  Metrics for goals per match, card rates, win ratios, and more.

- **Bilingual Ready**  
  Dashboard captions and tooltips easily translated for English and Arabic audiences.

---

## 🏗 Architecture

```plaintext
[ Raw CSV Files ]
        ↓ SSIS Extract
[ Staging Tables ]
        ↓ SSIS Transform
[ DimTeam, DimSeason, DimReferee, FactMatchResults ]
        ↓ Power BI Import
[ .pbix Report with DAX Measures & Visuals ]
