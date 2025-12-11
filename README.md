# ProjectDataVisualisation
## Samenvatting
Dit project is een weergave van de toegankelijkheid van de ziekenhuizen in de stad Antwerpen.
Er wordt per wijk gekeken naar het aantal inwoners van een bepaalde leeftijdsgroep, maar ook naar factoren zoals
de sociaal-economische status, en de afstand tot het dichtsbijzijnde ziekenhuis.

## Verwerking van data
1.  Ziekenhuis data ingelezen.
2.  Geografische data van de wijken ingelezen.
3.  Gemiddelde afstand berekend van wijk tot dichtsbijzijnde ziekenhuis.
4.  Sociaal-economische data ingelezen.
5.  Data over aantal inwoners van een wijk, per leeftijdsgroep ingelezen.
6.  Slider toegevoegd om te filteren op leeftijdsgroep.
8.  Map gemaakt.
9.  Wijkgrenzen toegevoegd.
10.  Ziekenhuismarkers toegevoegd aan map.
11.  Kleurcomponent afhankelijk van alle factoren met hun gewichten berekend en toegevoegd aan elke wijk.

## Ondervinding
De stad Antwerpen heeft een zeer goede toegankelijkheid, maar toch weegt het aantal inwoners het zwaarst op de toegankelijkheid.
Er kan gekeken worden naar elk van de factoren appart door de gewichten aan te passen naar keuze.

## Moeilijkheden
-   GEOJSON wijk features waren opgehaald op een random volgorde en hadden niet dezelfde naamgeving als de andere datasets. Dit zorgde ervoor dat wijken juist berekent werden, maar foutief op de map getoond werden.

    Oplossing: Foutieve kolomnamen gemapped op de kolomnamen van een dataset met de juiste namen.

    Resultaat: Consistente naamgeving.

- Code veralgemenen om later gemakkelijk andere factoren toe te voegen.

    Oplossing: Trial and error.

    Resultaat: Data verwerken volgens een bepaalde stappenplan: inladen, schoonmaken, filteren, omzetten naar dictionary (om gemakkelijk op te zoeken), normalize functie maken, verwerken in de style functie.

## Bronnen
GeoJSON
'https://geodata.antwerpen.be/arcgissql/rest/services/P_Portal/portal_publiek2/MapServer/97/query?outFields=*&where=1%3D1&f=geojson'

Overzicht ziekenhuizen
https://portaal-stadantwerpen.opendata.arcgis.com/datasets/ziekenhuis-overzicht

Leeftijd per wijk (per 10 jaar)
https://stadincijfers.antwerpen.be/viewer/ViewerTable.aspx?&wsguid=387f17df-bbb4-416b-b3b2-fb49f68570b5&ps=-529394

Wijkenranking: totaalscore sociaal-economische situatie (0 tot 100)
https://stadincijfers.antwerpen.be/viewer/ViewerTable.aspx?&wsguid=387f17df-bbb4-416b-b3b2-fb49f68570b5&ps=-529394