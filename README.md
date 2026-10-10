# 🌱 AI-Based Crop Recommendation System

An intelligent agriculture application that uses Machine Learning to recommend suitable crops based on soil nutrients, soil conditions, and climatic parameters. The system combines ML-based predictions, rule-based crop suitability analysis, and an economic engine to help farmers identify suitable and affordable crops.

## 🚀 Project Overview

Choosing the right crop is an important decision for farmers. Crop selection depends on soil fertility, pH, temperature, humidity, rainfall, and cultivation costs.

This project uses a trained Machine Learning model to predict suitable crops and further evaluates them using crop requirements and budget information. It aims to support data-driven agricultural decision-making.

## ✨ Key Features

- 🌾 **Crop Prediction:** Predicts suitable crops using a trained Machine Learning model.
- 📊 **Top 3 Crop Recommendations:** Identifies promising crop options using prediction probabilities.
- 🌱 **Crop Suitability Analysis:** Evaluates soil type, pH, temperature, and rainfall.
- 💰 **Budget-Based Recommendations:** Estimates cultivation costs based on land area and crop cost per acre.
- ⚖️ **Combined Scoring System:** Combines ML predictions with agronomic suitability scores.
- 🔌 **FastAPI Backend:** Provides API-based integration for crop recommendation functionality.
- 🖥️ **User-Friendly Interface:** Accepts agricultural inputs and presents recommendation results.

## 🛠️ Technologies Used

- **Programming Language:** Python
- **Machine Learning:** Scikit-learn
- **Data Processing:** Pandas, NumPy
- **API Development:** FastAPI
- **Model Storage:** Pickle
- **Data Sources:** CSV datasets
- **Server:** Uvicorn
- **Frontend:** HTML, CSS, JavaScript (if included in your project)

## 📥 Input Parameters

The system uses the following agricultural parameters:

| Parameter | Description |
|---|---|
| Nitrogen (N) | Nitrogen content in soil |
| Phosphorus (P) | Phosphorus content in soil |
| Potassium (K) | Potassium content in soil |
| Temperature | Environmental temperature |
| Humidity | Relative humidity |
| Soil pH | Soil acidity or alkalinity |
| Rainfall | Expected rainfall in millimetres |
| Soil Type | Type of soil used for cultivation |
| Land Area | Available land area in square feet |
| Budget | Farmer's available cultivation budget |

## ⚙️ How It Works

1. **User Input:** The user enters soil, climate, and agricultural information.
2. **ML Prediction:** The trained model predicts suitable crops and their probabilities.
3. **Top Crop Selection:** The system identifies the top three crop candidates.
4. **Suitability Evaluation:** The suitability engine checks soil type, pH, temperature, and rainfall using `crop_requirements1.csv`.
5. **Combined Ranking:** ML scores contribute 65% and suitability scores contribute 35% to the combined ranking.
6. **Economic Evaluation:** The economic engine uses `crop_economics1.csv` to estimate cultivation costs based on land area and cost per acre.
7. **Final Recommendation:** The system identifies suitable crop options and evaluates which options fit the user's budget.

## 📂 Important Project Files

- `crop_requirements1.csv` — Crop-specific agronomic requirements.
- `crop_economics1.csv` — Crop cultivation costs and related economic data.
- `models/crop_model.pkl` — Saved ML model, if present at this path.
- `prediction.py` — Crop prediction logic, if included.
- `suitability.py` — Crop suitability scoring, if included.
- `economic.py` — Economic calculations, if included.
- `api.py` — FastAPI application entry point, if included.

*The filenames above should be adjusted to match the actual files in your repository.*

## ▶️ Installation and Setup

### 1. Clone the repository

```bash
git clone YOUR_GITHUB_REPOSITORY_URL
cd "AI Crop Recommendation System"
```

Replace `YOUR_GITHUB_REPOSITORY_URL` with your actual GitHub repository URL.

### 2. Create a virtual environment

```bash
python -m venv venv
```

Activate it on Windows:

```bash
venv\Scripts\activate
```

### 3. Install dependencies

If your project includes a `requirements.txt` file:

```bash
pip install -r requirements.txt
```

Otherwise, install the dependencies used by your code:

```bash
pip install fastapi uvicorn pandas numpy scikit-learn
```

### 4. Run the application

If your FastAPI entry point is `api.py` and the FastAPI instance is named `app`, run:

```bash
python -m uvicorn api:app --reload
```

Open the API documentation in your browser:

```text
http://127.0.0.1:8000/docs
```

**Note:** Run the command from the directory containing `api.py`, and ensure the saved model and CSV datasets are available at the paths expected by the code.

## 🎯 Project Objectives

- Apply Machine Learning to agricultural crop recommendation.
- Evaluate crop suitability using agronomic requirements.
- Integrate economic calculations into crop selection.
- Develop an API-based application for accessing prediction functionality.
- Support informed agricultural planning through data-driven recommendations.

## 🔮 Future Enhancements

- Integration of real-time weather data.
- Support for additional crops and regional soil datasets.
- Fertilizer recommendations.
- Crop disease detection using Deep Learning.
- Multilingual support for farmers.
- Database integration to store prediction history.
- Cloud deployment for wider accessibility.

## 👨‍💻 Author

**Sahil Sohaliya**

BCA (AI/DA) Student | Python & Machine Learning Enthusiast

## 📌 Disclaimer

The recommendations generated by this project are intended for educational and decision-support purposes. Actual crop suitability and cultivation costs may vary according to local agricultural conditions, regional prices, and farming practices.
