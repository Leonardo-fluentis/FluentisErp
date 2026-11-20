Rappresenta il riepilogo delle scadenze del documento, per ogni *tipo* e *soluzione* di pagamento.  
- **Numero**: valore progressivo della riga.  
- **Pagamento**: rappresenta il codice alfanumerico del *Tipo pagamento* ripreso dalla *Testata del documento > tab Pagamenti*.  
- **Importo**: Importo della scadenza calcolato. Può essere forzato manualmente, in tal caso si attiva automaticamente il successivo flag *Modifica manuale*. (Scattano in automatico dei controlli e avvisi sulla quadratura tra i valori delle scadenze e il totale fattura)
- **Data scadenza**: data della scadenza calcolata. Può essere forzata manualmente, in tal caso si attiva automaticamente il successivo flag *Modifica manuale*.
- **Spese di incasso**: campo in cui vengono riportate le spese di incasso calcolate.
- **IVA**: da applicare alle spese di incasso (può essere impostata anche manualmente).
- **Causale pagamento**: è possibile inserire direttamente in fattura una causale contabile che da luogo ad una scrittura automatica di incasso / pagamento. **NB**: prestare attenzione al template della causale, perchè verranno utilizzati i relativi conti presenti anche senza sottoconto, motivo per il quale è presente il campo seguente.
- **Conto sottoconto cliente / fornitore** conto che usa per incassare/pagare (cassa o banca ad esempio) la scadenza andando a sovrascrivere il conto presente nella causale contabile di pagamento (o incasso).
- **N. ricevuta**: un eventuale numero della ricevuta per i soldi ricevuti.
- **Singolo**: attiva la contabilizzazione della chiusura scadenze nella scrittura automatizzata.
- **Tipo sconto**: tipo di sconto finanziario.
- **Valore sconto**: valore dello sconto finanziario su incasso.
- **Dettaglio dichiarazioni**: è il riferimento alla dichiarazione di intento. L’iva applicata alle spese incasso potrebbe essere sempre un’iva plafond, quindi è necessario poter inserire anche qui la dichiarazione di intento collegata (come per le righe articolo e le righe spese).

**FATTURE D'ACQUISTO:**

- **Segno**: solo le scadenze che hanno questo flag vengono poi gestite in pagamento con causale e conto impostato.
- **Modelli riferimento pagamento**: modello di creazione del codice di pagamento. In alcune localizzazioni estere ogni scadenza in fattura prevede un codice attribuito da chi fattura: questo codice è strutturato, secondo alcuni modelli specifici (tabella MB_PaymentReferenceModels), in modo da poter costruire il codice con un algoritmo.
- **Codici modelli pagamento**: questo è il codice (strutturato come da modello precedente) da riportare nella partita e quindi poi nei pagamenti che si inviano alla banca, in modo che questa comunichi al beneficiario qual è la scadenza che è stata pagata (e così automatizzare l’import dai movimenti bancari con chiusura partita). Da qui viene compilato dentro la partita e nel file Sepa.
- **Data limite pag anticipato**: questo è un campo previsto nel tracciato fatture Sdi, la data limite per poter applicare lo sconto finanziario.

