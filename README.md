## Data-Driven Insights: Warehouse, Clustering, Classification and Market Basket Analysis
```
This repository contains the submissions for the **DSA 2040 End Semester Practical Exam, covering Data Warehousing, K-Means Clustering, Classification, and Association Rule Mining. The project is organized into modular folders for clarity.
This is the General Overview specific reports are porvided in each folder.
```

## **Folder Overview**

```
DSA_2040_PRACTICAL_EXAM_AMBACHO_550/
├── Data_Mining/
│   ├── Data/                   # Preprocessed Iris dataset, synthetic transactional data
│   ├── scripts/
│   ├── Classification and Association Rule Mining/
│   ├── Clustering            # classification_iris.py, mining_iris_basket.py
│  
│ 
├── Data_Warehousing/
│   ├── data/                   # Raw or synthetic retail data
│   ├── design/                 # schema_diagram.png
│   ├── ETL/                    # etl scripts (etl_retail.py)
│   ├── images/                 # ETL or OLAP result plots
│   ├── OLAP/                   # SQL queries for roll-up, drill-down, slice
│   ├── reports/                # ETL and OLAP analysis
│   └── scripts/                # SQL scripts or additional Python scripts
├── README.md
└── requirements.txt
```

---

## **Data Warehousing**

* **ETL**: `etl_retail.py` handles extraction, transformation, and load into SQLite (`retail_dw.db`).
* **Schema**: `schema_diagram.png` shows the star schema design. Include in report under *Schema Design*.
## Star Schema
<img width="963" height="673" alt="image" src="https://github.com/user-attachments/assets/f16a6544-fec6-4e04-9512-8e909eb63152" />

I chose the Star Schema because it is simpler and denormalized, which allows for faster query performance in OLAP systems. It reduces the number of joins needed compared to a Snowflake Schema, making it easier for analysts to write and understand queries. This design also improves query execution speed and supports intuitive reporting and visualization.

  
* **OLAP Queries**: Located in `Data_Warehousing/OLAP/`. Visualize query results and save images in `Data_Warehousing/images/`.

---

## **K-Means Clustering**

* **Scripts**: `clustering_iris.py`
* **Dataset**: `Cleaned_iris_data.csv` in `Data_Mining/data/`
* **Visualizations**:

  * `elbow_curve.png` → Optimal K=3
  ### `cluster_scatter.png` → Scatter plots of clusters
  <img width="702" height="547" alt="image" src="https://github.com/user-attachments/assets/9e5d7ee7-3846-44e0-8f0a-a3b8654acdd8" />
Clustering Accuracy: 0.833
* **Analysis**: Discuss cluster quality, misclassifications, and applications. Include visuals in `Report/Report_Kmean_clustering.md`.

---

## **Classification & Association Rule Mining**

* **Classification**:

  * Decision Tree and KNN (k=5) in `scripts/`
 <img width="950" height="636" alt="image" src="https://github.com/user-attachments/assets/956ac3bd-9ff6-4e06-9331-a92e2f4f764a" />
 - Decision Tree Performance:
 - Accuracy: 1.00
 - Precision: 1.00
 - Recall: 1.00
 - F1-score: 1.00

* **Association Rule Mining**:

  * Synthetic transactional data generated in `scripts/`
  * Apriori applied; top 5 rules saved in `rules_top5.png`
<img width="1189" height="789" alt="image" src="https://github.com/user-attachments/assets/cf77f495-18be-4046-ab0c-f4b8817cb87a" />

Rule: {chips} → {beer} (Lift=5, Confidence=100%)

Retail Actions:

Place together – Same aisle or endcap display.

Bundle deals – "Buy chips, get beer discount."

Restock jointly – Avoid out-of-stock on either.

Recommend online – Suggest beer when chips are in cart.

Why?

Perfect association (always bought together).

Ideal for parties/game nights.

Much stronger than common pairs like milk/bread.

Profit Tip: Capitalize on this pair for promotions first!
---

## **Report**

* Include all plots and diagrams in `Report/` or as markdown embedded images.
* Sections: Introduction, Methodology, Results, Visualizations, Analysis, Conclusion.

---

## **Requirements**

* Python 3.x
* Packages: `pandas`, `numpy`, `matplotlib`, `seaborn`, `sklearn`, `mlxtend`
* Install via:

```bash
pip install -r requirements.txt
```

---


