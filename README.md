# Keldertijd — prototype 0.1

Een Nederlandstalige, mobielvriendelijke eerste versie van een persoonlijke drankkelder.

## Wat werkt al?
- Wijn, bier, whisky, rum, port, champagne en overige dranken registreren
- Naam, producent, jaar/batch, regio, aantal, prijs, drinkstatus, drinkvenster, proefnotities en eigen notities opslaan
- Zoeken en filteren
- Eenvoudige tips op basis van de gegevens die je zelf invult
- JSON-reservekopie exporteren
- Gegevens blijven in de lokale browseropslag

## Eerlijke beperkingen van versie 0.1
- Er is nog geen synchronisatie tussen apparaten.
- Er zijn nog geen externe drankendatabases of echte AI-integratie gekoppeld.
- De suggesties zijn eenvoudige regels op basis van je eigen invoer; geen professioneel rijpingsadvies.

## Eerst lokaal proberen
Open `index.html` in een moderne browser. Op sommige apparaten werken lokale bestanden anders; bij voorkeur publiceer je de bestanden als statische website.

## Volgende bouwstap: gratis cloudsynchronisatie
De logische volgende stap is een gratis Supabase-project met e-mailinlog en een database. Daarna kunnen we dezelfde kelder op computer en telefoon beschikbaar maken. Gebruik nooit een `service_role`-sleutel in de webapp; alleen de publieke anon/publishable key met Row Level Security.

Daarna voegen we een gegevensbron voor drankproducten toe en maken we een AI-advieslaag die expliciet onderscheid maakt tussen:
1. echte proefnotities van gebruikers/critici;
2. producentinformatie;
3. AI-schattingen met een onzekerheidslabel.
