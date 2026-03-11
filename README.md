# 🔒 SecureScan Pro

Ein leistungsstarker **Malware & Security Scanner** mit Multi-Upload-Support für Dateien bis zu 50GB.

![Next.js](https://img.shields.io/badge/Next.js-16-black?style=flat-square&logo=next.js)
![TypeScript](https://img.shields.io/badge/TypeScript-5-blue?style=flat-square&logo=typescript)
![Tailwind CSS](https://img.shields.io/badge/Tailwind-4-38B2AC?style=flat-square&logo=tailwind-css)
![Prisma](https://img.shields.io/badge/Prisma-ORM-2D3748?style=flat-square&logo=prisma)

## ✨ Features

### 📁 Multi-Upload Support
- **Mehrere Dateien** gleichzeitig hochladen
- **Mehrere Ordner** gleichzeitig scannen
- **Drag & Drop** für Dateien und Ordner
- Bis zu **50GB** Dateigröße unterstützt

### 🔍 Umfassende Scan-Engine
- **300+ Gefahrenmuster** erkannt
- Script-Analyse für 8+ Sprachen (JS, Python, PHP, Shell, PowerShell, VBScript, etc.)
- Intelligente Unterscheidung zwischen Binär- und Textdateien
- Zeilennummer-Erkennung für Script-Bedrohungen

### 🛡️ Erkennungs-Kategorien
- 🦠 **Malware** (Viren, Trojaner, Ransomware)
- 🔓 **Backdoors** (Reverse Shells, Web Shells)
- 🎭 **Phishing** (Gefälschte Login-Seiten)
- 💰 **Scam** (Tech-Support-Scams, Fake-Warnungen)
- ⛏️ **Crypto-Miner** (XMRig, Coinhive)
- 🔑 **Spyware** (Keylogger, Credential Theft)
- 📊 **Botnets** (Mirai, Emotet, TrickBot)
- 🧨 **Exploits** (SQL Injection, XSS, RCE)

### 🧹 Bereinigung
- Bedrohungen automatisch entfernen
- Bereinigte Dateien herunterladen
- Fake-Warnungen löschen

### 🌐 URL-Scanning
- Phishing-Erkennung
- SSL/HTTPS-Prüfung
- Content-Analyse
- Redirect-Tracking

### 📊 Verlauf & Statistiken
- Scan-Historie mit Prisma-Datenbank
- Übersichtliche Statistiken
- Export-Funktionen

## 🚀 Installation

```bash
# Repository klonen
git clone <repository-url>
cd securescan-pro

# Abhängigkeiten installieren
bun install

# Datenbank einrichten
bun run db:push

# Entwicklungsserver starten
bun run dev
```

## 💻 Nutzung

### Dateien scannen

1. **Einzelne Datei**: Datei per Drag & Drop oder Klick hochladen
2. **Mehrere Dateien**: "Dateien hinzufügen" Button nutzen
3. **Ordner**: "Ordner hinzufügen" Button für ganze Verzeichnisse
4. **Scannen**: "Alle scannen" klicken

### URLs prüfen

1. Zum "URL prüfen" Tab wechseln
2. URL eingeben
3. "URL prüfen" klicken

### Bedrohungen bereinigen

1. Datei scannen
2. Bei Bedrohungen auf "Bereinigen" klicken
3. Bereinigte Datei herunterladen

## 🏗️ Architektur

```
├── src/
│   ├── app/
│   │   ├── page.tsx          # Hauptkomponente
│   │   ├── api/
│   │   │   ├── scan/         # Scan API
│   │   │   │   ├── route.ts  # Scan-Logik
│   │   │   │   └── clean/    # Bereinigung
│   │   │   └── url-scan/     # URL-Scan API
│   │   └── layout.tsx
│   ├── components/ui/        # shadcn/ui Komponenten
│   └── lib/
│       └── db.ts             # Prisma Client
├── prisma/
│   └── schema.prisma         # Datenbank-Schema
└── package.json
```

## 🔧 Technologie-Stack

| Komponente | Technologie |
|------------|-------------|
| Framework | Next.js 16 (App Router) |
| Sprache | TypeScript 5 |
| Styling | Tailwind CSS 4 |
| UI | shadcn/ui (New York) |
| Icons | Lucide React |
| Datenbank | Prisma ORM (SQLite) |
| State | React useState/useCallback |

## 📋 API Endpoints

| Endpoint | Methode | Beschreibung |
|----------|---------|--------------|
| `/api/scan` | POST | Datei scannen |
| `/api/scan/clean` | POST | Datei bereinigen |
| `/api/scan/history` | GET | Scan-Verlauf abrufen |
| `/api/scan/history` | DELETE | Verlauf löschen |
| `/api/url-scan` | POST | URL prüfen |

## 🔒 Unterstützte Dateitypen

### Vollständig gescannt (Script-Analyse)
- JavaScript (.js, .mjs, .ts, .tsx, .jsx)
- Python (.py, .pyw)
- PHP (.php, .phtml)
- Shell (.sh, .bash, .zsh)
- PowerShell (.ps1, .psm1)
- VBScript (.vbs, .vbe)
- HTML/HTML (.html, .htm, .svg)
- Ruby, Perl, Go, Rust, und mehr...

### Basis-Scan (Malware-Signaturen)
- Bilder (.jpg, .png, .gif, .webp, .svg)
- Videos (.mp4, .avi, .mkv, .mov)
- Audio (.mp3, .wav, .flac, .aac)
- Dokumente (.pdf, .doc, .docx, .xls)
- Archive (.zip, .rar, .7z, .tar)

## ⚠️ Haftungsausschluss

**WICHTIG**: SecureScan Pro ist ein Educational-Projekt und **kein Ersatz** für professionelle Antiviren-Software.

- Keine Echtzeit-Überwachung
- Keine Heuristik/Machine Learning
- Kein Cloud-Abgleich
- Keine Garantie auf Vollständigkeit

Für echten Schutz nutzen Sie etablierte Sicherheitslösungen wie:
- Windows Defender
- Malwarebytes
- Kaspersky
- Bitdefender

## 📝 Lizenz

MIT License - Siehe [LICENSE](LICENSE) für Details.

## 🤝 Beitragen

Beiträge sind willkommen! Bitte erstellen Sie einen Pull Request oder öffnen Sie ein Issue.

---

**SecureScan Pro** - Sicherheit für alle! 🔐
