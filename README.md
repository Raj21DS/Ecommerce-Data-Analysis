# 🛒 PySpark E-Commerce Data Analysis (theLook Dataset)

## 📌 Overview

This project demonstrates **end-to-end data analysis using PySpark** on the *theLook eCommerce dataset*. The goal is to simulate a real-world scenario where a data analyst processes transactional data to generate meaningful business insights.

---

## 🎯 Objectives

* Load and inspect large datasets using **Spark DataFrames**
* Perform **data cleaning and preprocessing**
* Apply **transformations and feature engineering**
* Execute **joins across multiple datasets**
* Generate **aggregations and business insights**
* Implement **Spark optimizations** (cache, broadcast joins, repartitioning)

---

## 📂 Dataset

The project uses four CSV files:

| File Name         | Description                   |
| ----------------- | ----------------------------- |
| `users.csv`       | Customer information          |
| `orders.csv`      | Order-level data              |
| `order_items.csv` | Item-level transactional data |
| `products.csv`    | Product details               |

---

## 🛠️ Tech Stack

* **PySpark**
* **Apache Spark DataFrame API**
* Python (Jupyter Notebook / Script)

---

## 🚀 Project Workflow

### 1. Data Loading & Inspection

* Initialize Spark session
* Load CSV files into DataFrames
* Inspect schema and sample data
* Perform row count checks

### 2. Data Cleaning

* Handle null values in key columns
* Remove invalid records
* Standardize categorical fields
* Convert numeric columns

### 3. Transformations

* Select relevant columns
* Create derived column: `price_bucket`

  * Low (<25)
  * Medium (25–75)
  * High (>75)
* Filter meaningful records
* Compute distinct counts

### 4. Data Joining

* Join datasets using:

  * `users.id = orders.user_id`
  * `orders.order_id = order_items.order_id`
  * `order_items.product_id = products.id`
* Create final dataset: `final_df`

### 5. Aggregations & Analysis

* Top categories by sales volume
* Top brands by revenue
* State-wise order and sales analysis
* Average sale price by category
* Order status distribution

---

## 📊 Key Business Insights

* 🏆 Top-performing state by sales
* 📦 Highest revenue-generating category
* 🏷️ Most popular brand
* 👥 Gender-based order trends
* 🛍️ Multi-item order patterns

---

## ⚡ Spark Optimizations

### 🔹 Caching

* Cached `final_df` to improve performance
* Helps reuse the dataset across multiple analyses without recomputation

### 🔹 Broadcast Join

* Used for joining small `products` dataset
* Reduces shuffle and improves performance

### 🔹 Repartitioning

* Repartitioned data by `state`
* Improves parallel processing and query performance

---

## 📁 Output

* Final dataset saved in **Parquet format**
* Partitioned by `state` for efficient querying


---

## 🧠 Learning Outcomes

By completing this project, you will gain hands-on experience in:

* Distributed data processing using Spark
* Real-world data engineering workflows
* Performance optimization techniques in big data


## 🤝 Contributing

Feel free to fork this repository and enhance the analysis!


