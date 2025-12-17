# 🚨 Sesim Var - Akıllı Acil Durum Sistemi

**Sesim Var**, acil durumlarda hızlı ve etkili yardım sağlamak için tasarlanmış kapsamlı bir güvenlik platformudur. Yapay zeka destekli ses tanıma, hareket sensörleri ve konum takibi gibi modern teknolojileri kullanarak kullanıcıların güvenliğini en üst seviyede tutar.

---

## ✨ Özellikler

### 🎤 Sesli Komut Sistemi
- **Yapay Zeka Destekli Ses Tanıma**: Vosk kütüphanesi ile offline ses tanıma
- **Özelleştirilebilir Tetikleyici Kelimeler**: "İmdat", "Yardım edin" gibi kelimelerle acil durum tetikleme
- **Anlık Ses Kaydı**: Son 10 dakikalık ses kaydını acil kişilere gönderme

### 📍 Konum ve Güvenlik
- **Gerçek Zamanlı Konum Takibi**: GPS ile anlık konum paylaşımı
- **Güvenli Alan Belirleme**: Harita üzerinden güvenli bölge tanımlama
- **Çıkış Uyarıları**: Güvenli alan dışına çıkıldığında otomatik bildirim

### 🏃 Hareket Algılama
- **Akıllı Sensör Sistemi**: X ve Y eksenindeki hareket sensörleri ile sarsılma algılama
- **Ani Hareket Tespiti**: Koşma, düşme gibi ani hareketleri algılama
- **Otomatik Tetikleme**: Hareket bazlı acil durum uyarıları

### 👥 Acil Kişi Yönetimi
- **Hızlı Bildirim**: Acil durumda seçilen kişilere anında SMS ve bildirim
- **Sağlık Bilgileri Paylaşımı**: Kan grubu, kronik hastalıklar ve alerjiler otomatik paylaşım
- **Konum Bilgisi**: Anlık konum koordinatları acil kişilere gönderilir

### 🔋 Akıllı Pil Yönetimi
- **Düşük Pil Uyarısı**: Pil seviyesi belirli bir yüzdenin altına düştüğünde yakın kişilere bildirim
- **Veri Tasarrufu**: Mobil veri olmadan da konum paylaşımı

### 📊 İhbar Yönetim Sistemi
- **Merkezi İhbar Takibi**: Tüm acil durumların merkezi yönetimi
- **Durum Takibi**: Bekliyor, ekip yolda, müdahale ediliyor, tamamlandı gibi durumlar
- **Detaylı Loglama**: Tüm işlemlerin kayıt altına alınması

---

## 📁 Proje Yapısı

```
Sesim Var System/
│
├── 📱 Mobil/                    # Android Mobil Uygulama
│   ├── app/
│   │   └── src/main/
│   │       ├── java/           # Kotlin kaynak kodları
│   │       └── res/            # UI kaynakları ve görseller
│   └── build.gradle.kts        # Gradle yapılandırması
│
├── 🔧 Backend/                  # .NET 8.0 Web API
│   ├── Controllers/            # API endpoint'leri
│   ├── Models/                 # Veri modelleri
│   ├── Services/               # İş mantığı servisleri
│   ├── DTOs/                   # Veri transfer objeleri
│   ├── Data/                   # Veritabanı bağlamı
│   └── Migrations/             # Entity Framework migration'ları
│
└── 🌐 Web Site/                # PHP Web Sitesi
    ├── admin/                  # Admin paneli
    ├── pages/                  # Sayfa içerikleri
    └── modules/                # Modüler bileşenler
```

---

## 🛠 Teknolojiler

### Mobil Uygulama (Android)
- **Dil**: Kotlin
- **UI Framework**: Jetpack Compose
- **Ses Tanıma**: Vosk Android (Offline AI)
- **Konum**: Google Play Services Location
- **Network**: Retrofit 2, OkHttp
- **Mimari**: MVVM Pattern

### Backend API
- **Framework**: ASP.NET Core 8.0
- **Veritabanı**: SQL Server
- **ORM**: Entity Framework Core
- **Kimlik Doğrulama**: JWT Bearer Token
- **API Dokümantasyonu**: Swagger/OpenAPI
- **Güvenlik**: BCrypt şifreleme

### Web Sitesi
- **Dil**: PHP
- **Yapı**: Modüler routing sistemi
- **Admin Panel**: Özel yönetim paneli

---

## 🚀 Kurulum

### Gereksinimler

#### Backend için:
- .NET 8.0 SDK
- SQL Server (2019 veya üzeri)
- Visual Studio 2022 veya VS Code

