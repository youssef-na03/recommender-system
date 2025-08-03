# 🎬 Movie Recommender System

> This repository demonstrates how to build a movie recommender system using the MovieLens 100k dataset. It features two Jupyter notebooks, each implementing a different recommendation approach.

---

## 📓 Notebooks

### `SimilarMovies.ipynb`: Item-Based Collaborative Filtering

This notebook finds movies similar to a user-selected movie ("Star Wars") by analyzing rating patterns.

**Methodology:**
- **Create User-Movie Matrix**: Constructs a matrix where rows are users, columns are movies, and cell values are the ratings.
- **Calculate Correlation**: Computes the **Pearson correlation** between "Star Wars" and all other movies to find similarity scores.
- **Filter for Popularity**: To ensure reliable results, it filters out movies with fewer than 100 ratings, removing noise from movies with limited data.
- **Generate Similar Movies**: The final output is a list of movies ranked by their similarity to "Star Wars".

### `KNN.ipynb`: Generating User Recommendations

This notebook builds a recommender that suggests movies to a specific user based on their rating history.

**Methodology:**
- **Data Preparation**: Loads the MovieLens dataset and calculates properties for each movie, such as the total number and average of ratings.
- **Compute Correlation Matrix**: Creates a **Pearson correlation matrix** to understand the similarity between all movies.
- **Create Weighted Scores**: For a target user, it takes the movies they've rated and finds similar items from the correlation matrix. The similarity scores are weighted by the user's own ratings.
- **Recommend**: The system aggregates these weighted scores and suggests the top-ranked movies that the user has not yet seen.

---

## 🚀 How to Run

1.  **Clone the repository**:
    ```bash
    git clone [https://github.com/youssef-na03/recommender-system.git](https://github.com/youssef-na03/recommender-system.git)
    cd recommender-system
    ```
2.  **Install dependencies**:
    ```bash
    pip install pandas numpy requests notebook
    ```
3.  **Launch Jupyter Notebook**:
    ```bash
    jupyter notebook
    ```
4.  Open and run the `.ipynb` files.
    - `KNN.ipynb` downloads the data automatically.
    - `SimilarMovies.ipynb` requires the `ml-100k` dataset to be downloaded and placed in the project folder.
