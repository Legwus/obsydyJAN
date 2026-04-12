
**Phase 1:**
Entitätkandidaten:
- Bus
- Fahrer
- Haltestelle
- Linie
- Einsatz

Kandidaten für Beziehungen:
- Linie hat start und Endhaltestelle
- Linie hält and Haltestellen
- Fahrer hat Training für Bus
- Fahrer fährt bus auf linie an Tag

Entitäten:
- Bus: 
	- Attribute: Typ, <u>Seriennummer</u>, Sitzplätze, Stehplätze, Antriebsart,
		- **Beispiel:** 
		- Typ: MAN Lion's City 18 E
		- Antriebsart: Elektroantrieb
		- Stehplätze: 60
		- Sitzplätze: 25
		- Seriennummer: 123
- Fahrer:
	- <u>Name</u>, <u>Geburtsdatum</u>, Mobilfunknummer
		- Name: Bob Meier
		- Geburtsdatum: 3.10.2002
		- Mobilfunknummer: +49172123456
- Haltestelle:
	- Name, <u>GPS Koordinaten</u>
		- Name: Technische hochschule Ingolstadt
		- Koordinaten: 48.766752, 11.431659
- Linie:
	- <u>Liniennummer</u>, Starthaltestelle, <u>Endhaltestelle</u>, uhrzeitErsterFahrt, Umlaufdauer
		- Liniennummer: 22
		- Starthaltestelle: Isaak-Newton-Strasse
		- Endhaltestelle: Weiherfeld
		- Umlaufdauer: 35 minuten
		- uhrzeitErsterFahrt: 7:13 Uhr
- Einsatz: 
	- Fahrer Primärschlüssel, Bus.Seriennummer, Linie.Liniennummer, Datum, Schicht, <u>Einsatz_ID</u>, minutenNachEinsatzErstenBusses
		- Fahrer PS: Bob Meier 3.10.2002
		- Bus.Seriennummer: 42
		- Linie.Liniennummer: 22
		- Datum: 26.3.2023
		- Schicht: früh
		- Einsatz_ID: 12345
		- minutenNachEinsatzErstenBusses: 0

Beziehungen:
	Fahrer trainiert für Bus (0,n),(0,n)
	An welchen Haltestellen hält die Linie (1,n),(0,n) + nach wie vielen minuten
	