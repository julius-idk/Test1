# Arma 3 – Quad Airdrop (SQF)

**Was es macht:** Per Tastenkombi **CTRL + O** kann jeder Spieler ein **Quad** anfordern. Es wird per **Fallschirm** abgeworfen, ein **Kartenmarker** hilft beim Finden, und nach Nutzung räumt sich alles wieder auf. **Cooldown:** 5 Minuten pro Spieler.

## Features
- **Einfache Bedienung:** Keybind → Scroll-Menü → „Request / Confirm / Cancel“
- **Fallschirmabwurf** exakt zur Spielerposition
- **Marker** pro Team/Seite, Auto-Cleanup (Einsteigen / Zerstören / Löschen / Timeout)
- **Hold-Action „Delete Quad“** vor Ort
- **Mehrspieler-robust:** `remoteExec`, `publicVariable`, JIP-Handling, Respawn-Reinit
- **Sicherheit:** Doppeltstart-Schutz, Cooldown

## Demo
Kurzvideo: https://youtu.be/V0gydLsA_js

## Installation
1. `src/quad_airdrop.sqf` in die Mission kopieren.  
2. In `mission_demo/init.sqf` (Beispiel unten) einbinden.  
3. Spiel starten, **CTRL + O** drücken, mit Mausrad bestätigen.

## Konfiguration (optional)
In `quad_airdrop.sqf`:
- `DROP_HEIGHT = 100;`   (Abwurfhöhe)
- `COOLDOWN = 300;`      (Sekunden)
- `VEH_CLASS = "B_Quadbike_01_F";` (Fahrzeugklasse)

## Technik
- Netzwerk: `remoteExec`, `publicVariable`, JIP-IDs
- Events: KeyDown, AddAction, GetIn/Killed/Deleted, Respawn
- Cleanup: Timer + Event-basiert

## Rechtlicher Hinweis
Nur in autorisierten Umgebungen nutzen. Keine Tests auf fremden Servern ohne Erlaubnis.

## Lizenz
MIT
