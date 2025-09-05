
# COVID-19 Data Analysis Project

## 📌 Objective
This project analyzes the spread and impact of COVID-19 using confirmed and deaths datasets, and correlates the findings with the World Happiness Report.  
The aim is to explore whether country-level happiness indicators relate to COVID-19 outcomes.

---

## 📂 Dataset Files
- **covid19_Confirmed_dataset.csv**  
  - Wide-format cumulative confirmed cases from Johns Hopkins dataset.  
  - Columns: `Province/State`, `Country/Region`, `Lat`, `Long`, followed by daily dates (e.g., `1/22/20`, `1/23/20` ...).

- **covid19_deaths_dataset.csv**  
  - Wide-format cumulative deaths data (same structure as above).  

- **worldwide_happiness_report.csv**  
  - Snapshot from World Happiness Report.  
  - Columns: `Country or region`, `Score`, `GDP per capita`, `Social support`, `Healthy life expectancy`, `Freedom to make life choices`, `Generosity`, `Perceptions of corruption`.

---

## 🛠️ Steps Performed
1. **Data Loading & Cleaning**  
   - Mounted Google Drive in Colab.  
   - Loaded CSV files and reshaped COVID datasets from wide → long format.  
   - Standardized country names for merging.

2. **Feature Engineering**  
   - Computed daily confirmed cases, yearly totals, and Case Fatality Rate (CFR).  
   - Aggregated COVID data at **Country-Year** level.

3. **Merging with Happiness Data**  
   - Renamed columns (`Country or region → Country`, `Score → Happiness_Score`).  
   - Merged on `Country` and `Year` (if available).

4. **Exploratory Data Analysis (EDA)**  
   - Global cumulative cases timeline.  
   - Top 10 countries with highest cases (latest year).  
   - Scatter plots: Happiness Score vs COVID cases.  
   - Correlation tests (Pearson’s r).

5. **Visualization Tools**  
   - Plots created with Matplotlib.  
   - Results include time series, bar charts, scatter plots, and correlation matrix.

---

## 📊 Key Findings (fill after running notebook)
- Example: Global COVID cases showed exponential growth in early 2020.  
- Example: Top 10 countries by confirmed cases included US, India, Brazil...  
- Example: Weak/No correlation observed between Happiness Score and COVID cases.  

(Add your own findings here after running the notebook.)

---

## ▶️ How to Run in Google Colab
1. Upload all 3 datasets into a folder inside Google Drive (e.g., `MyDrive/covid_project/`).  
2. Open the Colab notebook and run:
   ```python
   from google.colab import drive
   drive.mount('/content/drive')
