
# IPL Auction Data Analysis

This project focuses on analyzing IPL Auction data to uncover insights about player bids, team strategies, and value optimization. Below is an overview of the analysis performed and how the results were derived.

## Table of Contents
1. [Data Preparation](#data-preparation)
2. [Analysis and Visualizations](#analysis-and-visualizations)
   - Value for Money Analysis
   - Team Spending Strategy
   - Distribution of Base Prices and Winning Bids
   - Outlier Detection
3. [Technologies Used](#technologies-used)
4. [How to Run](#how-to-run)
5. [Key Insights](#key-insights)

## Data Preparation
- The datasets for each IPL team were loaded as separate CSV files.
- The data was combined into a single DataFrame using:
  ```python
  df_team1 = [df for df in teams]
  merged_team1 = pd.concat(df_team1, ignore_index=True)
  ```
- Key metrics were calculated:
  - **Bid-to-Base Ratio**: `Winning Bid / Base Price`.
  - Additional filtering was applied to exclude extreme outliers (e.g., `Bid-to-Base Ratio < 20`).

## Analysis and Visualizations

### 1. Value for Money Analysis
- A boxplot was used to visualize the **Bid-to-Base Ratio** by team.
- Insights:
  - Teams like **RCB** and **KKR** spent significantly more than base prices for key players.
  - Teams like **MI** and **CSK** optimized their budgets effectively.

### 2. Team Spending Strategy
- **Total Spending**: A bar chart visualized the total amount spent by each team.
  - Example: **RCB** and **KKR** were top spenders.
- **Average Spending per Player**: Another bar chart showed the average cost of players by team.
  - Example: **PBKS** and **SRH** spent conservatively compared to other teams.

### 3. Distribution of Base Prices and Winning Bids
- A histogram compared the distributions of base prices and winning bids.
  - Winning bids exhibited a broader range and higher peaks than base prices.
  - High bids indicated fierce competition for certain players.

### 4. Outlier Detection
- A boxplot identified outliers in winning bids for each team.
  - Outliers often represented marquee players with exceptionally high bids.
  - Teams like **KKR** and **RCB** had several outliers.

## Technologies Used
- **Python Libraries**:
  - `pandas`: Data manipulation and aggregation.
  - `matplotlib` and `seaborn`: Data visualization.
- **Jupyter Notebook**: Interactive coding and analysis environment.

## How to Run
1. Clone the repository.
2. Ensure the following Python libraries are installed:
   ```bash
   pip install pandas matplotlib seaborn
   ```
3. Place the IPL team datasets (CSV files) in the project directory.
4. Run the Jupyter Notebook file (`IPL_Auction.ipynb`) for analysis.
5. Visualizations and insights will be displayed interactively.

## Key Insights
- **Value Optimization**: Teams like **MI** and **CSK** focused on cost-effective acquisitions.
- **Spending Patterns**: **RCB** and **KKR** spent heavily, while **PBKS** and **SRH** were more budget-conscious.
- **Demand vs. Supply**: High winning bids for certain players highlight their perceived value and demand.
- **Outliers**: Teams targeting marquee players often showed outliers in their spending patterns.

This project provides a comprehensive overview of IPL Auction strategies, revealing patterns and trends in player acquisitions.
