# 🧠 Clinical Note Segmentation and Clustering from MIMIC-III

This project explores the segmentation, embedding, and clustering of clinical notes from the **MIMIC-III** dataset, with a focus on **radiology** and **nursing notes**. We apply **document embeddings** using models like **BioClinicalBERT**, and perform **unsupervised clustering** (Hierarchical and TDA-based) to uncover patterns in clinical documentation.

---

## 🚀 Project Goals

- 📄 **Clean and preprocess** clinical notes (e.g., Nursing, Radiology)
- 🤖 **Generate embeddings** using Doc2Vec, TF-IDF, and BioClinicalBERT
- 🧩 **Cluster note segments** using:
  - Hierarchical Agglomerative Clustering (`n_clusters=50`)
  - Topological Data Analysis (TDA) via the Mapper algorithm
- 📊 **Visualize and analyze** document structure and thematic similarity

---

## 🛠️ Tools & Techniques

- **BioClinicalBERT** for contextual embeddings
- **Doc2Vec**, **TF-IDF** for vector representations
- **AgglomerativeClustering** from `sklearn` (bottom-up hierarchical clustering)
- **Mapper algorithm** from TDA for topological clustering
- **UMAP**, **t-SNE** for visualization
- **MIMIC-III** as the source of clinical notes

---

## 🗂️ Project Structure

```
data-engineering-project/
├── data/               # Raw and processed data (MIMIC III)
├── note_extraction/    # Jupyter notebooks for data cleaning and analysis
│   ├── exploratary_data_analysis.ipynb      # Analyze the entire MIMIC III note dataset
│   ├── radiology_classification.ipynb       # Classification of radiology notes into Head CT, Chest X-ray, and Abdomen CT
│   ├── create_segments.ipynb                # Segmenting the notes (e.g., Nursing) / Preprocessing
│   ├── train_vectors.ipynb                  # Train vectors (Doc2Vec and TF-IDF) for note segments
│   ├── vectors_for_cluster.ipynb            # Process/Save embeddings for clustering
│   ├── clustring_from_embedding.ipynb       # Clustering using Agglomerative Clustering
│   ├── clustring_from_embedding_tda.ipynb   # Clustering using Mapper (TDA)
├── README.md           # Project documentation (you're here!)
```

---

## 📌 How to Use

1. **Prepare the environment**:
    - Install required libraries:
    - Ensure you have access to the MIMIC-III dataset and place NOTEEVENTS.csv it in the `data/` directory.

2. **Run notebooks in order** (recommended path):
   - `exploratary_data_analysis.ipynb`
   - `create_segments.ipynb`
   - `train_vectors.ipynb`
   - `vectors_for_cluster.ipynb`
   - `clustring_from_embedding.ipynb` or `clustring_from_embedding_tda.ipynb`

3. **Explore clustering results** using visualization tools like UMAP or t-SNE.

---

## 📚 Dataset

- **MIMIC-III** clinical notes: freely available upon credentialed access via PhysioNet
- Note categories include:
  - Radiology
  - Nursing
  - Physician
  - Discharge summaries
  - and more...

---

## 🤝 Acknowledgments

- MIT's **MIMIC-III** team for the dataset
- HuggingFace for hosting **BioClinicalBERT**
- Scikit-learn and Kepler Mapper libraries

---
