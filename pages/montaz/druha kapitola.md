1. # **Vytvorenie základného simulačného modelu**
Na hlavné okno model presuňme objekt Source, Station a Drain. Tieto objekty prepojíme konektorom. Výsledný jednoduchý model ukazuje obrázok.

![Graphical user interface Description automatically generated](Aspose.Words.addb4a71-4055-4869-be72-dd749ac8e9a5.001.png)


Beh simulačného modelu ovláda objekt EventController. Tento objekt sa implicitne nachádza po vytvorení nového projektu na hlavnom okne model. Pokiaľ sa objekt EventControler na hlavnom okne nenachádza je možné ho doplniť za pomoci ToolBox panelu z karty Material Flow.  Po otvorení vlastností objektu EventControler(napr. dvojklikom) sa otvorí nastavovacie dialogove okno EventContorler obr.

![Graphical user interface, diagram Description automatically generated](Aspose.Words.addb4a71-4055-4869-be72-dd749ac8e9a5.002.png)

*Obr. 2.2 Nastavovacie okno objektu EventController*

Simuláciu je možné spustiť pomocou tlačidla Štart/Stop simulácia. Beh simulácie sa prejaví narastajúcim časom v informačnom okne Time a preblikávaním status lediek na simulačnom modeli ako ukazuje obr.

![Diagram Description automatically generated](Aspose.Words.addb4a71-4055-4869-be72-dd749ac8e9a5.003.png)

*Obr. 2.3 Ukážka behu základného simulačného modelu*

Zároveň sa na jednotlivých objektoch zobrazujú objekty MUs, čo sú v našom jednoduchom prípade objekty typu Part. Posúvaním nastavenia rýchlosti simulácie sa koriguje rýchlosť simulácie čo sa prejaví rýchlosťou ubiehajúceho času a zobrazovaním MUs objektov. Simuláciu je možné zastaviť opätovným stlačením tlačidla Štart/Stop. Reset simulácie je možné vykonať poklepaním na tlačidlo reset. Resetuje sa objekt EventControler, vynuluje sa odpočítavanie času vynuluje sa používané MUs a je možné simuláciu opätovne spustiť od východzieho stavu. V prípade, že chceme využiť funkcionalitu rýchle dopredu, a prejsť celou simuláciou v najkratšom možnom čase, je potrebné nastaviť dĺžku celkovej simulácie. Toto sa vykonáva na karte Settings objektu EventControler na položke End.
1. ## **Význam ukazovateľov stavu objektu.**
Objekty simulačného modelu sa môžu nachádzať v určitom prevádzkovom stave. Napr. objekt materiálového toku  Station sa môže nachádzať v stave, že pracuje, čaká , je blokovaný atď. Stav týchto objektov je možné ukazovať pomocou zmeny ikony alebo pomocou farebných ukazovateľov ktoré sa zobrazujú pri ikone daného objektu. Zobrazovanie stavov pomocou ukazovateľov a zobrazovanie materiálového toku je možné zapnúť alebo vypnúť na Ribon bare na paneli Home v časti Animations tlačidlami MUs a Icons, ako ukazuje obrázok.

![Graphical user interface, application

Description automatically generated](Aspose.Words.addb4a71-4055-4869-be72-dd749ac8e9a5.004.png)

*Obr. 2.4 Zmena stavov ukazovateľov objektov*

Základný význam jednotlivých stavov objektov sumarizuje tabuľka:

|Stav objektu|Ukážka|Farba Indikátora|
| - | - | - |
|Blokované|![](Aspose.Words.addb4a71-4055-4869-be72-dd749ac8e9a5.005.png)|źltá|
|Závada|![](Aspose.Words.addb4a71-4055-4869-be72-dd749ac8e9a5.006.png)|červená|
|Pauza|![](Aspose.Words.addb4a71-4055-4869-be72-dd749ac8e9a5.005.png)|modrá|
|Zapínanie/Vypínanie|![](Aspose.Words.addb4a71-4055-4869-be72-dd749ac8e9a5.007.png)|fialová|
|Reštartovanie|![](Aspose.Words.addb4a71-4055-4869-be72-dd749ac8e9a5.008.png)|tyrkysová|
|Nastavovanie|![](Aspose.Words.addb4a71-4055-4869-be72-dd749ac8e9a5.009.png)|hnedá|
|Zastavovanie|![](Aspose.Words.addb4a71-4055-4869-be72-dd749ac8e9a5.006.png)|ružová|
|Neplánované|![](Aspose.Words.addb4a71-4055-4869-be72-dd749ac8e9a5.009.png)|slabo modrá|
|Čakanie |![](Aspose.Words.addb4a71-4055-4869-be72-dd749ac8e9a5.010.png)|oranžová|
|Práca|![](Aspose.Words.addb4a71-4055-4869-be72-dd749ac8e9a5.009.png)|zelená|

