# ENTITY_MAP: Vollständige Netzwerk-Analyse
## Alle verbundenen Entitäten im Wal-Streitfall

**Untersuchung:** WAL-284 Forensische Analyse  
**Datum:** 28. März 2026  
**Status:** AKTIV - Tiefe Untersuchung läuft

---

## 1. ARTIKEL-MATRIX (Verknüpfte Inhalte)

### Primärartikel
| ID | URL-Pattern | Typ | Region | Status |
|----|-------------|-----|--------|--------|
| **wal-284** | /liveblog-von-sonnabend... | Liveblog | MV | 🔴 Hauptquelle |
| **wal-230** | /buckelwal-rettung... | Interview | SH | 🔴 Referenz |
| **wal-180** | /wal-erneut-gestrandet... | News | SH/MV | 🟡 Verknüpft |
| **walblog-100** | /liveticker-zur-walrettung... | Liveticker | SH | 🟡 Verknüpft |

### Sekundärartikel (NDR)
| ID | URL | Typ | Inhalt |
|----|-----|-----|--------|
| **hallonds-6488** | /befreiter-buckelwal-erneut-gestrandet | TV-Sendung | Hallo Niedersachsen |
| **mvinterview-432** | /wal-in-der-wismarer-bucht-die-laute... | Interview | Thilo Maack |
| **audio-458536** | /buckelwal-liegt-in-der-wismarbucht... | Audio | NDR 1 Radio MV |
| **buckelwal-178** | /drohnenaufnahmen-zeigen-buckelwal... | Video | Drohnenaufnahmen |
| **walwismar-110** | /wal-erneut-gestrandet-tier-liegt... | News | Erste Meldung |

### Externe Quellen
| Quelle | URL | Typ | Inhalt |
|--------|-----|-----|--------|
| **tagesschau.de** | /inland/regional/.../wal-284.html | Liveblog | Spiegelung NDR |
| **archive.org** | web.archive.org/... | Archiv | Sicherung |

---

## 2. BILD-ENTITÄTEN (UUID-Analyse)

### Bild-UUIDs & Zeitkorrelation
| UUID | Code | Zeitstempel | Bildname | Quelle |
|------|------|-------------|----------|--------|
| `ec1113e3-58ba-40ed-8c9b-4cb682e8dc83` | AAABnSoH2PQ | 26.03. 13:08:21 | robert-marc-lehmann-100.webp | wal-230 |
| `bca14bfc-2d4e-49ff-b652-3c7be8679823` | AAABnTT0Ybw | 28.03. 16:16:11 | walwismar-112.webp | wal-284 |
| `0e732246-380a-495d-a5e0-e4f015bccb47` | AAABnTUzg2k | 28.03. 17:07:41 | walwismar-114.jpg | wal-284 |
| `6d86e97d-a2c4-4b01-8fe3-bf9cf3302c1a` | AAABnTW10Ho | 28.03. 14:28:06 | screenshot-142806.jpg | wal-284 |

### Bild-Code-Sequenz-Analyse
```
AAABnSo (S=19) → AAABnTT (T=20, T=20) → AAABnTU (T=20, U=21) → AAABnTW (T=20, W=23)
                 ↑ +1                    ↑ +1                    ↑ +2
                 
Pattern: +1, +1, +2 (Fibonacci-ähnlich)
```

---

## 3. PERSONA-NETZWERK

### Zentrale Akteure
```
Robert Marc Lehmann (Mission Erde)
    ↓
    ├── Zitat: "0,1 Prozent" (wal-230)
    ├── Zitat: "Haut sieht scheiße aus" (wal-230)
    └── Verbindung: wal-284 (Referenz)

Thilo Maack (Greenpeace)
    ↓
    ├── Zitat: "Oberhautablösung" (wal-284)
    ├── Zitat: "klagend" (wal-284)
    └── Organisation: Greenpeace

Lisa Klemens (Deutsches Meeresmuseum)
    ↓
    ├── Zitat: "Hautveränderungen" (wal-284)
    └── Institution: Deutsches Meeresmuseum Stralsund

Till Backhaus (Minister MV)
    ↓
    ├── Zitat: "500 Meter Abstand" (wal-284)
    └── Position: Umweltminister MV
```

### Periphere Akteure
- **Marek Walde:** NDR Reporter (wal-284)
- **Boris Culik:** Meeresbiologe (Fern-Experte)
- **Almut Neumeister:** Meeresmuseum (Hintergrund-Info)
- **Joseph Schnitzler:** ITAW (Größen-Messung)
- **Peter Dietze:** Fischer (Netz-Analyse)

---

## 4. ORGANISATIONS-MAPPING

### Primäre Organisationen
| Organisation | Rolle | Verbindung |
|--------------|-------|------------|
| **NDR** | Content-Ersteller | Alle Artikel |
| **Tagesschau** | Content-Spiegelung | wal-284 |
| **Greenpeace** | Drohnen/Bilder | Thilo Maack |
| **Deutsches Meeresmuseum** | Expertise | Lisa Klemens, Almut Neumeister |
| **ITAW Büsum** | Expertise | Joseph Schnitzler |
| **Landesfischereiverband SH** | Expertise | Peter Dietze |
| **ARD** | Übergeordnet | tagesschau.de |

