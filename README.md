# Customer Segmentation Analysis using K-Means Clustering on Mall Customer Data

## Project Overview

This project focuses on performing customer segmentation using the K-Means clustering algorithm on a Mall Customer dataset. The primary goal is to group customers into distinct segments based on their `Annual Income` and `Spending Score`. This segmentation can help businesses understand their customer base better and develop targeted marketing strategies.

## Dataset

The dataset used for this project is `Mall_Customers.csv`. It contains customer information including `CustomerID`, `Gender`, `Age`, `Annual Income (k$)`, and `Spending Score (1-100)`.

## Features Used

For the K-Means clustering, the following features were selected:

  - `Annual Income (k$)`: Customer's annual income in thousands of dollars.
  - `Spending Score (1-100)`: A score assigned by the mall based on customer behavior and spending habits (1-100).

These features were chosen as they are most indicative of spending patterns and financial capacity, which are crucial for customer segmentation.

## Methodology

The project employs the K-Means clustering algorithm, a popular unsupervised machine learning technique.

1.  **Data Loading and Preprocessing**: The dataset is loaded, and relevant features (`Annual Income (k$)`, `Spending Score (1-100)`) are selected. Data is then scaled using `StandardScaler` to ensure that features with larger values do not dominate the clustering process.
2.  **Optimal K Determination (Elbow Method)**: The Elbow Method is used to identify the optimal number of clusters (`K`). This involves plotting the Within-Cluster Sum of Squares (WCSS) against the number of clusters and looking for the "elbow point" where the rate of decrease in WCSS significantly slows down.
3.  **K-Means Model Training**: The K-Means algorithm is trained on the scaled data with the determined optimal `K`.
4.  **Cluster Assignment**: Each customer is assigned a cluster label.
5.  **Cluster Visualization**: The clusters are visualized using scatter plots, with each cluster represented by a different color. Cluster centroids are also marked.
6.  **Clustering Evaluation**: The Silhouette Score is used to evaluate the quality of the clustering. A higher Silhouette Score indicates better-defined clusters.
7.  **Cluster Analysis**: The characteristics of each cluster (e.g., average age, income, spending score, gender distribution) are analyzed to understand the different customer segments.

## Key Steps

The Python script performs the following operations:

  - Loads the `Mall_Customers.csv` dataset.
  - Selects 'Annual Income (k$)' and 'Spending Score (1-100)' for clustering.
  - Scales the selected features.
  - Applies the Elbow Method to determine the optimal number of clusters.
  - Performs K-Means clustering with the optimal `K`.
  - Adds the assigned cluster labels back to the original DataFrame.
  - Visualizes the clusters using `matplotlib` and `seaborn`.
  - Calculates and prints the Silhouette Score.
  - Analyzes and summarizes the characteristics of each cluster.

## Results and Insights

The K-Means clustering typically identifies 5 distinct customer segments based on their income and spending habits. For example, these segments often include:

  - **High Income, High Spending**: Customers who earn and spend a lot (premium customers).
  - **High Income, Low Spending**: Customers with high income but low spending (potential to target with luxury items).
  - **Mid Income, Mid Spending**: Average customers.
  - **Low Income, High Spending**: Customers with lower income but high spending (e.g., impulse buyers, trendy items).
  - **Low Income, Low Spending**: Frugal customers.

These insights are crucial for tailoring marketing campaigns, product placement, and customer service strategies.

## How to Run

This project is designed to be easily runnable in Google Colab.

1.  **Open in Google Colab:** Click on the "Open in Colab" badge (if provided, otherwise create a new Colab notebook).
2.  **Copy the code:** Copy the entire Python code from the project file (`your_script_name.py` or directly from this README's code block if preferred) into a Colab cell.
3.  **Run the cells:** Execute the cells sequentially. The dataset will be loaded directly from the provided URL.

**Alternatively, for local execution:**

1.  **Clone the repository:**
    ```bash
    git clone https://github.com/SiddardhaShayini/Customer-Segmentation-Analysis-using-K-Means-Clustering-on-Mall-Customer-Data.git
    cd Customer-Segmentation-Analysis-using-K-Means-Clustering-on-Mall-Customer-Data
    ```
2.  **Install dependencies:**
    ```bash
    pip install pandas scikit-learn matplotlib seaborn
    ```
## Libraries Used

  - **Pandas**: For data manipulation and analysis.
  - **NumPy**: For numerical operations.
  - **Matplotlib**: For creating static, animated, and interactive visualizations.
  - **Seaborn**: For statistical data visualization, built on Matplotlib.
  - **Scikit-learn**: For machine learning algorithms (K-Means, StandardScaler, PCA, Silhouette Score).

## Visualizations

The project generates several plots to aid understanding:

  - **Raw Data Distribution**: A scatter plot showing `Annual Income` vs. `Spending Score` before clustering.
  - **Elbow Method Plot**: Displays the WCSS for different numbers of clusters to help identify the optimal `K`.
  - **K-Means Clusters Plot**: A scatter plot showing the data points colored by their assigned cluster, with cluster centroids marked.
  - **Average Spending Score per Cluster**: Bar chart showing the average spending score for each identified cluster.
  - **Average Annual Income per Cluster**: Bar chart showing the average annual income for each identified cluster.
  - **Gender Distribution Across Clusters**: Stacked bar chart illustrating the male/female breakdown within each cluster.

-----

## 🙋‍♂️ Author

**Siddardha Shayini**  

---
