# EcommerceSecondhand_Data_manipulation_Visualization
Analisi EDA per valutare ed identificare i migliori articoli per avviare un E-commerce di abbigliamento di seconda mano.
# Analisi EDA
- Prima analisi esplorativa per comprendere le dimensioni e i tipi di dati: df.shape, df.columns.tolist(), df.head(), df.isnull().sum()
1. Pulizia dei dati dai duplicati
   - Analisi delle frequenze e dei duplicati nel Dataset per le stesse combinazioni utente-articolo
   - Verifica dei Duplicati Perfetti nel Dataset, in cui lo stesso utente ha recensito lo stesso articolo
   - Esplorazione delle combinazioni (item_id, user_id) non perfettamente duplicati
   - Eliminazione dei duplicati perfetti (item_id + user_id)
2. Analisi univariate e bivariate
   - Creazione di un id univoco indispensabile per le oprazioni future
   - Analisi delle Categorie di Abbigliamento
   - Analisi della variabile di taglia
   - Analisi bivariata tra categorie e taglia: tutte le combinazioni
   - Analisi bivariata delle taglie più frequenti distribuite per categoria
   - Trasformazione delle istanze in unità di misura italiane
   - Analisi delle variabili fisiche delle utenti
3. Clustering
   - Preparazine di una copia del DataFrame per il clustering basato su misure corporee, rimuovendo i valori mancanti, normalizzando i dati e applicando KMeans per identificare 8 gruppi distinti
   - Analisi dei profili fisici medi di ciascun cluster e genera una descrizione testuale interpretabile
   - Calcola la distribuzione percentuale delle categorie presenti in una colonna target, opzionalmente filtrando per una o più condizioni
   - Calcolo e visualizzazione della distribuzione delle taglie italiane ('size_it') per ciascun cluster
   - Calcolo e visualizzazione della distribuzione percentuale e dei conteggi assoluti di `target_col` all'interno di ciascun valore di `group_col`, con possibilità di filtrare e ordinare
4.  Recensioni e valutazioni
    - Estrarre e visualizzare chiaramente le review testuali ('review_text') da un DataFrame applicando filtri precisi su colonne come 'cluster', 'category', 'fit', ecc.
    - Grafici di confronto tra i cluster di donne presi in considerazione
    - Raggruppare la 'quality' per ogni articolo, così da valutare se vi è qualche articolo particolarmente apprezzato
    - Visualizzazione della distribuzione generale delle misure delle donne che hanno acquistato una taglia, per ogni taglia
5. Ulteriori analisi
   - Analisi della variabile di taglia di piede
6. Considerazioni finali

