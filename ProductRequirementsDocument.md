## 📄 *Product Requirements Document (PRD)*

### Projektname (Arbeitstitel): **Morning Buddy** ☀️🎧

*(Name ist Platzhalter – kann später „lustiger“ werden)*

---

## 1. Ziel & Motivation

Ziel der App ist es, **Kinder morgens strukturiert, selbstständig und stressfrei** durch ihre Morgenroutine zu begleiten, damit sie **pünktlich zur Schule** kommen.

Die App nutzt:

* **akustische Signale**
* **kindgerechte, lustige Pop-ups**
* **klare, sequenzielle Aufgaben**
* **Bestätigung durch das Kind („Erledigt“)**

um Ablenkung (z. B. durch Hörspiele) zu reduzieren und Orientierung zu geben.

---

## 2. Zielgruppe

**Primäre Zielgruppe**

* Kinder im Grundschulalter
* eigenes Android-Smartphone
* hören morgens Hörspiele / Audioinhalte

**Sekundäre Zielgruppe**

* Eltern, die Struktur vorgeben wollen
* möglichst wenig manuell eingreifen möchten
* Transparenz über den Morgenablauf schätzen

---

## 3. Kernanforderungen (Must-Have)

### 3.1 Morgenroutine als geführte Sequenz

* Die Routine besteht aus **aufeinanderfolgenden Aufgaben**
* Immer **nur eine Aufgabe gleichzeitig sichtbar**
* Nächste Aufgabe erscheint **erst nach Bestätigung**

Beispiel:

1. 🍽️ Frühstück
2. 🪥 Zähne putzen
3. 🚽 Toilette
4. 👕 Anziehen
5. 💊 Medikamente
6. 🎒 Bereitmachen / Losgehen

---

### 3.2 Benachrichtigungen & Pop-ups

* Akustisches Signal (konfigurierbar)
* Heads-up / Fullscreen-Notification (Android)
* Kindgerechte Texte, Emojis, Humor
* Wiederholtes Erinnern, falls keine Reaktion erfolgt

---

### 3.3 Bestätigung & Interaktion

Jede Aufgabe bietet mindestens:

* ✅ **„Erledigt“**
* ⏰ **„Noch 2–5 Minuten“** (konfigurierbar)

Optional:

* 🤒 **„Heute krank“** → beendet alle weiteren Aufgaben

---

### 3.4 Zeitlogik

* Aufgaben können:

  * eine **empfohlene Dauer**
  * eine **späteste Endzeit** haben
* Bei Überschreitung:

  * Eskalation (anderer Ton, andere Nachricht)

---

## 4. Kalender- & Tageslogik

### 4.1 Schultage

* Routinen sind standardmäßig **Mo–Fr aktiv**
* Wochenenden optional eigene Routine

### 4.2 Ferien

* Unterstützung eines **Ferienkalenders (ICS)**

  * z. B. offizieller Ferienkalender Bundesland
* An Ferientagen:

  * Schulroutine deaktiviert
  * alternative „Ferienroutine“ möglich

### 4.3 Krankentag

* Schnell-Auswahl:

  * per Button im ersten Popup
  * optional für den ganzen Tag gültig
* Keine weiteren Reminder an diesem Tag

---

## 5. Konfiguration

### 5.1 Aufgabenverwaltung

* Aufgaben:

  * Name
  * Emoji/Icon
  * Dauer (optional)
  * Reihenfolge
* einfache Bearbeitung durch Eltern

### 5.2 Routinen

* Mehrere Routinen möglich:

  * Schule
  * Ferien
  * Wochenende
* Zuordnung nach Tagestyp

---

## 6. Nicht-funktionale Anforderungen

### 6.1 Plattform

* **Android**
* Offline-fähig
* Keine Cloud zwingend notwendig (MVP)

### 6.2 Zuverlässigkeit

* Alarme dürfen nicht von Energiesparmechanismen „geschluckt“ werden
* App führt Nutzer aktiv durch nötige Android-Berechtigungen

### 6.3 Datenschutz

* Keine personenbezogenen Daten nach außen
* Alle Daten lokal auf dem Gerät (MVP)

---

## 7. UX / Design-Leitlinien

* kindgerecht, freundlich, nicht überladen
* große Buttons
* klare Farben
* Humor statt Druck
* kein „Bestrafen“, nur Erinnern & Struktur

Optional später:

* Lobtexte
* kleine Animationen
* Fortschrittsanzeige („Noch 2 Schritte!“)

---

## 8. MVP-Abgrenzung (bewusst **nicht** enthalten)

* kein Login / Benutzerkonten
* keine Cloud-Synchronisation
* kein Punktesystem / Belohnungen
* keine Mehrkind-Verwaltung
* kein App-Store-Release-Overhead

---

## 9. Technische Umsetzung (MVP-Vorschlag)

**Frontend**

* Flutter (Android-Fokus)

**Logik**

* State-Machine für Aufgabenfolge
* lokale Persistenz (SharedPreferences / SQLite)

**Systemintegration**

* Android Notifications
* AlarmManager / WorkManager
* optionale Kalender-ICS-Imports

---

## 10. Erfolgskriterien

* Kind kommt häufiger pünktlich zur Schule
* weniger elterliche Eingriffe am Morgen
* Routine wird als „Hilfe“, nicht als Kontrolle wahrgenommen
* App wird morgens freiwillig akzeptiert
