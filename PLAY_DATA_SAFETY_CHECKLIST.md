# Play Data Safety Checklist (Quiz Fatihi)

Bu dosya, Play Console `App content > Data safety` formunu doldururken hizli kontrol icin hazirlandi.

## 1) Uygulama veri topluyor mu?

Evet. Firebase Auth/Firestore/Realtime Database ve AdMob kullanildigi icin veri toplanir ve/veya islenir.

## 2) Koddan gorulen veri turleri (on kontrol)

- `Kullanici kimligi`:
  - Firebase Auth `uid`
  - Giris saglayici bilgisi (Google/Apple)
- `Kisisel bilgiler`:
  - E-posta (Google/Apple sign-in ile gelebilir)
  - Gorunen ad / nickname
- `Uygulama etkinligi`:
  - Oyun ici ilerleme/puan/oda durumlari (Firestore/RTDB)
- `Cihaz veya tanimlayicilar`:
  - Reklam tanimlayicisi (AdMob kullaniminda)

Not: Yukaridaki maddeler Play formunda birebir kategori secimine cevrilmelidir.

## 3) Veri amaci (tipik)

- Hesap yonetimi ve kimlik dogrulama
- Cok oyunculu oyun durumunun senkronizasyonu
- Reklam gosterimi ve olasi olcumleme
- Guvenlik/istismar onleme

## 4) Paylasim kontrolu

- Reklam SDK'si (Google Mobile Ads) tarafina veri aktarimi olabilir.
- Firebase servisleri Google altyapisina veri isler.

Play formunda "third-party sharing" kisimlari buna gore isaretlenmeli.

## 5) Guvenlik beyanlari

- Veri aktarimi: TLS/HTTPS ile iletilmeli (Firebase/AdMob varsayilan olarak bunu saglar).
- Hesap silme: Uygulama icinde hesap silme akisi var.

## 6) Mutlaka eslesmesi gerekenler

- Play Console Data Safety beyanlari ile uygulamanin gercek davranisi birebir ayni olmali.
- Privacy Policy URL yayinlanmis ve herkese acik olmali.
- Uygulama icinde privacy/terms linkleri erisilebilir olmali.

## 7) Bu projede duzeltilen ilgili nokta

- Ayarlar ekranina `GIZLILIK POLITIKASI` ve `KULLANIM KOSULLARI` butonlari eklendi.
- URL'ler su an placeholder:
  - `https://example.com/privacy-policy`
  - `https://example.com/terms-of-service`

Canliya cikmadan once bunlari gercek URL ile degistir.
