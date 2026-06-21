# Netflix İçerik Sınıflandırma Projesi (Vize & Final Ödevi)

Bu proje, Netflix platformundaki film ve dizilerin analizini ve makine öğrenmesi
ile sınıflandırılmasını kapsayan uçtan uca bir çalışmadır.

---

## Projenin Amacı

Netflix veri seti üzerinde önce keşifsel veri analizi (EDA) yapılmış, ardından
bir içeriğin **Film mi yoksa Dizi mi** olduğunu tahmin eden bir sınıflandırma
modeli kurulmuştur.

---

## Neler Yaptım?

### Aşama 1 & 2 — Veri Analizi ve Ön İşleme (Vize)
- Eksik verileri analiz edip uygun değerlerle doldurdum
- Matplotlib ve Seaborn ile içerik türleri, üretim yapan ilk 10 ülke
  ve izleyici kitlesi dağılımını görselleştirdim
- Eklenme tarihlerinden yıl bilgilerini ayıklayarak yeni özellikler türettim

### Aşama 3 — Model Kurma (Final)
- **Hedef değişken:** `type` (Movie = 1, TV Show = 0)
- Kullanılan özellikler: `release_year`, `duration_val`, `genre_count`, `rating_enc`
- Kurulan modeller:
  - Karar Ağacı (Decision Tree)
  - Rastgele Orman (Random Forest)

### Aşama 4 — Model Değerlendirme (Final)
- Metrikler: Accuracy, Precision, Recall, F1 Skoru
- Confusion Matrix görselleştirmeleri
- Model karşılaştırması ve özellik önem analizi

---

## Sonuçların Değerlendirilmesi

İki model karşılaştırıldığında **Random Forest**, Karar Ağacı'na kıyasla daha
yüksek Accuracy ve F1 Skoru elde etmiştir. `duration_val` (içerik süresi)
en belirleyici özellik olarak öne çıkmıştır; filmler dizilere göre çok daha
uzun süreye sahip olduğundan model bu özelliği güçlü biçimde kullanmaktadır.

---

## Kullanılan Araçlar

- **Dil:** Python  
- **Kütüphaneler:** Pandas, NumPy, Matplotlib, Seaborn, Scikit-learn  
- **Platform:** Kaggle  

---

## Bağlantılar

- 📓 Notebook: https://www.kaggle.com/code/kardelentula/netflix-eda  
- 📦 Veri Seti: https://www.kaggle.com/datasets/shivamb/netflix-shows  

---

*Bu proje akademik bir vize & final ödevi çalışmasıdır.*
