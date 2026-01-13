# SAARTHI  
### System for Aadhaar Analytics, Risk & Trend Highlighting

SAARTHI is a data-driven analytical framework developed as part of the **UIDAI Data Hackathon**, aimed at uncovering meaningful societal and administrative insights from anonymised Aadhaar enrolment and update datasets.  
The project introduces a novel metric — the **Update Dependency Index (UDI)** — and applies statistical anomaly detection to identify regions exhibiting abnormal update behaviour.

---

## 🎯 Problem Statement

Aadhaar enrolment and update activities reflect large-scale demographic, societal, and operational dynamics across India.  
While high-level statistics are available, there is limited analytical visibility into **post-enrolment update dependency**, **regional instability**, and **anomalous update patterns**.

SAARTHI addresses this gap by:
- Quantifying update dependency using a unified index
- Detecting statistically abnormal regions
- Translating analytics into actionable insights for governance and system improvement

---

## 🧠 Key Concepts

### Update Dependency Index (UDI)

UDI measures how dependent Aadhaar records are on post-enrolment updates.

UDI = (Total Demographic Updates + Total Biometric Updates) / Total Enrolments

- **Low UDI** → Stable Aadhaar lifecycle  
- **High UDI** → Frequent corrections or lifecycle-driven updates  

---

### Anomaly Detection

Statistical Z-score–based anomaly detection is applied to UDI values to flag regions with unusually high update dependency, representing potential risk signals or areas requiring administrative attention.

---

## 📊 Datasets Used

The analysis uses anonymised, aggregated datasets provided by UIDAI:

1. **Aadhaar Enrolment Dataset**
   - Age-wise enrolment counts (0–5, 5–17, 18+)
   - Spatial attributes: State, District, Pincode
   - Temporal attribute: Date

2. **Aadhaar Demographic Update Dataset**
   - Aggregated demographic update activity across age groups and regions

3. **Aadhaar Biometric Update Dataset**
   - Aggregated biometric update information reflecting revalidation and lifecycle changes

> Due to large data volume, datasets are provided as multiple state-wise CSV files and consolidated programmatically.

---

## 🛠 Methodology Overview

1. Consolidation of state-wise CSV datasets  
2. Robust parsing of mixed-format date fields  
3. Aggregation of age-wise enrolments and updates  
4. Dataset integration using spatial and temporal keys  
5. Computation of Update Dependency Index (UDI)  
6. Statistical anomaly detection using Z-score analysis  
7. Visualisation and interpretation of findings  

---

## 📈 Key Insights

- Most regions exhibit low update dependency, indicating stable Aadhaar lifecycles  
- A limited subset of districts and pincodes shows disproportionately high UDI values  
- Demographic and biometric updates jointly contribute to observed instability  
- Anomalous regions are structurally distinct from normal regions  

---

## 🧪 Technology Stack

- **Language:** Python  
- **Libraries:**  
  - Pandas  
  - NumPy  
  - SciPy  
  - Matplotlib  
- **Environment:** Jupyter Notebook

---

## 📁 Repository Structure

```
SAARTHI/
│
├── data/
│ ├── enrolment-data/
│ ├── demographic-data/
│ └── biometric-data/
|
├── saarthi.ipynb
├── README.md
└── LICENSE
```

---

## 🚀 How to Run the Analysis

1. Clone the repository:

   ```
   git clone https://github.com/your-username/SAARTHI.git
   cd SAARTHI
   ```

2. Install required dependencies:

   ```
   pip install pandas numpy scipy matplotlib
   ```

3. Launch Jupyter Notebook:

   ```
   jupyter notebook
   ```

4. Open and run:

   ```
   saarthi.ipynb
   ```

Ensure the dataset folders are placed under the `data/` directory as shown above.

---

## 🔒 Data Privacy Notice

This project uses only anonymised and aggregated datasets provided for the UIDAI Data Hackathon.
No personal or sensitive resident-level information is used or inferred.

---

## 👤 Author

Vrajkumar Shah

B.Tech, Computer Science & Engineering

Dharmsinh Desai University, Nadiad

---

## 📜 License

This project is released under the MIT License.
See the LICENSE file for details.

---

## ⭐ Acknowledgements

- Unique Identification Authority of India (UIDAI)
- National Informatics Centre (NIC)
- Ministry of Electronics and Information Technology (MeitY)

for providing the datasets and organising the hackathon.

---
