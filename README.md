# Caduti-dal-Cielo-bot
Documentazione Bot Caduti dal Cielo
Descrizone: Il bot, nasce con lo scopo di ampliare ed in alcuni casi automatizzare l’esperienza di role play dei giocatori della campagna Caduti dal Cielo.
Features:Il bot dovrà essere dotato di : Trasporto automatico nei gruppi(Se possibile), Inventario del Personaggio, Sistema per la gestione delle abilità del Personaggio, Sistema per la creazione del Personaggio, Pannello di controllo del bot direttamente da Telegram in modo da non dover fermare l’esecuzione del server, Sistema di trasferimento oggetti e denaro.
Trasporto automatico:
Il personaggio che vuole cambiare luogo, clicca sul pulsante per spostarsi, il bot allora deve avere i permessi per cacciare e aggiungere al gruppo il personaggio, o comunque mandare il link per spostare il personaggio. 
N.B. Se manda il link, non può cacciare il personaggio perché altrimenti non avrebbe più accesso al link.
Inventario del Personaggio:
Ogni Giocatore che scrive in chat pvt al bot può accedere al proprio inventario, e buttare gli oggetti, o controllare le sue statistiche come abilità, punti esperienza etc etc.
Sistema per la creazione del Personaggio:
Il giocatore nuovo, può effettuare la registrazione dal bot direttamente. Il bot deve mostrargli quali abilità può acquistare e tenere conto dei punti exp spesi. NON CI DEVONO ESSERE BUG! Inoltre il bot all’inizio manda un breve testo dove spiega l’importanza di un Background e manda anche un link per accedere al form Google dove inserire il background.
Pannello di controllo del bot direttamente da Telegram:
Questo pannello lo possiamo usare solo io e luca, con questo si deve poter esiliare un chat_id, bannare temporaneamente, controllare i personaggi in viaggio, mandare post globali o solo ad alcune chat,poter spegnere il bot in caso di errori

Pseudocodice Viaggio automatico(gruppo):
1.	Premo sul luogo in cui voglio andare
2.	Il bot riceve il chat_id dal comando che è stato lanciato
3.	Ti espelle dal gruppo
4.	Ti aggiunge al gruppo selezionato
5.	Fine
Pseudocodice Viaggio automatico(globale):
1.	Vado nella chat singola del bot
2.	Seleziono la modalità viaggio
3.	Seleziono il luogo in cui voglio andare
4.	Il bot calcola il tempo che ci metto e lo invia
5.	Al termine del conteggio il bot aggiunge automaticamente(o invia il link per entrare) al giocatore.
6.	Il bot manda uno o due giorni prima il reminder che si sta avvicinando alla città.
7.	Il bot ti aggiunge ad un gruppo appartente a quella zona di viaggio(immaginare come una matrice), dove possono accadere cose al personaggio mentre è in viaggio, o si possono incontrare persone lungo la strada
8.	Fine
Inventario del personaggio
1.	Il giocatore usa il tasto inventario per accedere all’inventario
2.	Il bot si collega al database, cerca nella colonna del chat_id quello del giocatore
3.	Acquisisce in una variabile il contenuto e lo manda al giocatore
4.	Il giocatore poi attraverso vari script può decidere quali oggetti buttare, quanto denaro inviare ecc
Sistema per la creazione del Personaggio
1.	Il bot chiede step by step tutto ciò che c’è da sapere e lo aggiunge al database nella riga del chat_id del personaggio, ma prima di fare ciò invia il form per compilare il background.

Pannello di controllo del bot direttamente da Telegram:
1.	Il bot deve riconoscere solo comandi inviati da me e zio luca attraverso i nostri chat_id
2.	Per esiliare un chat_id il bot riceve il comando di bannare per sempre una persona da tutti i gruppi principali, poi manda in chat il messaggio di esilio
3.	Per bannare temporaneamente il bot utilizzando sempre il chat_id, si procede alla stessa maniera del comando di esilio
4.	Quando un personaggio entra nella sezione di viaggio, lo aggiunge ad un database e inserisce dove sta andando e da dove è partito, inoltre dice anche quando arriverà
5.	Per mandare un messaggio a delle particolari chat si utilizzeranno delle funzioni o librerie che hanno salvate tutti i chat_id dei gruppi, suddivisi per città o luogo.
Sistema di quest:
1.	Chiaramente uguale a quello di prima utilizzando delle funzioni random, implementando le foto


