# Storie e Incanti — Copia zero

Pagina animata: il libro ruota di 360° sull'asse Y, dalla copertina alla quarta e ritorno. Sfondo e scritte restano fermi.

## File

- `index.html`: pagina, stile e animazione (CSS 3D + JavaScript, nessuna libreria esterna)
- `assets/sfondo.jpg`: sfondo senza libro (2160×3840)
- `assets/scritte.png`: le due fasce di testo, che restano sopra al libro
- `assets/copertina.jpg`, `assets/quarta.jpg`, `assets/dorso.jpg`: le facce del libro, ritagliate dal template KDP della copertina completa
- `.nojekyll`: dice a GitHub Pages di servire i file così come sono

## Pubblicazione

1. Carica tutto il contenuto di questa cartella nella **radice** della repository, compresa la cartella `assets/` e il file nascosto `.nojekyll`.
2. Vai su *Settings → Pages → Build and deployment*, imposta *Source: Deploy from a branch*, branch `main`, cartella `/ (root)`.
3. Dopo 1-2 minuti la pagina è online su `https://<utente>.github.io/<repository>/`.

## Regolazioni

In `index.html`, all'inizio dello `<script>`:

- `HOLD_FRONT`: secondi di pausa sulla copertina
- `TURN`: secondi per mezzo giro
- `HOLD_BACK`: secondi di pausa sulla quarta

Nel CSS (`:root`): `--D` è lo spessore (56 px = 1,1 cm in scala) e `--spine` il blu dei bordi dei tagli.

Un clic o tap sulla pagina mette in pausa o fa ripartire l'animazione.
`index.html?angolo=45` mostra il libro fermo a 45° (utile per gli screenshot).
