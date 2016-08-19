# Priegelige data; hoe kan je die visualiseren in een prachtige kaart.


Er is een overvloed aan nauwkeurige data beschikbaar maar hoe kan je die met zo weinig mogelijk handwerk toch overzichtelijk presenteren? 

Voorbeeld 1: In OpenStreetMap.org krijg je details van alle straten en vele Points Of Interest (poi’s). 
Wat zijn de technische mogelijkheden als je daarmee een overzichtelijk kaartje van heel Nederland op schaal 1:1,5 miljoen (A4 formaat) moet maken?

Voorbeeld 2: Alle rivieren uit NaturalEarthData.com (1:10 miljoen) plus enkele GPS tracks toepassen in een kaartje van West-Europa op schaal 1:20 miljoen (A4 formaat)?


Op 20160616 noteerde Marijn alvast wat losse ideetjes, vragen en praktische tips, in willekeurige volgorde.
Deze kunnen we op Dag 5 (20160819) bespreken en er gezamenlijk wat mee oefenen. 
En hier op Github kan eenieder deze notities natuurlijk aanvullen!


### 01* Snelwegen    
(dus met meerdere rijbanen) en verkeersknooppunten:
de grote lijnen weergeven d.m.v. brede contourlijnen.


### 02* Losse huisjes “opdikken”   
d.m.v. outline zodat ze aaneengesloten vlakken gaan vormen, kleur dimmen, evt. slagschaduw toevoegen.


### 03* Generaliseren nabootsen   
door een grove kopie te maken, bijvoorbeeld de aquarel-vormgeving van Stamen
http://maps.stamen.com/watercolor/#12/37.7706/-122.3782


### 04* Echt generaliseren d.m.v. algoritmen
http://openstreetmapdata.com/processing/generalization
“The process of adapting the detailed map data as it has been surveyed to the target map scale and resolution is called cartographic generalization. This is neglected in most digital zoomable maps. Key to good quality generalization and ultimately clear and well readable maps is the elimination of unimportant details that cannot be properly shown and at the same time selection and emphasis of key elements. This is not to be confused with mere geometric simplification which is just one element of generalization and which is widely used in digital map production.”
“The technique used for that is a raster-based process implemented in the coastline_gen tool.”
https://github.com/imagico/coastline_gen


### 05* Extreem dunne lijnen op papier    
zoals wegen op papier afdrukken zonder rafelige rasterpuntjes d.m.v. kleurmengsel zoals 20c 40k. 
Lijn met volle kleur zoals 100c op papier niet dunner dan 0,1 of 0,08 mm.
Lijn met gemengde kleur zoals 20c 40k op papier niet dunner dan ??


### 06* Extreem dunne lijnen op beeldscherm    
afbeelden d.m.v. Anti-Alias.
(Het is in Adobe Illustrator mogelijk om een handige voorvertoning te krijgen d.m.v. Pixel Preview.)


### 07* Tekst plaatsing   
Selectie d.m.v. attributes, of Layer, of kleur, of font.
Anker / pivotpoint in het midden, of juist links.
“Kapitaal” of “Title Case” of “onderkast”.
Basislijn verschuiven, zodat namen van straten en rivieren een eindje naast het lijn-element worden gezet.


### 08* Puntsymbolen samenvoegen   
losse symbolen evt vervangen door 1 puntsymbool met getal 
proportioneel symbool
kleingeld-methode


### 09* Contouren weglaten   
van kusten en weggetjes 


### 10* Zoom-levels


### 11* Informatie pas zichtbaar maken na een muisklik   
“call outs” of “pop-ups”.


### 12* Asymetrische symbolen   
Puntsymbolen die elkaar per ongeluk grotendeels overlappen zichtbaar maken door aan elke soort puntsymbool een ander “oortje” te tekenen.


### 13* Kleuren dimmen of juist accentueren


### 14* Kleur rood helemaal weglaten    
zodat een bleke kaartachtergrond ontstaat waarop je later een roodgekleurd thema goed kan laten opvallen.
https://twitter.com/FrieseWoudloper/status/686231069713149955


### 15* Onderwerp opdelen en elk sub-onderwerp afzonderlijk vertonen   
Bijvoorbeeld in een kaart het autoverkeer en parkeerplaatsen, in een andere kaart de culturele instelingen en in een derde kaart de horeca.


### 16* Contrast   
Doe de “zwart-wit test”, maak een zwart-wit kopietje. 
Als het groene bos en de rode wandelroutes er dan even donkergrijs uitzien dan moet je in de originele kaart andere kleurtinten kiezen.


### 17* Plaatselijk loepje


### 18* Details extra uitlichten   
Bijvoorbeeld 1 routelijn met een extra felle kleur aangeven zodat die lijn zichtbaar wordt ten opzichte van de overige “spaghetti”.
https://www.europafietsers.nl/fietsroutes/routes-op-de-kaart-fietsweb


### 19* Lijnen die te dicht naast elkaar liggen gaan elkaar overlappen   
Na het verkleinen van de kaartschaal kan je sommige lijnen niet meer goed zien.
Bijvoorbeeld de middenlijn van de rivier de Rijn, de lijnen van de infrastructuur (spoorlijnen, jaagpaden, lokale wegen, snelwegen) die er op de linker- en rechter oever naast liggen, en de lijn van een fietsroute op de oever.
Voor je het weet gaat de fietsroute door het water ;-)
Wat zijn de mogelijkheden om sommige lijnen automatisch te laten verschuiven?


### 20*
Aan objecten kun je schaduw toevoegen. In QGIS kan dit heel eenvoudig, bij de stijl van de laag:
- Eigenschappen / stijl 
- Onderaan een deel Rendering. Hierin zit Tekeneffecten, daar kun je gloed/schaduw etc aangeven
 

### 21*
Je kaart moet natuurlijk ook weer kopie-veilig en kleurenblindlogisch zijn. In QGIS is dit heel makkelijk te checken, zowel in de printmodus als de werkmodus: Beeld / Modus voorvertoning
