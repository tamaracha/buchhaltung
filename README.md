# Buchhaltung

Dies ist meine Projektvorlage für freiberufliche Buchhaltung.

## Motivation

Viele Softwarelösungen für Buchhaltung werben zwar mit bequemen Workflows (natürlich mit Cloud und Webapp)
und gelegentlich auch hohen Standards beim Datenschutz,
nicht aber mit Nachhaltigkeit bei der Datenhaltung.

- Ich befürworte offene Standards und möchte die Daten möglichst auch mit offenen Technologien wieder lesen können.
- Ich möchte mir selbst aussuchen, wo ich diese Daten hoste.
- Ich kenne mich mit Programmiersprachen aus der Datenanalyse aus und möchte mir selbst Automatisierungen entwickeln.

## Spezifikation

So ist die Vorlage aufgebaut:

### Historie mit Git

Git ist ein Versionierungstool, das eine Änderungshistorie für einen Ordner mit seinen Dateien und Unterordnern bietet.
Die Änderungen kann man selbst in Schritte zusammenfassen, so dass eine inhaltlich nachvollziehbare Historie entsteht.

### Verschlüsselung mit Cryptomator (optional)

Git wurde für offenen Quellcode entwickelt und beherrscht für sich genommen keine Verschlüsselung.
[Cryptomator] verschlüsselt Ordner und Dateien als Container, die man in die Cloud laden und synchronisieren kann.
Man kann sich frei einen Cloud-Dienst aussuchen und die Anbieter können die Inhalte nicht einsehen.
Ein mit Git versionierter Ordner kann in einem Cryptomator-Container verschlüsselt werden.
Ein Container muss aber vor dem Bearbeiten entriegelt werden, dass macht es ein wenig umständlicher.

[cryptomator]: https://cryptomator.org

### Ordnerstruktur

Der Ordner enthält die folgenden Unterordner:

- data: die eigentlichen Inhalte
  - Debitoren: Umsatzgenerierende Vorgänge, Kundenvorgänge, etc.
  - Kreditoren: Vorgänge zu Betriebsaufwändungen etc.
  - Banken: Zahlungsbelege über Geschäftsvorgänge
- tasks: Materialien, Vorlagen, Scripts etc. zur Unterstützung von workflows

### Dateiformate

Besonders für Datendateien sollten textbasierte Formate wie CSV bevorzugt eingesetzt werden.
Die Standards von [frictionless] können dabei helfen, das Format zu dokumentieren.

- Sie sind nicht auf eine bestimmte Software festgelegt und können leicht wieder geöffnet und editiert werden.
- Git kommt damit besser zurecht und kann Unterschiede zwischen zwei Änderungsschritten anzeigen.
- Automatisierung kann flexibel nachgerüstet werden.
- Excel verleitet dazu, Daten, Metadaten und Code zu vermischen, was die Automatisierung und Auswertung langfristig erschwert.

Für Dokumente, die einmal erstellt, verschickt und archiviert werden, sind Formate wie PDF gut geeignet.

- PDF kann jeder sofort anzeigen.
- Die Datei wird einmal erzeugt (gedruckt) und nicht im Nachhinein verändert.
- Denkbar wäre auch der Einsatz von Publishing-Lösungen wie [Quarto] zur datengetriebenen auf Templates basierenden Dokumentenerstellung.

[frictionless]: https://frictionlessdata.io/
[quarto]: https://quarto.org/

### Automatisierung

Um angepasste Workflows zu implementieren, können hier Programmiersprachen aus dem Umfeld der Datenanalyse zum Einsatz kommen.
Dieser Abschnitt wird ausgebaut.

## Lizenz

Diese Projektvorlage ist unter der [MIT](license.md) lizensiert.
Nutzern der Vorlage ist es jedoch gestattet, diese Lizenz sowie die Vorlage betreffende Dokumentation aus ihren Projekten zu entfernen.
