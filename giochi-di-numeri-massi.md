# Giochi di numeri: Un Percorso Didattico per lo Sviluppo del Pensiero Computazionale

## Abstract

Questo articolo presenta un'esperienza didattica focalizzata sullo sviluppo del pensiero ricorsivo attraverso la costruzione formale dell'aritmetica. Partendo dalle funzioni primitive di riconoscimento dello zero, successore e predecessore, il corso guida gli studenti nella definizione ricorsiva di operatori di confronto e operazioni aritmetiche fondamentali (addizione, sottrazione, moltiplicazione e divisione intera). L'approccio si basa sull'utilizzo del linguaggio Scheme, ispirandosi al testo "The Little Schemer", e mira a evidenziare la profonda connessione tra ragionamento logico-deduttivo e problem-solving informatico. Verranno discussi gli obiettivi, la metodologia adottata, gli strumenti utilizzati e le riflessioni sull'efficacia di tale percorso nel promuovere una comprensione più profonda dei concetti informatici e stimolare l'interesse verso le discipline scientifico-tecnologiche.

## Introduzione

Nel panorama educativo odierno, la necessità di sviluppare il \emph{pensiero computazionale} è ampiamente riconosciuta come una competenza chiave per affrontare le sfide del XXI secolo. Tale pensiero non si limita alla mera capacità di programmare, ma abbraccia una serie di abilità cognitive essenziali, tra cui la scomposizione di problemi, il riconoscimento di pattern, l'astrazione e, in modo preminente, il \emph{pensiero ricorsivo}. Quest'ultimo, in particolare, costituisce la spina dorsale di numerosi algoritmi e strutture dati in informatica, ma la sua comprensione profonda spesso rappresenta una sfida per gli studenti.

Il corso nasce proprio con l'intento di affrontare questa sfida, proponendo un percorso didattico che, anziché introdurre la ricorsione in contesti complessi, la esplora a partire dalle sue radici più fondamentali: la costruzione dell'aritmetica stessa. L'idea centrale è che i ragionamenti sottostanti alle operazioni numeriche, se formalizzati in modo ricorsivo, rivelano una struttura universale applicabile alla risoluzione di un'ampia gamma di problemi computazionali. Questo approccio non solo rafforza le basi matematiche, ma getta anche le fondamenta per una comprensione meno superficiale e più consapevole degli oggetti di studio e dei metodi della disciplina informatica.

Esso è stato sviluppato nell'ambito del progetto scolastico dell'IIS ``Savoia Benincasa'', ``Citizen scientists of the future'' (C.U.P. H34D23002330006), finanziato dal Piano Nazionale di Ripresa e Resilienza (PNRR), Missione 4 -- Istruzione e Ricerca, Investimento 3.1 ``Nuove competenze e nuovi linguaggi'', con l'obiettivo di potenziare le competenze STEM e multilinguistiche ed è stato rivolto agli studenti della classe seconda del Liceo Matematico.

## Obiettivi del Corso

Gli obiettivi generali del corso sono stati definiti per andare oltre la mera acquisizione di nozioni, mirando a un impatto più profondo sulla formazione degli studenti:

* Comprendere meno superficialmente gli oggetti di studio e i metodi della disciplina informatica. L'esposizione alla costruzione formale dell'aritmetica e alla logica ricorsiva sottostante mira a demistificare concetti che altrimenti potrebbero apparire come "magie" della tecnologia, rivelandone la rigorosa base matematica e logica.
* Stimolare l’interesse verso le materie tecnico scientifiche e, in particolare, verso l’informatica. Rendere tangibili e "costruibili" concetti astratti può accendere la curiosità e la passione, motivando gli studenti a esplorare ulteriormente questi campi.
* Cogliere la stretta relazione tra pensiero scientifico e sviluppo tecnologico. Attraverso la formalizzazione delle idee e la loro implementazione in un linguaggio computazionale, gli studenti possono apprezzare come il ragionamento astratto e la logica siano i motori dell'innovazione tecnologica.
* Comprendere le strutture fondamentali dei ragionamenti logico-deduttivi e padroneggiare il linguaggio logico-formale per risolvere problemi di varia natura. La ricorsione è un potente strumento di ragionamento deduttivo. Il corso fornisce un contesto pratico per esercitare e affinare questa capacità.
* Utilizzare strumenti informatici per modellizzare e risolvere problemi. Sebbene il focus sia sui concetti, l'utilizzo di Scheme come strumento di formalizzazione permette agli studenti di tradurre le loro idee astratte in modelli computazionali concreti.

## Metodologia e Strumenti

Per perseguire questi obiettivi, è stato scelto un approccio basato sulla formalizzazione delle idee attraverso il linguaggio **Scheme**. Scheme, un dialetto di Lisp, è rinomato per la sua semplicità sintattica e la sua profonda aderenza ai principi del lambda calcolo, rendendolo uno strumento ideale per esplorare concetti come la ricorsione, l'astrazione e la manipolazione simbolica.

