# 🏡 Airbnb Pazar Dinamikleri Analizi  
### Interactive Looker Studio Dashboard

Bu proje, **Google Looker Studio** kullanılarak hazırlanmış interaktif bir Airbnb pazar analizidir.  
Analizin odağında; **fiyatlama, doluluk (occupancy), müsaitlik (availability), değerlendirme skorları ve host davranışları** arasındaki ilişkiler yer almaktadır.

Bu çalışma, klasik Airbnb analizlerinden farklı olarak **talep–arz dengesi** ve **host yanıt davranışlarının** rezervasyon performansı üzerindeki etkisini ön plana çıkarmaktadır.

---

## 🎯 Proje Amacı

Bu proje aşağıdaki temel iş sorularına yanıt aramaktadır:

- Fiyat, doluluk ve müsaitlik metrikleri zaman içinde nasıl etkileşiyor?
- Host yanıt süresi (host_response_time) doluluk oranını gerçekten etkiliyor mu?
- Oda tipleri (room_type) fiyatlama gücü ve talep açısından nasıl ayrışıyor?
- Yüksek review score her zaman daha yüksek fiyat anlamına mı geliyor?
- Daha fazla kiralama yapan host profilleri hangi özelliklere sahip?

---

## 🛠 Kullanılan Araçlar & Teknolojiler

- **Google Looker Studio** – Interactive dashboard & data storytelling  
- **Google Sheets / BigQuery** – Data source ve agregasyon  
- **SQL** – Metric hesaplamaları ve dönüşümler  

---

## 📊 Dashboard Yapısı

Dashboard dört ana analiz katmanından oluşmaktadır:

---

### 1️⃣ Genel Pazar Görünümü (KPI’lar)

Öne çıkan metrikler:

- Ortalama oda fiyatı: **158 €**
- Ortalama review score: **4.67**
- Ortalama doluluk oranı: **~%76**
- Ortalama müsaitlik oranı: **~%24**

📌 **Yorum:**  
Pazar yapısı yüksek talep ve düşük müsaitlik ile karakterize edilmektedir.

---

### 2️⃣ Oda Tipi & Talep Analizi

- **Entire home/apt** ilanları pazarın büyük çoğunluğunu oluşturmakta (~%90) ve en yüksek fiyat seviyesine sahiptir
- **Shared room** ilanları düşük fiyata rağmen en yüksek doluluk oranlarını göstermektedir
- **Private room** segmenti fiyat–talep dengesi açısından orta konumda yer almaktadır

📌 **Insight:**  
Doluluk yalnızca fiyatla değil, **erişilebilirlik ve hizmet kalitesiyle** birlikte şekillenmektedir.

---

### 3️⃣ Zaman Bazlı Trendler (Price, Availability & Occupancy)

- Müsaitlik arttıkça doluluk oranı düşmektedir (ters yönlü ilişki)
- Fiyatlar ortalama seviyede stabil seyretmekle birlikte dönemsel artışlar göstermektedir
- Boş gün sayısı arttıkça talep zayıflamaktadır

📌 **Insight:**  
Availability, talep değişimini öngörmede **öncü gösterge** olarak kullanılabilir.

---

### 4️⃣ Host Davranışı & Performans Analizi

Bu analizde en güçlü sinyallerden biri host yanıt süresidir:

- **“Within an hour”** yanıt veren hostlar:
  - Daha yüksek doluluk oranına sahiptir
  - Daha fazla toplam kiralama yapmaktadır
  - Piyasa ortalamasına yakın fiyatlandırma uygular
- Yavaş yanıt veren hostlar, benzer fiyatlara rağmen daha düşük rezervasyon alır

📌 **Insight:**  
**Hızlı yanıt süresi**, agresif fiyatlamadan daha güçlü bir doluluk belirleyicisidir.

---

## 📈 Price vs Review Score Analizi

- **4.7 – 5.0** arası review score’a sahip ilanlar yüksek dolulukta yoğunlaşmaktadır
- Review score arttıkça fiyat artma eğilimindedir ancak bir doygunluk noktası vardır
- Aşırı yüksek fiyat, tek başına yüksek talep garantisi sağlamaz

📌 **Insight:**  
Review score bir **güven çarpanı**dır, doğrudan fiyatlama aracı değildir.

---

## 💡 Temel İş İçgörüleri

- Yüksek talep her zaman yüksek fiyat anlamına gelmez
- Host yanıt hızı doluluk üzerinde kritik etkiye sahiptir
- Yüksek puanlı hostlar için hacim (volume) odaklı stratejiler daha etkilidir
- Availability trendleri kısa vadeli talep tahmini için kullanılabilir

---

## 🚀 İş Önerileri

- Host response time performans metriği olarak önceliklendirilmeli
- Availability bazlı **dynamic pricing** stratejileri uygulanmalı
- Oda tipine göre segment bazlı fiyatlama modelleri oluşturulmalı
- Yüksek puanlı hostlar için doluluk odaklı stratejiler teşvik edilmeli
- Müsaitlik artışı, fiyat revizyonu için erken uyarı sinyali olarak kullanılmalı

---

## 📁 Dataset

Bu projede, eğitim ve analiz amaçlı kullanılan açık kaynaklı bir **Airbnb dataseti** kullanılmıştır.  
Tüm metrikler, hesaplamalar ve görseller bu projeye özel olarak tasarlanmıştır.

---

## 👤 Author

Selen Çimen — Data Analyst  

**Skills & Tools:**  
SQL • Python • Google BigQuery • Looker Studio • Power BI  

🔗 GitHub: `selencimen`
