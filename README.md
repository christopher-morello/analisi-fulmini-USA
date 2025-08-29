# analisi-tempeste-USA

Questo dataset utilizza un file denominato `eda_using_basic_data_functions_in_python_dataset1.csv` e proviene dalla tabella dati pubblica bigquery-public-data.noaa_lightning.lightning_strikes.   

Il National Lightning Detection Network (NLDN) di Vaisala registra i fulmini che colpiscono la Terra. Per semplificare i dati, i ricercatori del National Centers for Environmental Information raggruppano tutti i fulmini che si verificano in un'area "quadrata" di circa 11x11 chilometri (0,1° di latitudine per 0,1° di longitudine) in un unico punto. Questo punto rappresenta la posizione media di tutti i fulmini in quell'area per un giorno specifico.

Per maggiori informazioni, consultare [qui](https://ghrc.nsstc.nasa.gov/uso/ds_docs/nldn/gai_dataset.html#) la documentazione.

## Panoramica del Dataset
Ogni riga del dataset rappresenta il conteggio totale dei fulmini (nube-suolo) registrati in una posizione e data specifiche. 

Di seguito sono riportate le informazioni sulle colonne.

|Nome colonna|	Type	|Descrizione|
|---|---|---|
|number_of_strikes|	int64|	Il conteggio totale dei fulmini in quella casella geografica in una data specificata|
|center_point_geom|	str|	Stringa di caratteri che rappresenta il punto centrale geografico dei fulmini in base alla latitudine e alla longitudine specificate|
|longitude|	float64|	Punto longitudinale estratto da center_point_geom |
|latitude	|float64|	Punto latitudinale estratto da center_point_geom |
|date	|str|	Data di registrazione (formato: YYYY/MM/DD)|
|zip_code|	float64|	Codice postale degli Stati Uniti in cui si trova il punto centrale specificato|
|city|	str	|Città degli Stati Uniti in cui si trova il punto centrale specificato |
|state	|str|	Stato degli Stati Uniti in cui si trova il punto centrale specificato |
|state_code|	str|	Abbreviazione di due lettere dello stato degli Stati Uniti in cui si trova il punto centrale|

## Riepilogo analisi

- [Analisi EDA Fulmini NOAA 2018](Analisi_EDA_fulmini_NOAA.ipynb)
In questo notebook, userò `pandas` per esaminare i dati sui fulmini del 2018 raccolti dalla National Oceanic and Atmospheric Administration (NOAA).
Successivamente calcolerò il numero totale di fulmini per ogni mese e visualizzerò queste informazioni su un grafico a barre.

**Fonte dataset**: BigQuey Public Dataset
 
