# 🤖 01 - Data Exploration: Manipulator Health Monitoring (EDA)

This notebook marks **Phase 1: Exploratory Data Analysis (EDA)** of the manipulator (robot arm) degradation project.

Our goal is to thoroughly explore the raw data from the UR5 robot arm degradation dataset to understand **trends, missing values, and key correlations** among variables before proceeding with feature engineering and modeling.

---

## 🎯 Objective

Perform an Exploratory Data Analysis (EDA) on the **UR5 robot arm degradation dataset** (source: NIST).

The dataset consists of multiple CSV files containing controller-level sensing data (collected at 125Hz) under various operational conditions:
* **Temperature**
* **Payload**
* **Speed**

---

## 💾 Data Sources and Structure

The data files are organized within the project's `data/` directory.

### Key Data Files

| File Name | Format | Content Description |
| :--- | :--- | :--- |
| `UR5TestResult_header.xlsx` | Excel (`.xlsx`) | **Metadata** and **header information** for the sensor data. |
| `Calculated deviation of actual position to nominal position.xls` | Excel (`.xls`) | **Summary of pose accuracy degradation** (calculated deviation of actual position to nominal position). |
| `~18 CSV files` | CSV (`.csv`) | **Joint-level sensing data** across different test conditions (the primary data for analysis). |

### Dataset Path Structure

The files reside in the `data/raw/` subdirectory:

data/ ├── raw/ │   ├── header/ │   │   └── UR5TestResult_header.xlsx │   ├── summary/ │   │   └── Calculated deviation...xls │   └── sensor_data/ │       └── <all CSV files> └── processed/