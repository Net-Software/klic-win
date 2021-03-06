﻿# Release notes

### 21 januari 2019
	In de NTD-omgeving zijn de wijzigingen reeds per 17 januari beschikbaar.

**Documentenbeheer**:
- Validatie dat een aangeleverd document maximaal 8 MB groot mag zijn. (ID 2653, ID 2654)
  * dit geldt zowel voor het actualiseren (centrale netbeheerder) als het aanleveren van beheerdersinformatie (decentraal)

**Performance**:
- Performance verbetering bij het genereren van het zipbestand met de BeheerdersinformatieLeveringen (ID 3558)

------------------------
### 11 januari 2019

**Bug-fixes NTD**:
- Bugfix: in de NTD omgeving worden nu alle statussen in de API response als volledige URL weergegeven. (ID 3557)
- Bugfix: in de NTD omgeving is het probleem opgelost waardoor nu tijdens het opvoeren van een BMKL 2.0 testmelding, niet meer versprongen wordt naar het beginscherm van een klasieke testmelding. (ID 3562)

------------------------
### 2 januari 2019

**Nieuwe ZIP-structuur**:  \
Vanaf 2 januari wordt het ZIP-bestand uitgeleverd met de nieuwe structuur.  \
Zie voor meer informatie over de nieuwe structuur [deze link op GitHub](https://github.com/kadaster/klic-win/tree/master/Uitleveren).  \
Hier is ook de presentatie 'WION levering - producten 2018-05-16.ppsx' te vinden.  \
De leveringen met de nieuwe structuur zijn alleen te bekijken met versie 4.3 van de Klic-viewer. Met deze versie van de Klic-viewer zijn zowel de oude, als de nieuwe leveringen te bekijken.


**Vector-aanlevering**:  \
Op 7 januari staat gepland om de eerste netbeheerder over te sluiten op het nieuwe aanleveringsformaat (IMKL 1.2.1). Netbeheerders die aanleveren via dit formaat, leveren hun netinformatie aan als geo-objecten (features, vectoren). De nieuwe ZIP-structuur, die vanaf 2 januari gebruikt wordt, is hiervoor geschikt.


**Tariefswijziging Klic-melding**:  \
De [tariefswijziging die per 1 januari 2019](https://www.kadaster.nl/-/tarieven-per-1-januari-2019) van kracht is, wordt zichtbaar op het scherm getoond bij een Tracémelding. 


**Synchronisatie API**:  \
Voor Agentschap Telecom zijn de API’s live gezet om KLIC procesgegevens te synchroniseren met hun eigen registratie.

------------------------
### 28 december 2018

**Huisaansluitschetsen**:
- In de productie omgeving is begin december het proces rondom de aanvraag en registratie van huisaansluitschetssen gewijzigd; Deze wijziging wordt ook doorgevoerd op NTD (ID 3246, ID 3457). Het betreft:
  * Voor de aanvraag voor huisaansluitschets (HAS) is er een maximum van 100 adresseerbare objecten (verblijfsobject, standplaats of ligplaats), waar dat voorheen was op basis van 100 unieke adressen. Soms is één unieke adres gerelateerd aan meerdere adresseerbare objecten in de Basisregistratie Adressen en Gebouwen (BAG). De telling van het maximum (100) is gebaseerd op adresseerbare objecten. (ID 3246, ID 3337, ID 3338, ID 3339, ID 3340, ID 3341)
- In de productie omgeving is 22 november het proces rondom de aanvraag en registratie van huisaansluitschetssen gewijzigd; Deze wijziging wordt ook doorgevoerd op NTD (ID 2728). Het betreft: 
    * Omdat ook KLIC aansluit op de wettelijke basisregistratie BAG, moet dit adres in de basisregistratie BAG bestaan. Hierdoor worden alleen nog maar hoofdadressen geaccepteerd, en geen nevenadressen meer. 
        - Bij bestellen via de website is het selecteren van nevenadressen niet meer mogelijk. 
        - Een B2B aanvraag met een HAS aanvraag op een nevenadres wordt afgekeurd.
        - Een HAS die bij de netbeheerder geregistreerd staat onder het nevenadres, kan dus niet meer opgevraagd worden.

------------------------
### release IMKL v1.2.1.2 - 13 december 2018
Naar aanleiding van de Keten Acceptatietesten zijn bevindingen geconstateerd op het IMKL.  \
De voorgestelde wijzigingen zijn geaccordeerd door Werkgroep standaarden KLIC en het BAO KLIC.
 
**[IMKL2015/visualisatie](https://github.com/Geonovum/imkl2015/tree/master/visualisatie)** (versie 1.2.1.2) en
**[IMKL2015/symbool](https://github.com/Geonovum/imkl2015/tree/master/symbool)** (versie 1.2.1.2):
- Aanpassingen van de visualisatie (en gebruikte symbolen) zijn beschreven in [IMKL2015-Handreiking-visualisatie_1.2.1.2.pdf](https://github.com/Geonovum/imkl2015/blob/master/visualisatie/1.2.1.2/IMKL2015-Handreiking-visualisatie_1.2.1.2.pdf)
- Er zijn geen aanpassingen aan het UML-model of het gml-applicatieschema gedaan
- Afgehandelde issues:
  * [Issue 221](https://github.com/Geonovum/imkl2015-review/issues/221)  \
Visualisatie van EV-gebieden is aangepast. Door gebruik te maken van een patroon (i.p.v. transparantie) blijft kabel- en leidinginformatie zichtbaar, ook bij meerdere, overlappende EV-gebieden.
  * [Issue 223](https://github.com/Geonovum/imkl2015-review/issues/223)  \
De visualisatie van de kop van een mantelbuis is aangepast. De kop eindigt nu op het einde van de geometrie van de mantelbuis.
  * [Issue 224](https://github.com/Geonovum/imkl2015-review/issues/224)  \
Het symbool en de grootte voor mof is aangepast (zie SLD).
  * [Issue 225](https://github.com/Geonovum/imkl2015-review/issues/225)  \
De grootte van de symbolen van overige leidingelementen (_Toren_, _Mast_, _Mangat_, _Kast_, _TechnischGebouw_) is aangepast.
  * [Issue 226](https://github.com/Geonovum/imkl2015-review/issues/226)  \
Ook de transparantie van de symbolen van overige leidingelementen is aangepast, om eigen geometrie te kunnen zien.
  * [Issue 227](https://github.com/Geonovum/imkl2015-review/issues/227)  \
Het aangrijpingspunt van het symbool voor een blaasgat op de leiding is verplaatst naar de onderkant.
  * [Issue 230](https://github.com/Geonovum/imkl2015-review/issues/230)  \
Het label met `dieptePeil` wordt nu (onderscheidend) getoond bij de features _DiepteTovMaaiveld_ en _DiepteNAP_.
- Onderstaande [SLD's](https://github.com/Geonovum/imkl2015/tree/master/visualisatie/1.2.1.2) zijn aangepast:
  * sld-aanduidingeisvoorzorgsmaatregel.xml
  * sld-dieptenap.xml
  * sld-dieptetovmaaiveld.xml
  * sld-kast.xml
  * sld-leidingelement.xml
  * sld-mangat.xml
  * sld-mantelbuis.xml
  * sld-mast.xml
  * sld-technischgebouw.xml
  * sld-toren.xml
- De volgende [iconen](https://github.com/Geonovum/imkl2015/tree/master/symbool/1.2.1.2/iconen) zijn aangepast: 
  * dieptenap
  * dieptetovmaaiveld
- Map met [patronen](https://github.com/Geonovum/imkl2015/tree/master/symbool/1.2.1.2/patronen) is toegevoegd; fonts worden niet meer toegepast.

------------------------
### 13 december 2018

**Synchronisatie API**:
- Voor Agentschap Telecom worden API's beschikbaar gesteld om KLIC procesgegevens te synchroniseren met hun eigen registratie. (ID 3409, ID 3492)

**B2B-koppeling BMKL 2.0**:
- Wijziging in de Scopes van OAuth: De benaming van de scope `klic.ntd` in de NTD-omgeving wijzigt. De scope `klic.ntd` zal worden vervangen door: `klic.ntd.centraal`, `klic.ntd.gebiedsinformatieaanvraag.readonly`, `klic.ntd.beheerdersinformatie`, `klic.ntd.beheerdersinformatie.readonly`. (ID 3231, ID 3353)
- De responses van alle BMKL api's bevatten het veld "mutatiedatum". Deze wordt soms gevuld met de default waarde '1999-12-31T23:59:59+01:00'. De Mutatiedatum van de API's krijgen de timestamp van de laatste wijziging. (ID 2673)
- Het veld `giAanvraagStatus` in de GebiedsinformatieAanvragen API wordt met de juiste status gevuld, in plaats van een default waarde `open`. (ID 1992)
- Wanneer je het BIL zip-bestand ophaalt middels de API, kijgt het bestand een naam die is opgebouwd uit "BeheerdersinformatieLevering", het Klicmeldnummer en de bronhoudercode. Bijvoorbeeld: `BeheerdersinformatieLevering_19G003456_kl4141.zip`. (ID 3448)
- Bugfix: Als er bij het opvragen van BeheerdersinformatieAanvraag ook een giAanvraagId wordt opgegeven, wordt vanaf nu alleen de BeheerdersinformatieAanvraag gefilterd met de opgegeven giAanvraagId. (ID 3468)
- BeheerdersinformatieLeveringen worden alleen uitgeleverd in de API als er een levering is geweest. (ID 3278)


**Keten Acceptatietest Bevindingen**:
- Uitlevering (Zip) Bugfix: In de LI.xml wordt nu maar een keer naar één bijlage verwezen. (ID 3438)
- Uitlevering (Zip) Bugfix: Bij het bekijken van de LI.pdf kwam soms een pop-up over mogelijk geen correcte weergave. Dit is opgelost. (ID 3429)
- Uitlevering (Zip) Bugfix: De rotatiehoekSymbool van DiepteNap en DiepeTovMaaiveld wordt nu getoond in png. (ID 3412)

**Bug-fixes**:
- Weer mogelijk voor nieuwe netbeheerder om belangen aan te maken. (ID 3404)
- Performance verbetering. (ID 3113)

------------------------
### 10 december 2018

**Huisaansluitschetsen**: <i>(let op: NTD volgt later)</i>

Het proces rondom de aanvraag en registratie van HAS gaat wijzigen:
- Voor de aanvraag voor huisaansluitschets (HAS) is er een maximum van 100 adresseerbare objecten (verblijfsobject, standplaats of ligplaats), waar dat voorheen was op basis van 100 unieke adressen. Soms is één unieke adres gerelateerd aan meerdere adresseerbare objecten in de Basisregistratie Adressen en Gebouwen (BAG). De telling van het maximum (100) is gebaseerd op adresseerbare objecten. (ID 3246, ID 3337, ID 3338, ID 3339, ID 3340, ID 3341)


Voor meer informatie, zie [deze link op GitHub](Toepassing%20IMKL/Gebruik%20huisaansluitschetsen%20in%20IMKL%20v1.2.1.md). <br>
<br>

------------------------
### 5 december 2018

**B2B-koppeling BMKL 2.0**:
- De API's voor GebiedinformatieLevering (voor AT) en BeheerdersinformatieLevering (voor netbeheerders en AT) worden nu gesorteerd met oplopende datum. (ID 3319)
- Documentatie van de API-sprecificatie (OAS, Swagger) van Beheerdersinformatie Services is geactualiseerd.

**Bug-fixes KLIC-WIN (in de NTD)**:
- Diverse performance verbeteringen. (ID 3272)

------------------------
### release IMKL v1.2.1.1 - 3 december 2018
Naar aanleiding van de Keten Acceptatietesten zijn bevindingen geconstateerd op beschrijvingen van het IMKL.  \
 
**[IMKL2015/regels](https://github.com/Geonovum/imkl2015/tree/master/regels)** (versie 1.2.1.1):
- Aanpassingen van extra regels zijn beschreven in [IMKL2015 v 1.2.1.1_object-attributen-ExtraRegels.xlsx](https://github.com/Geonovum/imkl2015/blob/master/regels/1.2.1.1/IMKL2015%20v%201.2.1.1_object-attributen-ExtraRegels.xlsx);  \
De aanpassingen zijn geel gemarkeerd in het document.
- Er zijn geen aanpassingen aan het UML-model of het gml-applicatieschema gedaan
- Afgehandelde issues:
  * Tabblad _Annotatie_ mist attribuut `labelpositie` met extra regels. Zie [issue 212](https://github.com/Geonovum/imkl2015-review/issues/212)
  * Bij tabblad _Maatvoering_ zijn extra regels toegevoegd bij attribuut `labelpositie`. Zie [issue 213](https://github.com/Geonovum/imkl2015-review/issues/213)
  * Bij tabblad _Utiliteitsnet_ is afkomstklasse van attribuut `beginLifespanVersion` aangepast. Zie [issue 217](https://github.com/Geonovum/imkl2015-review/issues/217)
  * Bij tabblad _Utiliteitsnet_ maar één keer attribuut `beginLifespanVersion`. Zie [issue 218](https://github.com/Geonovum/imkl2015-review/issues/218)
  * Bij attribuut `currentStatus` (afkomst: _UtilityNetworkElement_) is nilReason niet toegestaan. Zie [issue 220](https://github.com/Geonovum/imkl2015-review/issues/220)  \
Hierdoor worden netwerkelementen die hiervan overerven wél gevisualiseerd met de meegeleverde SLD.
  * Bij tabblad _ExtraDetailinfo_ zijn aan de attributen `bestandLocatie` en `bestandMediaType` extra regels toegevoegd. Zie [issue 222](https://github.com/Geonovum/imkl2015-review/issues/222)

------------------------
### 22 november 2018
	In de NTD-omgeving zijn de wijzigingen per 26 november beschikbaar.

**Huisaansluitschetsen**:

Het proces rondom de aanvraag en registratie van HAS is wijzigd:
- Omdat ook KLIC aansluit op de wettelijke basisregistratie BAG, moet dit adres in de basisregistratie BAG bestaan. Hierdoor worden alleen nog maar hoofdadressen geaccepteerd, en geen nevenadressen meer. 
	- Bij bestellen via de website is het selecteren van nevenadressen niet meer mogelijk. 
	- Een B2B aanvraag met een HAS aanvraag op een nevenadres wordt afgekeurd.
	- Een HAS die bij de netbeheerder geregistreerd staat onder het nevenadres, kan dus niet meer opgevraagd worden.


Voor meer informatie, zie [deze link op GitHub](Toepassing%20IMKL/Gebruik%20huisaansluitschetsen%20in%20IMKL%20v1.2.1.md). <br>
<br>

**Keten Acceptatietest Bevindingen**:
- Uitlevering (Zip) aanpassing: Markering Voorzorgsmaatregelen thema’s in leveringsbrief (weergeven in rood). (ID 3244)
- Uitlevering (Zip) Bugfix: In de leveringsbrief wordt nu altijd correct vermeld dat de netbeheerder heeft geleverd. (ID 3259)
- Uitlevering (Zip) Bugfix: Contactinformatie van Klassieke NB wordt in het LI.xml nu correct weergegeven. (ID 3293)
- Uitlevering (Zip) Bugfix: Visualisatie van labels DiepteTovMaaiveld en DiepteNAP (ID 3376)
- Bugfix: Een probleem die op kon treden tijdens het produceren is opgelost. (ID 3333)
- Bugfix: Geen excepties meer bij calamiteitenmelding met eisvoorzorgsmaatregel (EV). (ID 3418)

**B2B-koppeling BMKL 2.0**:
- In de BeheerdersinformatieAanvragen API is er voor de voor biProductiestatus een interne tussenstatus geïntroduceerd: `biGereedVoorLevering`.</br>
  De volgende waarden zijn nu mogelijk voor de biProductiestatus: `biWachtOpAntwoord`, `biInAanlevering`, `biOphalenUitCV`, `biGereedVoorLevering`, `biGereedVoorSamenstellenProduct`. (ID 2844, ID 3431)

**Bug-fixes KLIC-WIN (in de NTD)**:
- Diverse performance verbeteringen. (ID 2844, ID 3107, ID 3195, ID 3272)
- Aanleveren beheerdersinformatie houdt nu niet meer de status "Wordt gevalideerd". (ID 3316)

**Synchronisatie API**:
- Voor Agentschap Telecom worden API's beschikbaar gesteld om KLIC procesgegevens te synchroniseren met hun eigen registratie.

------------------------
### 9 november 2018

**Klic-viewer**:
- Er is een nieuw versie (4.3) beschikbaar van de Klic-viewer.

------------------------
### 7 november 2018

**Beheren communicatie gegevens**: Dienst onder Mijn Kadaster voor netbeheerders en de serviceproviders
- Aanpassen van de communicatiegegevens (URL netbeheerder & Uitvalcontact berichten) geen selfservice meer. Wijzigingsverzoeken worden voortaan afgehandeld via Klantenservice Klic. (ID 3218)
- Er komt een update van de pagina ‘ Beheren Communicatie gegevens”, waarin het mogelijk wordt een ‘WebsiteKlic’ (zie IMKL v1.2.1) op te geven. (ID 2192, ID 2970, ID 3067)
- Van netbeheerder wordt ‘WebsiteKlic’ gepresenteerd op leveringsbrief. (ID 2903, ID 2954,  ID 2955)
- Van netbeheerder wordt de ‘WebsiteKlic’ weergegeven in de GI.xml (KLIC-WIN per 1 januari 2019) (ID 2904)

**KLIC-WIN Voorzorgsmaatregelen (EV) (in de NTD)**:
- Uitleveren EV brief: In de brief wordt locatieWerkzaamheden correct gevuld. (ID 3112) 
- Aanleveren: Controleren of alle meegeleverde sjablonen gebruikt zijn in de beslisregels en een waarschuwing indien niet gebruikt. (ID 1964)
- Aanleveren: De contactpersoon van de aanvrager wordt opgeslagen. Voorheen was er een omissie en werd de contactgegevens van de organisatie opgeslagen. (ID 2260)
- Aanleveren: Keten Acceptaties bevinding: Bij het aanleveren van het voorzorgsmaatregelen bestand worden nu alle associaties met waardelijsten gecontroleerd. (ID 3248)

**B2B-koppeling BMKL 2.0: BeheerdersinformatieAanvragen**:
- De mogelijkheid om de resultaten uit de API te pagineren is in de NTD toegevoegd. (ID 2139)

**Synchronisatie API**:
- Voor Agentschap Telecom worden API's beschikbaar gesteld om KLIC procesgegevens te synchroniseren met hun eigen registratie.

**Keten Acceptatietest Bevindingen**:
- Uitlevering (Zip) aanpassing: Visualisatie bevindingen. Zie issues 221, 223, 224, 225, 226 en 227 op de [Github van Geonovum](https://github.com/Geonovum/imkl2015-review/issues). (KLIC-WIN ID 2838, ID 3186, ID 3207, ID 3208, ID 3209, ID 3253, ID 3264, ID 3265, ID 3266)   
- Uitlevering (Zip) bugfix: Sommige annotaties werden niet weergegeven (ID 3292)
- Uitlevering (Zip) bugfix: Het lettertype van het Maatvoering-/Annotatielabel is aangepast naar 'Liberation Sans' conform het visualisatie document van Geonovum. (ID 3314, ID 3296)
- Uitlevering (Zip) bugfix: EigenTopo met status "plan" wordt nu gevisualiseerd in de png. (ID 3310)
- Uitlevering (Zip) bugfix: ExtraDetailInfo type "profielschets" en "overig" worden nu ook gevisualiseerd in de png bij een 2500x2500 melding. (ID 3311)
- Uitlevering (Zip) bugfix: Alle appurtenances worden nu uitgeleverd in de png. (ID 3312)
- Uitlevering (Zip) bugfix: Visualisatie van ExtraDetailinfo in de png heeft nu juiste kleur bij alle zoomniveaus. (ID 3313)
- Aanleveren netinformatie: “nilReason” waarde bij "currentStatus" van UtilityNetworkElement, worden niet meer toegestaan. (ID 3221)

**Bug-fixes KLIC-WIN (in de NTD)**:
- Aanleveren Documenten houdt nu niet meer de status "Wordt gevalideerd". (ID 3089, ID 3202)
- Als er meer dan 1000 validatiemeldingen zijn bij het aanleveren van documenten, komt er te staan "Er zijn meer dan 1000 validatie meldingen. Meer meldingen worden niet getoond." (ID 3253, ID 2261)
- Testmeldingen met een grote (graaf)polygoon kunnen door de netbeheerder opgevraagd worden via de API. (ID 3276, ID 3350, ID 3355)
- Diverse performance verbeteringen. (ID 2338, ID 2687, ID 3277)

------------------------
### 29 Oktober 2018

**Beheren Belangen**:

Ter voorbereiding op de KLIC-WIN implementatie wordt binnenkort mogelijk gemaakt om 2 nieuwe contactsoorten op te voeren in de belangenregistratie.
- Contact netinformatie: De contactpersoon voor de grondroerder voor vragen over de kabels en leidingen. (ID 2361)
- Contact storing/schade: Contactgegevens voor de grondroerder bij schade of storing. (ID 2361)

**Aanpassing leveringsbrief**:
- Deze bovengenoemde contacten, indien gevuld, worden gebruikt in de leveringsbrief.
- De layout van de leveringsbrief wordt aangepast. Hiermee wordt de leveringsbrief overzichtelijker.

**BGT**:

De Basisregistratie Grootschalige Topografie (BGT) leidt tot een gedetailleerde digitale kaart van Nederland. De GBKN achtergrondkaart die gebruikt wordt binnen KLIC, zal vervangen worden door een BGT achtergrondkaart.

Deze nieuwe achtergondkaart zal op 3 plaatsen binnen KLIC gebruikt gaan worden:
- Klic-online (bij het doen van een graafmelding, oriëntatieverzoek en calamiteitenmelding);</br>
  Als achtergrondkaart wordt hier de visualisatie van "BGT omtrekgericht" gebruikt. (ID 2161)
- In de Klic-ontvangstbevestiging;</br>
  Als achtergrondkaart wordt ook hier de "BGT omtrekgericht" gebruikt.  (ID 2162)
- Binnen de Klic-levering;</br>
  Als achtergrondkaart wordt hier de visualisatie van "BGT pastel" gebruikt. (ID 2163)


Er zijn verschillende voorbeeldbestanden op [onze GitHub pagina](https://github.com/kadaster/klic-win/tree/master/Uitleveren/Voorbeelden%20met%20BGT) gepubliceerd.

**Synchronisatie API**:
- Voor Agentschap Telecom worden API's beschikbaar gesteld om KLIC procesgegevens te synchroniseren met hun eigen registratie. (ID 2137)

**KLIC-WIN Voorzorgsmaatregelen (EV)**:
- De controle op placeholdernamen is verruimd. (ID 2887, ID 2893)
- Vulling van EV bijlage placeholder "Avg-Contactpersoon-naam". Dit veld wordt nu met de correcte waarde gevuld. (ID 2243)

**Bug-fixes / Performance / Tekstueel**:
- Aanpassing van de tekstuele toelichting bij de 3 keuzes bij een Oriëntatieverzoek. (ID 2827)
- Tekstuele wijziging in het proces van het opvoeren van een graafmelding: WION is gewijzigd in WIBON. (ID 2564)
- Log-bestand na uploaden netinformatie m.b.t. aantal foutmeldingen aangepast. (ID 2842)
- Bij actualiseren documenten worden nu documenten correct opgeslagen als er meerdere malen worden verwezen naar hetzelfde bestand. (ID 2889)
- HAS-adressen toegevoegd aan LI.xml. (ID 2436)
- HAS-adressen en DAS-adressen toegevoegd aan GebiedsinformatieAanvraag via BMKL-API. (ID 2516, ID 2755, ID 2696)
- HAS adressen opgenomen in feature GebiedsinformatieAanvraag van GI.xml. (ID 2727)
- Geen foutmelding wanneer een serviceprovider alle BeheerdersinformatieAanvragen opvraagt.  (ID 2737)
- Tekst op scherm Actualiseren netinformatie veranderd van ‘IMKL2015’ naar ‘IMKL’. (ID 3150)
- Diverse performance verbeteringen met betrekking tot uitleveren en actualiseren.

------------------------
### 27 Augustus 2018
Algemeen:
- Performance verbetering voor grote oriëntatieverzoeken.
- Performance verbeterd voor actualiseren netinformatie.
- Minor upgrade van de visualisatie (SLD's) naar de IMKL 1.2.1 versie.

WION Levering:
- In de LI.xml worden nu ook de HAS bijlagen van netbeheerders met BMKL v1.2 genoemd.
- Bugfix: In de LI.xml wordt alleen maar gerefereerd naar beheerdersinformatie die volgens de administratie (ordermanagement) op dat moment is aangeleverd.
- Bugfix: Verwerken van speciale tekens (bv een letter met trema) in de GI.xml verbeterd.
- Bugfix: In GI.xml in feature _ExtraDetailinfo_ is het element <bestandMediaType> voor de centrale netbeheerders toegevoegd.
- Bugfix: Netinformatie buiten gebiedspolygoon wordt in PNG-bestand nu geclipped.

NTD:
- In de NTD is het mogelijk om WIBON-keuzes op te geven (verzoek tot medegebruik / coördinatie).
- In het "klassieke testmelding" scherm, zijn de opties voor WIBON keuzes (verzoek tot medegebruik / coördinatie) gedeactiveerd in geval van graafmeldingen en calamiteitenmeldingen.
- Bij testmelding via NTD wordt de gebiedspolygoon gevalideerd, zodat de gebruiker gelijk weet of de polygoon syntactisch goed is opgegeven.
- Performance verbeterd voor verwerken/valideren netinformatie (voor kleine aanleveringen (configuratie)) op NTD.
- Het maximaal aantal weer te geven fouten bij het aanleveren van netinformatie is verruimd.
- De telling van het aantal fouten in een aanlevering van netinformatie is verbeterd (i.v.m. multi-threading).
- Foutmelding verduidelijkt bij Actualiseren Netinformatie als er EV-documentsjablonen verwijzen naar hetzelfde bestand.
- Bugfix: namen van placeholders die vaker in een EV-sjabloon worden gebruikt, mogen nu ook een suffix hebben.
- Bugfix: Het is nu mogelijk om bij het aanleveren van netinformatie meerdere malen naar dezelfde bijlage te verwijzen.

------------------------
### 16 juli 2018
Algemeen:
- Clippen voor WION objecten is geïmplementeerd
- Onderstaande WION-objecten kunnen nog niet correct worden geclipped (zie https://github.com/Geonovum/imkl2015-review/issues/210)
  * _AanduidingEisVoorzorgsmaatregel_
  * _ExtraGeometrie_
- Multi-geometrieën in WIBON-features toestaan bij actualiseren/decentraal aanleveren (voor zover dit voor het geometrietype is toegestaan).

WION Levering: 
- Achtergrondkaart en selectie kaart ook meeleveren bij het opvragen van de namens de netbeheerder geleverde beheerdersinformatie.
- Gegenereerde bestandsnamen voor uitlevering op GDS worden uniek gemaakt.
- Gebruik default namespace voor leveringsinformatie (in LI.xml).
- Er wordt (ook) voor _ExtraDetailInfo_ een _Utiliteitsnet_ feature aangemaakt in GI.xml.

NTD:
- Aanpassen sortering en typo-correctie bij soort werkzaamheden in NTD "Opvoeren testmelding".
- Bericht in response van de API voor het initiëren van een upload in NTD in JSON formaat door meegeven "Content-Type: application/json".

HAS / DAS:
- Aan- en uitleveren HuisAansluitSchetsen (HAS) geïmplementeerd.
- Validatie dat bij HAS een verplicht adres-element is meegegeven bij aanleveren netinformatie of beheerdersinformatie.
- Aanpassingen bij een B2BAanvraag waarbij gecontroleerd wordt of er geldige adressen als HAS en DAS zijn opgegeven (alleen hoofdadressen).
- `BAGidAdresserbaarObject` wordt nu ook gevalideerd bij een decentrale aanlevering van beheerdersinformatie
- HAS adressen zijn opgenomen in feature _GebiedsinformatieAanvraag_ van GI.xml.

BMKL API v2.0:
- Via de BMKL wordt de interne webdav-locatie niet teruggegeven in de response.
- Ping zonder PKI certificaat mogelijk gemaakt
- BMKL API aangepast zodat adresgegevens correct gevuld worden (HAS/DAS)

Performance:
- Diverse performance verbeteringen t.b.v. uitlevering van vector-informatie.
- PNG's met IMKL-informatie zijn verkleind t.b.v. snelle levering.

Let op:  \
Door de structuurverbetering in de database is de eerder aangeleverde netinformatie in de testomgeving NTD in zijn geheel verwijderd (ook met de status ‘in productie’).  \
Indien er in de NTD de berichtenuitwisseling (BMKL) wordt getest voor de centrale variant (dienst ‘Opvoeren testmelding – BMKL 2.0 centraal): netinformatie dient nogmaals geactualiseerd te worden.

------------------------
### 16 mei 2018
Algemeen:
- Upgrade naar Java 8.
- Structuur verbetering in de database; hierdoor is de (eerder aangeleverde) netinformatie verwijderd.
- Validatie op gebruik standaard (namespace)prefixes in XML berichten.

WION Levering: 
- Complementeren gebiedsinformatielevering (GI.xml).
- Complementeren leveringsinformatie (LI.xml).

EV:
- Controleren op juiste gebruikte placeholders in aangeleverde EV-sjablonen.
- Controleren op netbeheerdernetaanduidingen in de AanduidingEisVoorzorgsmaatregel-features: de netbeheerdernetaanduidingen moeten voorkomen bij de beslissingsregels.

BMKL API v2.0:
- Agentschap Telecom (AT) leestoegang verlenen.
- Gebiedsinformatielevering (GIL.xml) toegevoegd aan de service ‘Opvragen beheerdersinformatie-levering zoals deze voor belanghebbende netbeheerder is uitgeleverd bij de aangegeven beheerdersinformatie-aanvraag.’ 
- Leveringsinformatie (LI.xml) toegevoegd aan de service ‘Opvragen beheerdersinformatie-levering zoals deze voor belanghebbende netbeheerder is uitgeleverd bij de aangegeven beheerdersinformatie-aanvraag.’
- Teksten ontwikkelaarsmelding uniform gemaakt en benaming gelijkgetrokken aan IMKL benaming.
- Indien geen gegevens voor API call dan httpstatus 200 +lege lijst geven i.p.v. httpstatus 404.
- Het is als Service Provider niet meer mogelijk om gebiedsinformatieAanvragen (GIA's) van meerdere netbeheerders tegelijkertijd op te vragen middels BMKL API.
- Update BMKL API's ten aanzien van naamgeving e.d. 

Performance:
- Diverse performance verbeteringen met betrekking tot levering en de gebruikerservaringen van de door netbeheerder geautoriseerde serviceprovider.

Let op:  \
Door de structuurverbetering in de database is de eerder aangeleverde netinformatie in de testomgeving NTD in zijn geheel verwijderd (ook met de status ‘in productie’).  \
Indien er in de NTD de berichtenuitwisseling (BMKL) wordt getest voor de centrale variant (dienst ‘Opvoeren testmelding – BMKL 2.0 centraal): netinformatie dient nogmaals geactualiseerd te worden.

------------------------
### 30 januari 2018
- Nieuwe functionaliteit: Beschikbaarheid van EV module. EV bijlagen met EV vlakken kunnen worden uitgeleverd.
- Nieuwe functionaliteit: Voorzorgsmaatregelen validatie op uniekheid prioritering per Thema en AanvraagSoort.
- Nieuwe functionaliteit: Voorzorgsmaatregelen validatie tegen KlicVoorzorgsmaatregelenBeheer-1.0.xsd.
- Nieuwe functionaliteit: Voorzorgsmaatregelen validatie op EV-sjabloon verwijzingen.
- Nieuwe functionaliteit: Voorzorgsmaatregelen validatie op bronhoudercode in attributen <lokaalID> en <bronhoudercode>.
- Fix: EV bijlagen aanwezig in de uitlevering wanneer er beheerdersinformatie (decentraal) met EV bijlagen wordt aangeleverd. Deze werden in de vorige versie niet uitgeleverd.
- Fix: EV vlak (AanduidingEisVoorzorgsmaatregel) wordt in de liggingskaart gevisualiseerd.
- Nieuwe functionaliteit: Netinformatie validatie op BAG-ID adresseerbaar object.
- Nieuwe functionaliteit: Als Centrale netbeheerder niet mogelijk om beheerdersinformatie (decentraal) aan te leveren op een gebiedsinformatieaanvraag.
- Nieuwe functionaliteit: In NTD wordt de GBKN-kaart en de selectiekaart opgenomen in de beheerdersinformatielevering.
- Verbetering: Tekst "Gereed voor handmatige controle" gewijzigd naar "Gereed voor beoordeling". Deze wordt gegeven bij het actualiseren van netinformatie en documenten.
- Diverse performance verbeteringen met betrekking tot Actualiseren netinformatie

------------------------
### 2 januari 2018
- KLIC is voorbereid om nieuwe orientatieverzoeken in het kader van de WIBON te kunnen afhandelen;
Het betreft \
 a. voorbereiding voor medegebruik fysieke infrastructuur \
 b. voorbereiding voor coordinatie civiele werken
- De functionaliteit wordt geactiveerd, zodra de wetgeving in werking mag worden gesteld.

### 24 november 2017
- OAuth (Open Authorization); een open standaard voor autorisatie bij elke B2B-koppeling (REST API) van de KLIC-WIN systemen
- BMKL API endpoints aanpassingen conform Kadasterbeleid API-management
- Diverse performance verbeteringen met betrekking tot Actualiseren netinformatie
- NTD BMKL klassiek; bug-fix met betrekking tot graafbericht: standaard `aanvangsdatum` en `soort werkzaamheid` weer opgenomen in het verzonden graafbericht naar de netbeheerder

### 16 oktober 2017
- BMKL2.0 in NTD als centrale netbeheerder beschikbaar
- Bugfix (mogelijk om beheerdersinformatie in de NTD conform IMKL v1.2.1 aan te leveren)

### 14 september 2017

#### _IMKL versie 1.2.1 in Kadaster KLIC-WIN systemen_

> ##### Wijzigingen in waardelijsten
>
> 1. http://definities.geostandaarden.nl/imkl2015/id/waardelijst/AnnotatieTypeValue \
> Toegevoegd: http://definities.geostandaarden.nl/imkl2015/id/waarde/AnnotatieTypeValue/annotatiepijlDubbelgericht \
> Toegevoegd: http://definities.geostandaarden.nl/imkl2015/id/waarde/AnnotatieTypeValue/annotatiepijlEnkelgericht
>
>
> 2. http://definities.geostandaarden.nl/imkl2015/id/waardelijst/MaatvoeringsTypeValue \
> Toegevoegd: http://definities.geostandaarden.nl/imkl2015/id/waarde/MaatvoeringsTypeValue/maatvoeringspijl
>
> ##### Wijzigingen in features
>
> 1. Belanghebbende (XSD-wijziging) \
> Element “netinformatie” is hernoemd naar “utiliteitsnet”. \
> Element “geraaktBelangGraafpolygoon” is hernoemd naar “geraaktBelangBijGraafpolygoon”. \
> Element “geraaktBelangInformatiepolygoon” is hernoemd naar “geraaktBelangBijInformatiepolygoon”. \
> Element “geraaktBelangOrientatiepolygoon” is hernoemd naar “geraaktBelangBijOrientatiepolygoon”.
>
> 2. Diepte (XSD-wijziging) \
> Element “inNetwork” kan nu meerdere keren voorkomen (wordt nog niet ondersteund door de software)
>
> 3. ExtraGeometrie (XSD-wijziging) \
> Element “inNetwork” kan nu meerdere keren voorkomen (wordt nog niet ondersteund door de software)
>
> 4. Diepte (XSD-wijziging) \
> Element “inNetwork” kan nu meerdere keren voorkomen (wordt nog niet ondersteund door de software)
>
> 5. Organisatie (XSD-wijziging) \
> “Organisatie” is geen gml-feature meer, maar een element dat binnen andere features kan worden gebruikt
>
>
> ##### Nieuwe controles (naast XSD-controle)
> 1. rotatiehoek is verplicht bij Maatvoering van het type maatvoeringslabel of maatvoeringspijlpunt.
> 2. rotatiehoek is verplicht bij Annotatie van het type annotatielabel of annotatiepijlpunt.
> 3. label is verplicht bij Maatvoering van het type maatvoeringslabel.
> 4. label is verplicht bij Annotatie van het type annotatielabel.
> 5. Binnen “Appurtenance”-features moet element “inNetwork” eenmaal voorkomen.
> 6. Binnen “Elektriciteitskabel”-features moet element “inNetwork” eenmaal voorkomen.
> 7. Binnen “OlieGasChemicalienPijpleiding”-features moet element “inNetwork” eenmaal voorkomen.
> 8. Binnen “Overig”-features moet element “inNetwork” eenmaal voorkomen.
> 9. Binnen “Rioolleiding”-features moet element “inNetwork” eenmaal voorkomen.
> 10. Binnen “Telecommunicatiekabel”-features moet element “inNetwork” eenmaal voorkomen.
> 11. Binnen “ThermischePijpleiding”-features moet element “inNetwork” eenmaal voorkomen.
> 12. Binnen “Waterleiding”-features moet element “inNetwork” eenmaal voorkomen.
> 13. Binnen feature “Overig” mag element “pipeDiameter” geen “nilReason” hebben.


### 1 juni 2017
- Validaties conform IMKL versie 1.2 in Kadaster KLIC-WIN systemen

### 13 april 2017
- BMKL2.0 in NTD beschikbaar

### 31 maart 2017
- Technische aanpassingen t.b.v. livegang BMKL2.0 in NTD
- Bugfixes

### 23 februari 2017
- Bugfix m.b.t. B2B aanleveren netinformatie/documenten

### 3 februari 2017
- Bugfixes (o.a. tabblad ‘Kaart’ weer actief bij NTD Actualiseren netinformatie)

### 17 januari 2017
- B2B aanleveren van netinformatie
- Aanpassing NTD-Portaal
- KLIC API documentatie beschikbaar gesteld in NTD
- Bugfixes
