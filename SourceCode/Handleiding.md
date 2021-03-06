Coos, [18.12.19 20:46]
Gebruiksaanwijzing voor de meetzender software V.3012

**********************************
*
* -------- Display -----------
* regel1: f=  432.260.000 kHz
* regel2:  3e harmonic -9.5 dB
* regel3: L= - 73 dBm  xxxxxxx 
* regel4:      50  uV S9 + 0dB
* ----------------------------
*
*
*         Draaischakelaars:
*    S1         S2         S3
*   Level      N.C.    Frekwentie
*
*
*           Drukknoppen:
*   S4      S5      S6      S7 
* Store    Get   HamBand  Config
* waarde  waarde   Menu    Menu
*
**********************************

(dubbel)Functies van de knoppen:

S1 draaien om verzwakking in te stellen, op regel3,
   regel4 geeft de uitgangsspanning in mV, uV of nV 
   en de S-schaal van  S9+73dB tot S0-23dB
   drukken keuze 0, -33, -73, -109, -127, -140 dB

S3 draaien voor continue frekwentie instellen
   drukken onm de digit (stap) te kiezen


S4 Store waarde, slaat level en Frekwentie op in EEprom 

S5 Get waarde, haal opgeslagen Level en Frekwentie uit EEprom

S6 HamBand Menu, Met S3 draaiknop kies je een HamBand

S7 Dubbele functie, kort drukken kom je in het configuratie menu
   Lang drukken (>3 seconden) een soft reset indien nodig.


Configuratie Menu, met S3 draaiknop de optie kiezen
1: calibratie xxx  ppm
2: Si5351 fMax <150 MHz
3: Harmonic factor 3-15
4: Drive Output 2,4,6,8 mA
5: Zet waarden in EEprom
   Met S1 de optie bevestigen en draaien voor waarde veranderen.
   Opnieuw S1 op de waarde te bevestigen.

1: calibreren van het 25MHz referentie Xtal 
Calibratie van het referentie Xtal frequentie, correctie in ppm
S1 drukken en dan met S1 de correctiewaarde instellen
S1 opnieuw drukken om de waarde te bevestigen

2: Si5351 fMax
Default waarde is 150MHz, kan met 25MHz stappen tot 300MHz.
N.B. door een beperking van de etherkit library kan bij frekwenties
vanaf 150 MHz de output willekeurig uitvallen, deze optie is voor test.
Met S1 kiezen en bevestigen.

3: Harmonic factor naar keuze 1, 3e, 5e, 7e, 9e, 11e, 13e, 15e
Te activeren met S1, draaien voor waarde en opnieuw S1 drukken om te bevestigen.
Bij 1 kan de meetzender tot 150MHz, met 3 tot 450 MHz enz.
1e-150 / 3e-450 / 5e-750 / 7e-1050 / 9e-1350 / 11e-1650 / 13e-1950 / 15e-2250MHz
Indien van toepassing staat op regel 2 de harmonische met de correctie.
Harmonischen van een blokgolf zijn minder sterk dan de grondgolf.
3e harminische is 1/3 in spanning, wat gelijk staat aan -9.5dB
5e=-14dB  7e=-17dB  9e=-19dB 11e=-21dB 13e=-22.5dB 15e=-23.5dB
N.B. deze waarden zijn afgerond op 0.5dB (onnauwkeurigheid +/-0.25dB
Deze waarde moet van de aangegeven waarde afgetrokken worden om het juiste niveau v/d harmonische te berekenen. 
B.v. L=-33dB en 3e harm=-9.5, dan is niveau (-33 -9.5) = -43.5dB. 
De grondtoon is ook aanwezig op -33dB, net als alle harmonischen aanwezig zijn met een afnemend niveau.
Dat is onvermijdelijk met een ongefilterde blokgolf.
 
4: Si5351 Drive Output kan ingesteld worden, default waarde = 2mA. 
Daarop is de meetzender geijkt. Tijdelijk kan er een grotere Drive output gekozen worden, op regel 3 bij xxxx wordt de correctie waarde in dB gezet.
4 mA = +3dB / 6 mA = + 9.5 dB / 8 mA = +12 dB op te tellen bij het niveau

5: Zet waarden in EEprom
Door S1 te drukken staat op regel 3 Level knop opslaan en regel 4 annuleren andere knop,
Door opnieuw S1 te drukken worden de Referentie correctie (ppm) en de harmonische opgeslagen in EEprom. 
Drive mA en fMax van Si5351-chip worden niet opgeslagen, zodat bij een koude start of reset de Maximale frekwentie 150 MHz is en de Drive 2 mA bedraagt.

Opnieuw drukken van S7, verlaat het configuratie menu.
