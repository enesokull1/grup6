# grup6
# 🚦 Trafik Kazaları Üzerine Veri Analizi ve Makine Öğrenmesi Uygulaması (Türkiye, 2024)

##  Proje Açıklaması

Bu projede Türkiye'deki 2024 yılına ait trafik kazası verileri incelenmiş, çeşitli faktörlere göre ölümlü ve yaralanmalı kaza sayıları analiz edilmiş ve ölü/yara sayılarının tahmini için makine öğrenmesi modelleri geliştirilmiştir. Veri kaynağı olarak *TÜİK (Türkiye İstatistik Kurumu)* kullanılmakta, veriler .xls formatında TÜİK’ten alınarak analiz edilmiştir.

---

##  Kullanılan Veri Setleri

- İllere göre ölümlü ve yaralanmalı trafik kazaları
- Kusur türlerine göre kazalar (sürücü, yolcu, yaya vb.)
- Taşıt cinsine göre kazaya karışma ve sürücü kayıpları
- Yaş grubu ve cinsiyete göre kazazedeler
- Aylara ve gün ışığı durumuna göre kaza dağılımları

---

##  Kullanılan Yöntemler

###  Keşifsel Veri Analizi (EDA)
- En riskli iller, taşıt türleri ve kusur türleri analiz edildi
- Ölüm ve yaralanma oranları hesaplandı
- Pasta ve çubuk grafiklerle görselleştirme yapıldı

###  Veri Temizleme
- Pandas kullanılarak sütun isimleri düzenlendi
- NaN ve açıklama satırları ayıklandı
- Veri tipleri sayısala dönüştürüldü

###  Makine Öğrenmesi
- *Random Forest Regressor* ve *Linear Regression* algoritmaları kullanıldı
- Toplam Kaza, Araç Sayısı, Yaralı Sayısı gibi değişkenlerden:
  - *Ölü Sayısı (Toplam)* tahmin edildi
  - *Yaralı Sayısı* tahmin edildi

---

##  Model Performansı (Random Forest)

| Tahmin Hedefi         | MAE   | RMSE  | R² Skoru |
|-----------------------|-------|-------|----------|
| Ölü Sayısı (Toplam)   | 10.2  | 17.5  | 0.96     |
| Yaralı Sayısı               | 15.7  | 25.8  | 0.99     |

---

##  Özet Sonuçlar

- Kazaların büyük çoğunluğu sürücü kusurundan kaynaklanmaktadır (%90+).
- Motosiklet sürücüleri orantısal olarak en yüksek ölüm/yaralanma oranına sahiptir.
- Yaz aylarında kazalar artmakta, kış aylarında ölüm oranı daha yüksektir.
- Random Forest modeli ölü sayısını ve yaralı sayısını oldukça yüksek doğrulukla tahmin edebilmektedir.

---

##  Geliştiriciler

- *İkbal Akyol*  
- *Enes Çelikkol*


Sunum süresi: 7 dakikayı geçmeyecek şekilde ayarlanmıştır.
