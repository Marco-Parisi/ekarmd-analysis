> Questa repository fa parte del topic: https://github.com/topics/ekar-muon-detector-project 
 
# Analisi comparativa EKAR vs OULU: Risposta al Forbush Decrease generato dall'X-Flare del 18/01/2026

<p align="center">
  <a href="https://drive.google.com/file/d/1chSIBGrRjRmNUi7_lBAMGsEk7vLY6qjA/view">
    <img src="https://github.com/user-attachments/assets/025aea90-1bf4-4d15-abf5-674e807bb49c">
  </a>
</p>

## Obiettivo dell'Analisi

* Validare e caratterizzare il rivelatore di muoni **EKAR** (bassa statistica $\approx 230$ CPM) confrontandolo con il monitor di neutroni **OULU** (alta statistica $\approx 5000$ CPM, standard scientifico), durante un evento di attività solare significativo (*Forbush Decrease*).

* Quantificare **come** la diversa fisica (Muoni vs Neutroni) e la diversa posizione geografica influenzano le misure.

## Metodologia

Poiché **OULU** ha una risoluzione temporale e statistica molto superiore, vengono eseguiti diversi passaggi di *resampling* e *scaling*:

- **Resampling:** trasformazione dei dati ad alta frequenza di **OULU** in una *banda di confidenza* oraria (Min-Max e IRQ).

- **Scaling:** Stima del coefficiente $k \approx 0.043$ per portare l'intensità del segnale di **OULU** alla scala di **EKAR**.

L'assunzione è: se **EKAR** misurasse esattamente la stessa fisica di **OULU**, il suo segnale dovrebbe rimanere confinato dentro questa banda.



## Analisi Effettuate

Sono state eseguite tre analisi principali, ognuna con uno scopo specifico:

### Analisi del Posizionamento (Fan Chart)

Verifica della stabilità del segnale e della risposta all'evento, sovrapponendo il trend di **EKAR** alle bande di confidenza di **OULU**.

**Risultato:**

- In fase di quiete, **EKAR** naviga stabilmente dentro la banda.

- Durante *Forbush Decrease*, **EKAR** esce dalla banda andando in **Overshoot**.

**Interpretazione:** **EKAR** subisce una diminuzione percentuale minore rispetto a **OULU** poiché i muoni, generati da raggi cosmici primari più energetici, sono meno influenzati dal campo magnetico terrestre.

### Cross-Correlazione

Quantificare il ritardo temporale tra i due strumenti, dovuto alla diversa posizione geografica, tramite cross-correlazione sui dati orari.

**Risultato:** si ha un ritardo sistematico di **+2 ore** per **EKAR** rispetto a **OULU**.

**Interpretazione:** Questo ritardo è la somma di due fattori:

1. **Rotazione Terrestre:** Differenza di longitudine (~1 ora).

2. **Fisica (Rigidità):** La diversa curvatura delle particelle nel campo magnetico terrestre fa sì che **EKAR** "guardi" in una direzione asintotica diversa.

_Tale risultato è confermato da una precedente analisi dove si confrontava l'andamento giorno-notte dei conteggi per i due rilevatori._

### Spazio delle Fasi

Studiare la dinamica dell'evento ovvero come il sistema reagisce e recupera, plottando **OULU** sull'asse $x$ e **EKAR** sull'asse $y$, colorando i punti in base al tempo.

**Risultato:** è visibile un **ciclo di isteresi**, un loop antiorario invece di una linea retta.

**Interpretazione:** **EKAR** recupera il livello di segnale pre-evento molto più velocemente di **OULU**. Le particelle ad alta energia risentono meno del disturbo magnetico rispetto a quelle a bassa energia.    


## Conclusioni

Nonostante la bassa statistica e il rumore intrinseco (che richiede smoothing come la media mobile), **EKAR è validato** e _vede la stessa fisica di **OULU**_. 

La differenza fondamentale è la **Rigidità di Taglio** $R_c$ :

- **OULU (~0.8 GV):** Misura neutroni generati da primari di bassa energia. È sensibilissimo alle variazioni solari con picchi profondi e recuperi più lenti.

- **EKAR (~4.0 GV):** Misura muoni generati da primari di alta energia. È meno sensibile con picchi meno marcati durante le tempeste solari e recuperi veloci.

Infine, il ritardo di 2 ore non è un difetto, ma una caratteristica del suo cono di accettazione nel campo geomagnetico e della posizione relativa.

In conclusione, **EKAR** è uno strumento complementare e molto meno costoso (**EKAR** $\sim$ 2800€ vs **OULU** più di 250 mila € solo il rivelatore) che sonda una porzione più energetica dello spettro dei raggi cosmici.

> Ho creato quest'animazione utilizzando python per il grafico e inserendolo ai video scaricati da: NASA/SDO (AIA), ESA/NASA SOHO (LASCO C3), NASA STEREO-A (SECCHI COR2)

