V121 — GERİ TUŞU + KEŞİF BİLGİLERİ
1) Telefon geri tuşu (www/v121.js):
   - Menülerde bir önceki adıma döner (Geri / Vazgeç / Kapat düğmesini bulup basar; Yeni Oyun → Mod seçimi → Geri gibi).
   - Maçta "Maçtan çıkmak istiyor musunuz?" sorar. Evet: tek kişilikte kayıt alınır ve ana menüye dönülür; Rank/online maçta
     terk = yenilgi (mevcut wcr_pending kuralı). Hayır: maça devam. Seçili ülke paneli açıksa önce panel kapanır; duraklatma menüsü açıksa oyuna döner.
   - Ana menüde 2 sn içinde iki kez geri = uygulamadan çıkış.
   - package.json'a @capacitor/app eklendi (kesin çıkış için). Yeni paket olduğundan: `npm install` sonra `npx cap sync android`.
     Paket yoksa history(popstate) yöntemi devreye girer.
2) Keşif bilgisi (www/v121facts.js): ikinci bilgisi olmayan 126 ülkeye 1'er ek bilgi (TR+EN). Artık 174 ülkenin hepsinde en az 2 bilgi var.
Test: cihazda/tarayıcıda ÇALIŞTIRILMADI (yalnızca sözdizimi kontrolü). Geri alma: V120 zip'i.
3) Üst bar yazı tipi: HUD çipleri (altın, ülke adı vb.) artık panelle aynı sans yazı tipini kullanır (www/v121.css).
4) Panel alt düğmeleri: Keşif / Elçi / Diplomasi 3 sütun, SALDIR tam genişlikte altta; artık sağdan taşmaz.
   Geri almak için index.html'deki v121.css satırını sil. Telefonda denenmedi.
5) Fethedilen bölgeye tıklayınca da "📜 Politikalar" menüsü açılır (kendi ülken gibi; Keşif/Saldır düğmeleri gösterilmez). Değişen: www/v17.js (satır ~120), www/v23.js (satır ~299). Telefonda denenmedi.
6) Seçili bölge artık oyuncunun değilse "📜 Politikalar" düğmesi panelden kalkar (www/v121.js sonu). Telefonda denenmedi.
