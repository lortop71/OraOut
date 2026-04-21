Questa versione dell'applicazione è un pratico **calcolatore dell'orario di uscita**, pensato specificamente per chi ha bisogno di sapere esattamente quando terminare il proprio turno (di 7 ore e 42 minuti) partendo da un orario di ingresso.

È un'interfaccia pulita, moderna e decisamente "thumb-friendly" (ottimizzata per l'uso con il pollice su smartphone).

---

### 1. Cosa fa l'applicazione?
L'obiettivo principale è **automatizzare il calcolo del fine turno**. 
L'utente inserisce l'ora di inizio (o preme un tasto per usare quella attuale) e l'app calcola istantaneamente l'orario risultante aggiungendo una durata fissa di **7 ore e 42 minuti**. Gestisce correttamente anche il superamento della mezzanotte (ad esempio, se inizi a lavorare alle 20:00, calcolerà l'uscita per il giorno successivo).

---

### 2. Analisi delle Funzioni (JavaScript)
Il "cervello" dell'app risiede in tre funzioni principali:

* **`calculate()`**: È il motore di calcolo. Legge il valore dall'input orario, lo trasforma in un oggetto `Date` di JavaScript, aggiunge i minuti totali (462 minuti, ovvero 7h 42m) e formatta il risultato in `HH:mm` per mostrarlo nel display blu.
* **`setToNow()`**: Una funzione di comodità. Rileva l'ora esatta del dispositivo dell'utente e la inserisce automaticamente nel campo di partenza, attivando subito il calcolo.
* **`adjustTime(minutes)`**: Permette l'interattività rapida. Invece di digitare l'orario, l'utente può sommare o sottrarre minuti (30 o 60) cliccando i tasti "+" e "-". Questa funzione aggiorna l'input e ricalcola tutto in tempo reale.

---

### 3. Componenti Utilizzate
L'app è un mix bilanciato di tecnologie moderne:

| Componente | Utilizzo |
| :--- | :--- |
| **HTML5** | Struttura semantica del documento e input di tipo `time`. |
| **Bootstrap 5** | Framework principale per il layout reattivo (griglie, card, utility di spaziatura). |
| **Bootstrap Icons** | Icone vettoriali per i tasti "+" e "-", e l'icona della posizione. |
| **CSS3 Custom** | Stilizzazione avanzata: gradienti, angoli arrotondati (24px) e ombre per l'effetto "App Nativa". |
| **Vanilla JavaScript** | Gestione della logica senza dipendenze pesanti, rendendo l'app leggerissima e veloce. |

---

### Punti di forza del design
> **L'ottimizzazione mobile**: L'uso di `touch-action: manipulation` e l'inibizione dello zoom automatico rendono l'app molto fluida. Inoltre, i pulsanti grandi (60x60px) evitano i "misclick", un dettaglio fondamentale quando si usa il telefono in movimento o appena arrivati al lavoro.

È un ottimo esempio di come un problema semplice possa essere risolto con un'interfaccia utente (UI) estremamente curata!
