# Trader Performance and Market Sentiment Analysis

**Author:** Maulik Bambhaniya
**Date:** July 28, 2025

## 📖 Project Overview

This project conducts an in-depth analysis of the relationship between trader performance and prevailing market sentiment. By merging historical trading data with the Fear & Greed Index, the analysis aims to uncover actionable insights that can help formulate more effective trading strategies. The core question explored is: **How does market sentiment impact a trader's profitability and success rate?**

---

## 📊 Key Findings & Summary

The analysis reveals a strong correlation between trader performance and market sentiment.

* **Best Performance:** Traders achieved the highest average Profit and Loss (PnL) of **$67.89** and the best win/loss ratio of **0.87** during periods of **"Extreme Greed"**. This suggests that market optimism and high confidence create the most favorable conditions for profitable trades within this dataset.
* **Worst Performance:** The most challenging environment for traders was during periods of **"Extreme Fear"**, which resulted in the lowest win/loss ratio of **0.59**.
* **Trading Volume:** Interestingly, trading volume remained relatively consistent across all sentiment conditions, indicating that traders in this dataset did not adjust their trade sizes based on market fear or greed.

---

## ⚙️ Methodology

The analysis was conducted in a Google Collab using Python and several data science libraries. The key steps included:

1.  **Data Preprocessing**:
    * Loaded two datasets: `fear_greed_index.csv` (market sentiment) and `historical_data.csv` (trade history).
    * Converted date/time columns to a consistent datetime format.
    * Merged the two datasets on the 'date' column to align trades with the sentiment of that day.

2.  **Feature Engineering**:
    * Created a `PnL_category` column to classify each trade as either 'profitable' (PnL > 0) or 'unprofitable'.

3.  **Exploratory Data Analysis (EDA)**:
    * Visualized the distribution of market sentiment, Closed PnL, and trading volume (in USD) to understand the underlying data characteristics.

4.  **Sentiment-Based Analysis**:
    * Grouped the data by market sentiment (`classification`) to calculate the average PnL and the win/loss ratio for each category.
    * Generated bar charts to visually compare performance across different sentiments.

---

## 📈 Visualizations

The key findings are supported by the following visualizations, which were generated and saved to the `outputs/` directory:

1.  **EDA Plots (`eda_plots.png`)**: A set of three charts showing the overall distribution of market sentiment, PnL, and trading volume.
2.  **Sentiment Performance Plots (`sentiment_performance_plots.png`)**: Two bar charts comparing the average PnL and win/loss ratio across the five sentiment categories.

---

## 💡 Insights & Next Steps

* **Strategic Recommendation**: The data suggests that a potentially effective strategy would be to trade more aggressively during "Extreme Greed" and adopt a more cautious, risk-averse approach during "Extreme Fear".
* **Future Research**: A deeper investigation could be conducted to analyze the types of assets traded or the duration of trades during "Extreme Greed" to identify the specific factors driving higher profitability.

---

## 🚀 How to Run the Analysis

To replicate this analysis, follow these steps:

1.  **Prerequisites**: Ensure you have Python installed along with the following libraries:
    * `pandas`
    * `numpy`
    * `matplotlib`
    * `seaborn`

    You can install them via pip:
    ```bash
    pip install pandas numpy matplotlib seaborn
    ```

2.  **Data**: Place the `fear_greed_index.csv` and `historical_data.csv` files in the csv_files.

3.  **Execution**: Run the `notebook_1.ipynb` Jupyter Notebook. The output plots will be saved to a newly created `outputs/` folder.
4.  **Use the Open in Collab Button**: Clicking the Open in collab button will open the notebook in collab to run place the data set in the collab directory and run all the cells.

