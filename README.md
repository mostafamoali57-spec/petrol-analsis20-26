# ⛽ Global Fuel Prices Analysis (2020–2026)

Exploratory data analysis (EDA) of weekly fuel prices across **84 countries** between **January 2020 and April 2026**, looking at how fuel prices differ by region, how they relate to Brent crude oil prices, and how taxes affect what consumers pay.

Built with Python, pandas, matplotlib and seaborn.

---

## 📊 Dataset

**File:** `global_fuel_prices_2020_2026.csv`
**Size:** 27,468 rows × 10 columns, with no missing values.

| Column | Description |
|---|---|
| `date` | Weekly observation date |
| `country` | Country name |
| `region` | Geographic region (7 regions) |
| `income_level` | Income classification of the country |
| `subsidy_level` | Level of fuel subsidy in the country |
| `petrol_usd_liter` | Petrol price (USD per liter) |
| `diesel_usd_liter` | Diesel price (USD per liter) |
| `lpg_usd_liter` | LPG price (USD per liter) |
| `brent_crude_usd` | Brent crude oil price (USD per barrel) |
| `tax_percentage` | Tax share of the fuel price (%) |

> The dataset is not included in this repo. Place the CSV in the project root (or update the path in the notebook).

---

## 🔍 What the Analysis Covers

1. **Data loading & inspection**: head/tail, data types, missing values, summary statistics.
2. **Cleaning**: converting `date` to datetime and checking for missing values (none found).
3. **Regional comparison**: average petrol price per region.
4. **Time trends**: global petrol and diesel prices over time.
5. **Top 10 countries** by average petrol price.
6. **Crude oil relationship**: scatter plot of Brent crude vs. petrol price, with correlation.
7. **Tax impact**: petrol price distribution across tax brackets (Low / Medium / High / Very High).

---

## 📈 Key Findings

- **Average petrol price by region (USD/liter):**

  | Region | Avg. price |
  |---|---|
  | Europe | 3.70 |
  | Oceania | 3.66 |
  | Asia | 2.14 |
  | North America | 2.06 |
  | Africa | 1.55 |
  | South America | 1.43 |
  | Middle East | 1.23 |

- Europe and Oceania are the most expensive regions; the Middle East is the cheapest.
- The correlation between Brent crude and petrol price across the whole dataset is **0.26**, a weak linear relationship. Local factors such as taxes and subsidies appear to matter a lot.
- Overall averages: petrol ≈ 2.28 USD/L, diesel ≈ 2.13 USD/L, LPG ≈ 1.71 USD/L.

---

## 🚀 Getting Started

### 1. Clone the repo
```bash
git clone https://github.com/<your-username>/<repo-name>.git
cd <repo-name>
```

### 2. Install dependencies
```bash
pip install pandas matplotlib seaborn jupyter
```

### 3. Add the dataset
Put `global_fuel_prices_2020_2026.csv` in the project folder, then update the path in the notebook:
```python
df = pd.read_csv("global_fuel_prices_2020_2026.csv")
```
(The notebook was originally written in Google Colab, so it reads from `/content/`.)

### 4. Run the notebook
```bash
jupyter notebook
```

---

## 🛠️ Tech Stack

- Python 3
- pandas
- matplotlib
- seaborn

---

## 🔮 Possible Next Steps

- Compare petrol prices by `income_level` and `subsidy_level`
- Country-level time series (e.g., effect of the 2022 price spike)
- Correlation analysis per region instead of globally
- Build a simple price-prediction model

---

## 👤 Author

**Mostafa**
Student in AI & Data Science

---

## 📄 License

This project is for educational purposes. Add a license of your choice (e.g., MIT) before publishing.
