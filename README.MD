### IPO Analysis: Pre- and Post-COVID Trends

This project provides a comprehensive analysis of Initial Public Offerings (IPOs) in the Indian stock market, examining trends before and after the COVID-19 pandemic. The analysis aims to identify key factors influencing IPO performance, including subscription rates, grey market premium (GMP) trends, and financial fundamentals of the companies involved.

---

### Project Objective

The primary goal of this analysis is to compare IPO trends and performance metrics from the pre-COVID era (2014-2019) with the post-COVID period (2020-2025). The project seeks to answer questions such as:

- How has the number of IPOs changed between the two periods?
- Which sectors and industries have seen the most significant growth in IPO activity?
- What is the relationship between an IPO's oversubscription rate and its first-day listing gains?
- Do a company's financial metrics (assets, revenue, profit) correlate with its IPO performance?
- How does the grey market premium (GMP) correlate with the actual listing day price?

---

### Data Sources

The analysis is based on two datasets:

- **Pre-COVID Data (2014-2019):** A dataset containing details of IPOs launched before the pandemic.
- **Post-COVID Data (2020-2025):** A dataset with IPO information from the post-pandemic period.

---

### Analysis Methodology

The analysis follows a structured data science workflow:

1.  **Data Loading and Initial Screening:** The datasets were loaded using Python's `pandas` library. An initial inspection of the data was performed to understand its structure, identify missing values, and check data types. The datasets contain a wide range of features, from IPO dates and issue prices to financial performance indicators and subscription rates.
2.  **Data Cleaning and Preprocessing:** To ensure data integrity, several cleaning steps were performed:
    - **Handling Missing Values:** Missing values in key financial and GMP columns were handled by imputation. For example, missing GMP values on a given day were filled with the value from the previous day. In cases where data on a fresh issue size was unavailable, the total issue size was used as a substitute.
    - **Data Type Conversion:** Object columns containing numerical data (e.g., issue price, issue size, gains/losses) were converted to appropriate numeric types (integers or floats) to enable mathematical operations and statistical analysis. Date columns were converted to datetime objects for time-series analysis.
3.  **Feature Engineering:** New features were created to enhance the analysis, such as a new `totalIssueAmount_inCr` column that was calculated using the `totalIssueSize` and the `issuePrice_perShareinRs`. An average GMP column was also calculated by averaging GMP values from day 1 to day 8.
4.  **Data Visualization and Insights:** The cleaned data was used to generate various plots and charts to visualize trends and patterns. The key findings were extracted from these visualizations.

---

### Key Findings

The analysis reveals several significant insights:

- **Increase in IPO Activity:** The number of IPOs has increased substantially in the post-COVID period. There are 289 IPOs in the post-COVID dataset (2020-2025) compared to 134 in the pre-COVID dataset (2014-2019). This shows that IPO activity has more than doubled after the pandemic.
  - - **Sector-wise Trends:** The "Financial Services" sector saw the highest number of IPOs in the pre-COVID era, while "Industrials" dominated the post-COVID period.
  - - **Grey Market Premium Analysis:** The histogram of listing day open prices for post-COVID IPOs closely follows a normal distribution curve, indicating a predictable relationship between the IPO issue price and its initial performance on the market.
  - ```
    The analysis also includes a day-by-day GMP trend, highlighting the volatility of the grey market before the official listing date.
    ```

---

### Project Structure

- **`MainAnalysisShreyansh.ipynb`**: The main Jupyter Notebook file containing the complete code for data analysis, cleaning, and visualization.
- **`.gitignore`**: A file to ignore unnecessary files and folders from version control.
- **`IPO Data Analysis.csv`**: The dataset for IPOs in the post-COVID era.
- **`Pre COVID Data 2014-19 Data Analysis.csv`**: The dataset for IPOs in the pre-COVID era.

---

### Technologies and Libraries

The project uses the following Python libraries for data analysis and visualization:

- `pandas`
- `matplotlib`
- `seaborn`
- `scipy.stats`
- `numpy`
- `datetime`
- `plotly.express`
- `plotly.graph_objects`

---

### Future Scope

This analysis provides a strong foundation for further research. Future work could include more advanced statistical modeling to predict IPO performance based on these variables, incorporating additional factors like market sentiment, and expanding the analysis to other global markets.
