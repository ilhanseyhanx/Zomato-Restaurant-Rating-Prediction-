# Zomato Restaurant Rating Prediction / Zomato Restoran Puanı Tahmin Sistemi

## Türkçe

Bu proje, Zomato restoran veri setini kullanarak restoran yemek puanlarını tahmin etmeyi amaçlayan bir makine öğrenmesi çalışmasıdır. Üç farklı algoritmaya sahip model karşılaştırılmış ve performansları değerlendirilmiştir.

## English

This project aims to predict restaurant food ratings using the Zomato restaurant dataset through machine learning. Three different algorithmic models have been compared and their performances evaluated.

---

## 📊 Veri Seti

Kullanılan veri seti `enhanced_zomato_dataset_clean.csv` dosyasında bulunmaktadır ve aşağıdaki özelliklere sahiptir:

* **Toplam Kayıt:** 123,657 satır
* **Özellik Sayısı:** 26 sütun
* **Hedef Değişken:** `Dining_Rating` (Restoran yemek puanı)

## 📊 Dataset

The dataset used is stored in `enhanced_zomato_dataset_clean.csv` file with the following characteristics:

* **Total Records:** 123,657 rows
* **Feature Count:** 26 columns
* **Target Variable:** `Dining_Rating` (Restaurant food rating)

### Veri Seti Özellikleri:

* Restaurant_Name, Cuisine, City, Item_Name, Place_Name
* Dining_Rating, Delivery_Rating, Votes, Prices
* Best_Seller kategorileri
* Popülerlik ve ortalama değerlendirme metrikleri

### Dataset Features:

* Restaurant_Name, Cuisine, City, Item_Name, Place_Name
* Dining_Rating, Delivery_Rating, Votes, Prices
* Best_Seller categories
* Popularity and average rating metrics

---

## 🛠️ Kullanılan Teknolojiler

* **Python 3.11**
* **Pandas** - Veri manipülasyonu
* **NumPy** - Sayısal işlemler
* **Scikit-learn** - Makine öğrenmesi algoritmaları
* **XGBoost** - Gradient boosting
* **LightGBM** - Hızlı gradient boosting
* **TensorFlow/Keras** - Derin öğrenme

## 🛠️ Technologies Used

* **Python 3.11**
* **Pandas** - Data manipulation
* **NumPy** - Numerical operations
* **Scikit-learn** - Machine learning algorithms
* **XGBoost** - Gradient boosting
* **LightGBM** - Fast gradient boosting
* **TensorFlow/Keras** - Deep learning

---

## 🔧 Veri Ön İşleme

1. **Eksik Veri Kontrolü:** Veri setinde eksik veri bulunmamaktadır

2. **Kategori Kodlama:** Label Encoding kullanılarak kategorik değişkenler sayısal forma dönüştürülmüştür

3. **Özellik Normalizasyonu:** Keras modeli için StandardScaler kullanılmıştır

## 🔧 Data Preprocessing

1. **Missing Data Check:** No missing data found in the dataset

2. **Categorical Encoding:** Label Encoding used to convert categorical variables to numerical format

3. **Feature Normalization:** StandardScaler applied for Keras model

---

## 🤖 Kullanılan Modeller

1. **XGBoost Regressor**

```python
from xgboost import XGBRegressor
```

2. **LightGBM Regressor**

```python
from lightgbm import LGBMRegressor
```

3. **Keras Neural Network**

```python
from tensorflow.keras.models import Sequential
from tensorflow.keras.layers import Dense, Dropout
```

## 🤖 Models Used

1. **XGBoost Regressor**

```python
from xgboost import XGBRegressor
```

2. **LightGBM Regressor**

```python
from lightgbm import LGBMRegressor
```

3. **Keras Neural Network**

```python
from tensorflow.keras.models import Sequential
from tensorflow.keras.layers import Dense, Dropout
```

### Ağ Mimarisi:

* **Input Layer:** 24 nöron (özellik sayısı)
* **Hidden Layer 1:** 128 nöron + ReLU + Dropout(0.3)
* **Hidden Layer 2:** 64 nöron + ReLU + Dropout(0.3)
* **Output Layer:** 1 nöron (regresyon)

### Network Architecture:

* **Input Layer:** 24 neurons (number of features)
* **Hidden Layer 1:** 128 neurons + ReLU + Dropout(0.3)
* **Hidden Layer 2:** 64 neurons + ReLU + Dropout(0.3)
* **Output Layer:** 1 neuron (regression)

---

## 📈 Model Performansları

### XGBoost

* **R² Score:** 0.9999992021450141
* **MSE:** 9.82e-08
* **MAE:** 0.00021

### LightGBM

* **R² Score:** 0.9999393212260673
* **MSE:** 7.47e-06
* **MAE:** 0.0019

### Keras Neural Network

* **R² Score:** 0.9857921242610077
* **MSE:** 0.0017
* **MAE:** 0.0235

## 📈 Model Performance

### XGBoost

* **R² Score:** 0.9999992021450141
* **MSE:** 9.82e-08
* **MAE:** 0.00021

### LightGBM

* **R² Score:** 0.9999393212260673
* **MSE:** 7.47e-06
* **MAE:** 0.0019

### Keras Neural Network

* **R² Score:** 0.9857921242610077
* **MSE:** 0.0017
* **MAE:** 0.0235

---

## 🏆 Sonuçlar

En iyi performansı **XGBoost** modeli göstermiştir. Neredeyse mükemmel bir R² skoru (0.999999) ile restoran puanlarını tahmin edebilmektedir. LightGBM de benzer şekilde çok yüksek performans gösterirken, Keras modeli daha düşük ancak yine de oldukça başarılı sonuçlar vermiştir.

## 🏆 Results

The **XGBoost** model demonstrated the best performance with an almost perfect R² score (0.999999) for predicting restaurant ratings. LightGBM also showed similarly high performance, while the Keras model delivered lower but still quite successful results.

---

## 📄 License / Lisans

This project is licensed under the MIT License / Bu proje MIT lisansı altında sunulmaktadır.
