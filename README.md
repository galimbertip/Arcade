# GPverse Arcade

La sala giochi GPverse: un'unica app da installare su PC, smartphone e tablet, da cui si aprono tutti i giochi.

**Versione attuale:** V.1.2.0 · App online: https://galimbertip.github.io/Arcade/

## Giochi

| Gioco | Categoria | Ispirato a |
|---|---|---|
| Micro Rush | Corse | Micro Machines + Out Run / World Rally |
| Nailcap | Puzzle | Lemmings + Portal |
| Saint Seiya: Sacro Imperio | GDR e Avventura | Saint Seiya, D&D, Football Manager |
| D&D Alone | GDR e Avventura | Dungeons & Dragons in solitaria |
| Gorilla 2026 | Strategia | Gorilla + Worms Armageddon |

Ogni gioco si apre nella sua pagina con i propri salvataggi. Micro Rush, Nailcap e Gorilla 2026 stanno su GitHub Pages; Sacro Imperio e D&D Alone per ora su claude.ai (serve l'accesso).

## Installare l'app

- **PC (Chrome / Edge):** apri il link e premi **INSTALLA** in alto, oppure l'icona di installazione nella barra degli indirizzi.
- **Android:** apri il link in Chrome → **INSTALLA**, oppure menu ⋮ → *Installa app*.
- **iPhone / iPad:** apri il link in Safari → Condividi → *Aggiungi alla schermata Home*.

## Aggiungere un gioco

In `index.html`:

1. aggiungi un disegno nell'oggetto `ART` (SVG 320×180);
2. aggiungi una voce nell'array `GAMES` (`id`, `name`, `sub`, `cat`, `accent`, `art`, `desc`, `url`);
3. alza `VERSION`, aggiungi la voce in `CHANGELOG` e in [CHANGELOG.md](CHANGELOG.md);
4. alza il nome `CACHE` in `sw.js` con la stessa versione.

## Struttura

```
index.html            app (pagina, catalogo, cronologia versioni)
manifest.webmanifest  dati per l'installazione come app
sw.js                 service worker (funzionamento offline)
icons/                icone dell'app
CHANGELOG.md          cronologia versioni
```

Versioni con schema **V.major.minor.patch** — major: cambi grossi · minor: nuovi giochi o funzioni · patch: correzioni.
