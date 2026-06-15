#  California House Price Prediction using Machine Learning

<p align="center">
  <img src="https://img.shields.io/badge/Python-3.8+-3776AB?style=for-the-badge&logo=python&logoColor=white"/>
  <img src="https://img.shields.io/badge/Scikit--Learn-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white"/>
  <img src="https://img.shields.io/badge/Jupyter-F37626?style=for-the-badge&logo=jupyter&logoColor=white"/>
  <img src="https://img.shields.io/badge/Type-Regression-9B59B6?style=for-the-badge"/>
  <img src="https://img.shields.io/badge/Status-Complete-brightgreen?style=for-the-badge"/>
</p>

<p align="center">
  A regression project predicting California housing prices — comparing <b>Linear Regression, Ridge & Lasso</b> with full EDA, correlation analysis, and model evaluation.
</p>

---

##  Table of Contents

- [Overview](#-overview)
- [Project Workflow](#-project-workflow)
- [Exploratory Data Analysis](#-exploratory-data-analysis)
- [Models Used](#-models-used)
- [Results](#-results)
- [Tech Stack](#-tech-stack)
- [How to Run](#-how-to-run)
- [Project Structure](#-project-structure)
- [Author](#-author)

---

##  Overview

This project applies **supervised regression** to the **California Housing Dataset** from sklearn to predict median house prices based on demographic and geographic features. Three regression models are trained, evaluated, and compared using RMSE, MAE, and R² — with a bar chart visualizing model performance.

---


**Features:**

| Feature | Description |
|:---|:---|
| MedInc | Median income in block group |
| HouseAge | Median house age in block group |
| AveRooms | Average number of rooms per household |
| AveBedrms | Average number of bedrooms per household |
| Population | Block group population |
| AveOccup | Average number of household members |
| Latitude | Block group latitude |
| Longitude | Block group longitude |

---

##  Project Workflow

```
Load Dataset ──► EDA ──► Correlation Analysis ──► Train/Test Split ──► Model Training ──► Evaluation ──► Best Model
```

| Step | Description |
|:---:|:---|
| 1 | Load California Housing dataset as DataFrame |
| 2 | Basic info, null & duplicate check |
| 3 | Target distribution, correlation heatmap, scatter plots |
| 4 | 80/20 Train-Test Split (`random_state=42`) |
| 5 | Three regression models trained |
| 6 | Evaluated on RMSE, MAE, R² |
| 7 | Best model identified and reported |

---

##  Exploratory Data Analysis

| Analysis | Method |
|:---|:---|
| Data Overview | `.head()`, `.describe()`, `.shape` |
| Null Check | `.isnull().sum()` |
| Duplicate Check | `.duplicated().sum()` |
| Target Distribution | Histogram with KDE (`PRICE`) |
| Feature Correlation | Heatmap (`seaborn`, `coolwarm` palette) |
| Top Feature Scatter | Scatter plots — top 4 correlated features vs PRICE |
| Model Comparison | Bar plot of RMSE across models |

**Top Features Correlated with Price:**

| Feature | Correlation Direction |
|:---|:---:|
| MedInc |  Strong Positive |
| AveRooms |  Moderate Positive |
| Latitude |  Negative |
| Longitude |  Negative |

---

##  Models Used

| Model | Library | Key Parameters |
|:---|:---|:---|
| Linear Regression | `sklearn.linear_model` | Default |
| Ridge Regression | `sklearn.linear_model` | Default (`alpha=1.0`) |
| Lasso Regression | `sklearn.linear_model` | Default (`alpha=1.0`) |

> No feature scaling applied — models used raw features from the dataset.

---

##  Results

| Model | RMSE ↓ | MAE ↓ | R² ↑ |
|:---|:---:|:---:|:---:|
| **Linear Regression**  | **~0.72** | **~0.53** | **~0.58** |
| **Ridge Regression**  | **~0.72** | **~0.53** | **~0.58** |
| Lasso Regression | ~0.85 | ~0.61 | ~0.42 |

>  Exact values may vary slightly. Results based on `random_state=42` with 80/20 split.
> ↓ Lower is better &nbsp;|&nbsp; ↑ Higher is better

**Best Model → Linear Regression / Ridge** — both perform equally well on this dataset.

---

##  Tech Stack

| Tool | Purpose |
|:---|:---|
| Python | Core language |
| Pandas | Data manipulation |
| NumPy | Numerical operations |
| Matplotlib | Visualization |
| Seaborn | Statistical plots |
| Scikit-learn | ML models & evaluation |
| Jupyter Notebook | Development environment |

---

## How to Run

**1. Clone the repository**

```bash
git clone https://github.com/your-username/california-house-price-prediction.git
cd california-house-price-prediction
```

**2. Install dependencies**

```bash
pip install pandas numpy matplotlib seaborn scikit-learn jupyter
```

**3. Launch Jupyter Notebook**

```bash
jupyter notebook house_price_prediction.ipynb
```

**4. Run all cells**

`Kernel` → `Restart & Run All`

---


##  Author

**Sadia Noreen**
*Software Engineering Graduate | AI & ML Enthusiast*

---

<p align="center">⭐ If you found this helpful, consider giving it a star!</p>
