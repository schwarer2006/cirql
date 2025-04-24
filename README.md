# cirql
Cirql – Kein Messenger für Katzenbilder 

# 🔐 Cirql – Secure POC Messenger (USB-ready)

**Cirql** ist ein experimentelles, modulares Kommunikationsprotokoll für sichere, verschlüsselte Nachrichtenübermittlung.  
Dieser Proof-of-Concept (POC) läuft vollständig lokal – ideal für den Einsatz auf USB-Sticks, in VirtualBox-Umgebungen oder abgesicherten Netzwerken.

---

## 🧰 Hauptfunktionen

- **Chunk-basierte Nachrichtenübertragung**  
  → Nachricht wird in gleich große Fragmente (Chunks) zerlegt.

- **AES-256-GCM Verschlüsselung pro Chunk**  
  → Jeder Chunk erhält eigene Nonce, sichere Einzelverarbeitung.

- **SHA3-256 Digest-Verifikation**  
  → Erkennt jede Manipulation durch Vergleich des Digests.

- **Dummy-Chunk Obfuskation**  
  → Schutz gegen Traffic-Analyse durch täuschend echte Platzhalterdaten.

- **Temporärer Relay-Puffer (volatile)**  
  → Kein Klartext, keine Logs, kein Social Graph.

- **Tor & Onion-Service Support**  
  → Cirql unterstützt den Betrieb über das Tor-Netzwerk – inklusive optionalem Onion-Link für relaybasierte Kommunikation ohne sichtbare IP, ideal für vertrauliche Umgebungen und anonyme Nutzung.
  

---

## 📁 Projektstruktur (Ausschnitt)

```bash
cirql_secure_gui_usb_poc/
├── backend/api/         # Verschlüsselung, Digest, I/O
├── frontend/            # Webbasierter Messenger-Client (PWA-kompatibel)
├── tmp/                 # Simulierter Relay-Buffer
└── README.md

