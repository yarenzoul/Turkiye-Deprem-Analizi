![ChatGPT Image 29 Nis 2025 00_53_57](https://github.com/user-attachments/assets/f5d5ae6a-ab28-4a13-bea1-90a78ed53124)

# Türkiye Deprem Analizi Projesi
Bu proje, Türkiye'deki depremleri analiz etmek için kullanılan veri bilimi ve görselleştirme tekniklerini içermektedir. Amaç, deprem verilerini anlamak ve görselleştirmelerle kullanıcıya sunmaktır.

## Proje İçeriği:
1. Deprem verilerinin toplandığı ve işlendiği Python kodları.
2. Görselleştirmeler: Çubuk grafikler, haritalar ve diğer etkileşimli görselleştirmeler.
3. İstatistiksel analizler.
4. Makine Öğrenmesi Modeli ile Deprem Türü Tahmini.

## Kullanılan Teknolojiler:
- **Python**: Veri işleme ve analiz için.
- **Pandas**: Veri manipülasyonu ve analizi.
- **Matplotlib & Seaborn**: Statik grafikler ve görselleştirmeler.
- **Plotly & Folium**: Etkileşimli haritalar ve grafikler.

![Ekran görüntüsü 2025-04-29 163205](https://github.com/user-attachments/assets/91e658a3-84ae-4fe0-a409-92a82ad300ce)
- **ML (Local Magnitude):** Yerel Büyüklük. "Richter ölçeği" olarak da bilinir. Genellikle yakınlarda ölçülen küçük-orta büyüklükteki depremler için kullanılır.
- **MW (Moment Magnitude):** Moment Büyüklük. Büyük depremler için daha güvenilir ve günümüzde en yaygın kullanılan büyüklük ölçeğidir. Enerjiye ve faydaki kaymaya dayanır.
- **Md (Duration Magnitude):** Süreye Bağlı Büyüklük. Deprem dalgalarının süresine göre hesaplanır.
- **Ml (veya mL) (Local Magnitude):** Yukarıda belirtilen ML ile aynıdır, yazım farkıdır (bazı yerlerde küçük harfle de yazılabilir).
- **Mw (Moment Magnitude):** "MW" ile aynıdır; yazım farkıdır (bazı veritabanlarında küçük harfle geçer). Yani Moment büyüklüğünü gösterir.
- **MI (Intensity Magnitude):** Bazen Intensity Magnitude veya Body-wave Magnitude (Mb) anlamına gelebilir. Bazı sismoloji kaynaklarında Intensity (Şiddet) olarak da geçebilir.
- **Mwp (Moment Magnitude, P-wave):** P dalgası ile hesaplanan moment büyüklüğü. Tsunami erken uyarı sistemlerinde kullanılır.
##
![Ekran görüntüsü 2025-04-29 163257](https://github.com/user-attachments/assets/1a78629d-df6e-4568-a661-30507051118b)
Bu haritada, Türkiye genelinde 1999-2024 yılları arasında kaydedilen depremlerin merkez üsleri (epicenter) turuncu noktalarla gösterilmiştir. Her bir daire, bir deprem olayını temsil eder. Bu görselleştirme, depremlerin coğrafi olarak en çok hangi bölgelerde yoğunlaştığını ve ana fay hatlarının izini takip etmeye imkân tanır.
##
![Ekran görüntüsü 2025-04-29 163319](https://github.com/user-attachments/assets/654b91f7-7b8d-4053-b239-980c3366fafc)
Bu ısı haritası, aynı deprem verisinin yoğunluk analizine odaklanır. Kırmızı alanlar, deprem aktivitesinin en yoğun olduğu bölgeleri gösterir; mavi/yeşil alanlar ise görece daha az sismik hareketliliğe sahip alanlardır. Türkiye'de sismik tehlike haritası çıkarımlarında ve risk analizlerinde önemli bir araçtır.




## Makine Öğrenmesi ile Deprem Türü Tahmini
Projenin son adımında, depremlerin lokasyon, büyüklük ve derinlik gibi özelliklerine göre deprem türünü tahmin eden bir sınıflandırma modeli geliştirildi.

### Kullanılan Yaklaşım:
**Type** sütunu Label Encoding ile sayısala çevrildi.

Özellik olarak **Longitude**, **Latitude**, **Depth**, **Magnitude** kullanıldı.

Veri %80 eğitim / %20 test olarak bölündü.

**Random Forest Classifier** ile model oluşturuldu ve başarı oranı değerlendirildi.

## Sonuç:
Random Forest algoritmasını kullanarak modeli eğittim ve test sonuçlarında genel doğruluk oranı %86 olarak elde edildi. **En sık rastlanan büyüklük tipinde yüksek başarı**, **nadir tiplerde ise daha düşük doğruluk** gözlendi.
