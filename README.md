# Capital Infrastructure Performance Dashboard (EVM)

## 📌 Project Overview
This repository contains an enterprise-level **Earned Value Management (EVM)** Project Controls Dashboard built in Power BI. The project simulates a **£12M UK infrastructure development** (*Manchester Road & Utilities Realignment - Phase 1*) to track real-time budgetary health, construction progress, and schedule delivery risks.

By combining an engineering project management framework with data analytics, this dashboard bridges the gap between raw construction site data and executive decision-making.

---

## 📊 Live Dashboard Preview
![Project Controls Dashboard Dashboard]((https://github.com/stephenjacobhussaini-sudo/Manchester-Road-Realignment-Project-Controls-/blob/main/Images/dashboard%20screenshot.JPG))

---

## 🛠️ Key Technical Features & DAX Measures
Rather than relying on default summaries, I built out the entire EVM engine using custom **Data Analysis Expressions (DAX)** to isolate performance constraints:

*   **Total Planned Value (PV):** `Total_PV = SUM('Sheet1'[Planned Value (PV)])` — *The baseline budget configuration.*
*   **Total Earned Value (EV):** `Total_EV = SUM('Sheet1'[Earned Value (EV)])` — *The budgeted cost of work actually performed.*
*   **Total Actual Cost (AC):** `Total_AC = SUM('Sheet1'[Actual Cost (AC)])` — *The actual expenditures incurred.*
*   **Cost Performance Index (CPI):** `CPI = DIVIDE([Total_EV], [Total_AC], 0)` — *Financial efficiency metric (Target >= 1.0).*
*   **Schedule Performance Index (SPI):** `SPI = DIVIDE([Total_EV], [Total_PV], 0)` — *Time efficiency metric (Target >= 1.0).*
*   **Estimate At Completion (EAC):** `EAC = DIVIDE([Total_PV], [CPI], 0)` — *Data-driven final cost forecasting based on current performance trend factors.*

---

## 🔍 Data Insights & Executive Recommendations
A summary of the project health derived from the data model:

1.  **The Core Bottleneck:** While the overall project budget is relatively stable with an acceptable **CPI of 0.94**, the schedule is in a critical condition, operating at an **SPI of 0.69** (running at only 69% time efficiency).
2.  **Root-Cause Isolation:** Using conditional formatting matrices, the delay was isolated directly to **WBS 3.20 (Structural Steel Framing)** within the Structural phase. It exhibits a massive schedule variance of **-£1.05M** and a critical SPI of **0.30**.
3.  **Strategic Deployment:** Because **Bulk Earthworks (WBS 2.10)** is currently performing ahead of schedule and under budget (CPI 1.05), project leadership should immediately reallocate site machinery and supervisory personnel to the structural steel package to mitigate downstream handover delays.

---

## 📂 Repository Structure
*   `data/`: Contains the baseline Excel master dataset.
*   `reports/`: Contains the compiled `.pbix` Power BI project file.
*   `images/`: Contains the visual documentation and screenshots used for this markdown file.

## 🚀 How to Review This Project
1. Download the `.pbix` file from the `reports/` folder.
2. Open it using **Power BI Desktop**.
3. Use the **Phase Dropdown Slicer** at the top right to filter between Structural, Groundworks, Civil Works, Preparation, and Handover phases to see full cross-filtering dynamics.

---
**Contact & Collaborations**  
I am a UK Master’s graduate in Engineering Project Management specializing in Digital Project Controls and Construction Data Analytics. If you're looking to scale data-driven insights in infrastructure development, let's connect on [LinkedIn][([YOUR_LINKEDIN_URL_HERE](https://www.linkedin.com/in/stephen-hussaini-248746371/))]
