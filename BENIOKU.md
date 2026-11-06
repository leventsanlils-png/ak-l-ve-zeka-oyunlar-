# İnegöl Akıl ve Zeka Oyunları Süper Ligi – Android Uygulaması

Bu klasör, programın Android Studio projesidir. Uygulamanın tamamı `app/src/main/assets/index.html` dosyasındadır; Android tarafı bu dosyayı tam ekran çalıştırır.

## APK oluşturma – Yol 1: Android Studio

1. Android Studio'yu kurun: https://developer.android.com/studio
2. Bu zip dosyasını açın. Android Studio'da **File › Open** ile `SuperLig` klasörünü seçin.
3. İlk açılışta Android Studio gerekli bileşenleri kendisi indirir (internet gerekir, birkaç dakika sürebilir). "Gradle sync" bitene kadar bekleyin.
4. Menüden **Build › Build App Bundle(s) / APK(s) › Build APK(s)** seçin.
5. Bitince sağ altta çıkan bildirimde **locate**'e tıklayın. APK dosyası şuradadır:
   `app/build/outputs/apk/debug/app-debug.apk`

## APK oluşturma – Yol 2: Bilgisayara kurulum yapmadan (GitHub)

1. https://github.com adresinde ücretsiz hesap açın ve yeni bir depo (repository) oluşturun.
2. Bu klasördeki tüm dosyaları depoya yükleyin ("Add file › Upload files"; `.github` klasörü de yüklenmeli).
3. Depodaki **Actions** sekmesine gidin. "APK oluştur" çalışması kendiliğinden başlar (başlamazsa "Run workflow").
4. Çalışma bitince (yaklaşık 5 dakika) sayfanın altındaki **SuperLig-APK** dosyasını indirin; içinde `app-debug.apk` vardır.

## Telefona kurma

1. APK dosyasını telefona gönderin (WhatsApp, e-posta, USB…).
2. Dosyaya dokunun. Android "bilinmeyen kaynaklardan yüklemeye izin ver" diye sorarsa izin verin.
3. Uygulama "İnegöl Süper Lig" adıyla telefona kurulur.

## Uygulama hakkında

- Android 7.0 ve üzeri telefonlarda çalışır.
- Veriler telefonda kalıcı olarak saklanır. Başka telefona taşımak için **Ayarlar › Yedeği indir / Yedekten yükle** kullanılır.
- Excel (CSV) raporları ve yedek dosyaları telefonun **İndirilenler/SuperLig** klasörüne kaydedilir.
- **PDF / Yazdır** butonu Android'in yazdırma ekranını açar; buradan "PDF olarak kaydet" seçilebilir.
- TAZOF kural belgeleri gibi dış bağlantılar telefonun tarayıcısında açılır.
- Not: Android uygulamasında bulut kaydı yoktur; bulut kaydı yalnızca programın yayınlanan bağlantısında çalışır.

## Programı güncellemek

`app/src/main/assets/index.html` dosyasını yeni sürümle değiştirin, `app/build.gradle.kts` içindeki `versionCode` sayısını bir artırın (örn. 1 → 2) ve APK'yı yeniden oluşturun.

## Google Play'e yüklemek isterseniz

Android Studio'da **Build › Generate Signed Bundle / APK** ile kendi imza anahtarınızı oluşturup imzalı sürüm alın. İmza anahtarını (.jks) kaybetmeyin; güncellemeler için aynı anahtar gerekir.
