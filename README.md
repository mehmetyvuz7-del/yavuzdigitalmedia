# Yavuz Digital Media — yavuzdigitalmedia.com.tr

Bu depo, Yavuz Digital Media web sitesini GitHub Pages üzerinde yayınlar.

## GitHub'da kurulum

1. github.com'da ücretsiz hesap açın (hesabınız yoksa).
2. Sağ üstteki **+ → New repository** ile yeni bir depo oluşturun.
   - Ad: `yavuzdigitalmedia` (istediğiniz bir ad olabilir)
   - Görünürlük: **Public** (ücretsiz planda GitHub Pages yalnızca herkese açık depolarda çalışır)
3. Depo sayfasında **Add file → Upload files** deyin ve bu klasördeki **tüm dosyaları** sürükleyip bırakın
   (`.nojekyll` ve `CNAME` dosyaları da dahil). **Commit changes** ile kaydedin.
   - Gizli dosyalar (`.nojekyll`) görünmüyorsa: Windows'ta Gezgin → Görünüm → Göster → Gizli öğeler.
4. **Settings → Pages** bölümüne gidin:
   - Source: **Deploy from a branch**
   - Branch: **main** ve **/ (root)** → **Save**
   - Custom domain alanında `yavuzdigitalmedia.com.tr` yazdığını kontrol edin (CNAME dosyası bunu otomatik doldurur).

## Alan adını bağlama (Turkticaret.net paneli)

Turkticaret.net'te alan adınızın **DNS Yönetimi** bölümüne şu kayıtları ekleyin
(varsa aynı ada ait eski A / CNAME kayıtlarını silin):

| Tür   | Ad / Host | Değer                    |
|-------|-----------|--------------------------|
| A     | @         | 185.199.108.153          |
| A     | @         | 185.199.109.153          |
| A     | @         | 185.199.110.153          |
| A     | @         | 185.199.111.153          |
| AAAA  | @         | 2606:50c0:8000::153      |
| AAAA  | @         | 2606:50c0:8001::153      |
| AAAA  | @         | 2606:50c0:8002::153      |
| AAAA  | @         | 2606:50c0:8003::153      |
| CNAME | www       | KULLANICIADINIZ.github.io |

`KULLANICIADINIZ` yerine GitHub kullanıcı adınızı yazın (depo adını eklemeyin).

## HTTPS (kilit simgesi)

DNS kayıtları etkinleştikten sonra (birkaç dakika – 24 saat) **Settings → Pages** sayfasında
**Enforce HTTPS** kutusunu işaretleyin. Bu seçeneğin görünmesi 24 saate kadar sürebilir.

## Siteyi güncelleme

Değişen dosyayı **Add file → Upload files** ile aynı adla tekrar yükleyin; site birkaç dakika içinde güncellenir.
