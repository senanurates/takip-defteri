<p align="center">
  <img src="icons/icon-192.png" width="96" height="96" alt="Takip Defteri">
</p>

<h1 align="center">Takip Defteri</h1>

<p align="center">
  <b>Seni kim geri takip etmiyor?</b> Instagram verini yükle; şifre vermeden, verin cihazından çıkmadan öğren.
</p>

<p align="center">
  <a href="https://senanurates.github.io/takip-defteri/">Canlı demo</a> ·
  <a href="https://senanurates.github.io/takip-defteri/gizlilik.html">Gizlilik politikası</a>
</p>

---

## Özellikler

- **Geri takip etmeyenler**: takip ettiğin ama seni takip etmeyen hesaplar
- **Takip etmediklerin**: seni takip eden ama senin takip etmediğin hesaplar
- **Karşılıklı takipler**
- **Takipten çıkanlar ve yeni takipçiler**: iki farklı tarihteki veriyi karşılaştırır
- Arama, sıralama, listeyi kopyalama ve profile tek tıkla gitme
- ZIP, JSON ve HTML dışa aktarma formatlarını destekler
- Örnek verilerle deneme modu

## Gizlilik

- Şifre ya da Instagram girişi **istemez**
- Dosya tamamen tarayıcıda işlenir, **hiçbir sunucuya gönderilmez**
- Arka uç (backend) yok, veritabanı yok, takip çerezi yok

## Nasıl çalışır?

1. Instagram'da **Hesap Merkezi → Bilgilerin ve izinlerin → Bilgilerini dışa aktar** adımlarını izleyerek "Takipçiler ve takip edilenler" verisini **JSON** formatında indir.
2. ZIP dosyasını siteye sürükle.
3. Uygulama `followers_*.json` ve `following.json` dosyalarını okur ve listeleri küme işlemleriyle karşılaştırır:

```
geri takip etmeyenler = takip edilenler − takipçiler
takip etmediklerin    = takipçiler − takip edilenler
karşılıklı            = takip edilenler ∩ takipçiler
takipten çıkanlar     = eski takipçiler − yeni takipçiler
```

## Teknolojiler

- Saf HTML, CSS ve JavaScript (framework yok)
- [JSZip](https://stuk.github.io/jszip/): tarayıcıda ZIP açma
- GitHub Pages: barındırma

## Yerelde çalıştırma

Kurulum gerekmez. `index.html` dosyasını tarayıcıda açman yeterli.

## Yol haritası

- [x] Web sürümü
- [ ] .NET MAUI Android uygulaması (geçmiş kayıtlar, takipçi grafiği, hatırlatma bildirimi)

## İletişim

Soru, öneri ve hata bildirimleri için: **takipdefteri.destek@gmail.com**

## Yasal not

Takip Defteri bağımsız bir projedir. Instagram veya Meta Platforms, Inc. ile bağlantılı değildir ve onlar tarafından onaylanmamıştır. Instagram, Meta Platforms, Inc.'nin ticari markasıdır.

© 2026 Sena Nur Ateş. Tüm hakları saklıdır.
