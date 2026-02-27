📊 Behavioral Trading Analysis: Sentiment & Performance EDA
This project explores the intersection of trader psychology (Sentiment) and execution performance (Win Rate, Volume, and Frequency). By analyzing trade logs, we identify behavioral archetypes and the correlation between emotional states and profitability.

🚀 Key Insights from EDA
1. Quality Over Quantity (Trades per Day vs. Win Rate)
Analysis of the relationship between trading frequency and success reveals a clear "Overtrading Trap":

High-Precision Traders: Trades with a Win Rate > 0.8 are exclusively associated with low daily trade counts. This suggests that selective, patient trading leads to higher accuracy.

The "Retail" Cluster: A massive volume of trades is concentrated in the 0.3 to 0.6 win rate range. Most market participants fall into this medium-win-rate, high-frequency category.
![Win Rate vs Sentiment](graphs_and_table/scatter_plot(trades_VS_winrate).png)


2. Emotional Drivers (Sentiment Distribution)
Sentiment data shows that "Greed" and "Fear" are the primary engines of market activity:

Greed is the Catalyst: The Greed sentiment accounts for the highest number of trades, likely representing aggressive entries.

Fear as an Exit Strategy: Fear shows the second-highest volume. This high frequency during fearful periods likely indicates "panic closing" or defensive position management.

Extreme Fatigue: "Extreme" sentiments (Extreme Fear/Greed) show significantly lower trade counts, suggesting that at emotional extremes, traders become paralyzed or "exhausted."

3. User Activity Distribution (Trades per Day Histogram)
The distribution of activity follows a power-law-like slope:

Core User Base: The majority of users perform between 0-50 trades per day.

Progressive Decay: There is a sharp, progressive decrease in the number of users as the trades-per-day count increases. This indicates that the "High Frequency" segment is a small, specialized subset of the total population.

4. Sentiment-Based Volatility (Trades vs. Sentiment)
I analyzed the stability of trading behavior across different emotional states:

Neutrality is Active: Surprisingly, Neutral sentiment has the highest average trade count, though it carries a huge standard deviation, indicating inconsistent behavior.

Fearful Variance: Fear and Extreme Fear exhibit the largest standard deviations in trade counts. Under stress, trader behavior becomes highly unpredictable.

Greed is Stable: Conversely, Greed and Extreme Greed have lower standard deviations and lower overall trade counts compared to Neutral/Fear, suggesting more "calculated" or slower decision-making when optimistic.

5. Win Rate Consistency under Stress
How does emotion impact the likelihood of a win?

The Volatility of Fear: Extreme Fear produces the highest variance in performance, with win rates swinging between 0.20 and 0.40.

The Baseline: All other sentiments (Neutral, Greed, Fear) gravitate toward a stable average win rate of 0.35 with significantly lower standard deviation. This suggests that while most emotions don't drastically change the win rate, Extreme Fear creates the most inconsistent performance outcomes.

🛠 Tech Stack
Language: Python

Data Manipulation: Pandas, NumPy

Visualization: Matplotlib, Seaborn

Machine Learning: Scikit-Learn (K-Means Clustering & Random Forest)

📂 Project Structure
data/: Raw and processed trading logs.

notebooks/: Detailed EDA and feature engineering.

models/: Behavioral clustering and predictive profitability models.

plots/: Exported visualizations for report generation.
