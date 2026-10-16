# Gajur Black Jack — Multiplayer

Multiplayer Blackjack (2–10 spelers) hostbaar op GitHub Pages. Spelers verbinden via WebRTC (PeerJS) met een host.

## Lokaal testen
Open `index.html` in je browser (of gebruik een lokale statische server).

## Hosten op GitHub Pages
1. Maak een nieuwe GitHub repository (bijv. `gajur-blackjack-mp`).
2. Push de bestanden (`index.html`, `README.md`) naar de `main` branch.
3. Ga naar **Settings → Pages**.
4. Bij *Source* kies **Deploy from a branch**, branch `main`, folder `/ (root)`.
5. Sla op. Na enkele minuten is het spel beschikbaar op `https://<jouw-gebruikersnaam>.github.io/gajur-blackjack-mp/`.

## Spelen
1. Één speler klikt **Host tafel**. Er verschijnt een *room code*.
2. De host deelt de room code (of de volledige URL) met vrienden.
3. Vrienden openen dezelfde GitHub Pages-link, voeren de room code in en klikken **Join**.
4. Iedereen zet een inzet in de lobby; de host klikt **Start ronde**.
5. Spelers gebruiken Hit/Stand/Double wanneer hun beurt is; dealer en afrekening worden door de host beheerd en gesynchroniseerd.

## Techniek
- PeerJS (WebRTC data channels) met de publieke PeerJS cloud als signalering.
- Host-autoritatieve spelstatus; clients renderen de gebroadcaste state.
- Geen backend nodig; puur statische frontend (geschikt voor GitHub Pages).

## Opmerkingen
- Werkt het beste met een fatsoenlijke internetverbinding voor alle spelers.
- Sommige institutionele netwerken blokkeren WebRTC; gebruik dan een ander netwerk of mobiele hotspot.
- Bij wegvallen van de host stopt het spel; een nieuwe host moet opnieuw starten.
