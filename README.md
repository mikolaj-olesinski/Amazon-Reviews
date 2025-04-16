# Amazon Nokia Reviews Analysis

## Project Overview
This README summarizes our comprehensive analysis of Nokia product reviews on Amazon. We examined various aspects of the review data to understand customer feedback, identify sentiment, and develop recommendation strategies.

## Main Components

### Data Analysis
- **Ratings & Products:**  
  - Analyzed 78,930 ratings across 7,438 unique products.
  - Identified review distribution patterns with an average of 10.6 reviews per product.
  - Found a highly skewed distribution where 10% of products received most of the reviews.
- **User Analysis:**  
  - Analyzed 68,040 unique users (after filtering out "unknown" users).
- **Review Length Patterns:**  
  - Calculated an average review length of 103 words.
 ![box_review_leghth](https://github.com/user-attachments/assets/fee392e9-3ab8-4178-b9ac-00fc4d3bd067)
 

### Sentiment Analysis
- **Classification:**  
  - Classified reviews as positive (4–5 stars) or negative (1–3 stars).
- **Models Implemented:**  
  - Tested various classification models including Logistic Regression, Naive Bayes, SVC, and Random Forest.
- **Results:**  
  - Achieved 85% accuracy with Logistic Regression.
  - Identified key words strongly associated with positive and negative sentiments.
![confusion_matrix](https://github.com/user-attachments/assets/8781bd47-1709-4f1d-85fb-2b3b967e8713)

### Text Clustering Analysis
- **Methodology:**  
  - Applied K-Means clustering using TF-IDF vectorization.
- **Clusters Created:**  
  - Identified 5 distinct product clusters:
    - Phone Cases and Accessories
    - Chargers and General Products
    - Phones and Electronics
    - Bluetooth Headsets
    - Phone Batteries
     ![clusters](https://github.com/user-attachments/assets/19d722f6-18df-4334-b1e7-789973e6448f)


### Product Recommendation System
- **Approach:**  
  - Developed a cluster-based recommendation strategy.
- **Techniques:**  
  - Created similarity measurements between product clusters.
  - Implemented composite scoring based on ratings, review count, and helpfulness.
![graph_recommendation](https://github.com/user-attachments/assets/071b4861-02a5-494a-a40d-128f54e9c9ca)

### Neural Collaborative Filtering (NCF)
- **Model Details:**  
  - Built a deep learning model for rating prediction using PyTorch.
  - Leveraged user and product embeddings.
- **Performance:**  
  - Achieved an RMSE of 0.4554 and an MAE of 0.2338.

### Word Embedding Analysis
- **Technique:**  
  - Trained a Word2Vec model on the review text.
- **Analysis:**  
  - Conducted word similarity analysis.
  - Applied a mean vector approach for sentiment analysis.
  - Extracted key product features based on semantic similarity.
- **Recommendations:**  
  - Developed product recommendations based on the semantic similarities between word embeddings.
![word_embedding_visualization](https://github.com/user-attachments/assets/d81c63d7-3525-4c52-bfae-62a2373e56c3)

### Negative Review Knowledge Graph
- **Graph Construction:**  
  - Built a knowledge graph connecting products with their negative features.
- **Insights:**  
  - Identified frequently mentioned negative aspects across reviews.
- **Visualization:**  
  - Created a visualization of product-feature relationships.
- **Statistics:**  
  - Constructed a graph with 7,849 nodes and 113,310 edges.
