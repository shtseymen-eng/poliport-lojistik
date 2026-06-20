# Poliport Lojistik — Kurulum ve Yayın Talimatı

## SEÇENEK 1 — Ücretsiz İnternet Linki (Netlify — En Kolay, 2 Dakika)

1. https://app.netlify.com/drop adresine gidin (hesap gerekmez)
2. `app/index.html` dosyasını sayfaya sürükleyin
3. Otomatik link oluşur: `https://xxxx.netlify.app`
4. İstediğiniz zaman güncellemek için aynı adımı tekrar yapın

---

## SEÇENEK 2 — GitHub Pages (Ücretsiz, Kalıcı Link)

### Adım 1: GitHub hesabı açın
https://github.com → Sign Up

### Adım 2: Yeni repo oluşturun
- New repository → name: `poliport-lojistik` → Public → Create

### Adım 3: `poliport-deploy` klasörünü yükleyin
```
git clone https://github.com/KULLANICI_ADI/poliport-lojistik
# İçine tüm dosyaları kopyalayın
git add .
git commit -m "ilk sürüm"
git push
```

### Adım 4: GitHub Actions otomatik çalışır
- Actions sekmesinde "Build & Deploy" işlemi başlar
- Biter bitmez:
  - 🌐 **Web linki**: `https://KULLANICI_ADI.github.io/poliport-lojistik`
  - 💾 **Windows .exe**: Actions → son run → Artifacts → indir
  - 🍎 **macOS .dmg**: Actions → son run → Artifacts → indir

---

## SEÇENEK 3 — Windows/Mac Masaüstü Uygulaması (Yerel Build)

Node.js kurulu bir bilgisayarda (https://nodejs.org):

```bash
cd poliport-deploy
npm install
npm run dist-win    # → dist/Poliport Lojistik Setup.exe
npm run dist-mac    # → dist/Poliport Lojistik.dmg
```

---

## Güncelleme Nasıl Yapılır?

`app/index.html` dosyasını yeni sürümle değiştirip:
- Netlify: tekrar sürükle-bırak
- GitHub: `git push` → Actions otomatik günceller
