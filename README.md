![gruppo lineCode](https://imagizer.imageshack.com/img923/557/86bUrf.png)

# Portacs
Applicativo 

Le componenti che lo compongono sono:

1. Server con mappa e motore di calcolo del percorso: [server](https://github.com/lineCode-swe/server)
2. Interfaccia grafica per la visualizzazione della mappa in tempo reale: [ui](https://github.com/lineCode-swe/ui)
3. Unità mobile all'interno della mappa: [unit](https://github.com/lineCode-swe/unit)
4. Sensori che forniscono dati sugli ostacoli presenti in mappa alle unità: [sensors](https://github.com/lineCode-swe/sensors) 

Viene inoltre presentata la documentazione prodotta in relazione allo svolgimento dell'intera attività di progetto.

## Installazione, dipendenze ed esecuzione
Dipendenze:
 - JDK 13
 - Maven
 - Node.js
 - npm
 - angular-cli
 - Docker
 
 Clonare repo e submodule con:
 ```shell
 git clone --recursive https://github.com/lineCode-swe/portacs.git
 ```
Eseguire le operazioni di configurazione per le singole componenti che precedono la compilazione e la creazione delle immagini Docker

Posizionarsi sulla root della repo ed eseguire:
```shell
./prepare
```

Una volta lanciato lo script, le singole componenti vengono compilate e viene creata la Docker image relativa a ciascuna di esse.
É sufficiente avviare i rispettivi container nel seguente ordine:
- Ui
- Server
- Sensors
- Unit
per avviare l'applicativo nella sua interezza.
Se si desidera simulare piú unità é sufficiente avviare container multipli.

Per cancellare gli artefatti e le Docker image creati con l'istruzione precedenti:
```shell
./reset
```
