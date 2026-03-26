# 🎬 Movie Recommender System (kNN)
## 📌 Overview

This project implements a k-Nearest Neighbors (kNN) based movie recommender system that identifies the most similar movies to a given query.

Given a movie (in this case, “The Post”), the model returns the Top 5 most similar movies based on genre and IMDB rating.

## 🎯 Objective

To build a recommendation engine that answers:

“Given a movie, what are the 5 most similar movies?”
## 🛠️ Technologies Used
- Python
- Pandas
- NumPy
- Scikit-learn
    - NearestNeighbors
    - StandardScaler
## 📁 How to Run
1. Clone the repository
2. Open the Jupyter Notebook
3. Run all cells to reproduce results
## 📊 Dataset
- Source: UCI / IMDb subset (provided via course repository)
- Size: 30 movies
- Features:
  - IMDB Rating (continuous)
  - Genre indicators (binary):
    - Biography, Drama, Thriller, Comedy, Crime, Mystery, History
## ⚙️ Methodology
1. Data Preparation
Removed non-numeric columns:
   - Movie ID
   - Movie Name
   - Label
Selected relevant features for similarity computation
2. Feature Scaling
   - Applied StandardScaler to normalize features
   - Prevents IMDB ratings from dominating binary genre variables
3. Model Selection
   - Algorithm: k-Nearest Neighbors (kNN)
   - Search Method: Brute Force
   - Distance Metric: Euclidean Distance

Why?
   - Small dataset → brute force is efficient and exact
   - Numeric feature space → Euclidean distance is appropriate
## 🔍 Query Movie

“The Post”

- IMDB Rating: 7.2
- Genres:
  - Biography: Yes
  - Drama: Yes
  - History: Yes
  - Thriller: No
  - Comedy: No
  - Crime: No
  - Mystery: No
## ⭐ Results

Top 5 most similar movies:

1. 12 Years a Slave (distance: 1.374)
7. Hacksaw Ridge (distance: 1.527)
8. Queen of Katwe (distance: 3.347)
9. The Wind Rises (distance: 3.457)
10. A Beautiful Mind (distance: 3.666)
    
## 🧠 Insights
Recommended movies share strong similarity in:
  - Biography Genres
  - Drama Genres
  - IMDB ratings
The model effectively captures both:
  - Thematic similarity (genres)
  - Quality similarity (ratings)
## ⚠️ Limitations
Does not consider:
  - Actors
  - Directors
  - Plot/themes
Similarity is based only on genres and ratings
## 🚀 Future Improvements
- Incorporate additional features (cast, director, keywords)
- Scale to larger datasets using optimized search methods
