# Sandık OCR + Tarayıcı Geri Sayım

Bu proje telefondaki ekranı Android MediaProjection ile yakalar, ML Kit OCR ile `MM:SS` benzeri süreleri arar ve telefonda `127.0.0.1:8765` adresinde bir tarayıcı sayfası açar.

## GitHub Actions ile APK oluşturma

1. GitHub'da yeni, boş bir repository oluştur.
2. Bu klasördeki dosyaların tamamını repository'ye yükle.
3. GitHub → Actions → `Build APK` → `Run workflow`.
4. İşlem bitince workflow çalışmasına gir.
5. `SandikOCR-debug-apk` artifact'ini indir.
6. ZIP'i aç ve `app-debug.apk` dosyasını telefona kur.

## Kullanım

1. Uygulamayı aç.
2. `Ekran OCR'yi Başlat` düğmesine bas ve Android'in ekran yakalama iznini ver.
3. Canlı yayını aç.
4. `Tarayıcı Geri Sayımını Aç` düğmesine bas.
5. Tarayıcıdaki sayfa OCR'nin bulduğu son `MM:SS` değerini geri saydırır.

### Önemli
- OCR tüm ekranı tarar; aynı ekranda birden fazla `MM:SS` varsa yanlış olanı seçebilir.
- Android ekran yakalama için sistem izni gerekir.
- Tarayıcı sayfası uygulamanın yerel sunucusundan gelir; internet sitesi değildir.
- İlk sürüm test amaçlıdır. Daha sonra yalnızca sandık sayacının bulunduğu bölgeyi OCR'layacak şekilde iyileştirilebilir.
