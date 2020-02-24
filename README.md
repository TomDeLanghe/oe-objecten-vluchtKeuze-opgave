oe-objecten-vluchtKeuze-start
# Vluchtgegevens verzamelen
## Opstarten
- Aan btnBevestig worden de functions BepaalVluchten, BepaalHoogsteEnLaagstePrijs en MaakPrijsKnoppen gekoppeld.
- Er worden enkele standaardwaarden ingevuld, nl. in txtVertrek en txtAankomst. In dtpVertrekDatum komt de datum die 2 maanden na vandaag ligt.

## function MaakPrijs
Genereert een prijs tussen de 100 en 150 euro (constanten) en retourneert die

## BepaalVluchten
- divDatumKeuze wordt leeggemaakt
- divPrijsKeuze wordt verborgen
- als de gekozen datum in de toekomst ligt, worden er een aantal vluchten aangemaakt (2 - het max. aantal vluchten) met de gekozen vertrekdatum en een prijs geretourneerd door MaakPrijs. Deze vluchten worden in een array **vluchten** bijgehouden.

## BepaalHoogsteEnLaagstePrijs
De variabelen hoogstePrijs en laagstePrijs worden bepaald.

## function MaakPrijsKnoppen
De array **vluchten** wordt overlopen en op basis van de gegevens worden er div-elementen (divDatumElement) aangemaakt die toegevoegd worden aan divDatumElement. divDatumElement heeft de volgende eigenschappen:
- toont datum van vertrek en de prijs (tot op 2 decimalen na de komma)
- heeft de class datumElement
- class datumElement wordt gecombineerd met goedkoopst en duurst, al naargelang het geval
- voert bij een muisklik de methode ToonPrijs uit, waarbij de datum, prijs, plaats van vetrek en aankomst worden meegegeven als parameters.

## function ToonPrijs()
- Alle vluchtgegevens worden getoond in divPrijsKeuze
- divPrijsKeuze krijgt de klasse eindDiv en wordt getoond

## Uitbreiding
Voorzie validatiecontrole bij een klik op de knop btnBevestig:
- Ligt de gekozen datum in de toekomst?
- Is de input in de textboxen lang genoeg?
- Zijn de vertrek- en aankomstplaats niet hetzelfde?

Laat de datums variëren met telkens 1 dag verschil
