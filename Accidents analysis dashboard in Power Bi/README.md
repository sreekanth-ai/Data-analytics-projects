# 🚧 Road Accident Analysis Dashboard (Power BI)

![Dashboard Image](https://github.com/IsaacMwendwa/PBI-Road-Accident-Analysis/blob/main/Final%20Dashboard%20Image.PNG "Final Dashboard Image")

## 📌 Overview

This project presents an interactive **Power BI Dashboard** built to analyze road accident data in the United Kingdom.
The goal is to identify accident trends, casualty patterns, and key risk factors to support data-driven decision making for road safety improvements.

---

## 🎯 Objectives

* Analyze total accidents and casualties over time
* Compare current year vs previous year performance
* Identify accident severity distribution
* Understand impact of vehicle type, road type, and location
* Study monthly trends and seasonal patterns

---

## 📊 Key Dashboard Features

### 🔹 Primary KPIs

* Total Casualties (Current Year vs Previous Year)
* Total Accidents (Current Year vs Previous Year)
* Year-on-Year (YoY) Growth in casualties and accidents

### 🔹 Secondary KPIs

* Casualties by Vehicle Type
* Casualties by Road Type
* Casualties by Area (Urban/Rural)
* Day vs Night accident analysis

### 🔹 Trend Analysis

* Monthly trend comparison (Current Year vs Previous Year)

---

## 🧮 DAX Measures Used

### 1. Casualties Analysis

**Current Year Casualties**

```DAX
CY Casualties = TOTALYTD(SUM(Data[Number_of_Casualties]), 'Calendar'[Date])
```

**Previous Year Casualties**

```DAX
PY Casualties = CALCULATE(SUM(Data[Number_of_Casualties]), SAMEPERIODLASTYEAR('Calendar'[Date]))
```

**YoY Growth**

```DAX
YoY Casualties = ([CY Casualties] - [PY Casualties]) / [PY Casualties]
```

---

### 2. Accident Analysis

**Current Year Accidents**

```DAX
CY Accidents = TOTALYTD(COUNT(Data[Accident_Index]), 'Calendar'[Date])
```

**Previous Year Accidents**

```DAX
PY Accidents = CALCULATE(COUNT(Data[Accident_Index]), SAMEPERIODLASTYEAR('Calendar'[Date]))
```

**YoY Growth**

```DAX
YoY Accidents = ([CY Accidents] - [PY Accidents]) / [PY Accidents]
```

---

## 🛠 Tools Used

* Power BI Desktop
* DAX (Data Analysis Expressions)
* Data Modeling
* Excel / CSV Dataset

---

## 🚀 How to Use

1. Download Power BI Desktop
2. Clone this repository
3. Open `.pbix` file in Power BI
4. Explore interactive dashboard filters and insights

---

## 🐞 Issues & Improvements

If you find any issue or want to suggest improvements:

* Open an issue in this repository [here](https://github.com/IsaacMwendwa/Power-BI-Road-Accidents-Analysis-Dashboard/issues/new)
* Provide details of the expected vs actual result

---

## 💡 What makes this project strong (for resume)

This project demonstrates:

* Data cleaning & modeling
* Advanced DAX calculations
* KPI design thinking
* Business insight generation
* Interactive dashboard development

---




  
