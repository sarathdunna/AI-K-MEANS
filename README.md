# K-Means: Choosing the Best k with the Silhouette Score

Finds the best number of clusters **k** for K-Means on the California housing dataset. It tries every k in a range you give and keeps the one with the highest **silhouette coefficient**.

## How it works

For each `k` from `min_k` to `max_k`:
1. Fit `KMeans(n_clusters=k)` on the dataset.
2. Compute the silhouette score of the resulting labels. The score ranges from -1 to 1; higher means tighter, better-separated clusters.
3. Keep the k with the best score.

## Run it

```bash
pip install pandas scikit-learn
python KMEANS.py 3 6
```

Output for `3 6`: **3**

`min_k` must be at least 2 (the silhouette score needs two or more clusters) and `max_k` must be at least `min_k`. Otherwise the script prints `Invalid input`.

## Files

| File | Description |
|---|---|
| `KMEANS.py` | Silhouette-based search for the best k |
| `housing.csv` | California housing data: median income, house age, rooms, population, location, value |
| `K-MEANS.pdf` | Write-up |

**Tech:** Python, pandas, scikit-learn
