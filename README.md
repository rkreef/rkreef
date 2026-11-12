<p align="center">
  <img src="logo.png" width="160" alt="RKREEF – Mořská akvária RK">
</p>

<h1 align="center">RKREEF · Mořská akvária RK</h1>

<p align="center">
  Mořská akvária na míru – návrh, výroba, montáž a servis po celé ČR.<br>
  <a href="https://rkreef.eu">rkreef.eu</a> · +420 735 548 756
</p>

---

## Co děláme

- **Mořská akvária na míru:** navrhneme, vyrobíme, dovezeme, zapojíme a předáme živé akvárium.
- **Vlastní přepadový systém**, chráněný užitným vzorem č. 38266.
- **Servis a havárie 24/7:** pomoc při poruše, péče o akvárium, ustájení zvířat.
- **Kurzy jeden na jednoho**, kde se naučíte o mořské akvárium starat sami.
- **E-shop** s technikou, chemií a vybavením pro mořskou akvaristiku: [rkreef.eu/eshop](https://rkreef.eu/eshop/)

## Software a firmware – vlastní vývoj

Elektroniku, firmware i aplikace si vyvíjíme sami. Zdrojový kód je zatím soukromý.

**RK LIGHT** (připravujeme): vlastní LED osvětlení mořského akvária.<br>
Hardware, firmware, aplikace i cloud jsou náš vlastní vývoj. Podali jsme přihlášku vynálezu PV 2026-277.
- **Světlo:** 6 nezávislých spektrálních kanálů (royal blue, blue, UV/violet, bílá, zelená, červená). Stmívání 19 kHz bez viditelného blikání, 1024 úrovní jasu, teplotní čidlo a řízený ventilátor.
- **Firmware** pro ESP32-C3 (C++, PlatformIO):
  - samostatná denní křivka pro každý kanál s plynulými přechody,
  - astronomický měsíční cyklus, efekty mraků a bouřky,
  - vícedenní aklimatizace korálů na nové světlo,
  - teplotní ochrana s postupným snížením výkonu,
  - nastavení Wi-Fi přes Bluetooth a aktualizace přes OTA.
  - Světlo jede podle programu samo, i bez aplikace a internetu.
- **Komunikace:** doma ovládání napřímo přes místní síť (rychlé a bez internetu), mimo domov přes cloud. Přepíná se automaticky.
- **Mobilní aplikace** (Flutter, Firebase):
  - průvodce prvním spuštěním,
  - ovládání jednoho světla i celého akvária naráz,
  - editor spektra a denního programu,
  - sdílení programů přes QR, zálohy v cloudu,
  - upozornění, když světlo vypadne.
  - Teď běží uzavřený test na Google Play.

**RK Control System** (ve vývoji, první deska jde do výroby): řídicí a měřicí jednotka celého akvária.<br>
Vlastní deska s ESP32, vlastní firmware a aplikace – navrženo podle profesionálních reef controllerů.
- **Měření:**
  - pH, ORP a salinita (vodivostní cela K=10) přes konektory BNC,
  - teplota (čidla DS18B20) a hladina (optický snímač pro dolívání nebo hlídání úniku vody),
  - přesný 16bitový převodník, měřicí část je **galvanicky oddělená** od napájení a Wi-Fi, takže sondy neruší zemní smyčky ani čerpadla v akváriu.
- **Řízení:** 2× výstup 0–10 V pro proudová čerpadla nebo stmívání (vlnové režimy, krmná pauza na tlačítko).
- **Kalibrace sond jako u profi controllerů:** pH dvoubodově, ORP a salinita jednobodově, hodnota se uloží až po ustálení sondy. Teplotní kompenzace pH i vodivosti.
- **Jak to funguje:**
  - jednotka měří a řídí sama, i bez internetu a bez aplikace; čas drží zálohované hodiny reálného času,
  - nastavení Wi-Fi přes Bluetooth, doma ovládání napřímo přes místní síť, mimo domov přehled stavu přes cloud,
  - aktualizace firmwaru přes OTA s digitálním podpisem a automatickým návratem k předchozí verzi při chybě,
  - hlídací watchdog a bezpečný režim, aby se jednotka po výpadku sama vzpamatovala.
- **Plán:** propojení s RK LIGHT, upozornění na mobil při odchylce hodnot, dávkování a chytré zásuvky.

**rkreef.eu**: web a e-shop
- Firebase Hosting, Firestore a Cloud Functions (Node.js).
- Vlastní pokladna, napojení na DPD, automatická synchronizace skladu a cen, faktury, věrnostní program, konfigurátor akvária a komunitní fórum.

<p>
  <img src="https://img.shields.io/badge/ESP32--C3-E7352C?logo=espressif&logoColor=white" alt="ESP32-C3">
  <img src="https://img.shields.io/badge/PlatformIO-F5822A?logo=platformio&logoColor=white" alt="PlatformIO">
  <img src="https://img.shields.io/badge/C%2B%2B-00599C?logo=cplusplus&logoColor=white" alt="C++">
  <img src="https://img.shields.io/badge/Flutter-02569B?logo=flutter&logoColor=white" alt="Flutter">
  <img src="https://img.shields.io/badge/Firebase-DD2C00?logo=firebase&logoColor=white" alt="Firebase">
  <img src="https://img.shields.io/badge/Node.js-339933?logo=nodedotjs&logoColor=white" alt="Node.js">
  <img src="https://img.shields.io/badge/Bluetooth_LE-0082FC?logo=bluetooth&logoColor=white" alt="Bluetooth LE">
</p>

## Kontakt

| | |
|---|---|
| Web | [rkreef.eu](https://rkreef.eu) |
| Telefon | +420 735 548 756 |
| E-mail | radekkrs@gmail.com |
| Instagram | [@morska_akvaria_rk](https://www.instagram.com/morska_akvaria_rk/) |
| TikTok | [@rkreef](https://www.tiktok.com/@rkreef) |
| Facebook | [Mořská akvária RK](https://www.facebook.com/profile.php?id=100016105538040) |
| YouTube | [@Morska-Akvaria](https://www.youtube.com/@Morska-Akvaria) |

<sub>Radek Kraus · IČO 19068085 · Šimonovice u Liberce</sub>
