# AI-Powered Manufacturing Quality Intelligence

## 🛠️ Project Title
AI-Driven Production Monitoring and Quality Intelligence System for Manufacturing Optimization

## 🎯 Goal
To analyze key manufacturing metrics like defect rate, downtime, and maintenance hours to:
- Predict quality and safety risks.
- Recommend SOP updates or Total Productive Maintenance (TPM) interventions.
- Enable proactive decision-making through data-driven flags.

## 👥 Intended Audience
- Production Managers and Coordinators
- Quality Assurance Specialists
- Operations Analysts
- Manufacturing Engineers
- Business Intelligence Teams

---

## 🚀 Strategy & ML Pipeline

### 1. **Data Simulation**
- Synthetic datasets generated to simulate real production KPIs:  
  - `DefectRate`
  - `SafetyIncidents`
  - `MaintenanceHours`
  - `DowntimePercentage`

### 2. **Feature Engineering**
- Derived flags for:
  - SOP Updates if `DefectRate > 3` or `SafetyIncidents > 1`
  - TPM flag if `MaintenanceHours > 5` or `DowntimePercentage > 2.5`

### 3. **Insight Generation**
- Visual and logical analysis on when operations require procedural changes or preventive maintenance.

---

## 🧪 Sample Code

```python
import pandas as pd
import numpy as np

# Generate synthetic quality-related data
np.random.seed(42)
n = 3240
df = pd.DataFrame({
    'DefectRate': np.random.gamma(2, 1.5, n),
    'SafetyIncidents': np.random.poisson(2, n)
})

# SOP update condition
df['SOP_Update_Required'] = (df['DefectRate'] > 3) | (df['SafetyIncidents'] > 1)

df.head()
```

```python
# Maintenance and downtime data
df2 = pd.DataFrame({
    'MaintenanceHours': np.random.randint(0, 25, n),
    'DowntimePercentage': np.random.uniform(0, 5, n)
})

# TPM flag condition
df2['TPM_Flag'] = (df2['MaintenanceHours'] > 5) | (df2['DowntimePercentage'] > 2.5)

df2.head()
```

---

## 🧠 Challenges Tackled
- Simulated realistic production data where privacy or live telemetry may be restricted.
- Designed logic-based quality flags with potential for expansion into ML classification/regression.
- Established a baseline for integration into factory BI dashboards (e.g., Power BI or Streamlit).

---

## 🔍 Problem Statement
**How can manufacturers proactively identify process improvements and prevent safety/quality failures using real-time production metrics and automated intelligence?**

---

## 📦 Repository Structure (Recommended)

```
├── README.md
├── quality_insight.ipynb
├── data/
│   ├── simulated_production.csv
│   └── simulated_maintenance.csv
├── scripts/
│   └── generate_synthetic_data.py
├── output/
│   └── insight_summary.csv
```

---

## 📈 Output Preview

### Sample SOP Update Conditions

| DefectRate | SafetyIncidents | SOP_Update_Required |
|------------|-----------------|----------------------|
| 3.12       | 0               | ✅                   |
| 0.82       | 7               | ✅                   |
| 0.64       | 8               | ✅                   |

### Sample TPM Flags

| MaintenanceHours | DowntimePercentage | TPM_Flag |
|------------------|--------------------|----------|
| 9                | 0.05               | ✅       |
| 0                | 4.87               | ✅       |
| 2                | 0.50               | ❌       |

---

## 📌 Future Work
- Integrate predictive ML (e.g., XGBoost) to forecast risk levels.
- Create Streamlit dashboard for real-time alerting.
- Expand KPI flags to include energy usage, scrap rate, and operator shift logs.

---

## 📄 License
This project is open-source under the MIT License. Attribution is appreciated.

---

## 📬 Contact
For questions, collaboration, or dashboard deployment:
**Ronald Kalani**  
📧 ronaldkalani@yahoo.ca  
📍 Brampton, ON, Canada  
🔗 [LinkedIn](https://www.linkedin.com/in/ronald-kalani-1a465533/)