V prípade nášho jednoduchého modelu je možné vidieť len stav Práca (zelený indikátor) kedy stanica vykonáva činnosť a stav Blokovanie (žltý indikátor) kedy objekt Source čaká na to kým stanica vykoná prácu a uvoľni  miesto pre ďalšie MU ktoré sa bude spracovávať.
1. ## **Nastavenie vlastností objektov materiálového toku**
Vlastnosti objektov simulačného modelu je možné meniť a nastavovať tak aby celkový model nadobúdal vlastnosti s realitou, a aby mohlo byť skúmané jeho správanie. Dialog nastavenia vlastností objektov sa otvára dvojklikom ľavým tlačidlom myši na objekt, alebo pravým tlačidlom myši z výberom možnosti Open v menu. Každý objekt obsahuje vlastnosti a nastavenia v závislosti od toho o aký objekt sa jedná a na čo sa používa. V prípade že potrebujeme objekt so špecifickou úlohou ktorá nie-je zahrnutá v základných objektoch, je možné vytvoriť si objekt vlastný.   
1. ## **Zmena základných vlastností objektu Station**
Dvojklikom na objekt station v základnom simulačnom modeli sa otvorí dialógové okno nastavenia tohto objektu. Základná vlastnosť ktorú je možné meniť je meno (Name) objektu. V prípade zmeny vlastnosti Name objektu platí zásada:

**!!!nepoužívať pri menách objektov ani celkovo diakritiku a ani medzery!!!** 

Vlastnosť objektu Name je špecifická pre daný objekt, nemôže byť v projekte viac objektov z rovnakým menom, a využíva sa na volanie objektu z ktorejkoľvek časti projektu. Zmeňme vlastnosť Name objektu Station na stroj tak ako ukazuje obrázok:

![Graphical user interface, application

Description automatically generated](Aspose.Words.addb4a71-4055-4869-be72-dd749ac8e9a5.011.png)

*Obr. 2.5 Zmena vlastnosti Name objektu Station*

Zmena názvu sa prejavila v popise objektu na hlavnom okne. Vedľa každej vlastnosti ktorú je možné nastavovať sa štandardne nachádza zeleno-modrý štvorček![](Aspose.Words.addb4a71-4055-4869-be72-dd749ac8e9a5.012.png). Tento znázorňuje že vlastnosť je zatiaľ nezmenená, jej hodnota je zdedená z predchodcu. Pokiaľ vlastnost zmeníme štvorček zmení farbu ![](Aspose.Words.addb4a71-4055-4869-be72-dd749ac8e9a5.012.png). Táto zmena indikuje zmenu implicitne nastavených vlastností objektu. Zmeny sa aplikujú až po poklepaní na tlačidlo Apply ![](Aspose.Words.addb4a71-4055-4869-be72-dd749ac8e9a5.013.png). Poklepaním na tento štvorček po zmene vlastností je možné nastaviť danú vlastnosť do pôvodného stavu(zdediť vlastnosť po rodičovi). 

Vlastnosti objektu sú usporiadané do skupín ktoré sa nachádzajú na kartách dialógového okna. V prípade objektu Station sa jedná o karty: “Times”, ”Set-Up”, ”Failures”, ”Controls”, ”Exit”, “Statistic”, “Importer”, “Energy”, “Cost” a “User-defined”. V prípade že chceme zmeniť dĺžku času práce stanice s aktuálnym MU, je možné toto nastaviť na karte Time zmenou položky Processing Time. Implicitne je táto položka nastavené na 10s. Zmeňme toto nastavenie na 1min 20s zadaním 1:20 a kliknutím na tlačidlo ![](Aspose.Words.addb4a71-4055-4869-be72-dd749ac8e9a5.013.png) ako ukazuje obr.

![Graphical user interface, application

Description automatically generated](Aspose.Words.addb4a71-4055-4869-be72-dd749ac8e9a5.014.png)

*Obr. 2.6 Princíp zadávania veličín času*

Aj v prípade zmeny vlastnosti času, zmení sa aj indikátor dedičnosti z![](Aspose.Words.addb4a71-4055-4869-be72-dd749ac8e9a5.012.png)na![](Aspose.Words.addb4a71-4055-4869-be72-dd749ac8e9a5.012.png). Nad oknom zadávania času je zobrazená nápoveda ktorá ukazuje formát zadávania času “DDD:HH:MM:SS.XXXX”. To znamená, že Dni-DDD, hodiny-HH, minúty-MM a sekundy-SS sú oddelené znakom dvojbodka ”:”. Ak je potrebné tak je možné zadávať aj desatiny, prípadne stotiny sekundy za znakom bodka”.” ktorý reprezentuje desatinnú čiarku. V prípade že zadáme údaj len v skundách “napr. 3860” po kliknutí na tlačidlo Apply sa automaticky tento údaj pretransformuj na 1 hod. 4 min. a 20 sekúnd “1:04:20”.

