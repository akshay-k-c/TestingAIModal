
# 🧪 AI Testing Basics – House Price Prediction

This project is a **hands-on demo** of how we can **test a simple AI model** beyond just training and accuracy.  
Instead of treating ML models as black boxes, we explore **data validation, edge cases, metamorphic testing, and sanity checks**.

---

## 📌 Features Covered

- ✅ **Data Validation** – Checking for nulls, invalid values, unrealistic ranges, and outliers  
- ✅ **Model Training** – Using `RandomForestRegressor` on California Housing dataset  
- ✅ **Edge Case Testing** – Feeding extreme/unusual inputs to see how the model behaves  
- ✅ **Metamorphic Testing** –  
  - Add noise to inputs and check stability  
  - Scale inputs and verify proportional changes  
- ✅ **Performance Evaluation** – Using MAE, MSE, R²  
- ✅ **Explainability** – Using SHAP (optional extension)

---

## 🚀 Getting Started

### 1. Clone the repo
```bash
git clone https://github.com/<your-username>/<repo-name>.git
cd <repo-name>
```

### 2. Install dependencies
```bash
pip install -r requirements.txt
```

### 3. Run the notebook
Open in **Jupyter Notebook / Google Colab**:
```bash
jupyter notebook DataValidation.ipynb
```

---

## 📂 Project Structure
```
├── DataValidation.ipynb   # Main notebook with code and tests
├── requirements.txt       # Python dependencies
└── README.md              # Project documentation
```

---

## 🧑‍🔬 Example Tests

### 🔹 Edge Case Input
```python
edge_input = {
    "MedInc": 20.0,   # Very high income
    "HouseAge": 0.0,  # New house
    "AveRooms": 1.0,  # Very few rooms
    ...
}
```
👉 Helps us see how the model reacts to **unusual but possible scenarios**.

### 🔹 Metamorphic Test
```python
# Add small noise to features
noise = np.random.normal(0, 0.01, X_test.shape)
X_test_noisy = X_test + noise
y_pred_noisy = model.predict(X_test_noisy)
```
👉 Checks if **small input changes cause reasonable output changes**.

---

## 📊 Why This Project?
Testing AI systems isn’t just about accuracy — it’s about **robustness, fairness, and reliability**.  
This project demonstrates **practical examples** of AI testing you can extend to real-world systems.

---

## 🛠️ Tech Stack
- Python 3.x
- Scikit-learn
- Pandas, NumPy
- SHAP (Explainability)
- Matplotlib, Seaborn (Visualization)

---

## 🌟 Future Enhancements
- ✅ Add SHAP explainability plots  
- ✅ Add drift detection example  
- ✅ Extend with adversarial testing  
