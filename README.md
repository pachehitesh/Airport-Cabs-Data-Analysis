### **NYC Taxi Data Analysis 🚖📊**  

```md
# NYC Taxi Data Analysis 🚖📊

This repository contains a Jupyter Notebook that analyzes NYC taxi trip data using NumPy. The dataset (`nyc_taxis.csv`) contains information about taxi rides, including trip distance, fare amount, and payment methods.

## 📌 Features & Analysis
- **Load Data:** Import and preprocess NYC taxi trip data.
- **Speed Calculation:** Compute average speed of taxi rides.
- **Ride Count in February:** Filter and count rides that happened in February.
- **Expensive Rides:** Count rides with fare amounts greater than $50.
- **Credit Card Transactions:** Count rides paid via credit cards.

## 📂 Files
- `analysis.ipynb` - Jupyter Notebook with all the analysis.
- `nyc_taxis.csv` - The dataset containing taxi ride details.

## 🛠️ Installation & Usage
1. Clone the repository:
   ```sh
   git clone https://github.com/your-username/nyc-taxi-analysis.git
   ```
2. Navigate to the project directory:
   ```sh
   cd nyc-taxi-analysis
   ```
3. Install dependencies:
   ```sh
   pip install numpy jupyter
   ```
4. Run the Jupyter Notebook:
   ```sh
   jupyter notebook
   ```

## 🖥️ Code Overview
### Load Data
```python
import numpy as np
taxi = np.genfromtxt('nyc_taxis.csv', delimiter=',', skip_header=True)
```

### Calculate Average Speed
```python
speed = taxi[:, 7] / (taxi[:, 8] / 3600)
mean_speed = speed.mean()
print(mean_speed)
```

### Filter Rides in February
```python
rides_feb = taxi[taxi[:, 1] == 2, 1]
print(rides_feb.shape[0])
```

### Count Expensive Rides
```python
expensive_rides = taxi[taxi[:, -3] > 50, -3].shape[0]
print(expensive_rides)
```

### Count Credit Card Payments
```python
credit_card_rides = taxi[taxi[:, 6] == 2, 6].shape[0]
print(credit_card_rides)
```

## 📊 Data Insights
- The **average taxi speed** is approximately **32.24 mph**.
- There were **13,333 rides in February**.
- **16 rides** had fares exceeding **$50**.
- **11,832 rides** were paid using credit cards.

## 🤝 Contributing
Feel free to fork this repo and contribute by improving analysis or adding visualizations!

## 📜 License
This project is open-source and available under the MIT License.
```

This README provides:
✅ Clear description 
✅ Code snippets  
✅ Setup guide  
✅ Insights from analysis  

