# DroneSkyCheck Ecosystem – APK Distribution

Questo repository contiene gli **APK ufficiali** delle applicazioni che compongono l’ecosistema **DroneSkyCheck**.

Le app qui presenti **non sono distribuite tramite Google Play Store** e sono destinate a utenti tecnici, piloti UAS e sviluppatori che desiderano installarle manualmente su dispositivi Android e Wear OS.

---

## 📦 Applicazioni disponibili

- **DroneSkyCheck.apk**  
  App principale per la consultazione dello spazio aereo UAS, meteo, NOTAM e traffico.

- **DroneSkyCheckCompanion.apk**  
  Companion app per smartphone Android, utilizzata in supporto all’ecosistema DroneSkyCheck.

- **AirSense.apk**  
  App Android per la ricezione e visualizzazione di traffico UAS tramite Remote ID / Drone ID.

- **DroneSkyCheckHUD_1.5.apk**  
  App standalone per smartwatch Wear OS, pensata come HUD informativo per il pilota.

---

## ⚠️ Avvertenze importanti

- Gli APK sono **firmati e pronti all’uso**, ma **non aggiornati automaticamente**.
- L’installazione richiede l’abilitazione delle **origini sconosciute**.
- Per Wear OS è necessario utilizzare **ADB**.
- Questo repository **non contiene il codice sorgente**.

---

## 📲 Installazione su smartphone Android

### Requisiti
- Smartphone Android
- File APK scaricato
- Abilitazione installazione da origini sconosciute

### Procedura
1. Scarica l’APK desiderato sullo smartphone
2. Apri il file APK
3. Concedi il permesso di installazione da origini sconosciute
4. Completa l’installazione

Le seguenti app possono essere installate direttamente su smartphone:
- DroneSkyCheck
- DroneSkyCheckCompanion
- AirSense

---

## ⌚ Installazione su smartwatch Wear OS (ADB)

Le app Wear OS **non possono essere installate aprendo direttamente l’APK**.  
È necessario utilizzare **ADB**.

### Requisiti
- Smartwatch Wear OS
- PC (Windows / Linux / macOS)
- ADB installato
- Smartwatch e PC sulla **stessa rete Wi-Fi**

---

### 1️⃣ Abilitare le Opzioni sviluppatore sullo smartwatch

- Impostazioni → Informazioni
- Tocca più volte **Versione** fino ad abilitare le opzioni sviluppatore
- Abilita:
  - Debug ADB
  - Debug tramite Wi-Fi

---

### 2️⃣ Collegare ADB allo smartwatch

Dal PC:

```bash
adb connect IP_DELLO_SMARTWATCH:5555
```

Verifica la connessione:

```bash
adb devices
```

---

### 3️⃣ Installare l’APK Wear OS

Esempio per **DroneSkyCheckHUD**:

```bash
adb install DroneSkyCheckHUD_1.5.apk
```

Per aggiornare una versione già installata:

```bash
adb install -r DroneSkyCheckHUD_1.5.apk
```

Al termine, l’app comparirà nel launcher dello smartwatch.

---

## 🔄 Aggiornamenti

Gli aggiornamenti avvengono manualmente:
- scaricare il nuovo APK
- reinstallare l’app su smartphone
- oppure usare `adb install -r` su Wear OS

---

## 🛠️ Destinatari

Queste applicazioni sono pensate per:
- Piloti UAS
- Operatori tecnici
- Utenti avanzati
- Attività di test e sperimentazione operativa

Non sono pensate per un’installazione consumer “one-click”.

---

## 📌 Note finali

- Le app non sostituiscono servizi ufficiali di controllo o autorizzazione al volo.
- Le informazioni fornite sono **di supporto alla consapevolezza operativa**.
- L’utilizzo delle app è sotto la **responsabilità dell’utente**.
