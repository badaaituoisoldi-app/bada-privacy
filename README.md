# Informativa sulla privacy di Bada!

Questo repository esiste per una ragione sola: **dare all'informativa privacy di
Bada! un indirizzo pubblico e stabile**, che è ciò che Google Play richiede per
pubblicare un'app.

Contiene solo le due pagine dell'informativa. Il codice sorgente dell'app non
sta qui.

- 🇮🇹 [`Privacy-it.html`](Privacy-it.html) — italiano
- 🇬🇧 [`Privacy-en.html`](Privacy-en.html) — inglese

`index.html` non è una terza pagina: è un rimando alle due, e serve perché
GitHub Pages risponde 404 a una cartella che non ne contiene uno. Chi accorcia
l'indirizzo troverebbe un errore al posto di un'informativa.

`.nojekyll` è vuoto apposta: conta che esista, non cosa contiene. Fa saltare a
Pages il passaggio per Jekyll e pubblicare la cartella così com'è. Oggi non
cambia niente di visibile — nessun file che inizia con `_`, nessuna sintassi
Liquid — ma toglie di mezzo una build che può fallire, su un indirizzo che deve
restare in piedi.

## Come si pubblica

Il repository deve essere **pubblico**: sul piano gratuito GitHub Pages non
pubblica repository privati. Pubblico non vuol dire open source — il testo
resta dell'autore, come spiega il [LICENSE](LICENSE).

*Settings → Pages → Source: Deploy from a branch → `main` / `(root)`.*

Dopo un paio di minuti le pagine sono raggiungibili a:

```
https://badaaituoisoldi-app.github.io/bada-privacy/Privacy-it.html
https://badaaituoisoldi-app.github.io/bada-privacy/Privacy-en.html
```

**A Google Play va dato il primo dei due**, per esteso e non accorciato alla
cartella. Lo stesso indirizzo va nel campo *Privacy Policy* delle impostazioni
dell'app in Play Console e nel README del repository dell'app.

Verificalo **da una finestra anonima**: l'errore più comune è consegnare a
Google un URL che funziona solo perché sei già collegato.

## Da dove viene questo testo, e come si aggiorna

**La fonte è il repository dell'app**, in `docs/privacy-policy.md` e
`docs/privacy-policy-en.md`. Queste pagine ne sono la versione impaginata.

Sono quindi due copie dello stesso documento, ed è esattamente il tipo di cosa
che diverge in silenzio. Quando l'informativa cambia:

1. si modifica prima il markdown nel repository dell'app;
2. si riporta la modifica qui, in **entrambe** le lingue;
3. si aggiorna la data di *Ultimo aggiornamento* in tutti e quattro i file.

Se le due copie non dicono la stessa cosa, quella pubblicata è quella che conta
per Google e per chi la legge — ma quella sbagliata non lo dice da sola.

## Vincoli da rispettare

Google verifica l'URL, e alcune cose fanno fallire la pubblicazione:

- la pagina deve aprirsi **senza login** e senza redirect verso un altro dominio;
- deve nominare l'app e lo sviluppatore;
- deve restare raggiungibile **dopo** la pubblicazione: un URL che smette di
  rispondere può far sospendere l'app;
- non può essere un PDF su Drive né un documento modificabile da chiunque.

Le pagine sono HTML statico senza dipendenze esterne: nessun font remoto,
nessuno script, nessuna richiesta di rete. Si aprono anche offline, e non c'è
niente che possa smettere di funzionare per conto suo.

## Licenza

Testo dell'informativa © 2026 Antonio Marinelli.

È scritta per essere letta: leggerla, salvarla, stamparla e citarla va
benissimo — tenersi una copia dell'informativa dell'app che si sta installando
è un diritto, non una concessione. L'unica richiesta è di non riusarla come
informativa di un altro prodotto: descrive come si comporta questa app, e
altrove direbbe cose non vere.

Dettagli in [LICENSE](LICENSE).
