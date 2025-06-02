# 📚 Collaborative Filtering with PySpark

## 📌 Objective

This project implements **Collaborative Filtering** for recommendation systems using **PySpark**. The notebook demonstrates methods to load, preprocess, and split data, and apply user-item collaborative filtering techniques for predicting user preferences.

---

## ⚙️ Technologies & Tools

- **PySpark** (Apache Spark with Python)
- **Google Colab** (for running the notebook)
- **Pandas**, **NumPy**, and **Matplotlib** (for analysis and visualization)
- **RegressionEvaluator** (for evaluating model performance)

---

## 🗂️ Dataset

- Input file: `ratings2k.csv`
- Columns include:
  - `index`: Unique identifier for each row
  - `user`: User ID
  - `item`: Item ID
  - `rating`: Rating given by the user to the item

---

## 🚀 Workflow

### Step 1: Data Loading
- Load the dataset (`ratings2k.csv`) using PySpark's `read.csv` method.
- Validate the schema and preview the dataset.

### Step 2: Data Preprocessing
- Perform user-wise stratified splits:
  - Assign row numbers to ratings per user for random ordering.
  - Stratify data into training (80%) and testing (20%) sets, ensuring each user has at least one test entry.

### Step 3: Model Training
- Apply **Matrix Factorization** using ALS (Alternating Least Squares) for collaborative filtering.
- Optimize the model with hyperparameters like:
  - Number of latent factors
  - Regularization parameter
  - Iteration count

### Step 4: Model Evaluation
- Evaluate performance using:
  - **Root Mean Squared Error (RMSE)**
  - **Mean Absolute Error (MAE)**

### Step 5: Recommendation Generation
- Generate personalized recommendations for users and evaluate them.

---

## 💻 How to Run

1. Ensure **Google Colab** is set up with `pyspark` installed:
   ```bash
   pip install pyspark
   ```

2. Upload the dataset `ratings2k.csv` to the Colab workspace or provide its path.

3. Open and execute the notebook `Colaborative_Filtering.ipynb`.

4. Modify hyperparameters (if necessary) and run all cells to train the model and evaluate results.

---

## 📎 Project Structure

```
📦 Collaborative Filtering
├── Colaborative_Filtering.ipynb  # Main notebook implementing collaborative filtering
├── ratings2k.csv                # Input dataset (required for execution)
├── README.md                    # Project description
```

---

## 🚀 Features & Improvements

- User-wise stratified splitting ensures fairness in training and evaluation.
- PySpark implementation supports scalability for large datasets.
- Advanced techniques like ALS and evaluation metrics for robust model performance.

---

## 📬 Contact

For questions or suggestions, feel free to open an issue or contact the project maintainer.

Email: haidangforworks@gmail.com