Il corso si basa in gran parte sui primi capitoli di "The Little Schemer", un testo del 1974 che introduce il concetto di ricorsione in modo giocoso e incrementale, attraverso una serie di domande e risposte che guidano il lettore a "scoprire" le definizioni ricorsive. Questa scelta didattica è fondamentale: il libro non fornisce ricette pronte, ma stimola un processo di scoperta attiva, portando gli studenti a costruire i propri schemi cognitivi.

Per facilitare l'apprendimento e ridurre la barriera linguistica, i termini chiave di Scheme e Lisp sono stati tradotti in italiano, come mostrato nella tabella seguente:

| Scheme       | Corso               |
| :----------- | :------------------ |
| `car`        | `primo`             |
| `cons`       | `anteponi`          |
| `cdr`        | `resto`             |
| `list`       | `lista`             |
| `list?`      | `lista?`            |
| `null?`      | `lista-vuota?`      |
| `'()`        | `lista-vuota`       |
| `eq?`        | `uguale?`           |

Questa traduzione ha permesso di concentrarsi sui concetti logici senza aggiungere un carico cognitivo eccessivo dovuto alla memorizzazione di termini in lingua straniera o legati ai registri di un processore.

Un elemento visivo cruciale del corso è la rappresentazione delle \emph{strutture dati come liste} e delle \emph{espressioni come alberi sintattici}. Ad esempio, la rappresentazione di una lista come `' (primo secondo contorno)`:

```plantuml
  primo     resto         primo     resto           primo       resto   lista-vuota
.-------.--------.       .---------.--------.       .----------.--------.       |
| primo |   *---|----->| secondo |   *---|----->| contorno |   *---|----->|
|_______|________|       |_________|________|       |__________|________|       |
```

E la visualizzazione delle applicazioni di procedure come alberi:

```
      .           .-------.   
    / | \         |   +   |
   /  |  \        |-------|
  /   |   \       | 1 | 2 |
 +    1    2      |___|___|
```

Queste visualizzazioni sono state utilizzate in aula per aiutare gli studenti a "vedere" la struttura sottostante delle espressioni e comprendere il processo di valutazione ricorsiva.


## Il Percorso Didattico

Il cuore del corso risiede nella progressiva costruzione di concetti, partendo dalle operazioni fondamentali sulle liste per arrivare alla definizione delle operazioni aritmetiche.

### 1. Atomi, Operatori, Predicati e Liste di Atomi

Si è iniziato con la definizione di **atomo** e le operazioni basilari sulle liste, come `lista?`, `lista-vuota?`, `primo`, `resto`, `anteponi` e `uguale?`. Queste funzioni primitive, sebbene semplici, sono gli ingredienti fondamentali per la costruzione di strutture dati più complesse e per l'implementazione delle procedure ricorsive.

Esempi di definizioni chiave includono:

```scheme
; Predicato atomo?
(define atomo?
  (lambda
    (x)
    (and (not (pair? x)) (not (null? x)))))

; Primo elemento di una lista
(define primo
  (lambda (l)
    (cond
      [(not (lista? l)) (display "'primo' è definito solo per le liste")]
      [(null? l) (display "'primo' non è definito per la lista vuota")]
      [else (car l)])))
```

Gli esercizi iniziali si sono concentrati sulla manipolazione di liste di atomi, introducendo gradualmente il concetto di ricorsione attraverso funzioni come `lista-di-atomi?` e `membro?`. Queste prime esperienze hanno permesso agli studenti di familiarizzare con la sintassi di Scheme e il paradigma ricorsivo in un contesto semplice e intuitivo.

```scheme
; Predicato lista-di-atomi?
(define lista-di-atomi?
  (lambda (l)
    (cond
      [(lista-vuota? l) #t]
      [(atomo? (primo l)) (lista-di-atomi? (resto l))]
      [else #f])))

; Predicato membro?
(define membro?
  (lambda (a lda)
    (cond
      [(lista-vuota? lda) #f]
      [else (or (uguale? a (primo lda))
                (membro? a (resto lda)))])))
```

### 2. Manipolazione Ricorsiva delle Liste

Il corso è poi progredito nella manipolazione più complessa delle liste, definendo funzioni come `rimuovi-un-membro`, `primi`, `inserisci-a-destra`, `inserisci-a-sinistra`, `sostituisci`, `rimuovi-tutti-i-membri`, `inserisci-tutti-a-destra`, `inserisci-tutti-a-sinistra` e `sostituisci-tutti`. Ogni funzione è stata costruita ricorsivamente, enfatizzando il pattern base della ricorsione: un caso base (solitamente la `lista-vuota`) e un caso ricorsivo che opera sul `primo` elemento e invoca la funzione sul `resto` della lista.

Ad esempio, la funzione per rimuovere un membro:

```scheme
; Rimuovi un membro
(define rimuovi-un-membro
  (lambda (a lda)
    (cond
      [(lista-vuota? lda) lista-vuota]
      [(uguale? a (primo lda)) (resto lda)]
      [else (anteponi (primo lda) (rimuovi-un-membro a (resto lda)))])))
```

E la funzione per inserire tutti i membri a destra:

