# A-visualisering
Pathfinding bygger på den matematiske gren “grafteori”, hvor man undersøger den optimale vej ud fra forskellige kriterier - vejlængde, hastighed, pris osv - gennem forskellige figurer eller netværk.

## Fobedring af heristics

I A*-metoden indgår valg og vægtning af to afstandsmål. Jeg vil teste os frem til den optimale løsning
ved at sammenligne 10.000 gentagelser af en række mulige valg og vægtning af afstandsmål.

Der er tre elementer, der varierer i vores sammenligninger.

● Afstandsmål mellem startpunkt og aktuelt evalueringspunkt. Her afprøver jeg faktisk antal
blokke samt Manhattan-målet

● Afstandsmål mellem evalueringspunkt og slutpunkt. Her afprøver jeg Euklid og Manhattan
målene.

● Vægtning af disse mål. Her varierer jeg vægten på målet mellem evalueringspunkt og slutpunkt
og afprøver vægt 1 (de to afstande vejer lige); 1,25; 1,5; 2; 3; 5 og 10.

Dette giver i alt 2 x 2 x 7 = 28 forskellige varianter. Alle er afprøvet i 10.000 gentagelser og nedenfor
ser jeg på gennemsnitlig køretid og gennemsnitlig vejlængde for de fundne stier. Det gælder om, at
finde den bedste kombination af lav vejlængde og hurtig beregning.
Som illustration ser vi nedenfor resultaterne:
![tidstagning](https://user-images.githubusercontent.com/24294632/114031676-e24c9080-987b-11eb-8330-4e63ece9c0e9.PNG)

Jeg vælger således at Faktisk/Euklid og arbejde videre med

![heristic](https://user-images.githubusercontent.com/24294632/114030543-d3b1a980-987a-11eb-95d0-6affce05785e.png)
A* metoden med Faktisk/Euklid i samme system med forskellig vægt på Euklid. Første graf viser vægt = 1, anden graf vægt =1.25,
graf tre vægt = 1.5, graf fire vægt = 2, graf fem vægt = 3 og graf seks vægt = 5. Vægt = 10 er ikke med da den er ens med vægt = 5
