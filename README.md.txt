# Olist E-Commerce Supply Chain & Customer Analysis

## Business Question
Where is the business losing revenue due to supply chain inefficiencies (late deliveries, seller performance), and can we predict which orders are at risk of a bad review?

## Dataset
[Brazilian E-Commerce Public Dataset by Olist](https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce) (Kaggle). Not included in this repo due to file size — download directly from the link above and place the CSVs in a `data/` folder to run the notebook.

## Key Findings
- **Late delivery significantly lowers review scores** (4.21 average for on-time orders vs. 2.54 for late ones), confirmed statistically significant via an independent t-test (p < 0.001).
- **Health & beauty, watches & gifts, and bed/bath/table** are the top revenue-generating product categories; **São Paulo** drives over 2.8x the revenue of the next-highest state.
- **Repeat customers make up only ~3% of the customer base but contribute ~5.6% of revenue** — a small but real sign of higher per-customer value among returning buyers.
- Several **data quality issues** were uncovered during cleaning, including orders marked "delivered" with no delivery date, and "canceled" orders with full delivery timelines and inconsistent review evidence.
- Built a **logistic regression model** to predict bad reviews (89% accuracy, but only 25% recall on actual bad reviews — improved to 48% recall using class rebalancing, at a cost to precision).

## Tools Used
Python, pandas, NumPy, SciPy (hypothesis testing), scikit-learn (classification model), matplotlib & seaborn (visualization), Jupyter Notebook.

## How to Run
1. Clone this repository.
2. Download the dataset from the Kaggle link above and place the CSVs in a `data/` folder in the project root.
3. Install dependencies: `pip install -r requirements.txt`
4. Open and run `01_data_exploration.ipynb` in Jupyter Notebook, top to bottom.

## Project Structure
```
├── 01_data_exploration.ipynb   # Full analysis notebook
├── README.md
├── requirements.txt
└── data/                       # Not included — see "Dataset" above
```