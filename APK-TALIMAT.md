# O'Nail APK Oluşturma Talimatı

## En Kolay Yol: PWABuilder (Önerilen)

1. Tarayıcıda şu siteye git:
   👉 https://www.pwabuilder.com

2. URL kutusuna gir:
   ```
   https://ilgazkaragenc.github.io/tirnak-studyo/randevu-app.html
   ```

3. "Start" butonuna bas → Analiz tamamlanana kadar bekle

4. "Package for stores" → **Android** seç

5. "Generate Package" butonuna bas

6. APK dosyasını indir → Telefona kopyala → Yükle

---

## Alternatif: Bubblewrap CLI

```bash
npm install -g @bubblewrap/cli
bubblewrap init --manifest=https://ilgazkaragenc.github.io/tirnak-studyo/manifest.json
bubblewrap build
```

---

## ÖNEMLİ: assetlinks.json

APK'nın çalışması için GitHub'a şu dosyayı yüklemelisin:
- Klasör: `.well-known/`
- Dosya adı: `assetlinks.json`
- İçerik: `assetlinks.json` dosyasındaki SHA256 fingerprint'i
  PWABuilder'dan indirdiğin APK'nın SHA256'sıyla güncellemelisin.

PWABuilder bunu otomatik yapar ve SHA256'yı sana verir.
