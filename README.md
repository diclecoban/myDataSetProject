# Flight Delay Prediction and Clustering Analysis

**Projenin Amacı**
Bu proje, uçuş gecikmelerini analiz etmek ve bu gecikmelere etkili olan faktörleri belirlemek amacıyla bir dataset kullanmaktadır. Veri setinde uçuş bilgileri ve gecikme nedenleri yer almaktadır. Proje, uçuş gecikmelerini tahmin etmek ve uçuşları belirli kümelere ayırarak analiz etmek üzerine odaklanmaktadır.

**Veri Seti**
Kullanılan veri seti, uçuş gecikmeleri hakkında çeşitli bilgileri içermektedir. Sütun isimleri şu şekildedir:

•FlightID: Uçuş kimlik numarası

•Airline: Havayolu şirketi

•FlightNumber: Uçuş numarası

•Origin: Kalkış noktası

•Destination: Varış noktası

•ScheduledDeparture: Planlanan kalkış tarihi ve saati
•ActualDeparture: Gerçek kalkış tarihi ve saati
•ScheduledArrival: Planlanan varış tarihi ve saati
•ActualArrival: Gerçek varış tarihi ve saati
•DelayMinutes: Gecikme süresi (dakika)
•DelayReason: Gecikme nedeni
•Cancelled: İptal durumu
•Diverted: Yön değişikliği durumu
•AircraftType: Uçak tipi
•TailNumber: Kuyruk numarası
•Distance: Mesafe

**Değişkenler**
•Bağımlı değişken (y): DelayMinutes
•Bağımsız değişkenler (X): Airline, FlightNumber, Origin, Destination, ScheduledDeparture, ActualDeparture, ScheduledArrival, ActualArrival, DelayReason, Cancelled, Diverted, AircraftType, TailNumber, Distance

**Veri Ön İşleme**
•Eksik Veriler: Eksik veriler, en sık görülen gecikme nedeni ile doldurulmuştur.
•One-Hot Encoding: Kategorik değişkenler sayısal verilere dönüştürülmüştür.
•Datetime İşlemleri: Tarih ve saat sütunları ayrıştırılmış ve gecikme süreleri hesaplanmıştır.
**Modelleme**
Projede kullanılan regresyon algoritmaları:

•RandomForestRegressor: Karar ağaçlarının rastgele ormanını kullanarak tahmin yapılmıştır.
**Model Seçimi**
En iyi performansı veren modelin değerlendirilmesi için K-Fold çapraz doğrulama kullanılmış ve Ortalama Mutlak Hata (MAE) ve R-kare (R²) skorları hesaplanmıştır. Ayrıca, modelin önemli özellikleri değerlendirilmiş ve K-Means kümeleme yöntemi ile veriler kümelere ayrılmıştır.

**Performans Değerlendirme**
•Ortalama Mutlak Hata (MAE): Modelin tahmin hatalarının ortalama büyüklüğünü gösterir.
•R² Skoru: Modelin veriyi ne kadar iyi açıkladığını gösterir.
**Kümeleme**
•K-Means kümeleme yöntemi kullanılarak veriler kümelere ayrılmış ve kümelerin içeriği analiz edilmiştir. Küme dağılımları pasta grafiği ile görselleştirilmiştir.

**Sonuçlar**
Modelleme ve kümeleme sonuçları, uçuş gecikmelerini etkileyen faktörlerin anlaşılmasına ve uçuşların benzerliklerine göre gruplandırılmasına yardımcı olmuştur.
