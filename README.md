# Tool gratuito di Fisioterapisti.org per imparare a creare gratis le fatture

## Come funziona?
La struttura di base è un semplice form HTML, che quando viene compilato genera un PDF lato client con la libreria jsPDF.

## Com'è strutturato?
C'è una prima pagina (home.html) con un po' di informazioni su cosa aspettarsi e come funziona, e il tasto per andare sulla pagina per creare la fattura. 
Dentro la cartella "modal" troviamo:

1) Gli "asset" (cioè le librerie jsPDF e jsPDF-autotable che permettono di creare la fattura in PDF direttamente dal browser);
2) "fatture.html" che è la pagina web contenente il form;
3) "function.js" che contiene il codice che permette di avere il form in 4 passaggi e la validazione dei campi;
4) "generapdf.js" che contiene il codice che prende i valori immessi nel form e regola la struttura che deve avere il PDF finale della fattura;
5) Immagine di benvenuto a cura di Undraw.co;
6) Lo style per la maggior parte è Bootstrap (ver.5 per la home, ver.4 per il form), in minima parte c'è anche style.css.

Un po' di info sugli script e le librerie Javascript:
1) La maggior parte è Vanilla JS;
2) JQuery per disattivare il tasto Invio ed inviare inavvertitamente il form;
3) jsPDF che è la libreria js che permette di generare i pdf lato client;
4) auto-table per jsPDF che è il plugin di jsPDF per creare la tabella dove sono riportati quantità, descrizioni e importi.

## Privacy
Questa applicazione web non ha back-end. 
Al momento della conferma del form, i dati non vengono inviati e rielaborati da un server, perché la libreria jsPDF funziona lato client - quindi è il browser dell'utente che realizza il PDF.
Una semplice verifica di questo si può fare scaricando il contenuto di questo repository e provare a generare una fattura offline: viene generata comunque, perché i dati restano confinati all'interno del dispositivo dell'utente.
Non c'è un database su cui raccogliamo i dati dei professionisti, dei pazienti o delle fatture. 
Non è il nostro scopo, che resta quello di offrire un tool gratuito (e non pagare server su cui ospitare back-end e database vari ci permette di renderlo gratuito) e semplice da usare, anche per chi non ha mai emesso una fattura prima d'ora.

## Limitazioni
Visto che non c'è un database collegato, per ogni utente non sappiamo nemmeno qual è l'ultima fattura emessa e in che data. 
Non salviamo le anagrafiche e il tool non permette di inviare i dati a Sistema Tessera Sanitaria. 
I browser con Javascript disattivato o vecchio, per ovvi motivi non riescono a generare una fattura.
Le fatture sono cartacee - _non sono fatture elettroniche xml compatibili con il SDI_ - e sono senza IVA e per forfettari.

## Utilizzo
Se ti serve il codice copialo pure: hai la massima libertà di farlo, non ci interessa.

## Segnalazioni bug, richiesta informazioni, contatti:
Si prega di scrivere all'indirizzo email: fisioterapistiorg@gmail.com
