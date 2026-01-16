# Sağlık Eczanesi Web Sitesi

Eczane yönetim sistemi için modern ve responsive bir web sitesi. **Tailwind CSS** tabanlı modern tasarım!

## 📁 Dosya Yapısı

```
sonsite/
├── index.html           # Ana sayfa (Tailwind CSS CDN ile)
├── medicines.html       # İlaçlar listeleme sayfası (Tailwind CSS CDN ile)
├── style.css           # Minimal CSS (Tailwind için referans)
├── README.md           # Bu dosya
└── DETAY.txt          # Detaylı proje bilgileri
```

## 🎨 Tasarım Özellikleri

- **Tailwind CSS CDN** - Modern ve responsive tasarım
- **Yeşil Tema** - Sağlık/eczane konusuna uygun
- **Gradient Arka Planlar** - Profesyonel görünüm
- **Smooth Animations** - Hoş kullanıcı deneyimi
- **Mobile-First Responsive** - Tüm cihazlarda mükemmel

## 🎯 Özellikler

### Ana Sayfa (index.html)

- Modern hero bölümü
- 6 hizmet kartı (İlaç Danışmanlığı, Aşı, Reçete, Ev Teslimi, Nöbetçi, Telefon Danışması)
- Öne çıkan 4 ilaç kategorisi
- Sağlık rehberi bölümü (3 makale)
- İletişim bilgileri ve Google Maps
- Sticky navbar ile kolay navigasyon
- İlaçlar sayfasına hızlı erişim

### İlaçlar Sayfası (medicines.html)

- **12 farklı ilaç** örneği içeren kapsamlı veritabanı
- **JavaScript Veri Yapısı**:
  - İlaç ID
  - İlaç Adı
  - Kategori
  - Etken Madde
  - Dozaj
  - Üretici
  - Fiyat
  - Açıklama
  - Kullanım Talimatları
  - Kontrendikasyonlar
  - Yan Etkiler
  - Görsel İkon
  - Stok Miktarı

### Dinamik Özellikler

#### 🔍 Arama Fonksiyonu

- İlaç adına göre arama
- Etken maddeye göre arama
- Açıklamaya göre arama (gerçek zamanlı)

#### 🏷️ Kategori Filtreleme

- Ağrı Kesici
- Antibiyotik
- Vitamin & Takviye
- Soğuk Algınlığı

#### 💳 Sepete Ekleme

- Kullanıcı dostu satın alma
- Stok durumu gösterimi
- Fiyat görüntüleme

## 🚀 Nasıl Kullanılır

1. **index.html** dosyasını tarayıcıda açın
2. Navbardaki "İlaçlar" linki veya ana sayfadaki linklerle medicines.html'e gidin
3. İlaçları görmek, aramak ve filtrelemek için interact edin

### Arama Örneği

```javascript
// medicines.html içindeki JavaScript
const medicines = [
  {
    id: 1,
    name: "Paracetamol 500mg",
    category: "Ağrı Kesici",
    activeIngredient: "Paracetamol",
    dosage: "500mg",
    // ... diğer özellikler
  },
  // Daha fazla ilaç...
];
```

### Filtreleme Fonksiyonları

```javascript
// Arama (gerçek zamanlı)
function filterMedicines() {
  const searchValue = document
    .getElementById("searchInput")
    .value.toLowerCase();
  const categoryValue = document.getElementById("categoryFilter").value;

  const filtered = medicines.filter((medicine) => {
    const matchSearch =
      medicine.name.toLowerCase().includes(searchValue) ||
      medicine.activeIngredient.toLowerCase().includes(searchValue);

    const matchCategory =
      categoryValue === "" || medicine.category === categoryValue;

    return matchSearch && matchCategory;
  });

  displayMedicines(filtered);
}
```

## 🎨 Tasarım Özellikleri

- **Renkler**:

  - Birincil: `#0055ff` (Mavi)
  - İkincil: `#1a7e3a` (Yeşil)
  - Vurgu: `#10b981` (Açık Yeşil)

- **Typography**: Segoe UI, modern sans-serif

- **Responsive**: Mobile, Tablet, Desktop için optimize edilmiş

- **Hover Efektleri**: Smooth transitions ve shadow efektleri

## 📊 İlaç Kategorileri ve Sayıları

| Kategori          | Sayı   |
| ----------------- | ------ |
| Ağrı Kesici       | 2      |
| Antibiyotik       | 2      |
| Vitamin & Takviye | 4      |
| Soğuk Algınlığı   | 4      |
| **Toplam**        | **12** |

## 💡 JavaScript Kullanılan Teknikler

1. **Array Methods**: `filter()`, `map()`, `find()`
2. **Event Listeners**: `onkeyup`, `onchange`, `onclick`
3. **DOM Manipulation**: `getElementById()`, `innerHTML`
4. **Template Literals**: ES6 string interpolation
5. **Arrow Functions**: Modern JavaScript syntax
6. **Conditional Rendering**: Stok durumuna göre buton değişimi

## 🔧 Temel JavaScript Yapısı

```javascript
// Veri Tanımlaması
const medicines = [...];

// Sayfada Gösterme
function displayMedicines(medicinesList) {
    // HTML template oluştur
}

// Filtreleme
function filterMedicines() {
    // Filter ve display
}

// Sepete Ekleme
function addToCart(medicineId) {
    // Alert göster
}

// Sayfa Yükleme
window.addEventListener('DOMContentLoaded', function() {
    displayMedicines(medicines);
});
```

## 📱 Responsive Breakpoints

- **Desktop**: 1200px+
- **Tablet**: 768px - 1200px
- **Mobile**: 480px - 768px
- **Small Mobile**: < 480px

## 🔗 Navigasyon Akışı

```
index.html (Ana Sayfa)
    ↓
    ├─ "İlaçlar" link → medicines.html
    ├─ "Kategori Linki" → medicines.html#kategori
    └─ Footer linki → index.html

medicines.html (İlaçlar Sayfası)
    ↓
    ├─ Arama (JavaScript)
    ├─ Filtreleme (JavaScript)
    ├─ Ana Sayfaya Dön (Link)
    └─ Sepete Ekleme (JavaScript)
```

## 📝 Notlar

- Tüm veriler **JavaScript'te tanımlanmış** olup, **dinamik olarak ekrana yazılmıştır**
- Sepete ekleme fonksiyonu şu an **alert** göstermekte, geliştirilebilir
- Arama **gerçek zamanlı (real-time)** çalışmaktadır
- Tüm stok seviyeleri renkli göstergelerle belirtilmiştir

## 🎯 Geliştirme Önerileri

1. Backend API entegrasyonu eklenebilir
2. LocalStorage ile sepet verisi kaydedilebilir
3. Daha fazla ilaç kategorisi eklenebilir
4. Kullanıcı değerlendirme sistemi eklenebilir
5. İlaç detay sayfası oluşturulabilir

---

**Oluşturulma Tarihi**: 2024-01-16
**Versiyon**: 1.0
