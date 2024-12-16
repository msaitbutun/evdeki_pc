
## 💾 Veritabanı Yapısı

Proje için gerekli olan MySQL veritabanı, aşağıdaki tabloları içermektedir:

### 1. **Urunler**
| Kolon Adı   | Veri Tipi  | Açıklama               |
|-------------|------------|------------------------|
| `UrunID`    | INT        | Birincil anahtar       |
| `UrunAdi`   | VARCHAR(50)| Ürünün adı            |
| `Kategori`  | VARCHAR(50)| Ürünün kategorisi     |
| `Fiyat`     | DECIMAL    | Ürünün fiyatı         |
| `Stok`      | INT        | Stok miktarı          |

### 2. **Musteriler**
| Kolon Adı   | Veri Tipi  | Açıklama               |
|-------------|------------|------------------------|
| `MusteriID` | INT        | Birincil anahtar       |
| `AdSoyad`   | VARCHAR(50)| Müşteri adı ve soyadı |
| `Telefon`   | VARCHAR(15)| Müşteri telefon numarası |
| `Email`     | VARCHAR(50)| Müşteri e-posta adresi |

### 3. **Satislar**
| Kolon Adı   | Veri Tipi  | Açıklama               |
|-------------|------------|------------------------|
| `SatisID`   | INT        | Birincil anahtar       |
| `UrunID`    | INT        | Satılan ürünün ID'si  |
| `MusteriID` | INT        | Satışı yapan müşteri ID'si |
| `Adet`      | INT        | Satıştaki ürün adedi  |
| `Tarih`     | DATETIME   | Satış tarihi          |

> Not: Tablo ilişkileri oluşturulurken `Urunler` ve `Musteriler` tabloları `Satis
