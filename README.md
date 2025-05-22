# 🎓 Öğrenci Kayıt Sistemi

Bu proje, öğrencilerin ve öğretmenlerin kayıt işlemlerini ve yönetimini sağlayan çok katmanlı bir ASP.NET Core MVC uygulamasıdır. Sistem; servis, veri erişim ve sunum katmanlarını temiz bir şekilde ayırarak **SOLID prensiplerine uygun** geliştirilmiştir.

---

## 🧠 Katmanlı Mimari Hakkında

Proje 4 ana katmandan oluşur:

- **Business**: İş kurallarının tanımlandığı ve servislerin yer aldığı katman.
- **DataAccess**: Entity Framework ile veri işlemlerinin yapıldığı katman.
- **Entities**: Veri modelleri, DTO'lar ve Enum'ların tanımlandığı katman.
- **Presentation**: ASP.NET Core MVC ile kullanıcıya arayüz sunan katman.

---

## 📁 Proje Yapısı

```plaintext
OgrenciKayitSistemi.sln
│
├── 📦 Business
│   ├── Abstract
│   │   ├── IGenericService.cs
│   │   ├── IStudentService.cs
│   │   └── ITeacherService.cs
│   ├── Concrete
│   │   ├── StudentManager.cs
│   │   └── TeacherManager.cs
│   └── DependencyResolvers
│       └── BusinessModule.cs
│   └── Business.csproj
│
├── 🧱 Core
│   ├── DataAccess
│   │   ├── EfEntityRepositoryBase.cs
│   │   └── IEntityRepository.cs
│   ├── Entities
│   │   └── IEntity.cs
│   └── Core.csproj
│
├── 💾 DataAccess
│   ├── Abstract
│   │   ├── IStudentDal.cs
│   │   └── ITeacherDal.cs
│   ├── Concrete
│   │   └── EntityFramework
│   │       ├── Context
│   │       │   └── ProjeContext.cs
│   │       ├── StudentDal.cs
│   │       └── TeacherDal.cs
│   ├── Migrations
│   └── DataAccess.csproj
│
├── 📦 Entities
│   ├── DataTransferObjects
│   │   └── StudentModel.cs
│   ├── Enums
│   │   ├── BransEnum.cs
│   │   ├── CinsiyetEnum.cs
│   │   └── SinifEnum.cs
│   ├── Models
│   │   ├── BaseEntity.cs
│   │   ├── Student.cs
│   │   └── Teacher.cs
│   └── Entities.csproj
│
├── 🌐 Presentation
│   ├── Controllers
│   │   ├── HomeController.cs
│   │   ├── StudentController.cs
│   │   └── TeacherController.cs
│   ├── Models
│   │   └── ErrorViewModel.cs
│   ├── Views
│   │   ├── Home/
│   │   ├── Shared/
│   │   ├── Student/
│   │   └── Teacher/
│   ├── wwwroot/
│   │   ├── Img/
│   │   ├── css/
│   │   ├── js/
│   │   ├── lib/
│   │   └── favicon.ico
│   ├── _ViewImports.cshtml
│   ├── _ViewStart.cshtml
│   ├── launchSettings.json
│   ├── appsettings.json
│   ├── appsettings.Development.json
│   ├── Program.cs
│   └── Presentation.csproj
│
├── .gitignore
├── .gitattributes
## 🧩 Kullanılan Teknolojiler

| Teknoloji               | Açıklama                                 |
|------------------------|------------------------------------------|
| ⚙️ ASP.NET Core MVC     | Sunum katmanı (UI)                        |
| 🗃️ Entity Framework Core | ORM, veri işlemleri                      |
| 🧱 Katmanlı Mimari      | Temiz kod, bağımsız modüller             |
| 🧭 SOLID Principles     | Yazılım geliştirme prensipleri           |
| 🔄 Dependency Injection | IoC Container ile yönetilen servisler    |

---

## ✨ Proje Özellikleri

- 🧑‍🎓 **Öğrenci kayıt**, listeleme ve güncelleme
- 👨‍🏫 **Öğretmen bilgisi yönetimi**
- 🏷️ Enum tabanlı **Cinsiyet**, **Sınıf**, **Branş** seçimi
- 📦 Repository ve servis katmanları ile yapılandırma
- 🌐 Razor View'lar ile kullanıcı dostu arayüz


![WhatsApp Image 2025-05-22 at 15 56 42](https://github.com/user-attachments/assets/f0793117-bd3b-437f-af46-495c478df068)


![WhatsApp Image 2025-05-22 at 15 56 50-min](https://github.com/user-attachments/assets/aee888fd-e578-42b8-9919-187668bb45b2)

---![WhatsApp Image 2025-05-22 at 15 56 42-min](https://github.com/user-attachments/assets/b2b2af3e-142d-4099-ac28-7f5c8f47befb)