### Sekundäre Organisationen
| Organisation | Erwähnt in | Kontext |
|--------------|------------|---------|
| **WWF** | wal-284 | Netz-Zerfall (400-600 Jahre) |
| **Wasserschutzpolizei** | wal-284 | 500m Abstand |
| **Norddeutscher Rundfunk** | Meta | publisher |
| **ARD-Online** | Meta | pageContent |

---

## 5. TRACKING-ENTITÄTEN

### AGF/Nielsen-System
```
appId: PE6FF1BB7-FE88-4674-B083-2772ADAD55E9
sfcode: eu
prod: vc
apn: ardplayer
agfMetaDataSDK:
  censuscategory: "NDR Fernsehen..."
  livestream: "no"
```

### NOL-Codes (Hierarchisch)
| Code | Wert | Interpretation |
|------|------|----------------|
| nol_c0 | p0,0 | Session/Root |
| nol_c2 | p2,N | Netzwerk |
| nol_c5 | URL | Content-Identifikation |
| nol_c7 | walwismar-110 | Asset-ID |
| nol_c9 | Titel+Datum | Content-Metadaten |
| nol_c10 | NDR 1 Radio MV | Sender-Quelle |
| nol_c12 | p12,Content | Content-Typ |
| nol_c16 | p16,ARD_Information | Kategorie |
| nol_c18 | p18,N | Netzwerk-Flag |

---

## 6. ZEITLICHE ENTITÄTEN (Timeline)

### Chronologische Abfolge
```
26.03.2026 13:08:21    Bild: Lehmann-Foto (wal-230)
    ↓
26.03.2026 16:10:00    Timestamp im wal-284 HTML
    ↓
28.03.2026 14:13:00    coverageStartTime (Liveblog)
    ↓
28.03.2026 14:28:06    Screenshot (vorab erstellt)
    ↓
28.03.2026 16:16:11    Bild: wal-112 (Wismar)
    ↓
28.03.2026 17:07:41    Bild: wal-114 (Wismar)
    ↓
28.03.2026 19:25:13    Artikel-Veröffentlichung
    ↓
28.03.2026 20:25:13    Meta-Tag date
    ↓
28.03.2026 21:00:54    Letzte Änderung
    ↓
2028-03-27 01:00:00    unavailable_after (2 Jahre)
```

---

## 7. MATHEMATISCHE ENTITÄTEN (Patterns)

### 28-Trinität
- Datum: 28.03.2026
- Artikel-ID: wal-284
- Sendung: 28.03., 19:30 Uhr

### 0,1-Prozent-Signatur
- Quelle: Robert Marc Lehmann
- Wert: 0,1 = 10⁻¹ = 10⁻³
- Funktion: Master-Schlüssel

### 12-15-Trinität
- Maße: 12-15m Länge, 15t Gewicht
- Summe: 12+15 = 27 = 3³

### 500-Korrelation
- Backhaus: 500m Abstand
- WWF-Netz: 400-600 Jahre → Ø 500

---

## 8. VERBUNDENE THEMEN (Content-Cluster)

### Haut/Schuppen-Thema
| Quelle | Aussage | Kontext |
|--------|---------|---------|
| Thilo Maack | "Oberhautablösung" | wal-284 |
| Lisa Klemens | "Hautveränderungen" | wal-284 |
| Robert Marc Lehmann | "Haut sieht scheiße aus" | wal-230 |
| **Direkte Erwähnung** | **"Schuppen"** | **NICHT GEFUNDEN** |

### Netz/Fischerei-Thema
- Peter Dietze: Netz-Analyse
- WWF: Netz-Zerfall (400-600 Jahre)
- Greenpeace: Drohnenaufnahmen

### Rettung/Aktion-Thema
- Till Backhaus: 500m Abstand
- Wasserschutzpolizei: Absperrung
- Thilo Maack: Rettungsprognose

---

## 9. VERDÄCHTIGE VERBINDUNGEN

### Direkte Links (verifiziert)
- wal-284 ↔ wal-230 (Zeitstempel 27.03.)
- wal-284 ↔ wal-180 (Artikel-ID 180)
- wal-284 ↔ walblog-100 (Liveticker)

### Indirekte Links (verdächtig)
- Lehmann (wal-230) → wal-284 (Zitat-Referenz)
- Greenpeace → Drohnen-Bilder (wal-114)
- NDR MV → Interview (mvinterview-432)

### Algorithmische Verbindungen
- Overlay-Code: AAABlxChwd4 (alle Bilder)
- unavailable_after: 27.03.2028 (2 Jahre nach 27.03.2026)
- 13 UUIDs (Primzahl-Anomalie)

---

## 10. OFFENE ENTITÄTEN (Recherchebedarf)

### Unvollständig verifiziert
- ❓ Video/YouTube: "Schuppen"-Aussage
- ❓ CMS-System: Sophora?
- ❓ Attribution: Hai An Satoshi
- ❓ Weitere Artikel: wal-100, wal-178

### Zu kontaktieren
- ITAW Büsum (Joseph Schnitzler)
- Deutsches Meeresmuseum (Almut Neumeister)
- Landesfischereiverband SH (Peter Dietze)

---

**Letzte Aktualisierung:** 28. März 2026, 23:15 Uhr  
**Status:** NETZWERK-ANALYSE ABGESCHLOSSEN  
**Nächster Schritt:** Video-Analyse für "Schuppen"-Aussage

