# Analyzing Business Integrity and Consumer Trends

## Overview
This project investigates the presence of fraudulent reviews and suspicious business activity in the digital marketplace using unsupervised machine learning. By analyzing a large-scale review dataset (10M+ records) alongside business metadata, the goal is to detect manipulated ratings and fake reviews. Techniques such as Isolation Forest, K-Means, DBSCAN, and LDA are used to segment businesses, detect anomalies, and identify suspicious text patterns.

## Course Information
- **Course**: BA820 - Unsupervised Machine Learning, Boston University  
- **Team Members**: Quan Nguyen, Ruoxian Zhang, Yiyou Chen, Phunsok Norboo

## Dataset
We used two datasets from the UC San Diego McAuley Lab:
- **Review Dataset**: Over 10.4 million records, including ratings, review text, and business responses.
- **Metadata Dataset**: Contains business attributes like categories, location, and review counts.

The datasets were merged on `gmap_id`. Missing values were dropped or filled, and both numerical and textual data were cleaned, standardized, and transformed for modeling.

## Installation
1. Clone the repository:
```bash
git clone https://github.com/git-qmn/Review-Fraud-Detection-BA820-Group6.git
```
2. Install dependencies:
```bash
pip install -r requirements.txt
```
3. Run the Jupyter Notebook:
```bash
jupyter notebook
```

## Usage
- Open the notebook(s) and execute each cell sequentially.
- Modify parameters in model sections to explore different clusterings or anomaly detection results.

## Methodology
- **K-Means Clustering**: Used to segment businesses and detect abnormal patterns (k=3 selected).
- **DBSCAN**: Spatial clustering based on reprojected coordinates and fine-tuned parameters.
- **LDA (Topic Modeling)**: Used stratified sampling, coherence scoring, and cosine similarity to uncover themes in reviews and responses.
- **Isolation Forest**: Applied for anomaly detection, including text-based similarity to detect repetitive/fake reviews.

## Challenges
- High RAM usage required data sampling (1M–2M rows).
- Computational inefficiency of text similarity and LDA led to technique changes (e.g., Gensim → Scikit-Learn).
- False positives from franchises with naturally similar reviews.

## Contribution
Each member contributed equally across Milestones 1 & 2:
- **Yiyou**: HDBSCAN, K-Means rework, DBSCAN tuning
- **Ruoxian**: K-Means, preprocessing, DBSCAN refinement
- **Phunsok**: Isolation Forest tuning, LDA, dataset merging
- **Quan**: LDA optimization, cosine similarity, Isolation Forest scoring

## Contact
For questions or suggestions, reach out via email at [qmn@bu.edu](mailto:qmn@bu.edu).

## GitHub Repository
[GitHub - BA820-Group6](https://github.com/yycyy0722/BA820-Group6/tree/main)

