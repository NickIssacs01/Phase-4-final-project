## **Movie Recommendation System Using Collaborative Filtering**

#### **Introduction**
This project aims to build a movie recommendation system using collaborative filtering techniques. The goal is to recommend personalized movies to users based on their past ratings. The project uses the MovieLens dataset, which contains user ratings for various movies.

---

### **Business Understanding**

#### **Problem Statement**
Streaming platforms like Netflix, Hulu, and Amazon Prime Video rely heavily on recommendation systems to suggest movies and shows to their users. These systems enhance user experience by providing tailored content, which increases user retention and engagement.

**Objective**: To build a recommendation system that suggests the top 5 movies to a user based on their past interactions and preferences.

---

### **Data Understanding**

#### **Dataset**
The project uses the **MovieLens Small Dataset**, which contains:
- `movies.csv`: Movie information (movie ID, title, genres).
- `ratings.csv`: User ratings for movies (user ID, movie ID, rating, timestamp).

**Key Insights**:
- Ratings range from 1 to 5, with most ratings being 4 or 5.
- The dataset has high sparsity in the user-movie interaction matrix.

---

### **Methodology**

#### **Approach**
The project employs two main collaborative filtering models:
1. **KNNBasic (User-Based Collaborative Filtering)**: Recommends movies liked by similar users.
2. **SVD (Matrix Factorization)**: Uses Singular Value Decomposition to uncover latent factors in the data.

**Evaluation Metrics**:
- **RMSE (Root Mean Squared Error)**: Measures prediction accuracy.
- **Precision@5 and Recall@5**: Measure ranking quality.

---

### **Modeling**

#### **Training Process**
1. Split the data into training (80%) and testing (20%).
2. Train the KNNBasic and SVD models on the training set.
3. Generate predictions on the test set.

#### **Results**
- **RMSE Comparison**:
  - KNNBasic: 0.8814
  - SVD: 0.8813

- **Precision@5 and Recall@5**:
  - KNNBasic: Precision = 0.72, Recall = 0.65
  - SVD: Precision = 0.74, Recall = 0.67

**Key Takeaways**:
- Both models perform well on this dataset, with SVD slightly outperforming KNNBasic in both RMSE and ranking metrics.

---

### **Recommendations**

#### **Top-N Recommendations Example**
The project includes functionality to generate the top 5 recommended movies for a sample user. For example, for User ID 1, the recommendations are visualized as a bar chart showing predicted ratings for each recommended movie.

#### **Hybrid Approach**
A hybrid approach combining collaborative filtering with content-based filtering (using movie genres) can address the cold-start problem and improve recommendation diversity.

---

### **Business Insights**

#### **Popular Movies**
The project identifies the top-rated movies with high average ratings and sufficient reviews. A bar chart shows the top 10 most popular movies.

#### **Genre Trends**
Identifying the most popular genres among users helps tailor recommendations further. A pie chart or bar chart shows genre distribution.

---

### **Challenges and Future Work**

#### **Challenges**
- Cold-start problem for new users or movies.
- Sparsity of the user-movie interaction matrix.

#### **Future Enhancements**
- Incorporate advanced techniques like neural collaborative filtering.
- Add real-time recommendation capabilities.
- Explore hybrid models further.

---

### **Conclusion**

#### **Summary**
The project successfully built a recommendation system using collaborative filtering and evaluated it using RMSE, Precision@5, and Recall@5. SVD performed slightly better than KNNBasic, demonstrating the ability to build a scalable and interpretable recommendation system.

#### **Impact**
- Demonstrated the ability to build a recommendation system that improves user engagement and satisfaction.
- Provided actionable insights for streaming platforms to enhance their recommendation engines.

---

### **How to Use This Project**
1. Clone the repository.
2. Install the required libraries (`pandas`, `numpy`, `matplotlib`, `seaborn`, `surprise`).
3. Load the MovieLens dataset.
4. Run the Jupyter Notebook to see the full implementation and results.

