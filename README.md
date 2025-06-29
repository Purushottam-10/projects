
# 🎵 Spotify Music Recommendation System

This project applies clustering techniques to group similar songs based on their audio features and provides song recommendations accordingly. It uses both **K-Means** and **DBSCAN** clustering algorithms to analyze the Spotify dataset and suggests similar tracks.

---

## 📦 Dataset

The project uses the **SpotifyFeatures.csv** dataset, which contains various audio features for a large number of songs.

### Selected Features:
- Danceability  
- Energy  
- Loudness  
- Speechiness  
- Acousticness  
- Instrumentalness  
- Liveness  
- Valence  
- Tempo  

---

## ⚙️ Technologies & Libraries

- Python  
- Pandas & NumPy (Data Handling)  
- Matplotlib & Seaborn (Visualization)  
- Scikit-learn (Clustering & Evaluation)  

---

## 🛠️ Project Workflow

1. **Data Preprocessing**
   - Load the dataset
   - Handle missing values
   - Select relevant audio features
   - Standardize the features for better clustering performance

2. **K-Means Clustering**
   - Find the optimal number of clusters using the Silhouette Score
   - Apply K-Means with the best `K`
   - Evaluate using Silhouette Score and Davies-Bouldin Index

3. **DBSCAN Clustering**
   - Apply DBSCAN algorithm
   - Handle noise points
   - Evaluate clusters (excluding noise)

4. **Recommendation System**
   - Recommend 5 similar songs based on cluster membership
   - Supports both K-Means and DBSCAN methods for recommendations

---

## 📊 Evaluation Metrics

- **Silhouette Score**  
  Measures how well samples are clustered; higher is better.

- **Davies-Bouldin Index**  
  Measures cluster separation and compactness; lower is better.

---

## 💡 How to Use

1. Ensure `SpotifyFeatures.csv` is in the project directory.  
2. Run the Python script or Jupyter Notebook.  
3. Use the function `recommend_similar(song_index, method='KMeans')` to get similar songs.  

**Example:**

```python
recommend_similar(0, method='KMeans')  # Recommends songs similar to the song at index 0
```

You can also use:
```python
recommend_similar(5, method='DBSCAN')
```

---

## 🚀 Future Improvements

- Accept song names instead of index for recommendations  
- Integrate with a front-end for better user interaction  
- Experiment with additional clustering algorithms  
- Improve recommendation logic using popularity or genre filters  

---

## 📂 Project Structure

```
│  SpotifyFeatures.csv  
│  clustering_recommender.py / .ipynb  
│  README.md  
```

---

## 📝 License

This project is for educational purposes.

---

**Enjoy exploring and recommending music using unsupervised learning! 🎶**
