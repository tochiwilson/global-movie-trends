# Global Movie Trends Analysis with PySpark

![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![Spark](https://img.shields.io/badge/Apache%20Spark-PySpark-orange)
![License](https://img.shields.io/badge/License-MIT-green)

A data science project analyzing global movie production trends using **Apache Spark**. This project explores the relationship between a country's population and its movie output, both in terms of **quantity** (films per capita) and **quality** (IMDb Top 1000 representation).

## 📊 Key Features & Insights
This project demonstrates several advanced Data Engineering & Analysis techniques:

* **Data Cleaning:** Parsing complex JSON strings in the `production_countries` column using both **RDDs** (for unstructured data) and **DataFrames** (for structured processing).
* **Data Enrichment:** Joining three disparate datasets (Metadata, Population, Ratings) to normalize statistics.
* **Robustness:** Handling "dirty data" (malformed CSV rows) using regex, AST parsing, and type casting validation.
* **Spark SQL:** Demonstrating the use of SQL queries within the Spark environment for complex aggregations.
* **Visualization:**
    * Interactive Choropleth World Map using **Plotly**.
    * Statistical Bar Charts using **Seaborn**.
    * Interactive Dashboard using **ipywidgets**.

## 📂 Datasets & Project Structure
This project uses three open datasets from Kaggle.

> **⚠️ Note:** Due to Kaggle’s data license and file size limits, the CSV files are **not included in this repository**. You must download them manually.

### Required Folder Structure
To run the analysis successfully, you must create a `data` folder in the root of the project and organize the downloaded CSV files into specific subfolders as shown below. This structure is required for the relative paths in the code to work.

```text
global-movie-trends/
├── data/
│   ├── movies_dataset/
│   │   └── movies_metadata.csv
│   ├── imdb_top_1000/
│   │   └── IMDB top 1000.csv
│   └── population_by_country/
│       └── population_by_country_2020.csv
├── exploration.ipynb
└── README.md
```

### Download Links
Please download the datasets from the links below and place them in the folders mentioned above:

1.  **[The Movies Dataset](https://www.kaggle.com/datasets/rounakbanik/the-movies-dataset/data)**
    * *File:* `movies_metadata.csv`
2.  **[IMDb Top 1000 Movies](https://www.kaggle.com/datasets/omarhanyy/imdb-top-1000)**
    * *File:* `IMDB top 1000.csv`
3.  **[World Population by Country (2020)](https://www.kaggle.com/datasets/tanuprabhu/population-by-country-2020)**
    * *File:* `population_by_country_2020.csv`

## 🛠️ Installation & Setup

1.  **Clone the repository:**
    ```bash
    git clone [https://github.com/tochiwilson/global-movie-trends.git](https://github.com/tochiwilson/global-movie-trends.git)
    cd global-movie-trends
    ```

2.  **Install dependencies:**
    Ensure you have Python and Java (for Spark) installed. Then run:
    ```bash
    pip install pyspark pandas seaborn matplotlib plotly ipywidgets
    ```

3.  **Setup Data:**
    Follow the **Folder Structure** guide above. Create the `data/` folder and its subfolders, then place the CSV files inside.

4.  **Run the Analysis:**
    Open `exploration.ipynb` in Jupyter Notebook or VS Code.
    * Click `Kernel` -> `Restart & Run All` to execute the full pipeline.
    * Scroll to the bottom to see the interactive dashboard.

## 👤 Author
**Wilson Tochi Uduma** - Student Applied Computer Science: Artificial Intelligence

*Project for Data Visualization*