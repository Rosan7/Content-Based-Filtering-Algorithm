# 🎬 Content-Based Movie Recommender System

A machine learning project that implements a **content-based filtering algorithm** to recommend movies to users based on item features such as genres, cast, and director. Built using **Pandas**, **TensorFlow**, **Scikit-learn**, and **NumPy**.

---

## 📌 Features

- Content-based filtering using movie metadata  
- Neural network model to learn user preferences  
- Preprocessing and scaling of user/item features  
- Integration of custom datasets with CSV parsing  
- Cosine similarity and vector-based recommendation  

---

## 🛠️ Technologies Used

- **Python**
- **Pandas** – for data preprocessing  
- **NumPy** – numerical operations  
- **TensorFlow / Keras** – neural network modeling  
- **Scikit-learn** – preprocessing and train-test split  
- **CSV & Pickle** – for reading datasets and storing models  

---

## 📂 Dataset Structure

Located in `./sample_data/`:
- `content_item_train.csv` – Movie feature data  
- `content_user_train.csv` – User feature data  
- `content_y_train.csv` – Training labels (ratings or preferences)  
- `content_item_vecs.csv` – Precomputed item vectors  
- `content_movie_list.csv` – Movie metadata (titles, IDs)
---

## ⚙️ How It Works

1. **Data Loading:**  
   CSV files are loaded and parsed using `pandas` and `csv` module.

2. **Feature Preprocessing:**  
   Scaled using `StandardScaler` and `MinMaxScaler` for uniform input distribution.

3. **Model Architecture:**  
   A feedforward neural network is built using TensorFlow’s `Model` API.

4. **Training:**  
   Combined user-item features are fed into the model to learn the likelihood of user interest.

5. **Recommendation:**  
   After training, the system recommends movies based on content similarity and learned preferences.

---

## 🚀 Getting Started

### Prerequisites
- Python 3.7+
- TensorFlow
- pandas
- numpy
- scikit-learn

### Installation
```bash
git clone https://github.com/your-username/content-based-movie-recommender.git
cd content-based-movie-recommender
pip install -r requirements.txt
Run
bash
Copy
Edit
python content_based_model.py
(Or run the Jupyter Notebook ContentBasedFilteringAlgorithm.ipynb)

📊 Output
Trained model recommendations based on user content features

Accuracy or loss evaluation on the test set

Similar movies based on learned vector space

📈 Sample Neural Network Architecture
Input: Concatenated user and item features

Dense Layer (128 units, ReLU)

Dropout Layer

Dense Layer (64 units, ReLU)

Output Layer (Sigmoid or regression based on target)
