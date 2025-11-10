AI-Powered Product Trend Prediction System

📋 Objective

To predict which products are likely to trend next month using market indicators such as search volume, social media buzz, sentiment, influencer mentions, and sales performance.

🧩 Project Workflow
1️⃣ Data Preparation & Feature Engineering

Collected synthetic market dataset simulating real-world signals:
['product_name', 'search_volume', 'social_mentions', 'news_articles', 'sales_usd_million', 'influencer_mentions', 'sentiment_score', 'trend_score', 'next_month_trend']

Engineered meaningful ratios & indicators:

social_to_search_ratio

news_to_influencer_ratio

overall_engagement index

2️⃣ Feature Selection

Used only key predictive features to reduce overfitting:

['search_volume', 'social_mentions', 'news_articles',
 'sales_usd_million', 'influencer_mentions', 'sentiment_score']

3️⃣ Model Building

Trained a Random Forest Classifier with hyperparameter tuning to prevent overfitting:

RandomForestClassifier(
    n_estimators=100,
    max_depth=2,
    min_samples_leaf=6,
    max_features='sqrt',
    random_state=42
)

4️⃣ Model Evaluation

5-Fold Cross-Validation Accuracy: ~0.88

ROC-AUC Score: 0.87

Balanced performance across both classes (Trending vs Non-Trending)

5️⃣ Visualization & Insights

Feature Importance chart shows:

social_mentions and sentiment_score → strongest drivers of product trends.

influencer_mentions also plays a major role.

Trend Distribution shows around 25–30% of products likely to trend next month.

📊 Key Insights

📈 Social buzz strongly correlates with upcoming product trends.

💬 Positive sentiment is a major leading indicator of future product sales.

🎯 Influencer mentions amplify product visibility and trend probability.

💡 Data-driven marketing can help brands forecast trends before they peak, optimizing inventory & campaigns.

⚙️ Tech Stack

Python

Pandas, NumPy for data preprocessing

Scikit-learn for model building

Matplotlib, Seaborn for visualization

Jupyter Notebook / Colab for analysis
