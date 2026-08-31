# 🏡 Real Estate & Housing Price Prediction with TensorFlow

Bu repo, Kaggle üzerindeki **Real Estate and Housing Price Prediction** veri seti kullanılarak konut fiyatlarını tahmin etmek amacıyla geliştirilen uçtan uca regresyon analizi ve derin öğrenme modelleme çalışmasını içermektedir.

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/gulcansercekus-svg/Regresyon-analizi/blob/main/Real-EstateAndHousingPricePrediction.ipynb)

---

## 🎯 Projenin Amacı ve Özeti

Gayrimenkul fiyatlarını etkileyen çeşitli öznitelikleri (konum, yatak odası, banyo, park vb.) analiz ederek sürekli bir sayısal değer olan **konut fiyatını (Price)** en düşük hata payıyla tahmin eden bir Yapay Sinir Ağı (ANN) regresyon modeli geliştirmek.

Bu proje kapsamında:
- Kapsamlı Keşifçi Veri Analizi (EDA) ile fiyatı en çok etkileyen faktörlerin incelenmesi,
- Veri temizleme, aykırı değer yönetimi ve ölçeklendirme adımları,
- **TensorFlow & Keras** mimarisi kullanılarak çok katmanlı regresyon modelinin eğitilmesi ve optimize edilmesi gerçekleştirilmiştir.

---

## 🛠️ Kullanılan Teknolojiler & Kütüphaneler

- **Programlama Dili:** Python 3.x
- **Platform:** Google Colab
- **Kütüphaneler:**
  - `TensorFlow` & `Keras` (Regresyon Modeli, Katman Mimarisi, Optimizasyon)
  - `Pandas` & `NumPy` (Veri Manipülasyonu ve Sayısal İşlemler)
  - `Matplotlib` & `Seaborn` (Fiyat Dağılımları, Korelasyon Isı Haritası ve Loss Grafikleri)
  - `Scikit-Learn` (MinMaxScaler/StandardScaler, Train-Test Split, Regresyon Metrikleri)

---

## 📌 İş Akışı (Pipeline)

1. **Veri Ön İnceleme ve Keşifçi Veri Analizi (EDA):**
   - Eksik ve tutarsız değerlerin kontrolü.

2. **Veri Ön İşleme (Data Preprocessing):**
   - Sayısal değişkenlerin düzenlenmesi,
   - `Scikit-Learn` kullanılarak özelliklerin ölçeklendirilmesi (Scaling),
   - Veri setinin Eğitim (`Train`) ve Test (`Test`) kümelerine ayrılması.

3. **Yapay Sinir Ağı (ANN) Regresyon Mimarisi:**
   - **Girdi Katmanı:** Veri setindeki öznitelik sayısına göre yapılandırılmış giriş,
   - **Gizli Katmanlar:** `ReLU` aktivasyon fonksiyonlu `Dense` katmanları ve aşırı öğrenmeyi (overfitting) engellemek için `Dropout` / `EarlyStopping` mekanizması,
   - **Çıktı Katmanı:** Tek bir sürekli değer tahmin ettiği için aktivasyon fonksiyonsuz tek nöronlu `Dense(1)`.

4. **Model Derleme ve Optimizasyon:**
   - **Kayıp Fonksiyonu (Loss):** `MSE` (Mean Squared Error) / `MAE` (Mean Absolute Error) / `R2 Score` 
   - **Optimizatör:** `Adam`

---

## 📊 Değerlendirme ve Sonuçlar

Modelin eğitim ve test aşamalarındaki kayıp grafikleri incelenmiş, test verisi üzerindeki tahmin performansı aşağıdaki metriklerle ölçülmüştür:

- **MAE (Mean Absolute Error):** 790,726.36
- **MSE / RMSE (Root Mean Squared Error):** 1,042,764.59
- **$R^2$ Scoru (Belirleme Kaatsayısı):** 0.5332
- **Eğitim vs. Doğrulama Kaybı (Loss Curves):** Modelin öğrenme eğrileri görselleştirilerek aşırı öğrenme durumu kontrol edilmiştir.

---

## 🚀 Çalıştırma

Projeyi doğrudan tarayıcı üzerinden çalıştırmak için sayfanın başındaki **"Open In Colab"** rozetine tıklayabilir veya repoyu yerel ortamınıza klonlayabilirsiniz:

```bash
git clone [https://github.com/](https://github.com/)gulcansercekus-svg/Regresyon-analizi.git
