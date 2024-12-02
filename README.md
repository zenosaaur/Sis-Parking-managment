# Progetto: Gestione Parcheggio con Sistema Automatizzato

## Descrizione
Questo progetto implementa un sistema di gestione per un parcheggio suddiviso in tre settori (A, B e C) con ingressi e uscite automatizzate. Il sistema è in grado di gestire la registrazione dei posti occupati e liberi, verificare errori di input, e operare in modo autonomo dopo un'inizializzazione manuale.

### Specifiche del Parcheggio
- **Settori**:
  - Settore A: 31 posti
  - Settore B: 31 posti
  - Settore C: 24 posti
- **Modalità di Operazione**:
  - **Ingresso/Uscita**: L'utente specifica il settore desiderato (codifica one-hot).
  - **Modalità Notte**: Sbarre aperte per la libera circolazione.
  - **Accensione Manuale**: Sequenza di inizializzazione con 5 bit (`11111`).
  - **Spegnimento Manuale**: Sequenza di spegnimento con 5 bit (`00000`).

### Funzionalità Principali
- Gestione di errori di input e anomalie (codici non validi).
- Controllo dello stato dei settori:
  - Sbarre aperte solo se ci sono posti disponibili.
  - Segnalazione di settore pieno o vuoto.
- Minimizzazione e ottimizzazione del circuito per area e ritardo.

---

## Architettura
Il sistema è composto da:
- **FSM**: Controllore a stati per la gestione delle transizioni operative.
- **Data-path**: Moduli combinatori e sequenziali per il trattamento dei dati.
  
### Componenti Utilizzati
- Comparatori, sommatori, sottrattori
- Multiplexer
- Registri
- Logiche combinatorie (AND, OR)

---

## Ottimizzazione
- **Minimizzazione per area**:
  - Numero di letterali ridotto del 230%.
  - Numero di nodi ridotto del 202%.
- **Mapping ottimizzato**:
  - Riduzione del numero di gate del 39%.
  - Riduzione del ritardo del 22%.

---

## Diagrammi
- **Diagramma FSM**: Controllo degli stati principali (SLEEP, A, B, C, AUTO).
- **Data-path**: Connessione tra moduli principali per il calcolo e la gestione.

---

