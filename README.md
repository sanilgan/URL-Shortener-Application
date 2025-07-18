# URL KISALTICI UYGULAMASI – PROJE RAPORU

**Hazırlayan:** Zeynep Anılgan  
**Şirket:** Talya Bilişim  
**Tarih:** 16.07.2025

---

## 1. Proje Başlığı  
**URL Kısaltıcı Uygulaması**

---

## 2. Proje Açıklaması  
Bu proje, kullanıcıların uzun URL’leri daha kısa, paylaşılabilir ve izlenebilir bağlantılara dönüştürmesini amaçlamaktadır. Sistem, oluşturulan kısa bağlantıları veritabanında saklar ve her tıklamada kullanıcıyı orijinal uzun URL’ye yönlendirir. Aynı zamanda tıklama sayısını ve (opsiyonel olarak) IP, zaman gibi detayları kaydederek analiz yapılmasını sağlar.

**Kullanılacak Temel Teknolojiler:**
- **Backend:** Node.js (Express.js)
- **Veritabanı:** Microsoft SQL Server
- **Frontend:** HTML / CSS / JavaScript

---

## 3. Pazar Araştırması ve Kullanım Verileri  

**URL Kısaltıcıların Kullanımı:**
- **Kullanım Oranı:** Tüm web sitelerinin yaklaşık %4.5’i URL kısaltıcı kullanmaktadır.
- **Kullanım Yoğunluğu:**
  - %95.2’si yalnızca bir URL kısaltıcı kullanıyor.
  - %4.3’ü iki tane kullanıyor.
  - %0.6’sı ise üç veya daha fazla URL kısaltıcı entegre etmiş.

---

## 4. Rakip Analizi  

| Platform      | Özellikler                                                                 |
|--------------|-----------------------------------------------------------------------------|
| **Bitly**     | Gelişmiş analiz ve markalı bağlantılar sunar. Ücretsiz planda sınırlamalar vardır. |
| **TinyURL**   | Basit, kullanıcı dostu ve ücretsizdir; ancak analiz seçenekleri sınırlıdır.|
| **Rebrandly** | Markalı URL oluşturma ve detaylı analiz özellikleri ile öne çıkar.         |
| **ShortenWorld** | Hızlı çalışması ve çok yönlülüğüyle dikkat çeker.                        |

---

## 5. Potansiyel Fırsatlar  

Bu projede uygulanabilecek bazı fark yaratan özellikler:
- **Gelişmiş Analizler:** Tıklama verilerinin detaylı şekilde izlenmesi.
- **Markalı URL Desteği:** Şirketlere özel kısa alan adlarıyla güven artırma.
- **Mobil Uyumlu Tasarım:** Tüm cihazlarda kullanıcı dostu deneyim.
- **API Entegrasyonu:** Harici sistemlerle bağlantı kurmak için REST API desteği.

---

## 6. Proje Amacı  
- Uzun URL’leri daha kısa ve kolay paylaşılabilir hale getirmek.  
- Her tıklamada, kısa URL’yi orijinal adrese yönlendirmek.  
- Bu tıklamaları saymak ve (gerekirse) analiz etmek için kayıt altına almak.  

---

## 7. Kullanıcı Akışı  
1. Kullanıcı sisteme uzun bir URL girer.  
2. Sistem benzersiz kısa bir kod oluşturur.  
3. Bu kod ve URL, veritabanına kaydedilir.  
4. Kullanıcıya kısa link gösterilir.  
5. Kısa link tıklandığında sistem yönlendirme yapar.  
6. Aynı zamanda tıklama sayısı artar ve detaylı kayıt tutulur.  

---

## 8. Temel Proje Gereksinimleri  

- Kısa URL üretme (otomatik kısa kod)  
- Yönlendirme işlemi (GET /:shortcode)  
- Tıklanma sayısını güncelleme  
- IP adresi, tarih gibi verileri loglama (opsiyonel)  
- En çok tıklanan linkleri listeleme (2. hafta eklenecek)  
- RESTful API aracılığıyla erişim sağlama  

---

## 9. Teknik Altyapı Özeti  

| Bileşen             | Açıklama                                      |
|---------------------|-----------------------------------------------|
| **Backend**         | Node.js + Express.js                          |
| **Veritabanı**      | Microsoft SQL Server                          |
| **Frontend**        | HTML / CSS / JavaScript                       |
| **Veritabanı Aracı**| DBeaver ile yönetim ve sorgulama              |
| **Bağlantı Kütüphanesi** | `mssql` npm paketi ile Node.js–MSSQL bağlantısı |

---

## 10. Gelecek Geliştirmeler  

- En çok tıklanan URL’leri sıralayan istatistik sayfası  
- Kullanıcı girişi / hesap oluşturma  
- QR kod üretimi  
- IP adresine göre coğrafi analiz  

---

## 11. Projemizde Fark Yaratacak Özellikler  

| Özellik                       | Açıklama                                                                 |
|-------------------------------|--------------------------------------------------------------------------|
| **Gelişmiş Tıklama İstatistikleri** | Kullanıcı linke tıkladığında IP adresi, tarayıcı türü, tıklanma zamanı gibi veriler loglanabilir. |
| **Basit ve Hızlı Yapı**       | Üyelik veya giriş olmadan direkt URL kısaltma kullanılabilir. Kullanıcıyı yormaz. |
| **Açık API**                  | Dış sistemlerin bağlanabileceği bir REST API sunulacak. Yani geliştiriciler sizin sistemi kullanabilir. |

