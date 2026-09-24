# Global Temperature Change Analysis (1961–2022)

**Author:** Arush

## Project Description

This project analyzes country-level annual temperature anomalies (°C,
relative to a 1951–1980 baseline) from 1961 to 2022, to understand how
global warming has progressed over time, which countries have warmed the
most, and how warming is distributed across decades and regions.

The analysis:
- Reshapes the raw wide-format data (one column per year) into a clean
  long-format table (`Country`, `year`, `temp_change`).
- Computes and visualizes the **global average temperature trend**.
- Ranks countries by **total warming** (early 1960s vs. most recent 5 years).
- Compares **average anomaly by decade**.
- Shows the **distribution of anomalies** across all countries for the
  latest year on record.
- Produces a **heatmap** of the 15 most-warmed countries across decades.

## Dataset

- **File:** `data/climate_change_indicators.csv`
- **Source:** Food and Agriculture Organization of the United Nations
  (FAO), FAOSTAT Climate Change — Climate Indicators, Temperature Change.
  https://www.fao.org/faostat/en/#data/ET
- **License:** CC BY-NC-SA 3.0 IGO
- **Shape:** 225 countries/territories × temperature anomaly for each
  year from 1961 to 2022 (plus metadata columns).

## Technologies Used

- Python 3
- pandas — data loading, reshaping, aggregation
- NumPy — numeric helpers
- Matplotlib — all charts (line, bar, histogram, heatmap)
- Jupyter Notebook format (`.ipynb`)

## Project Structure

```
.
├── Arush_ClimateChangeAnalysis.ipynb   # Main notebook (code + charts + narrative)
├── Arush_ProjectReport.docx            # Written project report
├── README.md                           # This file
├── requirements.txt                    # Python dependencies
├── data/
│   └── climate_change_indicators.csv   # Source dataset
└── outputs/                            # Chart images exported from the notebook
    ├── global_temperature_trend.png
    ├── top_bottom_warming_countries.png
    ├── decade_comparison.png
    ├── warming_distribution.png
    └── top15_heatmap.png
```

## Setup & Run Instructions

1. **Install dependencies** (Python 3.9+ recommended):
   ```bash
   pip install -r requirements.txt
   ```
2. **Launch the notebook:**
   ```bash
   jupyter notebook Arush_ClimateChangeAnalysis.ipynb
   ```
   or open it in JupyterLab / VS Code / Google Colab and run all cells.
3. The notebook expects the dataset at `data/climate_change_indicators.csv`
   (already included). Running all cells regenerates every chart into
   `outputs/`.

## Key Findings

- The global average temperature anomaly rose from close to 0°C in the
  early 1960s to roughly **+1.4°C by 2022**.
- Warming has **accelerated since the 1990s**, with the last two decades
  showing the sharpest year-over-year increases.
- Warming is **not uniform**: some countries show anomalies well above the
  global average, while a small number show little change or slight
  cooling.
- **Every decade since the 1960s has been warmer than the previous one**
  on average.

See `Arush_ProjectReport.docx` for the full write-up, and the notebook for
all code, charts, and analysis in detail.
