# WeatherDataAnalysis
This project focuses on analyzing historical weather data using Python and essential data analysis libraries. The goal is to uncover patterns, trends, and anomalies that influence weather behavior, enabling better understanding and decision-making based on past climate records.

*📘 Jupyter Notebook*  
*🛠️ pandas, Python*  

By **Harshavardhan Bommalata**

# 🌦️ weather_data_analysis

This project is a beginner-friendly, hands-on notebook created to strengthen your data analysis skills using a real-world weather dataset. It includes practical exercises involving data filtering, condition-based selection, aggregation, group operations, and simple visualizations using `pandas` and `matplotlib`.

The notebook helps you understand how to:
- Extract meaningful patterns from weather data
- Work with textual and numeric columns
- Apply functions and aggregations
- Identify unique conditions like snowfall or high wind speed
- Visualize trends and distributions in the dataset

---

## 📘 Project Overview

**Project Title**: Weather Data Analysis  
**Level**: Beginner to Intermediate  
**Tool**: Jupyter Notebook  
**Libraries Used**: `pandas`, `numpy`, `matplotlib`, `seaborn`

This project demonstrates beginner-friendly data analysis techniques using a real-world weather dataset. It walks through practical use cases such as filtering conditions (e.g., snowfall, high wind speed), identifying unique weather patterns, handling missing data, grouping, aggregating, and visualizing the weather trends. This notebook serves as a great entry point for learning how to explore and analyze time-series or categorical data using Python.

---

## 🎯 Objectives

1. Understand and apply basic pandas operations on a real-world weather dataset.
2. Perform filtering and conditional selection (e.g., days with snowfall or high wind speed).
3. Use grouping and aggregation methods to summarize weather trends.
4. Identify unique weather conditions and count their occurrences.
5. Visualize weather distributions using bar plots and count plots.

---

## 🏗️ Project Structure

### 1. Data Setup

- Real-world weather dataset with columns like `Weather`, `Visibility_km`, `Wind Speed_km/h`, `Temperature_C`, etc.
- Loaded using pandas from a CSV file.

```python
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns

# Reading the dataset
data = pd.read_csv("weather.csv")

# Display first few rows
data.head()
```

### 2. Data Analysis Tasks

#### ✅ Task 1: Find Unique Weather Conditions  
```python
data['Weather'].unique()
Absolutely! Here's the **complete Task 2 section** in the **exact format** you want:

---

````markdown
### 2. Data Analysis Tasks

### Task 2:

#### ✅ Task 1: Find Unique Weather Conditions  
```python
data['Weather'].unique()
````

#### ✅ Task 2: Find Instances of Snowfall

```python
data[data['Weather'].str.contains("Snow")]
```

#### ✅ Task 3: Find Number of Times Weather is Exactly Clear

```python
data[data['Weather'] == "Clear"]
```

#### ✅ Task 4: Find Wind Speed Above 24 km/h

```python
data[data['Wind Speed_km/h'] > 24]
```

#### ✅ Task 5: Find All Null Values in the Dataset

```python
data.isnull().sum()
```

#### ✅ Task 6: Rename Column ‘Weather’ to ‘Weather Condition’

```python
data.rename(columns={'Weather': 'Weather Condition'}, inplace=True)
```

#### ✅ Task 7: Mean Visibility When Weather is Fog

```python
data[data['Weather Condition'] == 'Fog']['Visibility_km'].mean()
```

#### ✅ Task 8: Group Weather and Find Mean

```python
data.groupby('Weather Condition').mean()
```

#### ✅ Task 9: Find Maximum Wind Speed When Visibility > 40

```python
data[data['Visibility_km'] > 40]['Wind Speed_km/h'].max()
```

#### ✅ Task 10: Plot Frequency of Weather Conditions

```python
import matplotlib.pyplot as plt
import seaborn as sns

plt.figure(figsize=(12,6))
sns.countplot(x='Weather Condition', data=data)
plt.xticks(rotation=90)
plt.title("Frequency of Weather Conditions")
plt.show()
```
---

## 🔍 Summary & Learnings

- Practiced core pandas operations on real-world weather data  
- Learned how to filter data using conditions and string matching  
- Explored usage of `.groupby()`, `.mean()`, and `.unique()`  
- Applied data transformations using `.rename()` and `.apply()`  
- Created visualizations using `matplotlib` and `seaborn`  
- Strengthened understanding of DataFrame indexing, null checks, and column manipulation

---

````markdown
---

## 💻 How to Use

1. Clone the repository:
   ```bash
   git clone https://github.com/harshavardhanBOMMALATA/DataAnalysisWarmUpExercises.git
````

2. Navigate into the folder:

   ```bash
   cd DataAnalysisWarmUpExercises
   ```

3. Open the notebook:

   ```bash
   jupyter notebook weather.ipynb
   ```

4. Run all the cells one by one to explore the analysis

---

