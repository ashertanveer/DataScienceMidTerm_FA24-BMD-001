
# DataScienceMidTerm_<FA24-BMD-001>

Student Name: <M.Asher Tanveer>  
Course Title: Data Science Fundamentals  
Instructor:Dr. Fakhar Mustafa  
Date:13-Nov-2025  

# Dataset Source and Description

Source: [OpenAQ Global Air Quality Data](https://openaq.org/)  
File Used:`openaq_location_8876_measurments.csv`

This dataset contains real-time measurements of major air pollutants collected from various monitoring stations worldwide.  
The main variables include:
- **Location and Country** — where the air quality measurement was taken  
- **Pollutant Type** — e.g., PM2.5, PM10, NO2, CO, SO2  
- **Value** — measured pollutant concentration  
- **Date and Time** — timestamp of measurement  

The dataset is used to analyze global air pollution trends, data quality, and relationships between different pollutants.

---

# Steps Performed in Analysis

1. **Data Import**
   - Loaded the dataset using `read.csv()` in R.  
   - Checked structure, summary statistics, and data dimensions.  
   - Counted missing values per column.

2. **Data Cleaning**
   - Removed duplicate records using `distinct()`.  
   - Renamed columns for readability (e.g., `value` → `pollutant_value`).  
   - Converted `date.utc` column to proper Date-Time format using `as.POSIXct()`.  
   - Converted pollutant concentration variables to numeric.  
   - Handled missing values by removing rows with `NA` in key columns.  
   - Detected and handled outliers using the Interquartile Range (IQR) method.

3. **Exploratory Data Analysis (EDA)**
   - Calculated **mean, median, variance, and standard deviation** for major pollutants (PM2.5, PM10, NO2, CO, SO2).  
   - Created a **correlation matrix** and **heatmap** to observe relationships among pollutants.  
   - Plotted **histograms and density plots** to visualize pollutant distributions.  
   - Used **boxplots** to compare pollutant variation across locations.  
   - Developed **time-series plots** to show pollution trends over time.

---

# Summary of Main Insights

- **High correlation** observed between particulate pollutants (PM2.5 and PM10), indicating they often increase together.  
- **Pollution spikes** were detected in specific time periods, suggesting possible seasonal or event-based variations.  
- **Certain locations** consistently recorded higher pollutant levels, showing geographic variability in air quality.

---

# Repository Contents

| File Name | Description |
|------------|-------------|
| `midterm_analysis.R` | Main R script containing full data import, cleaning, and analysis code |
| `openaq_location_8876_measurments.csv` | Original dataset used in analysis |
| `README.md` | Documentation file summarizing dataset, methods, and insights |

---

✅ **Note:** Run `midterm_analysis.R` in RStudio to reproduce results.  
Required R packages: `dplyr`, `ggplot2`, `tidyverse`, `ggcorrplot`.

