# PFDA_2025_Project-
Final project submission for PFDA - This project looks at windspeed around the country with the aim of identifying the best place to put windfarms. 

---
This project prepares, analyses, and visualises long-term wind data to:

- Clean and validate daily and monthly datasets
- Categorise wind conditions into turbine performance thresholds
- Identify quarterly patterns in wind speed
- Estimate annual wind energy production (GWh)
- Compare energy output against industry benchmarks
- Summarise operational vs non-operational wind days
- Rank stations by energy output and relative productivity

---

### 1. **Data Cleaning**
- Skip metadata rows
- Standardise column names
- Enforce correct types (dates, numeric)
- Drop incomplete rows

### 2. **Threshold Classification**
Wind speeds are classified into turbine stages based on:
- Cut-in (start generation)
- Optimal range (high efficiency)
- Rated (max production)
- Cut-out (shutdown threshold)

### 3. **Quarterly and Annual Aggregation**
- Quarterly mean wind speed and gust analysis
- Annual energy estimation using the power equation:  
  `P = 0.5 × ρ × A × Cp × V³`
- Industry benchmark comparison

### 4. **Visualisation & Outputs**
Plots are saved in the `figures/` directory and include:
- Turbine threshold bar charts
- Quarterly performance diverging bars
- Gust exceedance analysis
- Pie charts showing distribution of day types
- Annual energy production vs benchmarks

---

Scripts & Functions

All core logic is structured as functions, enabling:

- Batch processing of all station files
- Cleaned data previews saved to disk
- Automated plot generation to the figures folder
- Reproducible analysis pipeline

Key function categories:
- `clean_daily_wind_files` — clean and save daily data previews
- `plot_daily_turbine_thresholds` — turbine threshold plots
- `plot_bad_days_summary` — summary of cut-in/cut-out/extreme days
- `plot_daily_pie_charts` — pie charts for distribution & loss
- `estimate_and_plot_annual_wind_energy` — annual energy estimates
- `plot_quarterly_means_2019_2024` — quarterly wind mean plots
- `plot_quarterly_gust_exceedance` — moderate gust frequency

