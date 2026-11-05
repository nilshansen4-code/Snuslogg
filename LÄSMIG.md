# Snuslogg

En webbapp för iPhone som du lägger på hemskärmen. Ett tryck sparar klockslag och GPS-position. All data finns bara på telefonen.

## Installera (cirka 5 minuter)

Appen behöver HTTPS för att få använda GPS. Enklast är GitHub Pages:

1. Skapa ett nytt repo på GitHub, t.ex. `snuslogg`. Ett privat repo kräver GitHub Pro för Pages, annars publikt.
2. Ladda upp alla filer i mappen (`index.html`, `manifest.json`, `icon-*.png`).
3. Gå till Settings → Pages → Source: *Deploy from a branch* → `main` / root → Save.
4. Öppna adressen (`https://<användarnamn>.github.io/snuslogg/`) i **Safari** på iPhonen.
5. Dela → **Lägg till på hemskärmen**.
6. Öppna appen från hemskärmen och tillåt platsåtkomst. Välj *Fråga nästa gång eller när jag delar* eller *När appen används*.

Adressen innehåller ingen data och syns inte för någon som inte känner till den. Själva loggningarna lämnar aldrig telefonen.

## Så fungerar den

- **Logga**: ett tryck sparar tid direkt. Positionen hämtas i bakgrunden.
- **Plats som lär sig**: första gången skapar du en plats (Hemma, Jobbet …). Nästa gång du är inom cirka 150 m föreslår appen den automatiskt (markeras *Föreslagen*). Tryck på en annan plats om förslaget är fel. Varje bekräftat val finjusterar platsens mittpunkt.
- **Situation**: valfri tagg. Egna taggar kan läggas till.
- **Historik**: tryck på en loggning för att ändra plats, situation eller tid, eller ta bort den.
- **Mönster**: tid på dygnet, veckodag, plats, situation och korta iakttagelser för 7 dagar, 30 dagar eller allt.
- **Data**: exportera CSV (semikolonseparerad, öppnas i Numbers/Excel) eller en JSON-säkerhetskopia via delningsmenyn. Säkerhetskopian kan läsas in igen.

## Bra att veta

- Data sparas i Safaris lagring för appen. Om du tar bort appen från hemskärmen eller rensar webbplatsdata i Safari försvinner den. **Exportera en säkerhetskopia ibland.**
- Om du uppdaterar `index.html` i repot behålls din data, så länge adressen är densamma.
