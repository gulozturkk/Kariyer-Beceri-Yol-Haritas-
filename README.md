# 🗺️ Kariyer & Beceri Yol Haritası

Bu proje, kullanıcıların kariyer hedeflerini, öğrenmek istedikleri becerileri ve kişisel gelişim adımlarını modern bir Kanban arayüzüyle takip edebileceği orta seviye bir web uygulamasıdır. Uygulama, hedef takibi, beceri planlaması, ilerleme analizi ve yapay zeka destekli yönlendirme gibi özellikleri bir araya getirmeyi amaçlar.

---

## 🚀 Proje Amacı

- Kişisel kariyer hedeflerini düzenlemek
- Öğrenilecek becerileri kategorilere ayırmak
- Gelişim adımlarını görsel olarak takip etmek
- İş önceliklerini yönetmek
- Son tarih ve tamamlanma oranını izlemek
- Yapay zeka destekli öneriler sayesinde daha verimli ilerlemek

---

## ✨ Özellikler

- 3 sütunlu Kanban düzeni: Başlanacak / Devam Ediyor / Tamamlandı
- Beceri ekleme ve düzenleme modalı
- Kategori filtreleme ve arama özelliği
- Zorluk seviyesi, öncelik ve bitiş tarihi takibi
- Sürükle-bırak ile sütunlar arası taşıma ve aynı sütunda sıralama
- LocalStorage ile otomatik veri kaydı
- İstatistik ekranı ve genel ilerleme görünümü
- Yapay zeka önerileri paneli
- Modern koyu tema ve responsive tasarım
- Mobil uyumlu arayüz

---

## 🛠️ Kullanılan Teknolojiler

- React 18
- Vite
- JavaScript
- Tailwind CSS
- @dnd-kit / sürükle-bırak
- Vitest / ESLint
- LocalStorage API
- GitHub sürüm kontrolü

---

## 📁 Proje Yapısı

```text
.
├── .gitignore
├── .env.example
├── eslint.config.js
├── index.html
├── package.json
├── package-lock.json
├── vite.config.js
├── tailwind.config.js
├── postcss.config.js
├── public/
│   └── favicon.svg
├── screenshots/
│   ├── kanban-board.png
│   └── yeni-hedef-ekle.png
└── src/
    ├── App.jsx
    ├── constants.js
    ├── index.css
    ├── main.jsx
    ├── components/
    │   ├── ErrorBoundary.jsx
    │   ├── kanban/
    │   │   ├── KanbanBoard.jsx
    │   │   └── KanbanColumn.jsx
    │   ├── layout/
    │   │   └── StatsHeader.jsx
    │   ├── skill/
    │   │   ├── AddSkillModal.jsx
    │   │   ├── EditSkillModal.jsx
    │   │   └── SkillCard.jsx
    │   ├── stats/
    │   │   └── StatsPage.jsx
    │   └── ui/
    │       ├── Modal.jsx
    │       ├── ProgressBar.jsx
    │       └── SearchBar.jsx
    ├── hooks/
    │   ├── useLocalStorage.js
    │   └── useSkills.js
    └── utils/
        ├── helpers.js
        └── helpers.test.js
```

---

## ⚙️ Kurulum

### Gereksinimler
- Node.js 18+
- npm

### Adım adım çalıştırma

```bash
# Projeyi klonlayın
git clone <repo-url>
cd kariyer-yol-haritasi

# Bağımlılıkları yükleyin
npm install

# Geliştirme sunucusunu başlatın
npm run dev
```

Tarayıcıda aşağıdaki adresi açın:

```bash
http://localhost:5173/
```

### Production build

```bash
npm run build
```

### Test ve kod kontrolü

```bash
npm test
npm run lint
```

---

## 🧠 Yapay Zeka Destekli Geliştirme

Geliştirme sürecinde **GitHub Copilot** aşağıdaki aşamalarda aktif olarak kullanılmıştır:

| Aşama | Yapay Zeka Kullanımı |
|-------|---------------------|
| **Planlama** | Proje fikri oluşturma, özellik listesi çıkarma ve dosya yapısı tasarlama |
| **Bileşen Geliştirme** | React bileşenlerinin iskelet kodlarının üretilmesi, JSX ve Tailwind CSS sınıflarının yazılması |
| **Hata Ayıklama** | Çalışma zamanı hatalarının tespiti ve çözüm önerilerinin alınması |
| **Kod İnceleme** | Yazılan kodun okunabilirlik, performans ve en iyi uygulama açısından gözden geçirilmesi |
| **Dokümantasyon** | README.md ve kod içi yorum/docstring'lerin hazırlanması |

### OpenRouter API entegrasyonu

AI öneri paneli, API anahtarı tanımlandığında OpenRouter Chat Completions API'sine istek gönderir. Proje kökünde `.env.local` dosyası oluşturun:

```bash
VITE_OPENAI_API_KEY=your_openrouter_api_key_here
VITE_OPENAI_MODEL=openai/gpt-4o-mini
```

Değişken adındaki `OPENAI` ifadesine rağmen istek OpenRouter'a gider; bu nedenle OpenRouter API anahtarı kullanılmalıdır. Anahtar tanımlı değilse uygulama yerel, kural tabanlı önerileri gösterir. `VITE_` değişkenleri istemci paketine dahil edildiğinden bu API anahtarı tarayıcıda görülebilir. Bu entegrasyon yalnızca yerel demo içindir; üretim ortamında anahtarı sunucu tarafında saklayan bir API katmanı kullanılmalıdır. `.env.local` dosyasını Git'e eklemeyin.

---

## 📦 Çalışma Mantığı

Uygulama kullanıcıdan hedef ve beceri bilgilerini alır. Bu veriler:

1. Kanban sütunlarına göre ayrılır,
2. öncelik ve zorluk seviyeleriyle etiketlenir,
3. LocalStorage'a kaydedilir,
4. arama ve kategori filtreleri ile kullanıcıya sunulur,
5. istatistik ekranında ilerleme takibi yapılır.

---

## 🌍 Yayına Alma

Proje Netlify veya Vercel üzerinden kolayca yayınlanabilir.

```bash
npm run build
```

Sonrasında `dist/` klasörü deploy platformuna yüklenebilir.

---
### Canlı Demo

[Uygulamayı canlı görüntüle](https://web-gelistirme-yapay-zeka.vercel.app)

---

## ✅ Son Durum

Bu proje, orta seviye bir kariyer planlama ve web geliştirme eğitim projesidir. Görsel tasarım, istemci tarafı veri yönetimi, Kanban çalışma akışı ve yapay zeka destekli geliştirme yaklaşımını bir araya getirir.

---

## 📄 Lisans

Bu proje eğitim amaçlı geliştirilmiştir.



