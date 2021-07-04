# smartPulse

## TASK 1 : Benzer Özellikteki Günlerin Belirlenmesi

### AMAÇ :  nisan_ptf_smf_netYon excel dosyasındaki verilerden yararlanarak ve kendi belirleyeceğiniz bir kümeleme algoritmasını kullanarak birbiri ile benzer özellik taşıyan günlerin belirlenmesi.

**BEKLENENLER :**

1-	Veriseti üzerinde gerekli ön işlemlerin yapılması

2-	Verisetindeki patternların (eğer varsa) belirlenmesi

3-	Verisetinde üzerinde gerekli görselleştirme işlemlerinin yapılması, ve grafikler üzerinde analizler yaparak hangi kümeleme algoritmasının neden seçildiğinin açıklanması.

4-	Seçilen kümeleme algoritmasıyla en optimum modelin tasarlanması.

5-	Kümeleme sonuçlarını görselleştirerek sonuçlar üzerinden analiz yapılması ve tüm bu adımların bir rapor halinde sunulması.

## TASK 2 : Santral Üretim Tahmini

### AMAÇ : powerplant_data excel dosyasındaki verilerden yararlanarak her hangi bir makine öğrenmesi ve ya derin öğrenme algoritması ile, ilgili rüzgar enerjisi santraline ait yeni üretim tahminin, bir backtest algoritması tasarlanarak yapılması.

#### VERİSETİ TANIMI : 

**instrument: İlgili t anı**

**forecast_t-75m_value: İlgili t anından 75 dakika önce, t anına ait yapılan üretim tahmini**

**generation_meteredby_device_t-0h: t saatinde santrale ait gerçekleşmiş üretim değeri**

**powerplantdata_t-0h_part0: t saatinin 0-10. dakikaları arasında santralin ortalama gücü.** 

**powerplantdata_t-0h_part1: t saatinin 10-20. dakikaları arasında santralin ortalama gücü.**

**powerplantdata_t-0h_part2: t saatinin 20-30. dakikaları arasında santralin ortalama gücü.** 

**powerplantdata_t-0h_part3: t saatinin 30-40. dakikaları arasında santralin ortalama gücü.**

**powerplantdata_t-0h_part4: t saatinin 40-50. dakikaları arasında santralin ortalama gücü.**

**generation_meteredby_device_t-1h: t-1 saatinde santrale ait gerçekleşmiş üretim değeri**

#### BEKLENENLER :

1-	Daha önce yapılmış olan üretim tahminini, ve santrale ait part verilerini kullanarak, makine öğrenmesi ve ya derin öğrenme tabanlı her hangi bir regresyon algoritması ile t saatine ait yeni bir üretim tahmini oluşturulması.

2-	Oluşturulan makine öğrenmesi algoritmasına ait hiperparametre optimizasyonlarının yapılması.

3-	Tahminleri 2020-10-01 / 2020-12-31 tarihleri arasına 2 ayı kapsayacak şekilde yapılması.

4-	Üretilen tahminlerin başarısı, excel dosyasında forecast_t-75m_value kolonundaki tahminlerin başarısı ile karşılaştırılması. 

#### DİKKAT EDİLMESİ GEREKENLER :

1-	Santraller üretim tahmin değelerini ilgili t anının en geç 1 saat öncesine kadar ilgili kurumlara bildirmek zorundadırlar. Örneğin saat 14:00 için yapılacak üretim tahminini en geç saat 12:59’da yapabilirsiniz. Bu yüzden model geliştirmeye başlamadan önce veriseti üzerinde bu kurala uygun bazı kaydırma işlemleri yapmanız gerekmektedir.

2-	Geliştirilen model 1 haftalık tahmin ürettikten sonra yeni veriler ile güncellenmelidir. Örneğin 2020-10-01 ile 2020-10-07 tarihleri arasına tahmin ürettikten sonra bu aralıktaki yeni veriler ile kendini tekrar eğitmelidir.

3-	Bazı part verilerinin virgülden sonra 2 basamaklı olduğunu göreceksiniz. Bu veriler okuma cihazında bir arıza olduğu durumlarda santral operatörü tarafından el ile girilmiştir ve hatalı olma olasılıkları diğer verilere göre daha yüksektir. 

4-	Bazı part verilerinin virgülden sonraki basamak sayısı normal olmasına rağmen birkaç saat boyunca bu verilerin hep aynı tekrar ettiğini göreceksiniz. Bu veriler cihaz tarafından gönderilmiş olmasına rağmen hatalı olma olasılıkları diğer verilere göre daha yüksektir.

5-	Yukarıdaki maddelerdeki tüm durumların kontrollerinin kod ile yapılması gerekmektedir.

## TASK 3 : SQL Sorguları

### AMAÇ : Aşağıda verilen veritabanı şemasına göre belirtilen SQL sorgularının yazılması.

1-	İsmi Ahmet olan kullanıcıların email adresleri.

2-	user_id’si 1234 olan kullanıcının; adı, soyadı ve son login olduğu tarih. 

3-	Kayıt tarihi 1 Ocak 2021’den büyük ve post sayısı 3’ten büyük olan her bir kullanıcının user_id’si ve post sayısı


 




