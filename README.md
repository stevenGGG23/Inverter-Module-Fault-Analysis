# Inverter-Module-Fault-Analysis

This project is designed to automate the monitoring and classification of inverter module health across multiple utility-scale solar sites. It integrates directly with Seeq, a time-series analytics platform, to extract real-time data and analyze signal behavior from each inverter module on every site listed.

- The system detects and categorizes performance issues such as:

- Communication Outages – when the inverter is no longer transmitting data

- Data Freezes – when the data values remain constant due to signal failure

- Offline States – when inverters stop producing power during valid sunlight conditions

- Active Faults – when the inverter itself reports a fault via internal fault codes

- Once the analysis is complete, the following happens:

Two CSV Excel files are automatically generated:

- A detailed breakdown of inverter module statuses across all sites

- A summarized report that flags fault periods and site-level metrics

Automation with API Scheduling:

   - A scheduled Python API runs this analysis every Monday and Wednesday

   - Upon completion, the program sends the results directly to a designated Outlook email inbox, making reporting hands-free and immediate
---

## 📌 Project Purpose

Utility-scale solar sites often have hundreds of inverter modules. Manually reviewing performance and fault signals for each one is time-consuming and error-prone. This notebook streamlines the process by:

- Pulling relevant signal data from Seeq
- Identifying inverter offline/fault states
- Categorizing fault conditions into meaningful states
- Generating site-wide summaries for quick diagnostics

---

## ⚙️ Features

- ✅ Multi-site support (reads from a configuration CSV file)
- ✅ Modular code structure for reuse and debugging
- ✅ Signal filtering for inverter Active Power, Fault Code, and Comms Status
- ✅ Fault state classification using Seeq formulas
- ✅ Summary report generation with key fault metrics

---

## 📂 Files

| File                          | Description                              |
|-------------------------------|------------------------------------------|
| `FINAL_Inv_Module_Analysis.ipynb` | Main Jupyter notebook for analysis       |
| `PE(Sheet1).csv`              | Input configuration file for site names  |
| `inverter_fault_analysis_report.csv` | Output summary of inverter states    |
| `README.md`                   | You’re reading it!                       |

---

## 🧪 Output Example
--- 
Starting Multi-Site Inverter Module Fault Analysis...
Date Range: 2025-07-07 to 2025-07-09
Grid Resolution: 5min
Output File: inverter_fault_analysis_report.csv

Total Sites Analyzed: 21
Sites with Faults: 0
Total Fault Periods: 0
---
