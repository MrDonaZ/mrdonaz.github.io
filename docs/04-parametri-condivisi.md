# Parametri condivisi

## Informazioni generali

All'interno di Progetto CMR, la gestione dei dati è centrale nel processo BIM. Per questo motivo, l'utilizzo dei **Parametri Condivisi** (Shared Parameters) **non è considerato una scelta opzionale**, ma un requisito obbligatorio per la creazione e la gestione dei modelli.

Qualsiasi parametro personalizzato creato per contenere informazioni rilevanti per abachi, etichette, esportazioni o per rispondere a requisiti informativi (PIR), deve obbligatoriamente essere un Parametro Condiviso derivato dal file template aziendale.

All’inizio della commessa il referente BIM dovrà copiare il file dei parametri condivisi standard di Progetto CMR all’interno della cartella di commessa al percorso XXXX/FASE/Dis/BIM/Arc/PARAMETRI CONDIVISI. Se il progetto prevede la necessità di aggiungere nuovi parametri condivisi, essi dovranno essere aggiunti esclusivamente nel file parametri condivisi di commessa.

**È vietato l'uso di Parametri di Progetto o di Famiglia per dati che devono essere condivisi o estratti dal modello.**

> **💡 Nota bene:**
> 
> Revit di default permette all’utente di collegare al proprio account un file dei parametri condivisi. Controllare **SEMPRE** che Revit stia puntando al file di commessa.



## CAM (CAM)

In questo gruppo si trovano tutti i parametri condivisi che servono per gestire i **dati relativi ai Criteri Ambientali Minimi**all'interno del modello BIM.

Sono tutti parametri di istanza applicati sia alle categorie di modellazione comunemente utilizzate, sia ai Materials (in modo da "intercettare" i singoli strati di pavimenti, tetti e solidi topografici).

*Sono ancora in fase di sviluppo le strategie e procedure per automatizzare la compilazione di questi parametri e la loro estrazione e condivisione con i consulenti ambientali*

| **Nome Parametro**        | **Descrizione**                                                                                                                                                                           | **Tipo di parametro** |
| ------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------- |
| CAM_Conforme              | Specifica se l'elemento seve essere conforme ai CAM. Va compilato con **S** o **N**                                                                                                       | Testo                 |
| CAM_EPD_Presente          | Specifica se per l'elemento è necessaria una certificazione EPD. Va compilato con **S** o **N**                                                                                           | Testo                 |
| CAM_Fine vita             | Specifica il tipo di rifiuto per categoria di elemento. Va compilato con un valore tra quelli nella **tabella "Compilazione Fine Vita"**                                                  | Testo                 |
| CAM_Materiale             | Specifica il materiale principale di cui è composto l'elemento. Va compilato con il riferimento dei CAM (es. **2.4.2** per Calcestruzzi confezionati in cantiere e preconfezionati)       | Testo                 |
| CAM_Percentuale_Riciclato | Specifica il contenuto di materia recuperata, riciclata o di sottoprodotti minimo che deve soddisfare l'elemento, come da tabelle CAM. Va compilato con il numero percentuale **es. 75%** | Testo                 |
| CAM_Smontabile            | Specifica se l'elemento è smontabile o no. Va compilato con **S** o **N**                                                                                                                 | Testo                 |
| CAM_Vita utile            | Specifica la vita utile dell'elemento minima richiesta dai CAM. Indicare un valore in ore (**es. 50000h per le sorgenti luminose LED**)                                                   | Testo                 |

**Tabella 1 Compilazione Fine Vita**

| **Categoria CAM**                      | **Fine vita da inserire nel BIM**                |
| -------------------------------------- | ------------------------------------------------ |
| Calcestruzzi                           | Recupero come inerte riciclato                   |
| Prodotti prefabbricati in calcestruzzo | Recupero/riuso parziale + riciclo inerte         |
| Prodotti in acciaio                    | Riciclo completo                                 |
| Prodotti in laterizio                  | Recupero inerte / riciclo aggregato              |
| Prodotti di legno o a base legno       | Riuso / riciclo / recupero energetico            |
| Isolanti termici ed acustici           | Recupero specializzato o smaltimento controllato |
| Cartongesso e sistemi a secco          | Recupero gesso / riciclo                         |
| Pietra naturale                        | Riuso / recupero inerte                          |
| Pavimenti resilienti                   | Riciclo specializzato                            |
| Ceramica                               | Recupero inerte                                  |
| Serramenti                             | Disassemblaggio e riciclo materiali              |
| Tubazioni in materiale plastico        | Riciclo plastica specializzato                   |
| Tubazioni in Gres ceramico             | Recupero inerte                                  |
| Pitture e vernici                      | Smaltimento rifiuto speciale                     |
| Rubinetteria e sanitari                | Riciclo metalli + recupero inerte                |
| Impianti tecnologici                   | RAEE / recupero componenti                       |
| Vetrate isolanti                       | Riciclo vetro specializzato                      |

Per avere maggiori informazioni circa questo tema si può fare riferimento al documento linea guida alla quale ci siamo ispirati, condiviso dai consulenti ambientali.

Lo trovate sul server al percorso: [U:\Divisioni\BIM & DIGITAL\14 UTILITA'\CAM\informazioni utili CAMBIM 2025.pdf](\\progettocmr.loc\ResourcesPCMR\Divisioni\BIM & DIGITAL\14 UTILITA'\CAM\informazioni utili CAMBIM 2025.pdf)
