# Portfolio Financed Emissions Engine & AASB S2 Climate Risk Framework

## Project Overview

This project provides an end-to-end analytical framework for measuring, managing, and reporting **Scope 3 Category 15 (Financed Emissions)** for a diversified global financial portfolio. Developed to align with the **Macquarie CGM (Commodities and Global Markets)** operational context, the engine automates the ingestion of internal ledger data, integrates live market financial metrics, and applies global carbon accounting standards.

The framework ensures compliance with **AASB S2 (Climate-related Disclosures)** and follows the **PCAF (Partnership for Carbon Accounting Financials)** Global Standard.

## Key Features

* **Hybrid Data Architecture:** Combines Level 1 verified emissions (e.g., BHP 2025 Sustainability Reports) with Level 4/5 sector-specific proxies.
* **Automated Data Pipeline:** Python-based extraction of live Enterprise Value (EVIC) and Revenue via the YFinance API.
* **Regulatory Alignment:** Integrated lookup tables for **NGA Factors 2025** (Australia) and PCAF Building Embodied Emission Intensities.
* **Risk Modeling:** Transition risk assessment through carbon-price stress testing ($100/tCO2e scenario).
* **Audit-Ready Quality Scoring:** Automated assignment of PCAF Data Quality Scores (1-5) to ensure transparency in climate disclosures.

## Tech Stack

* **Data Engineering:** Python (Pandas, NumPy, YFinance API)
* **Analytics:** Excel Power Query (M-Code), Power Pivot (DAX)
* **Frameworks:** PCAF, GHG Protocol, AASB S2
* **Data Sources:** Yahoo Finance, Australian National Greenhouse Accounts (2025), BHP Annual Report 2025

## Repository Structure

```text
├── Data/
│   ├── CGM_Internal_Ledger_Source.csv  # Simulated internal banking ledger
│   ├── Master_Ledger_Data.csv          # Final processed dataset with emissions
│   └── Real_Market_Data.csv            # Live ASX 50 financial extraction
├── Scripts/
│   └── Market_Data_Extractor.py        # Python script for EVIC & Revenue sourcing
├── Documentation/
│   └── BHP_Annual_Report_2025.pdf      # Source for verified emission factors
└── Portfolio_Carbon_Engine.xlsx        # Master Excel Dashboard & Power Query Model

```

## Methodology & Calculations

### 1. Attribution Factor

The portion of the borrower's emissions attributed to the financial institution is calculated using **EVIC** (Enterprise Value Including Cash):


### 2. Financed Emissions

### 3. Data Quality Hierarchy

* **Score 1-2:** Verified reported emissions (e.g., BHP row verified via 2025 Annual Report).
* **Score 4-5:** Estimated emissions using **Carbon Intensity Proxies** () when primary data is unavailable.

## How to Use

1. **Run Python Scripts:** Execute `Market_Data_Extractor.py` to refresh live market valuations for ASX constituents.
2. **Power Query Refresh:** Open `Portfolio_Carbon_Engine.xlsx` and click "Refresh All" to ingest the cleaned CSVs.
3. **Analyze Dashboard:** View the **Sector Concentration Heatmap** and **Data Quality Summary** tabs for portfolio insights.

## Author

Developed as a technical showcase for Climate Risk and ESG Data Analytics roles. This project demonstrates the ability to translate complex regulatory requirements (AASB S2) into scalable, automated financial tools.
