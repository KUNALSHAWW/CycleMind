# ⚡ CycleMind  
### Predictive Intelligence for UCI Combined Cycle Power Plant

> “An end‑to‑end, research‑grade toolkit implementing every major regression paradigm, with plug‑and‑play templates for instant insights.”

---

## 🧩 Project Overview  
CycleMind harnesses the full spectrum of regression techniques—linear, polynomial, decision‑tree, SVR, and random forest—to model and predict the electrical power output (PE) of a Combined Cycle Power Plant. Built with meticulous attention to best practices, this repository serves both as a bench‑tested research project **and** a jump‑start template for anyone tackling regression on their own data.

---

## 🔬 Why This Project Stands Out  
- **Breadth & Depth**: Implements **every** key regression model, from the simplest OLS to ensemble forest techniques.  
- **Research‑Driven**: Hyperparameters tuned, performance compared via R² & Adjusted R², MAE & RMSE.  
- **Ready‑to‑Use Templates**: Simply change `Data.csv` to your dataset and run—no boilerplate hunting.  
- **Clean, Modular Code**: Each model in its own script, with unified evaluation and visualization functions.  
- **Insightful Visuals**: Pair‑plots with regression overlays, Actual vs. Predicted scatter & trend‑comparison plots.

---

## 🔍 Dataset  
- **Name**: Combined Cycle Power Plant  
- **Source**: [UCI Machine Learning Repository](https://archive.ics.uci.edu/ml/datasets/Combined+Cycle+Power+Plant)  
- **Features**:  
  - AT: Ambient Temperature  
  - V: Exhaust Vacuum  
  - AP: Ambient Pressure  
  - RH: Relative Humidity  
- **Target**: PE (Net hourly electrical energy output)

---

## 🚀 Quick Start  

1. **Clone the repository**  
   ```bash
   git clone https://github.com/KUNALSHAWW/CycleMind.git
   cd CycleMind
   ```

2. **Place your dataset**  
   Rename your CSV to `Data.csv` and drop it in the root folder.

3. **Install dependencies**  
   ```bash
   pip install -r requirements.txt
   ```

4. **Run any model script**  
   ```bash
   python linear_regression.py
   python polynomial_regression.py
   python decision_tree_regression.py
   python svr_regression.py
   python random_forest_regression.py
   ```

5. **Visualize results**  
   - **Pair Plots**: `visualizations/pairplot.ipynb`  
   - **Actual vs. Predicted (Scatter)**  
   - **Trend Comparison Plot**  
     ```python
     plt.figure(figsize=(10,4))
     plt.plot(y_test[:50], label='Actual', marker='o')
     plt.plot(y_pred[:50], label='Predicted', marker='x')
     plt.xlabel('Test Sample Index')
     plt.ylabel('Power Output (PE)')
     plt.title('Trend Comparison: Actual vs. Predicted')
     plt.legend()
     plt.grid(True)
     plt.show()
     ```

---

## 🗂️ Repository Structure  
```
CycleMind/
├── Data.csv                       # Your input dataset
├── README.md                      # Project overview & instructions
├── requirements.txt               # Python dependencies
├── linear_regression.py           # Ordinary least squares regression
├── polynomial_regression.py       # Polynomial regression (degree 4)
├── decision_tree_regression.py    # Decision tree regressor
├── svr_regression.py              # Support vector regression
├── random_forest_regression.py    # Random forest regressor
├── pairplot.ipynb                 # Jupyter notebooks & plot exports
```

---

## 📊 Evaluation Metrics  
- **R² & Adjusted R²** — model explanatory power  

---

## 👩‍💻 Usage & Extensibility  
- **To adapt**: simply update the CSV file name, adjust column indices if needed, and run.  
- **To extend**: drop in your own model script following the existing pattern—data loading, `train_test_split()`, `fit()`, `predict()`, `evaluate()`, and visualization.

---

## 🏆 Acknowledgments & License  
Built for clarity, reproducibility, and deep exploration.  
Licensed under the MIT License — feel free to adapt and build upon!

---

> Ready for your next regression challenge? Fork, clone, and explore. CycleMind awaits.
