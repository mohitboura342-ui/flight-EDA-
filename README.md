# ✈️ Flight Delay Analysis and Prediction

## 📌 Project Overview

Flight delays are a major challenge in the aviation industry, impacting airline efficiency, airport operations, and passenger satisfaction. This project performs a comprehensive Exploratory Data Analysis (EDA) on flight operations data to identify the primary factors contributing to arrival delays and build a foundation for predictive modeling.

The analysis investigates operational, environmental, and scheduling factors such as departure delays, carrier delays, weather disruptions, NAS congestion, airport traffic, and late aircraft arrivals.

---

## 🎯 Project Objectives

* Analyze flight delay patterns and operational disruptions.
* Identify the strongest factors influencing arrival delays.
* Explore relationships between delay causes and flight performance.
* Understand airport-level and day-of-week delay trends.
* Generate actionable insights for airlines and airport management.
* Prepare the dataset for machine learning-based delay prediction.

---

## 📂 Dataset Description

The dataset contains information related to:

### Flight Information

* Flight Number
* Origin Airport
* Destination Airport
* Distance
* Scheduled Departure Time
* Day Of Week

### Delay Components

* Departure Delay
* Carrier Delay
* Weather Delay
* NAS Delay
* Late Aircraft Delay

### Target Variable

* **Arr_Del_morethan15**

  * 0 → On-Time Flight
  * 1 → Flight Delayed More Than 15 Minutes

---

## 🧹 Data Preprocessing

Several preprocessing steps were performed before analysis:

### Feature Removal

The following columns were removed:

* Cancelled
* Diverted
* Top_Carriers
* ArrDelay
* ArrTime
* DepTime

These features either contained minimal information or introduced target leakage.

### Data Cleaning

* Duplicate inspection
* Missing value handling
* Data type verification
* Feature consistency checks

### Target Engineering

Arrival delay was transformed into a binary classification target:

```python
Arr_Del_morethan15
```

---

## 📊 Exploratory Data Analysis

### Univariate Analysis

Analyzed:

* Flight delay distribution
* Departure delay distribution
* Distance distribution
* Carrier delay distribution
* Weather delay distribution
* NAS delay distribution
* Late aircraft delay distribution
* Airport traffic volume
* Day-of-week traffic patterns

### Bivariate Analysis

Investigated relationships between:

* Departure Delay vs Arrival Delay Status
* Carrier Delay vs Departure Delay
* Weather Delay vs Arrival Delay Status
* Distance vs Arrival Delay Status
* NAS Delay vs Arrival Delay Status
* Airport Activity vs Delay Status

### Multivariate Analysis

Explored interactions among:

* Departure Delay + Late Aircraft Delay + Arrival Delay
* Carrier Delay + Weather Delay + NAS Delay
* Day Of Week + Carrier Delay + Arrival Delay
* Airport Activity + Delay Probability

---

## 🔍 Key Insights

### 1. Departure Delay is the Strongest Indicator

Flights experiencing higher departure delays have a significantly higher probability of arriving late.

### 2. Late Aircraft Delays Propagate Through the Network

Aircraft arriving late often cause downstream scheduling disruptions, increasing future delays.

### 3. Carrier Delays Strongly Influence Operations

Carrier-related disruptions exhibit a strong positive relationship with departure delays.

### 4. Weather Delays are Less Frequent but Severe

Although weather delays occur less frequently, they can generate substantial operational disruptions.

### 5. Hub Airports Experience Higher Delay Concentration

Airports such as:

* LAX
* DFW
* JFK

show elevated levels of flight delay activity.

### 6. NAS Delays Contribute to Arrival Delays

National Airspace System congestion is a notable contributor to delayed arrivals.

---

## 📈 Correlation Findings

Strongest positive relationships:

| Variable Pair                          | Correlation |
| -------------------------------------- | ----------- |
| Departure Delay ↔ Carrier Delay        | 0.69        |
| Departure Delay ↔ Late Aircraft Delay  | 0.68        |
| Arrival Delay Status ↔ Departure Delay | 0.47        |
| Arrival Delay Status ↔ NAS Delay       | 0.40        |

Distance and Day Of Week show relatively weak direct relationships with arrival delay status.

---

## 🛠️ Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Jupyter Notebook

---

## 🚀 Business Recommendations

### Improve Departure Delay Monitoring

Implement real-time monitoring systems to identify flights at risk of arriving late.

### Optimize Aircraft Turnaround Time

Reduce delay propagation by improving aircraft scheduling and gate management.

### Focus on Hub Airport Congestion

Allocate additional operational resources to high-traffic airports.

### Strengthen Weather Response Planning

Develop proactive scheduling strategies for adverse weather conditions.

### Enhance Predictive Analytics

Utilize delay-cause variables to develop machine learning models for early delay prediction.

---

## 📌 Conclusion

This analysis demonstrates that flight delays are primarily driven by operational factors such as departure delays, carrier disruptions, late aircraft arrivals, and NAS congestion. While weather-related delays occur less frequently, they can significantly impact flight performance. The insights generated from this project can support airlines in reducing delays, improving scheduling efficiency, and enhancing passenger experience.

---

## 👨‍💻 Author

**Mohit Boura**

Aspiring Data Scientist | Machine Learning Enthusiast | Data Analytics

