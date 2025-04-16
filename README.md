# Clayton-Kershaw-Pitch-Performance-Analysis-Project

This project analyzes the pitching performance of Clayton Kershaw, starting pitcher for the Los Angeles Dodgers, from 2015 to 2019 using **MLB Statcast data**. Through advanced statistical techniques such as **K-means clustering**, we identify pitch types, examine trends in release speed, movement, and evaluate pitch effectiveness.

---

## ⚾ Objective

To assess how Clayton Kershaw's pitch characteristics and performance evolved over five MLB seasons by:
- Analyzing pitch usage and effectiveness
- Classifying pitch types with K-means clustering
- Tracking performance changes over time

---

## 📊 Dataset

- **Source**: MLB Statcast via the `baseballr` package in R
- **Years**: 2015–2019
- **Pitcher**: Clayton Kershaw (`mlbam_id = 477132`)
- **Variables analyzed**: pitch type, release speed, spin rate, pitch movement, launch angle, hit events

---

## 🔍 Methods Used

### 1. Data Wrangling
- Cleaned and merged data across seasons
- Filtered for pitch outcomes: strikes, balls in play

### 2. Descriptive Statistics
- Calculated average release speeds by pitch type and year
- Tracked frequency of pitch types (fastballs, sliders, curveballs)

### 3. K-means Clustering
- Variables used: release speed, spin rate, pitch movement, launch speed, launch angle
- Elbow method to select **3 clusters**
- Each pitch was assigned to a cluster and evaluated for:
  - Frequency
  - Hit rate
  - Pitch profile

---

## 📈 Key Results

### 🧬 Cluster Profiles

| Cluster | Description                        | Avg Speed | Hit Rate |
|---------|------------------------------------|-----------|----------|
| 1       | Balanced pitches (e.g. sliders)     | 88.6 mph  | 21.1%    |
| 2       | High-speed pitches (e.g. fastballs) | 92.4 mph  | 19.4%    |
| 3       | Slower breaking pitches (curveballs)| 73.5 mph  | 20.1%    |

### 📉 Trends & Insights
- **Pitch speed declined** slightly over time, especially for fastballs.
- Kershaw relied more on **sliders** over time and less on high-speed fastballs.
- Cluster 2 (high-speed, high vertical movement) had the **lowest hit rate**, making it the most effective pitch group.

---

## 📊 Visualizations

- Boxplot of release speeds
- Pitch type frequency bar charts
- Heatmaps and loess plots showing pitch evolution over time
- Hit rate by year and cluster
- Cluster composition trends over time
- Scatterplots of release speed vs. launch angle by cluster

---

## 📚 Tools & Libraries

- R
- `baseballr`
- `ggplot2`, `dplyr`, `factoextra`, `reshape2`, `zoo`

---

## 👥 Authors

- Brett Loy
- Mateo Escobar  
- Abhi Gupta  
- Yucheng Zhao  
 