#### Mobil için:
- Android Studio (Hedgehog veya üzeri)
- Android SDK 24+ (Minimum SDK)
- Java 11

#### Web Sitesi için:
- PHP 7.4 veya üzeri
- Web sunucusu (Apache/Nginx)

---
## 📱 Kullanım

### Mobil Uygulama

1. **İlk Kurulum:**
   - Uygulamayı açın ve onboarding ekranlarını tamamlayın
   - Gerekli izinleri verin (mikrofon, konum, SMS)

2. **Hesap Oluşturma:**
   - TC Kimlik No, e-posta ve şifre ile kayıt olun
   - Sağlık bilgilerinizi ekleyin (kan grubu, hastalıklar, alerjiler)

3. **Acil Kişi Ekleme:**
   - Ayarlar menüsünden acil durum kişilerinizi ekleyin
   - Bu kişilere acil durumda otomatik bildirim gidecektir

4. **Anahtar Kelime Ayarlama:**
   - Özelleştirilebilir tetikleyici kelimeler ekleyin
   - "İmdat", "Yardım edin" gibi kelimeleri tanımlayın

5. **Acil Durum Tetikleme:**
   - **Sesli**: Tetikleyici kelimeyi söyleyin
   - **Buton**: Acil durum butonuna basılı tutun
   - **Hareket**: Sarsılma veya ani hareket algılandığında otomatik

### Backend API

API endpoint'lerine Swagger üzerinden erişebilirsiniz:
- **Swagger UI**: `http://localhost:5000/swagger`

**Temel Endpoint'ler:**
- `POST /api/Auth/kayit` - Kullanıcı kaydı
- `POST /api/Auth/giris` - Kullanıcı girişi
- `POST /api/Ihbar` - Yeni ihbar oluşturma
- `GET /api/Ihbar` - Tüm ihbarları listeleme
- `PUT /api/Ihbar/{id}/durum` - İhbar durumu güncelleme

---

## 📚 API Dokümantasyonu

Backend API'nin detaylı dokümantasyonu Swagger UI üzerinden erişilebilir. Uygulama çalışırken şu adresi ziyaret edin:

```
http://localhost:5000/swagger
```

Swagger UI'da:
- Tüm endpoint'leri görebilirsiniz
- Request/Response örneklerini inceleyebilirsiniz
- Doğrudan API'yi test edebilirsiniz
- JWT token ile kimlik doğrulama yapabilirsiniz

---

## 🔐 Güvenlik

- **Şifreleme**: Tüm şifreler BCrypt ile hash'lenir
- **JWT Authentication**: Güvenli token tabanlı kimlik doğrulama
- **CORS**: Yapılandırılmış CORS politikaları
- **HTTPS**: Production ortamında HTTPS kullanımı önerilir
- **Veri Validasyonu**: Tüm girişler validasyon kontrolünden geçer

---

## 🗄 Veritabanı Yapısı

### Ana Tablolar:
- **Kullanicilar**: Kullanıcı bilgileri ve kimlik doğrulama
- **Ihbarlar**: Acil durum ihbarları ve durum takibi
- **Acil_Kisiler**: Kullanıcıların acil durum kişileri
- **Hastaliklar**: Kronik hastalıklar ve alerjiler
- **Anahtar_Kelimeler**: Sesli tetikleyici kelimeler
- **Logs**: Sistem logları ve aktivite kayıtları

---

## 🤝 Katkıda Bulunma

1. Bu repository'yi fork edin
2. Yeni bir feature branch oluşturun (`git checkout -b feature/AmazingFeature`)
3. Değişikliklerinizi commit edin (`git commit -m 'Add some AmazingFeature'`)
4. Branch'inizi push edin (`git push origin feature/AmazingFeature`)
5. Bir Pull Request oluşturun

---

## 📝 Lisans

Bu proje özel bir lisans altındadır. Detaylar için `LICENSE` dosyasına bakın.

---

## 👥 Geliştirici Ekibi

Bu proje, acil durum yönetimi ve güvenlik alanında yenilikçi çözümler sunmak amacıyla geliştirilmiştir.

---

## 📞 İletişim

Sorularınız veya önerileriniz için lütfen issue açın veya geliştirici ekibi ile iletişime geçin.

---

## 🎯 Gelecek Özellikler

- [ ] iOS uygulaması desteği
- [ ] WebSocket ile gerçek zamanlı bildirimler
- [ ] Gelişmiş yapay zeka modelleri
- [ ] Çoklu dil desteği
- [ ] Offline mod iyileştirmeleri
- [ ] Gelişmiş analitik ve raporlama

---

**Sesim Var ile güvende kalın! 🛡️**

