# FinSent: Decoding Market Hype through Sentiment Intelligence

##  Project Overview

The convergence of natural language processing (NLP) and financial analytics has established new frames of interpretation of market dynamics. FinSent proposes a machine learning-based solution to forecast short-term stock market indexes by analyzing the sentiment behind financial news headlines. Using the NLP 2025 Financial News Markets Events dataset, this project applies the VADER sentiment analysis tool to measure the emotional tone of market news.

##  Tech Stack

* **Language:** Python


* **Data Processing:** Pandas, NumPy


* **NLP / Sentiment Analysis:** NLTK (VADER)


* **Machine Learning:** Scikit-Learn (Random Forest Classifier)


* **Data Visualization:** Matplotlib, Seaborn



##  Methodology

1. **Data Preprocessing:** Ingested the dataset using Pandas, handled missing values, and cleaned the textual data while preserving punctuation and capitalization, which are crucial for VADER's intensity scoring.


2. **Sentiment Extraction:** Applied the VADER algorithm to compute compound polarity scores for individual news headlines, categorizing them as positive, negative, or neutral.


3. **Target Engineering:** Binarized the continuous `Index_Change_Percent` variable into a categorical `Market_Direction` target (1 for upward movement, 0 for downward movement).


4. **Predictive Modeling:** One-Hot Encoded categorical variables and trained a Random Forest Classifier using 100 estimators to predict market direction.



##  Key Results & Insights

* **Predictive Edge:** The inclusion of sentiment scores provides a statistically significant edge over random guessing, particularly when identifying downward movements correlated with highly negative sentiment.


* **Model Performance:** The Random Forest model achieved an accuracy of 51.84% on the unseen test dataset.


* **Hype vs. Reality:** Data visualizations (including a custom scatter plot) successfully highlight the presence of "Hype Bubbles"—instances where highly positive news sentiment does not linearly equate to market gains, validating the "buy the rumor, sell the news" phenomenon.



##  Repository Structure

* `finsent_model_analysis.ipynb`: The complete, commented Jupyter Notebook containing the data pipeline, model training, and visualizations.


* `FinSent_Project_Report.pdf`: The comprehensive academic report detailing the project background, literature review, and extended methodology.


* `requirements.txt`: The library dependencies required to run the notebook.
