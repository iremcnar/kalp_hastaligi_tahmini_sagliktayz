# 🏥 Sağlıkta Yapay Zeka: Kalp Hastalığı (Heart Disease) Tahmini

Bu proje, **Burdur Mehmet Akif Ersoy Üniversitesi** bünyesindeki **Sağlıkta Yapay Zeka** dersi uygulama çalışmaları kapsamında geliştirilmiştir. Projenin amacı, hastaların klinik bulgularını ve laboratuvar sonuçlarını analiz ederek kalp hastalığı varlığını önceden tahmin edebilen makine öğrenmesi modelleri geliştirmektir.

## 📌 Proje Özeti
Kalp hastalıkları (koroner arter hastalığı, aritmi vb.) erken teşhis edildiğinde müdahale şansı büyük oranda artmaktadır. Bu çalışmada, UCI Heart Disease veri seti kullanılarak hastaların sağlık verileri üzerinden sınıflandırma yapılmış ve farklı algoritmaların performansları karşılaştırılmıştır.

**Veri Seti:** [Heart Disease UCI](https://www.kaggle.com/datasets/mragpavank/heart-diseaseuci)

## 🛠️ Kullanılan Teknolojiler
- **Python** (Veri Bilimi Ekosistemi)
- **Pandas & NumPy** (Veri analizi ve işleme)
- **Matplotlib & Seaborn** (EDA ve görselleştirme)
- **Scikit-Learn** (Model eğitimi, topluluk öğrenmesi ve metrikler)

## 🚀 Proje Uygulama Adımları

### 1. Keşifsel Veri Analizi (EDA) ve Ön İşleme
- **Veri Analizi:** Yaş, cinsiyet, göğüs ağrısı tipi (cp), kolesterol ve kan basıncı gibi öznitelikler arasındaki ilişkiler görselleştirilmiştir.
- **Eksik Veri Yönetimi:** Veri setindeki eksik değerler kontrol edilerek temizlenmiştir.
- **Kategorik Veri Dönüştürme:** Kategorik değişkenler (Encoding) sayısal formatlara getirilmiştir.
- **Standartlaştırma:** Özelliklerin birbirine üstünlük sağlamaması için sayısal veriler `StandardScaler` ile ölçeklendirilmiştir.

### 2. Modelleme Yaklaşımları
Projede yüksek doğruluk ve genelleme kapasitesi elde etmek için şu algoritmalar kullanılmıştır:
- **K-Nearest Neighbors (KNN):** Benzerlik tabanlı sınıflandırma.
- **Random Forest (RF):** Karar ağaçlarından oluşan topluluk öğrenmesi (ensemble) yöntemi.
- **Voting Classifier:** KNN ve Random Forest modellerinin tahminlerini birleştirerek (çoğunluk oylaması - Hard Voting) en kararlı sonucu hedefleyen hibrit yaklaşım.

### 3. Performans ve Değerlendirme
- **Karışıklık Matrisi (Confusion Matrix):** Modelin Doğru Pozitif (TP) ve Yanlış Negatif (FN) oranları üzerinden performans analizi yapılmıştır.
- **Multiclass vs Multilabel Analizi:** Proje sonunda, hastalık evrelerinin tahmini (multiclass) ile birden fazla hastalığın aynı anda bulunması (multilabel) durumları arasındaki farklar teknik olarak incelenmiştir.

## 📊 Öne Çıkan Bulgular
- **Topluluk Öğrenmesi:** Voting Classifier yönteminin, tekil modellerin zayıf yanlarını kapatarak daha dengeli bir tahmin başarısı sunduğu gözlemlenmiştir.
- **Öznitelik Önemi:** Kalp hastalığı tahmininde göğüs ağrısı tipi (cp) ve maksimum kalp atış hızı (thalach) gibi değişkenlerin en yüksek ayırt ediciliğe sahip olduğu saptanmıştır.

## 📂 Dosya Yapısı
- `kalp_hastaligi_tahmini.ipynb`: Veri ön işleme, EDA, KNN, RF ve Voting Classifier modellerini içeren ana çalışma dosyası.
- `heart.csv`: Projede kullanılan klinik verileri içeren ham veri seti.

---
**Not:** Bu çalışma akademik bir uygulama olup, gerçek tıbbi tanılar için sadece uzman doktor görüşlerine başvurulmalıdır.
