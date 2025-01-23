[![License](https://img.shields.io/badge/License-MIT-green.svg)](https://github.com/lucabordignonb/modello_classificazione/blob/main/LICENSE)
[![Python version](https://img.shields.io/badge/Python-3.7%2B-blue.svg)](https://www.python.org/downloads/)
[![TensorFlow](https://img.shields.io/badge/TensorFlow-2.0%2B-orange.svg)](https://www.tensorflow.org/)

# Classificazione loghi real e fake
Questo progetto si propone di distinguere loghi autentici e falsi utilizzando reti neurali convoluzionali (CNN). L'obiettivo principale è analizzare un modello preesistente basato su EfficientNet, sviluppare due modelli distinti e confrontarne le performance. 

Il progetto si articola in tre fasi:
1. **Analisi di un modello preesistente**: abbiamo commentato e documentato un modello basato su EfficientNet già sviluppato su Kaggle.
2. **Implementazione di modelli personalizzati**: abbiamo creato due modelli CNN, uno di base e uno migliorato.
3. **Confronto delle performance**: abbiamo valutato i modelli utilizzando metriche come precision, recall, e F1-score e capendo quale sia più efficace.

<img src="https://i.imgur.com/8qVjwHE.jpeg" alt="Descrizione immagine" width="200"/>

## Indice

- [Come iniziare](#come-iniziare)
  - [Dipendenze](#dipendenze)
  - [Come installare](#come-installare)
  - [Documentazione](#documentazione)
- [Come contribuire](#come-contribuire)
  - [Installare le dipendenze di sviluppo](#installare-le-dipendenze-di-sviluppo)
  - [Struttura del progetto](#struttura-del-progetto)
- [Manutenzione](#manutenzione)
- [Licenza](#licenza)
- [Miglioramenti Futuri](#miglioramenti-futuri)
- [Autori e Copyright](#autori-e-copyright)

---

## Come iniziare

### Dipendenze

Per eseguire il progetto, è necessario avere installate nel proprio ambiente virtuale le seguenti librerie:

- **Python 3.7+**: Linguaggio di programmazione necessario per il progetto.
- **TensorFlow 2.0+**: Framework per il machine learning e il deep learning, utilizzato per costruire le reti neurali.
- **Keras**: API di alto livello integrata in TensorFlow per costruire e addestrare modelli di machine learning.
- **Scikit-learn**: Libreria per il calcolo di metriche e l'analisi delle performance.
- **Matplotlib**: Utilizzata per creare grafici e visualizzare le performance del modello.
- **Seaborn**: Libreria per la visualizzazione avanzata, utile per creare la matrice di confusione.
- **Pandas**: Utilizzata per manipolare i dati di input e output.
- **Pillow**: Libreria per il caricamento e la manipolazione delle immagini.

---

### Come installare

1. **Scarica il dataset da Kaggle**:
   - Vai al [dataset di Kaggle](https://www.kaggle.com/datasets/gauravduttakiit/fakereal-logo-detection).
   - Scarica il dataset e posizionalo nella directory del progetto. Mantieni la struttura delle cartelle `train` e `test` come segue:
     ```
     /train/Fake
     /train/Genuine
     /test/Fake
     /test/Genuine
     ```

2. **Scarica e analizza il modello preesistente**:
   - Il progetto include l'analisi del modello preesistente [EfficientNet Fake Real Logo Detection](https://www.kaggle.com/code/gauravduttakiit/efficientnet-fake-real-logo-detection).
   - Questo modello è stato eseguito e commentato dettagliatamente nel file **MOD_EFF.ipynb** per comprenderne il funzionamento.

3. **Clona il repository del progetto**:
   - Per scaricare i file del progetto, utilizza:
     ```bash
     git clone https://github.com/lucabordignonb/modello_classificazione.git
     cd <nome_cartella>
     ```

4. **Esegui i file principali del progetto**:
   - **File 1 (Codice Commentato)**: Analizza il modello preesistente con commenti dettagliati.
     ```bash
     jupyter notebook MOD_EFF.ipynb
     ```
   - **File 2 (Modello con Prestazioni Non Buone)**: Mostra le performance di un modello iniziale.
     ```bash
     jupyter notebook MOD_CNN.ipynb
     ```
   - **File 3 (Modello Migliorato)**: Presenta il modello ottimizzato con tecniche avanzate.
     ```bash
     jupyter notebook MOD_FIN.ipynb
     ```

### Documentazione

Il progetto è suddiviso in tre file principali, che rappresentano le diverse fasi di analisi e sviluppo. L'obiettivo principale è confrontare un modello preesistente con due modelli sviluppati durante il progetto, evidenziando i punti di forza, i limiti e le differenze tra le implementazioni, così da valutare quale modello sia più efficace per la classificazione dei loghi.

1. **MOD_EFF.ipynb**:
   - Contiene l'analisi e i commenti dettagliati su un modello preesistente basato su EfficientNet, pubblicato su Kaggle ([link al modello](https://www.kaggle.com/code/gauravduttakiit/efficientnet-fake-real-logo-detection)).
   - Questo file si concentra sulla comprensione del funzionamento del modello originale, senza modificarne la struttura.
   - Rappresenta un punto di riferimento per confrontare le prestazioni degli altri modelli sviluppati durante il progetto.

2. **MOD_CNN.ipynb**:
   - Include la creazione di un modello CNN iniziale per la classificazione dei loghi, sviluppato senza ottimizzazioni avanzate.
   - Le prestazioni di questo modello sono di base e servono come confronto diretto con il modello migliorato (File 3).
   - Questo file aiuta a identificare le carenze di un'implementazione standard e senza tecniche di ottimizzazione.

3. **MOD_FIN.ipynb**:
   - Contiene un modello migliorato, sviluppato da zero, con l'inclusione di tecniche avanzate come data augmentation, bilanciamento del dataset e ottimizzazione dei parametri.
   - Sebbene migliori rispetto al modello iniziale (File 2), l'obiettivo è capire le differenze rispetto al modello basato su EfficientNet.
   - Lo scopo principale è analizzare le differenze tra le varie implementazioni e comprendere quali fattori influiscono maggiormente sulle prestazioni.

## Come contribuire
### Installare le dipendenze
Per configurare l'ambiente di sviluppo ed eseguire i file del progetto, segui i passaggi seguenti:

1. **Crea un ambiente virtuale**:
   È consigliato utilizzare un ambiente virtuale per gestire le dipendenze, noi abbiamo utilizzato Anaconda.
2. **Attiva l'ambiente su Python**:
   Dopo aver creato l'ambiente lo abbiamo attivato con il comanda conda activate e il nome dell'ambiente scelto.
3. **Installa le librerie richieste**:
   Successivamnete abbiamo installato tutte le librerie necessarie per il progetto con il comando pip install tensorflow keras scikit-learn matplotlib seaborn pandas pillow   
4. **Mantieni nella directory la cartella archive con il dataset diviso**
5. **Avvia i file del progetto**


### Struttura del progetto

La struttura del progetto è organizzata come segue:

- **MOD_EFF.ipynb**: Codice commentato di un modello preesistente basato su EfficientNet, pubblicato su Kaggle. Questo file analizza e documenta il funzionamento e le scelte implementative del modello originale.
- **MOD_CNN.ipynb**: Modello iniziale sviluppato durante il progetto. Questo modello mostra prestazioni di base ed evidenzia le limitazioni di un'implementazione senza ottimizzazioni avanzate.
- **MOD_FIN.ipynb**: Modello migliorato con tecniche avanzate come data augmentation e bilanciamento del dataset. È utilizzato per confrontare le performance rispetto al modello iniziale e a quello preesistente.
- **dataset/**: Contiene i dati di training e test organizzati nelle seguenti sottocartelle:
  - `/train/Fake`
  - `/train/Genuine`
  - `/test/Fake`
  - `/test/Genuine`


## Manutenzione
Attualmente, il progetto è mantenuto attivamente. Per eventuali problemi o richieste, non esitare a segnalare issue o a contribuire con nuove idee.

## Licenza

Questo progetto è rilasciato sotto licenza [MIT](LICENSE). Sei libero di utilizzare, modificare e distribuire il codice seguendo i termini di questa licenza.

## Miglioramenti Futuri
Il progetto può essere ulteriormente migliorato implementando le seguenti idee:
- **Bilanciamento delle classi**: Utilizzo di tecniche più avanzate per migliorare il bilanciamento tra classi Fake e Genuine.
- **Modelli pre-addestrati**: Integrazione di modelli come ResNet o VGG per migliorare le performance.
- **Espansione del dataset**: Aggiunta di nuove immagini tramite GANs o raccolta di nuovi dati.
- **Nuove metriche**: Introduzione di metriche come ROC/AUC per una valutazione più completa delle performance.

---


## Autori e Copyright
Il progetto è stato sviluppato e mantenuto da Ilaria Mennella, Luca Bordignon e Rosaria Ajdini. Eventuali contributi futuri saranno ben accetti e attribuiti. Per dettagli sui diritti, consulta il file [LICENSE](LICENSE).
