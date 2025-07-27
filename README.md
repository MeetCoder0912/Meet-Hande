# Sentiment-Driven-Trading-Analysis

Graphs for analysis of both the datasets.

<img width="1798" height="964" alt="image" src="https://github.com/user-attachments/assets/284047be-0049-4fcb-aece-6780b5a68794" />

 It illustrates the number of trades categorized by their profit and loss (PnL) outcome (Breakeven, Profit, Loss) across different market sentiments. The market sentiments are classified using the "Fear and Greed Index Classification" and are labeled as "Extreme Greed," "Extreme Fear," "Fear," "Greed," and "Neutral."
 "Fear" sentiment shows the most activity, with the highest numbers of both breakeven and profitable trades.

Losses are consistently lower than breakeven and profit trades across all sentiments.

"Greed" sentiment has the highest number of losing trades, despite generally having a high volume of overall trades.

Breakeven trades are a significant portion of outcomes, often rivaling or exceeding profit trades in volume.


<img width="1794" height="585" alt="image" src="https://github.com/user-attachments/assets/0fc63657-01b5-4464-ab9e-d29578c28907" />

The image contains two bar charts showing financial outcomes based on market sentiment.

Left Chart (Total PnL):

"Fear" sentiment generated the highest total profit/loss (PnL) (around $3.4 million), followed by "Extreme Greed" ($2.7 million).

"Extreme Fear" had the lowest PnL (around $0.75 million).

Right Chart (Total Trading Volume):

"Fear" sentiment also had the highest total trading volume (almost $4.9 billion), significantly more than any other sentiment.

"Greed" sentiment was second in volume (around $2.9 billion).

"Extreme Fear" and "Extreme Greed" had the lowest trading volumes.

Overall takeaway: "Fear" sentiment periods were the most active and profitable, while "Extreme Fear" periods were the least active and least profitable. "Extreme Greed" showed good profitability despite lower volume compared to "Greed."


<img width="1801" height="1188" alt="image" src="https://github.com/user-attachments/assets/2b810095-ec26-4f15-a277-864f9ddb2618" />


The image shows two bar charts analyzing trading activity by "Day of Week" and "Market Sentiment."

Top Chart: "Total PnL by Day of Week and Market Sentiment"

This chart shows the total profit/loss (PnL) for each day of the week, broken down by market sentiment (Extreme Fear, Extreme Greed, Fear, Greed, Neutral).

Key points:

Monday and Tuesday (Fear sentiment): Show the highest PnL.

Thursday: Generally shows lower PnL, with some negative PnL for "Extreme Fear."

Overall: "Fear" and "Extreme Greed" sentiments tend to have higher PnL across most days.

Bottom Chart: "Total Trading Volume (USD) by Day of Week and Market Sentiment"

This chart shows the total trading volume in USD for each day of the week, also broken down by market sentiment.

Key points:

Monday, Saturday, and Wednesday (Fear/Greed sentiments): Show the highest trading volumes.

Trading volume generally high for "Fear" and "Greed" sentiments throughout the week.

Sunday: Shows comparatively lower overall volume.

In essence: The charts highlight how market sentiment influences PnL and trading volume differently across the days of the week, with "Fear" and "Greed" sentiments often associated with higher activity and "Fear" frequently leading to higher PnL.


<img width="1793" height="1068" alt="image" src="https://github.com/user-attachments/assets/ce6a1c08-cbac-4375-9427-b0e958cc680d" />


This bar chart titled "Total PnL by Trade Side and Market Sentiment" shows the total profit and loss (PnL) from trades, categorized by whether the trade was a "BUY" or a "SELL" and by the prevailing market sentiment (Extreme Fear, Extreme Greed, Fear, Greed, Neutral).

BUY Side:

"Fear" sentiment (light gray bar) resulted in the highest PnL for BUY trades, close to $2 million.

Other sentiments on the BUY side generated significantly less PnL.

SELL Side:

"Extreme Greed" sentiment (light blue bar) generated the highest PnL for SELL trades, reaching approximately $2.5 million.

"Fear" (light gray bar) and "Greed" (light orange bar) also show substantial PnL for SELL trades.

<img width="1523" height="1365" alt="image" src="https://github.com/user-attachments/assets/91a41c8c-066c-49d5-a3c6-e055be0277e2" />

Numbers Range: Values range from -1 to 1.

1 (Red): Perfect positive correlation (variables move in the same direction).

-1 (Dark Blue): Perfect negative correlation (variables move in opposite directions).

0 (White/Light Blue): No linear correlation.

Key Observations:

Execution Price has a weak positive correlation with Size USD (0.19) and Fee (0.23).

Size USD has a strong positive correlation with Fee (0.75). This means larger trade sizes tend to incur higher fees.

Closed PnL shows very weak correlations with all other features (close to 0), indicating that these specific features (Execution Price, Size USD, Fee, value) don't strongly predict the Closed PnL in a linear fashion.

Value has very weak (close to 0 or slightly negative) correlations with all other features.

In essence, the matrix tells us how much and in what direction one feature tends to change when another feature changes. The strongest relationship observed is between "Size USD" and "Fee."


Built a Machine Learning Model to predict the outcome of a trade based on a combination of trade details and market sentiment. This demonstrates that there are predictable patterns in the data that can be learned and potentially used to inform trading strategies. For instance, we could use this model to identify the characteristics of trades that are most likely to be profitable.

Model Accuracy:- 

<img width="971" height="420" alt="image" src="https://github.com/user-attachments/assets/38a322a1-5621-4239-aa32-ad78676b832d" />


Here's a structured and properly formatted section for your GitHub README, detailing the tools and technologies used:

---

## 🛠️ Tools & Technologies

This project leverages a robust set of tools and technologies to perform data analysis, machine learning, and interactive visualization.

* **Python:** The foundational programming language for all analytical scripts and model development.
* **Data Manipulation & Analysis:**
    * **Pandas:** Utilized extensively for efficient data loading, cleaning, transformation, and analysis of trading and market sentiment data (Fear & Greed Index).
    * **NumPy:** Employed for high-performance numerical operations and mathematical computations throughout the analysis.
* **Data Visualization:**
    * **Matplotlib:** Used for creating static, animated, and interactive visualizations.
    * **Seaborn:** Built on Matplotlib, it provided a high-level interface for drawing attractive and informative statistical graphics, enhancing the visual understanding of data relationships.
* **Machine Learning:**
    * **Scikit-learn:** The primary library for building and evaluating our predictive model.
        * `RandomForestClassifier`: The chosen algorithm for the classification task.
        * `train_test_split`: For robust splitting of data into training and testing sets to evaluate model generalization.
        * `accuracy_score` & `classification_report`: Metrics used to comprehensively assess the model's performance.
* **Development Environment & Interactivity:**
    * **IPython / Google Colab:** The interactive environment for executing code, developing the analysis, and presenting findings. Google Colab served as the cloud-based platform.
    * **Ipywidgets:** Integrated to build an interactive user interface (UI) directly within the notebook, enabling real-time testing of the machine learning model.
* **AI-Assisted Development:**
    * **Large Language Models (LLMs):** Leveraged as an invaluable development assistant for various tasks including:
        * Code generation
        * Debugging support
        * Generating explanatory text and documentation
        This significantly accelerated the development workflow.
    * **Prompt Engineering:** Systematic techniques were applied to effectively communicate with and guide the LLM, ensuring the generated outputs were precise, relevant, and aligned with the project's analytical objectives.

---

