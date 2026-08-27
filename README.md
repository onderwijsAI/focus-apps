# Focus Apps

Personal focus tools: FocusTube (YouTube wrapper) and Focus Dashboard.

## LinkedIn-inbox (contract voor Dispatch/Claude)

`linkedin-inbox.json` is de brug tussen het Focus Dashboard en Davids LinkedIn-contentsysteem op de Mac. David kopieert in het dashboard zijn LinkedIn-wachtrij (knop "Kopieer voor Dispatch" in de instellingen, of het kopieer-icoon per artikel) en plakt die opdracht in een Dispatch-sessie op deze repo.

Wat Dispatch dan doet:

1. Voeg de items toe aan de lijst in `linkedin-inbox.json`. Nooit overschrijven, altijd toevoegen.
2. Per item drie velden: `titel` (string), `link` (URL), `datum` (ISO 8601, moment van doorgeven).
3. Sla geen item op dat er al in staat (zelfde `link`).
4. Commit en push naar `main`.

De LinkedIn-ochtendbriefing op de Mac leest dit bestand via de raw-URL en behandelt elk item als eigen aandracht van David. Verwerkte items blijven staan; het systeem ontdubbelt zelf tegen eerdere briefings.
