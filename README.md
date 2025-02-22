# Modello statistico per prevedere il peso dei neonati

## Descrizione e obiettivi del progetto
Questo progetto, realizzato durante il Master in Data Science di ProfessionAI, utilizza il linguaggio **R** per sviluppare un modello statistico in grado di prevedere il peso dei neonati alla nascita. Basato su 10 variabili cliniche raccolte da tre ospedali (2500 osservazioni), esso mira a migliorare la gestione delle gravidanze ad alto rischio, ottimizzare le risorse ospedaliere e garantire migliori risultati per la salute neonatale.

## Struttura del repository
Il repository contiene i seguenti file e cartelle:

- **`modello_statistico_previsione_peso_neonati.Rmd`**: file R Markdown con il codice e le analisi statistiche.
- **`modello_statistico_previsione_peso_neonati.html`**: versione HTML generata dal file R Markdown.
- **`neonati.csv`**: dataset utilizzato per le analisi.
- **`images/`**: cartella contenente immagini utilizzate nel progetto.

Le variabili presenti nel dataset sono: `Anni.madre`, `N.gravidanze`, `Fumatrici`, `Gestazione`, `Peso`, `Lunghezza`, `Cranio`, `Tipo.parto`, `Ospedale` e `Sesso`.

## Fasi operative
Il progetto è suddiviso in due parti:

1. **Analisi preliminare**:
    - Esplorazione delle variabili tramite **analisi descrittiva**.
    - Test statistici per verificare ipotesi su peso, lunghezza, differenze di sesso e tipo di parto.
  
2. **Analisi multidimensionale**:
    - **Matrice di correlazione e boxplot**: esame delle relazioni tra le variabili, con focus sul target `Peso`.
    - **Creazione del modello di regressione**: modello di **regressione lineare multipla** con tutte le variabili.
    - **Selezione del modello ottimale**: uso di criteri di selezione, come AIC e BIC, per scegliere il modello più parsimonioso, includendo interazioni e effetti non lineari.
    - **Analisi della qualità del modello**: diagnostica dei residui e identificazione di eventuali valori influenti da rimuovere.
    - **Valutazione del modello**: valutazione della bontà del modello finale tramite R²(adj) e RMSE e suddivisione del dataset in train set e test set per osservare le capacità di generalizzazione.
    - **Previsioni e visualizzazioni**: una volta validato il modello, viene usato per fare previsioni pratiche e si costruiscono grafici per comunicare i risultati.
  
## Risultati sintetici
Al termine delle analisi, il modello più parsimonioso per prevedere il peso dei neonati utilizza come regressori le variabili `Gestazione`, `Lunghezza`, `Cranio` e `Sesso` spiegando il **73.58 %** della variabilità del peso:

- Peso ~ Gestazione + Lunghezza + Cranio + Sesso
- R² (adj) = 0.7358

## Prerequisiti
- **Software richiesti:**
  - [R](https://www.r-project.org/) 
  - [RStudio](https://posit.co/download/rstudio-desktop/)
- **Pacchetti R necessari:**
  - `gghalves`
  - `car`
  - `dplyr`
  - `lmtest`
  - `caret`
  - `rgl`
  - `moments`

## Guida rapida
1. Clona o scarica questo repository sul tuo ambiente locale.
2. Apri il file `modello_statistico_previsione_peso_neonati.Rmd` in RStudio.
3. Esegui le analisi nel file R Markdown.

## Autore
[Virginio Cocciaglia](https://github.com/VirginioC)

---
