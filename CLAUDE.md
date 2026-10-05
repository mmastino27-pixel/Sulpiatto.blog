# Sul Piatto: istruzioni di lavoro

Blog italiano di recensioni di dischi, vinili, concerti e guide: sulpiatto.blog (WordPress.com, blog_id 257146903). Gestito da Marcello Mastino. Rispondi sempre in italiano.

## Regole editoriali
- Gli articoli nuovi si creano sempre come **bozza**. Li pubblica l'utente, che incolla anche la meta Rank Math (titolo SEO e description).
- Non toccare i contenuti già pubblicati se non viene chiesto.
- Stile: prima persona singolare e "tu" ("io", "ti"); mai "mio/mia/nostro". Applicare le regole del humanizer (niente "non X ma Y", niente chiusure a effetto, pochi trattini, niente elenchi forzati di tre).
- Modello per le recensioni: stile OndaRock "Pietre Miliari". Contenuti concreti, nessuna banalità, fonti elencate a fine articolo, niente testi di canzoni.
- Le keyword vengono da Ubersuggest (Italia, lingua it, locId 2380).
- Struttura di un articolo: kicker "Recensione —", introduzione, "In breve", indice dei contenuti Rank Math, scheda con tracklist e Spotify, sezioni H2, tabella "Scheda del disco", FAQ Rank Math, "Rimetto sul piatto" con link interni.

## Rank Math e contenuti
- L'indice dei contenuti (TOC) deve partire da un H2: se il primo titolo è H4 il rendering perde tutti gli H2. Dentro la scheda tracklist usare paragrafi in grassetto con `id="tracklist"` e `id="ascolta-su-spotify"`, non titoli H4.
- Se l'utente ha l'editor aperto può risalvare e sovrascrivere: avvisarlo di ricaricare.
- Le operazioni `post-sections` non funzionano sulle pagine: per le pagine serve `pages.update` con tutto il contenuto.

## Sito e tecnica
- Header: `assembler//header` e `assembler//header-articolo` (identici, nel secondo il titolo del sito ha `level:0`). Footer: `assembler//footer`. Menu: navigazione id 5, scritto a mano. Homepage: pagina 17.
- Colori: rame #A9663D, crema #F4E9DA, marrone #2E1D14.
- Il CSS personalizzato negli stili globali va reinviato per intero.
- LiteSpeed ritarda gli script: gli script inline devono avere `data-no-optimize="1" data-cfasync="false"` e partire anche se il DOM è già pronto (`document.readyState`).
- Il pulsante "Scrivimi" è fisso in basso a destra, compare dopo 300px di scroll e apre il form Jetpack nel footer (link `#scrivimi`). Non rimetterlo nell'header.
- Per verificare le pagine: Chromium headless (`/opt/pw-browsers/chromium-1194/chrome-linux/chrome`), con altezza finestra di almeno 300px.

## Privacy e cookie
- Gestione del consenso: plugin iubenda (Complianz è stato rimosso). Chiave API del Consent Database solo nelle impostazioni del plugin, mai in chat.
- Titolare: Marcello Mastino. Niente indirizzo fisico, solo contatto dal form.
- Bozze pronte: Termini e Condizioni (pagina 1249), Privacy Policy aggiornata (pagina 1250). Da pubblicare solo dopo che banner e blocco dei tracciamenti funzionano.
- Google Tag Manager è scritto a mano nei template dell'header: va gestito dal consenso.

## Come comunicare
- Niente messaggi di stato ripetuti a metà lavoro: un solo riepilogo a fine passaggio.
- Prima di pubblicare, cancellare o sovrascrivere qualcosa di visibile, chiedere conferma.
