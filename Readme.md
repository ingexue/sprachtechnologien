# Sprachtechnologien

_Elective for [CS students](https://www.fh-rosenheim.de/technik/informatik-mathematik/) at the [University of Applied Sciences Rosenheim](https://www.fh-rosenheim.de). --- Wahlmodul in den [Bachelorstudiengängen Informatik](https://www.fh-rosenheim.de/technik/informatik-mathematik/) an der [Hochschule Rosenheim](https://www.fh-rosenheim.de)._


## Motivation

Ziel des Moduls ist es den aktuellen Stand von Sprachtechnologien als _user interface (UX)_ kennen und nutzen zu lernen.
Techologien wie Spracherkennung, Sprecherverifikation, Biometrie, Sprachsynthese oder Dialog ermöglichen es Anwendungen zu entwickeln, welche Sprache als Ein- und/oder Ausgabemodalität verwenden, oder aber Sprache in anderer Weise weiterverarbeiten, wie z.B. zur Benutzerauthentifizierung oder der automatischen Auswertung von Telefondialogen in Callcentern.

Die verwendeten Toolkits sind zum Teil quelloffen (open source, i.d.R. Apache2 lizenziert) aber zum Teil auch kostenpflichtige Services welche i.d.R. einen kostenlosen Zugang für die Entwicklung anbieten.


## Vorlesung und Leistungserbringung

**Zeit und Ort:** Donnerstags um 8, B0.09

**Kommunikation** via [Mattermost](https://inf-mattermost.fh-rosenheim.de/st-2018/channels/town-square) ([anmelden](https://inf-mattermost.fh-rosenheim.de/signup_user_complete/?id=dbikwed4jjy3t83icbjctitair)).

**Format:** Die Veranstaltung besteht zu etwa je einem Drittel aus Theorie, Einführungen in aktuelle Toolkits sowie einer (mehrteiligen) Projektarbeit.
Pairprogramming ist wünschenswert, [_BYOD_](https://en.wikipedia.org/wiki/Bring_your_own_device) stark empfohlen!

**Credits:** Semesterbegleitende mehrteilige Projektarbeit, vorzugsweise in Zweierteams.


## Empfohlene Literatur

_Wird noch ergänzt._


## Semesterterminplan

- **15. März: Einführung ([Folien](01-intro/))**
	
	Sprechende Computersysteme -- ewige Science Fiction?

- **22. März: Merkmale**
	
	Wir besprechen Verfahren um Merkmale aus Audiosignalen zu berechnen um das analoge Signal auf eine Folge von reelwertigen Vektoren zu reduzieren.
	Im [Tutorial 1]() verwenden wir [Opensmile](https://audeering.com/technology/opensmile/) um eine Vielzahl solcher Merkmale auf verschiedenen Audiodateien zu berechnen.

- _29. März: entfällt (Ostern)_

- **5. April: Klassifikation, Teil 1: Modellierung**
	
	Die extrahierten Merkmale müssen nun geeiget modelliert werden.
	Wir wiederholen Normal- und Mischverteilungen, wie man diese schätzt ("lernt") und besprechen den optimalen Klassifikator.
	Im [Tutorial 2]() verwenden wir das [Java Speech Toolkit](https://github.com/sikoried/jstk) um erste Erfahrungen mit statistischer Modellierung zu sammeln.

- **12. April: Klassifikation, Teil 2: Klassifikatoren**

	Wir kombinieren Merkmalextraktion und Modellierung um Dauerinvariante Mermkale für ganze Audiodateien zu berechnen.
	Im [Tutorial 3]() verwenden wir neben dem JSTK auch [WEKA](https://www.cs.waikato.ac.nz/~ml/weka/) um diese Merkmale zu klassifizieren.

- **19. April: Biometrie**
	
	Wir begeben uns auf eine Rundreise durch die Biometrie der Stimme (und Sprache) und schließen mit einer Einführung in [Teilaufgabe 1](teilaufgabe1/).

- **26. April: Tutorium für [Teilaufgabe 1](teilaufgabe1/)**

	Eine REST API für Sprecherverifikation und Altersbestimmung.
	**Abgabe bis 2.5. 23:59 Uhr!**

- **3. Mai: Klassifikation, Teil 3: Sequenzen**
	
	Bisher haben wir Audiodateien nur im ganzen klassifiziert.
	Wir wiederholen nun die Grundlagen von hidden Markov models (HMM) und wie diese zur Sequenzklassifikation verwendet werden.
	Im [Tutorium 4]() verwenden wir das JSTK um einzelne Wörter sowie DTMF Sequenzen zu klassifizieren.

- _10. Mai: entfällt (Christi Himmelfahrt)_

- **17. Mai: HMM Modellierung; Sprachsynthese**

	Ein HMM allein reicht nicht um komplexere Sequenzen zu modellieren.
	Die Modellierung von Untereinheiten erlaubt es sehr ausdrucksstarke Modelle zu genieren und gleichzeitig die Effizienz und Robustheit des Trainings zu bewahren.

	Von HMMs schlagen wir die Brücke zur Sprachsynthese, wo wir regelbasierte, konkatenative und modellgetriebene Synthese unterscheiden.

	Wir schließen mit einer Einführung in [Teilaufgabe 2](teilaufgabe2/).

- **24. Mai: Tutorium für [Teilaufgabe 2](teilaufgabe2/)**

	Sprachein- und -ausgabe im Browser.
	**Abgabe bis 30.5. 23:59 Uhr!**

- _31. Mai: entfällt (Fronleichnam)_

- **7. Juni: Texmining**
	
	Wir verlassen die Welt der _gesprochenen_ Sprache (_speech_) und wenden unseren Blick auf die _geschriebene_ Sprache (_language_):
	Charakteristika, Merkmale, Anwendungen.
	Im [Tutorial 5]() berechnen wir einfache Statistiken wie Term- und Dokumentenfrequenz, und wenden das Vektorraummodell an um Dokumente zu Klassifizieren.

- **14. Juni: Tutorium für [Teilaufgabe 3](teilaufgabe3/)**

	Autovervollständigung mit [SRILM](http://www.speech.sri.com/projects/srilm/); Schlüssenphrasen mit [NLTK](https://www.nltk.org/).
	**Abgabe bis 20.6. 23:59 Uhr!**
	

- **21. Juni: Machine Translation; Dialogsysteme**

	Machine Translation ist die automatische Übersetzung von einer Quell- in eine Zielsprache.
	Deep Learning (genauer: Encoder/Decoder Netze) haben hier kürzlich entscheidende Fortschritte gebracht.

	Obwohl es auch Deep Learning Ansätze für Dialogsysteme gibt, sind tranditionelle "Slotfiller" immer noch das Arbeitstier im Produktivbetrieb.

	Wir schließen mit einer Einführung in die [Teilaufgabe 4](teilaufgabe4/).

- **28. Juni: Tutorium für [Teilaufgabe 5](teilaufgabe4/)**

	Dialoganwendung (Skill) für [Alexa](https://developer.amazon.com/alexa), [Cortana](https://docs.microsoft.com/en-us/cortana/skills/get-started) oder [Home](https://dialogflow.com/) mit Anbindung von mind. einer externen API.
	**Abgabe bis 4.7. 23:59 Uhr!**

- **5. Juli: Wiederholung**
	
	Wir fassen nochmal die wichtigsten Methoden und Anwendungen zusammen und ziehen eine Bilanz im Hinblick auf die verfügbaren Toolkits und Services.


_Subscribe to [https://github.com/sikoried/sprachtechnologien/](https://github.com/sikoried/sprachtechnologien/) repository to follow updates._
