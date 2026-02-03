# London Crime Analysis

This repository contains a Colab / Jupyter Notebook that performs exploratory analysis and simple visualizations on the `London_Crimes_2024_Expanded.csv` dataset.

Files
- `London_crime.ipynb` — main notebook that:
  - loads the CSV,
  - computes basic summaries (crime counts, crime types, monthly counts),
  - draws and saves plots,
  - creates a sample location scatter plot and top LSOA counts.
- `London_Crimes_2024_Expanded.csv` — input dataset (place this file in the same folder or upload to Colab when prompted).
- Output images saved by the notebook:
  - `top_10_crime_types.png`
  - `crimes_per_month_2024.png`
  - `crime_locations_scatter.png`
  - `top_10_lsoas.png`

Quick start (Google Colab)
1. Open [Google Colab](https://colab.research.google.com/).
2. Upload `London_crime.ipynb` (or open it from this repo).
3. Upload `London_Crimes_2024_Expanded.csv` when prompted by the notebook (the notebook uses `files.upload()`).
4. Run cells in order. The notebook mounts drive (if used), reads the CSV, prints summaries and saves images in the notebook working directory.

Requirements (if running locally)
- Python 3.8+
- The notebook uses the following packages (typical installation):
```bash
pip install pandas matplotlib notebook jupyter
```
(If you run in Colab, these are preinstalled.)

Notebook highlights / cell summary
- Data load: reads `London_Crimes_2024_Expanded.csv` into a pandas DataFrame and prints basic info (`df.info()`, `df.head()`).
- Summary statistics:
  - Unique crime types and top counts.
  - Crimes per month (monthly totals).
- Visualizations:
  - Bar chart: top 10 crime types → `top_10_crime_types.png`
  - Line chart: crimes per month → `crimes_per_month_2024.png`
  - Scatter: sample of crime locations (Latitude vs Longitude) → `crime_locations_scatter.png`
  - Bar chart: top 10 LSOAs by crime count → `top_10_lsoas.png`
- Sampling note: for plotting the full location cloud the notebook samples (e.g. 50,000 rows) to speed rendering.

Notes and tips
- The notebook expects the CSV column names used in the code (e.g. `Crime type`, `Month`, `LSOA name`, `Latitude`, `Longitude`). If your CSV has different headers, update the notebook accordingly.
- The dataset used in the notebook may be large (~1M rows). When working locally you may prefer to sample or use chunked processing.
- If you run into memory issues in Colab, either increase the runtime RAM or reduce the sample size for the scatter plot.

License
- Add your preferred license file if you plan to publish this repository (e.g., `LICENSE`).

Contact / attribution
- Add project author / contact information here if desired.
