CryptoClustering-Machine Learning-CH19
# CryptoClustering

## **Overview**
This project applies **unsupervised machine learning** techniques to analyze **cryptocurrency market data**. The goal is to use **K-Means clustering** and **Principal Component Analysis (PCA)** to group cryptocurrencies based on **24-hour and 7-day price changes**.

## **Project Structure**
📂 CryptoClustering │── 📄 Crypto_Clustering.ipynb # Jupyter Notebook with full analysis │── 📄 crypto_market_data.csv # Dataset containing crypto price changes │── 📄 README.md # Project documentation │── 📂 Resources # Additional resources (if any)
## **Technologies Used**
- **Python**
- **Pandas** - Data manipulation
- **scikit-learn** - StandardScaler, KMeans, PCA
- **hvPlot** - Interactive visualization
- **Matplotlib** - Data plotting

## **Analysis Workflow**
### **1. Load and Explore Data**
- Load `crypto_market_data.csv` into a DataFrame.
- Generate summary statistics.
- Plot data to understand trends.

### **2. Data Preprocessing**
- Use `StandardScaler()` from `scikit-learn` to normalize the data.
- Create a new DataFrame with scaled values.
- Set `"coin_id"` as the index.

### **3. Find the Best K Value (Elbow Method)**
- Compute **inertia values** for `k = 1 to 11`.
- Plot **Elbow Curve** to identify the optimal cluster count.

### **4. Cluster Cryptocurrencies using K-Means**
- Initialize and fit the K-Means model using the best \( k \).
- Predict clusters for the cryptocurrencies.
- Create a scatter plot showing clusters (`price_change_percentage_24h` vs. `price_change_percentage_7d`).

### **5. Optimize Clusters using PCA**
- Reduce dimensions to **3 principal components**.
- Retrieve **explained variance** to analyze information retention.
- Create a new DataFrame with PCA data.

### **6. Find the Best K Value (PCA Data)**
- Use **Elbow Method** again on PCA data.
- Compare results with the original dataset.

### **7. Cluster Cryptocurrencies using PCA Data**
- Perform K-Means clustering on PCA-reduced features.
- Visualize clusters (`PC1` vs. `PC2`).

### **8. Compare Original vs. PCA Results**
- Create **composite plots**:
  - **Elbow Curve (Original vs. PCA)**
  - **Cluster Plots (Original vs. PCA)**

## **Key Findings**
- **Best \( k \) Value**:
  - **Original Data**: \( k = X \) (Replace with your observed value)
  - **PCA Data**: \( k = Y \) (Replace with your observed value)
  - **Impact of PCA**: PCA reduces dimensionality while retaining significant variance.

## **Instructions to Run**
1. Clone the repository:
   ```sh
   git clone https://github.com/Neda2020/CryptoClustering.git
Navigate to the project directory:
sh
Copy
Edit
cd CryptoClustering
Install dependencies:
sh
Copy
Edit
pip install pandas scikit-learn hvplot matplotlib
Run the Jupyter Notebook:
sh
Copy
Edit
jupyter notebook Crypto_Clustering.ipynb   
   
