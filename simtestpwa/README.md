# Compensi S&T — Progressive Web App (PWA)

Questa cartella contiene una app web completa e installabile, pronta per essere
pubblicata online. Una volta ospitata su un dominio https, i partner possono
installarla come un'app vera sul telefono, senza passare da App Store o Google Play.

I dati inseriti (partner, attivazioni, importi) restano salvati **sul dispositivo**
di chi usa l'app (tramite `localStorage`), non su un server condiviso — ogni
telefono ha i propri dati.

## Pubblicarla online (gratis, senza scrivere codice)

**Opzione consigliata — Netlify Drop:**

1. Vai su https://app.netlify.com/drop
2. Trascina l'intera cartella `pwa` (questa cartella) nella pagina
3. In pochi secondi ottieni un link pubblico tipo `https://nome-a-caso.netlify.app`
4. Fatto — la app è online e installabile

**Alternativa — GitHub Pages:**

1. Crea un repository su GitHub e carica il contenuto di questa cartella
2. Vai in Settings → Pages, attiva la pubblicazione dal branch principale
3. Ottieni un link tipo `https://tuonome.github.io/repo`

Qualunque hosting statico https va bene (Vercel, Firebase Hosting, un tuo dominio, ecc.).

## Come i partner la installano sul telefono

**Su Android (Chrome):**
1. Apri il link della app in Chrome
2. Tocca il menu (⋮) → "Aggiungi a schermata Home" o "Installa app"
3. Conferma — comparirà un'icona come un'app normale

**Su iPhone (Safari — deve essere Safari, non funziona da Chrome su iOS):**
1. Apri il link della app in Safari
2. Tocca l'icona di condivisione (il quadrato con la freccia verso l'alto)
3. Scorri e tocca "Aggiungi a Home"
4. Conferma — comparirà un'icona sulla schermata Home

Da quel momento la app si apre a schermo intero, senza barra del browser, e
funziona anche offline dopo il primo avvio.

## File in questa cartella

- `index.html` — l'app vera e propria (versione aggiornata con: grafico a torta
  con fette toccabili e colori più luminosi, scontrino di componente con
  dettaglio completo, spaziature corrette in tutte le sezioni)
- `manifest.json` — dice al telefono nome, icona e colori dell'app
- `service-worker.js` — abilita il funzionamento offline
- `icons/` — icone dell'app nei formati richiesti da Android e iOS