```scheme
; Inserisci tutti a destra
(define inserisci-tutti-a-destra
  (lambda (nuovo vecchio lista-di-atomi)
    (cond
      [(lista-vuota? lista-di-atomi) lista-vuota]
      [(uguale? (primo lista-di-atomi) vecchio)
               (anteponi vecchio
                        (anteponi nuovo
                                  (inserisci-tutti-a-destra nuovo vecchio
                                                            (resto lista-di-atomi))))]
      [else (anteponi (primo lista-di-atomi) (inserisci-tutti-a-destra nuovo vecchio (resto lista-di-atomi)))])))
```

Questi esercizi hanno consolidato la comprensione del **pattern ricorsivo** e della sua applicazione a problemi di manipolazione dati.

### 3. Giochi di Numeri: La Costruzione Ricorsiva dell'Aritmetica

Il culmine del corso è stato la costruzione delle operazioni aritmetiche utilizzando solo le funzioni primitive `zero?`, `s` (successore) e `p` (predecessore). Questo approccio, radicalmente diverso dalla semplice memorizzazione di regole, ha permesso agli studenti di "ricostruire" l'aritmetica da zero, apprezzandone la struttura ricorsiva intrinseca.

Definizioni chiave includono:

```scheme
; Successore di un numero naturale n
(define s
  (lambda (n)
    (+ n 1))) ; Notare che si usa la primitiva Scheme + per semplificare, ma il focus è sulla relazione ricorsiva.

; Predecessore di un numero naturale n
(define p
  (lambda (n)
    (- n 1))) ; Anche qui, uso della primitiva Scheme -
```

L'addizione, ad esempio, è stata definita come:

```scheme
; Operatore più
(define più
  (lambda (n m)
    (cond
      [(zero? m) n] ; Caso base: aggiungere zero non cambia il numero
      [else (s (più n (p m)))]))) ; Caso ricorsivo: n + m = successore di (n + predecessore di m)
```

Similmente, la moltiplicazione:

```scheme
; Operatore per
(define per
  (lambda (n m)
    (cond
      [(zero? m) 0] ; Caso base: moltiplicare per zero produce zero
      [else (+ n (per n (p m)))]))) ; Caso ricorsivo: n * m = n + (n * predecessore di m)
```

E la divisione intera:

```scheme
; Operatore diviso
(define diviso
  (lambda (n m)
    (cond
      [(minore? n m) 0] ; Caso base: se n è minore di m, il quoziente è 0
      [else (s (diviso (- n m) m))]))) ; Caso ricorsivo: sottraggo m da n e aggiungo 1 al quoziente della ricorsione
```

Queste definizioni, spesso sorprendenti per gli studenti abituati alle operazioni dirette dei linguaggi di programmazione, hanno evidenziato come concetti complessi possano essere ridotti a un insieme minimo di primitive e regole ricorsive. Il percorso ha incluso anche la definizione di operatori di confronto (`maggiore?`, `minore?`, `stesso-numero?`) e altre funzioni sulle liste e i numeri, come `lunghezza`, `seleziona`, `rimuovi-selezionato`, `rimuovi-numeri`, `solo-numeri`, `stesso-atomo?`, `occorrenze` e `uno?`.

---

## Conclusioni

L'esperienza del percorso ha dimostrato l'efficacia di un approccio che pone il pensiero ricorsivo al centro dell'apprendimento dell'informatica. Costruire l'aritmetica "da zero" in un contesto formale ma accessibile come quello offerto da Scheme e "The Little Schemer" ha permesso agli studenti di:

* Sviluppare un'intuizione più profonda per la ricorsione. Anziché vederla come un costrutto sintattico, l'hanno sperimentata come un principio fondamentale di risoluzione dei problemi, applicabile sia all'aritmetica che alla manipolazione simbolica.
* Migliorare le capacità di ragionamento logico-deduttivo. La necessità di definire ogni operazione in termini di casi base e ricorsivi ha affinato le loro abilità di pensiero strutturato.
* Comprendere la natura formale dell'informatica. L'uso di un linguaggio come Scheme, con la sua chiara corrispondenza con il lambda calcolo, ha svelato la base matematica rigorosa dietro la programmazione.
* Aumentare la consapevolezza sulla relazione tra matematica e informatica. Il corso ha reso esplicita la continuità tra il pensiero matematico e le tecniche computazionali, superando la percezione di queste discipline come entità separate.

Sebbene la curva di apprendimento iniziale possa essere ripida per alcuni, l'esperienza ha rivelato che, una volta compreso il paradigma ricorsivo, gli studenti acquisiscono una potente lente attraverso cui analizzare e risolvere una vasta gamma di problemi. Questo approccio non solo arricchisce il loro bagaglio di conoscenze tecniche, ma coltiva anche una mentalità più critica e analitica, essenziale per navigare nel mondo sempre più complesso dell'informatica.

In conclusione, percorso rappresenta un modello promettente per l'insegnamento del pensiero computazionale, dimostrando che un ritorno alle basi formali e la costruzione incrementale dei concetti, guidati da strumenti adeguati, possono portare a una comprensione più profonda e duratura delle discipline informatiche.
