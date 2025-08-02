# 🚗 Car Price Prediction

This project predicts the selling price of used cars using machine learning. It uses an XGBoost model trained on data like brand, mileage, engine, fuel type, etc., and provides a user interface through a Streamlit app.

---

## 📁 Project Structure

| File         | Description                                         |
|--------------|-----------------------------------------------------|
| `main.py`    | Trains the model using XGBoost and log-transformed target |
| `main2.py`   | Loads the saved model & pipeline, predicts from `input.csv`, and generates `Output.csv` |
| `app.py`     | Streamlit app for live predictions from user input |
| `data.csv`   | Dataset used for training                          |
| `input.csv`  | Sample input data for predictions                  |

> ⚠️ Files like `model.pkl`, `pipeline.pkl`, and `Output.csv` are generated **after running** the code.  
> They are not stored in the GitHub repo by default.

---

## 🧠 Features Used for Prediction

- Brand  
- Vehicle age  
- Kilometers driven  
- Seller type  
- Fuel type  
- Transmission type  
- Mileage  
- Engine capacity  
- Max power  
- Number of seats

---

## 💡 How the Project Works

1. **`main.py`**  
   - Preprocesses data using pipelines  
   - Applies log1p transformation on price  
   - Trains an XGBoost model  
   - Model and pipeline are saved as `.pkl` files

2. **`main2.py`**  
   - Loads saved `.pkl` files  
   - Takes data from `input.csv`  
   - Predicts selling prices  
   - Saves the result to `Output.csv`

3. **`app.py`**  
   - A Streamlit-based user interface  
   - User fills in car details  
   - Predicts and displays the price

---

## 🚀 How to Run

### 🔹 Step 1: Train the Model
```bash
python main.py
