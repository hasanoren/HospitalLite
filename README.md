# HL (HospitalLite) - Katmanlı Mimari .NET Projesi

Bu proje, ASP.NET Core Web API kullanılarak geliştirilmiş basit bir **katmanlı mimari (N-Tier Architecture)** örneğidir.

---

## 📁 Proje Yapısı

Solution içerisinde 4 adet proje bulunmaktadır:

- HL.Core → Domain (Entity, Interface, temel modeller)
- HL.DataAccess → Veri erişim katmanı (Repository, EF Core vb.)
- HL.Business → İş mantığı katmanı (Service, business rules)
- HL.API → Web API (Controller, HTTP endpoints)

---

## 🧠 Katmanların Görevleri

### HL.Core
- Entity sınıfları
- Interface tanımları
- Proje bağımsız temel yapı

### HL.DataAccess
- Veritabanı işlemleri
- Repository implementasyonları
- EF Core veya ORM yapıları

### HL.Business
- İş kuralları
- Validasyonlar
- Servis katmanı

### HL.API
- HTTP endpoint’leri (Controller’lar)
- Client ile iletişim
- Dependency Injection yapılandırması

---

## 🔗 Katman Bağımlılıkları

HL.API → HL.Business  
HL.API → HL.DataAccess  

HL.Business → HL.Core  
HL.DataAccess → HL.Core  

---

## 🚀 Projeyi Çalıştırma

### Bağımlılıkları yükle
```bash
dotnet restore