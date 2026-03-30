# 🎓 School Club Management System

[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

Modern web teknolojileri ile geliştirilmiş kapsamlı bir **Okul Kulübü Yönetim Sistemi**.  
Kulüp etkinliklerinin yönetimi, üye takibi, denetim (audit) ve finansal kayıtların tutulması gibi gelişmiş özelliklere sahip dijital bir platform sunar.

---

## 🏗️ Genel Yazılım Mimarisi ve Teknoloji Yığını

Proje, ölçeklenebilirlik ve performans için **Next.js 16+ (App Router)** mimarisi üzerine inşa edilmiştir.

**Frontend:**  
Next.js (App Router), TypeScript, Tailwind CSS, React

**Backend:**  
Next.js Route Handlers (API), Prisma ORM

**Veritabanı:**  
MySQL (Prisma üzerinden yönetilir)

**Güvenlik:**  
- Password Hashing (Argon2)  
- NextAuth / Auth.js  
- CORS & CSRF (Auth.js ile yerleşik)  
- Memory bazlı rate limiter

---

## 🗂️ Proje Yapısı

src/  
├── app/            # Sayfalar ve API rotaları  
│   ├── home/       # Misafir ve üye kullanıcı sayfaları
│   ├── api/        # API rotaları  
│   └── dashboard/  # Yönetim paneli sayfaları (finans, audit, üye yönetimi)  
├── components/     # Yeniden kullanılabilir UI parçaları (home/admin)  
├── lib/            # Yardımcı araçlar  
├── types/          # TypeScript için gerekli type tanımları (interface/type)  
prisma/             # Veritabanı şeması ve migration dosyaları  

---

## ⚙️ Kurulum ve Gereksinimler

### 1️⃣ Ortam Değişkenleri (.env)

Kök dizinde `.env` dosyası oluşturun ve aşağıdaki değişkenleri tanımlayın:

DATABASE_URL=  
AUTH_SECRET=  
AUTH_URL=  
NODE_ENV=  

### 2️⃣ Yerel Çalıştırma

# Bağımlılıkları yükleyin  
npm install  

# Veritabanı şemasını oluşturun  
npx prisma generate  
npx prisma db push  

# Geliştirme modunda başlatın  
npm run dev  

### 3️⃣ Docker ile Çalıştırma

docker-compose up -d  

---

## 🎨 Temel Özelleştirmeler

### 1️⃣ Sosyal Medya Linkleri
Sosyal medya linklerinizi `/src/components/home/layout/Footer.tsx` içerisindeki social listesine icon ile birlikte ekleyebilirsiniz.

### 2️⃣ Favicon Değiştirme
Favicon dosyanızı `.ico` formatında `favicon.ico` ismiyle doğrudan `src/app/` klasörüne yerleştirerek değiştirebilirsiniz.

### 3️⃣ Logo Değiştirme
Logonuzu `public/` klasöründeki hazır gelen `logo.png` dosyasını silip yerine kendi `logo.png` dosyanızı ekleyerek değiştirebilirsiniz.

### 4️⃣ Privacy Policy Ekleme
Privacy policy metinlerinizi `/src/app/(home)/home/policy/page.tsx` dosyasına ekleyebilirsiniz.

---

## 🛡️ Lisans

Bu proje MIT Lisansı altında lisanslanmıştır.  
Bu, projenin ticari veya kişisel amaçlarla özgürce kullanılabileceği, kopyalanabileceği ve değiştirilebileceği anlamına gelir; ancak orijinal yazarın belirtilmesi zorunludur.

---

## ⚠️ Önemli Not / Sorumluluk Reddi

Bu proje sadece teknik bir araç olarak geliştirilmiştir.  
Projeyi kullanırken meydana gelebilecek hatalı, kötü niyetli veya yasadışı kullanımlardan projenin orijinal yazarı/geliştiricisi sorumlu tutulamaz.  
Kullanıcılar, projeyi kendi sorumlulukları altında kullanmayı kabul etmiş sayılır.

---

## 📧 İletişim

Geliştirici: Ramazan Özkan  
E-posta: officallozkan@gmail.com  
GitHub: [@offical00ozkan](https://github.com/ozkan00offical)
