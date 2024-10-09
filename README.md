# VAST Challenge 2018 - Mini Challenge 2: Water Sensor Data Analysis

## Project Overview

This project is part of the **CST4060 - Coursework 2** and revolves around analyzing water sensor data collected from various locations in the Boonsong Lekagul Wildlife Preserve. The data is crucial for investigating the potential contamination of water sources, which may be linked to the declining population of the **Rose-Crested Blue Pipit**, a locally loved bird.

Through a series of visual and statistical analyses, we aim to:
- Identify **trends** and **anomalies** in the water quality data.
- Assess the **data quality** and handle missing or unrealistic data points.
- Provide meaningful insights into possible environmental issues in the wildlife preserve.

## Table of Contents
- [Project Overview](#project-overview)
- [Dataset](#dataset)
- [Objective](#objective)
- [Methodology](#methodology)
- [Technologies Used](#technologies-used)
- [Results](#results)

## Dataset

The dataset comes from the **VAST Challenge 2018 - Mini Challenge 2** and includes water sensor readings from various rivers and streams in the **Boonsong Lekagul Wildlife Preserve**. The data contains multiple years of measurements of different chemicals, such as **ammonium**, **nitrates**, **phosphorus**, and **water temperature**, among others.

Each entry in the dataset contains:
- **ID**: Unique identifier for each reading.
- **Value**: The measured value of a specific chemical.
- **Location**: The sensor's location within the wildlife preserve.
- **Sample Date**: The date the sample was collected.
- **Measure**: The type of chemical or physical measurement (e.g., ammonium, temperature, etc.).

## Objective

The primary objectives of this analysis are:
1. **Describe Trends and Anomalies**: Identify changes over time and across locations for various water measurements, and highlight any sudden or unusual deviations in the data.
2. **Assess Data Quality**: Analyze the presence of missing data, changes in the frequency of data collection, and identify unrealistic values (e.g., water temperature exceeding 100°C).

## Methodology

1. **Data Loading and Preprocessing**:
   - Loaded the dataset into a Pandas DataFrame.
   - Handled missing data and identified gaps in the collection frequency.
   - Filtered out unrealistic values using domain knowledge and statistical thresholds.

2. **Trends and Anomalies Analysis**:
   - Created pivot tables to calculate the yearly average of each measure.
   - Used the `diff()` function to observe yearly differences and identify trends and anomalies.
   - Visualized trends and anomalies using **Altair** charts, allowing for a detailed exploration of water contamination over time.

3. **Data Quality Assessment**:
   - Generated heatmaps to visualize missing values for each measure over time.
   - Investigated the frequency of data collection using visualizations of the number of samples collected per year and month.
   - Detected unrealistic values by examining extreme outliers and inconsistent data points.

4. **Visualization and Analysis**:
   - Employed **Altair** to generate a wide range of visualizations, including:
     - Heatmaps for missing data.
     - Line charts to show trends in water quality over time.
     - Scatter plots to identify outliers and anomalies.

## Technologies Used
- **Python**: The core programming language for data manipulation and visualization.
- **Pandas, NumPy**: Libraries used for data manipulation and analysis.
- **Altair**: A declarative statistical visualization library used to generate interactive charts and dashboards.
- **Jupyter Notebook**: For conducting and documenting the analysis.

## Results

### Trends and Anomalies
- **Trends**: Several chemicals, such as **arsenic** and **total hardness**, showed increasing trends, while others, like **lead** and **zinc**, displayed a decreasing pattern over time.
- **Anomalies**: Significant anomalies were detected, particularly in locations like **Kohsoom** and **Somchair**, where unusual values were recorded for fecal coliforms and methylosmoline.

### Data Quality
- **Missing Data**: A detailed heatmap was generated to visualize missing data points across years and locations.
- **Collection Frequency**: The data collection frequency peaked in 2007 but then showed a declining trend in subsequent years.
- **Unrealistic Values**: Measures like **nitrites** and **ammonium** in the **Tansanee** location exhibited unrealistic spikes, likely due to faulty sensor readings.
