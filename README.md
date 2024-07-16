# Schulung Quarto, Git und MVSC

## Git

Git ist eine Versionsverwaltung für digitale Artefakte. Es wird überlicherweise von Softwareentwickler*innen verwendet, um gemeinsam an Dateien zu arbeiten und Änderungen verfolgen zu können.

Hier mal der Link zu Git: [](https://git-scm.com)

Nach der Installation auf einem PC, kann mit Hilfe von Git-Befehlen eine Versionskontrolle lokaler Dateien erfolgen. Es gibt sehr viele mögliche Befehle. Hier mal die wichtigsten Befehle auf einen Blick: [](https://training.github.com/downloads/de/github-git-cheat-sheet)

Einen guten und leicht verständlichen Einblick bietet auch diese Seite: [](https://rogerdudler.github.io/git-guide/index.de.html)

### Was ist Git-Hub?

Git-Hub ist eine Plattform, die Git zur Versionsverwaltung nutzt und zusätzliche Funktionen bietet, wie bspw. Cloud-Speicher, Dokumentation, Werkzeuge zum kollaborativen Arbeiten und vieles, vieles mehr. Als Gegenstück zu Git-Hub sei an dieser Stelle mal Git-Lab genannt.

In Git-Hub kann man nach Anmeldung ein Repository erzeugen. Dieses Repo enthält dann alle Dateien, die einer Versionskontrolle unterliegen sollen. Das Repo kann lokal auf einen PC gespiegelt werden (clonen). Änderungen können dann lokal erfolgen und auf Wunsch wieder in das Repo hochgeladen werden. Hierfür werden die Git-Befehle genutzt. Auf diese Weise können mehrere Personen Änderungen an den Dateien eines Repos erzeugen und somit gemeinsam die Code-Entwicklung vorantreiben.

Git-Hub bietet auch die Funktion eine Webseite zu hosten. Das wird später im Zusammenhang mit Quarto noch wichtig.

## Microsoft Visual Studio Code (MVSC)

MVSC ist eine kostenfreie Entwicklungsumgebung (IDE) für die Entwicklung von Software. MVSC stellt hierfür eine Reihe von Programmierwerkzeugen zur Verfügung und unterstützt alle gängigen Programmiersprachen und die Versionsverwaltung mittels Git. MVSC kann um viele weitere Funktionen erweitert werden. Hier mal der Link zu MVSC: [](https://code.visualstudio.com)
Es gibt viele weitere IDE's, diese Schulung bezieht sich allerdings auf MVSC.

Quarto
Quarto ist ein umfangreiches Werkzeug für die Erstellung wissenschaftlicher Dokumentationen. Auf Grundlage von speziellen Quarto-Dateien (.qmd) und Konfigurationsdateien (.yml, .json etc.) können kompakte Webseiten, PDF- oder Word-Dateien erzeugt werden (rendern). 

Hier der Link zur Quarto Dokumentation: https://quarto.org/docs/guide/
Wie nutzen wir Quarto für die TBA-Doku?
Quarto erzeugt in unserem Fall eine Website, also Html-Dateien. Diese Webseite hosten wir auf Git-Hub mit Hilfe der kostenfreien Funktion: Git-Hub Pages. Alle Dateien von Quarto, die zur Erzeugung der Webseite benötigt werden, befinden sich in dem folgenden Git-Hub Repository: https://github.com/iqb-berlin/tba-info

Die daraus erzeugte Webseite ist hier zu sehen: https://iqb-berlin.github.io/tba-info/
Wie werden Quarto Inhalte bearbeitet?
Das oben genannte Repo wird mit Hilfe des Befehls: git clone https://github.com/iqb-berlin/tba-info.git auf den lokalen PC kopiert, mit MVSC geöffnet und bearbeitet. Jede Änderung wird in MVSC mit Hilfe der integrierten Git-Funktion angezeigt und kann bei Bedarf mit den Git-Befehlen in das Remote-Repo geladen werden. Die gleichzeitige Bearbeitung einer Datei von mehreren Personen kann zu Konflikten führen, die dann mühselig behoben werden müssen. Daher sollten im Vorfeld Absprachen getroffen werden, wer an welcher Datei arbeitet. Ist eine gemeinsame Bearbeitung einer Datei gewünscht, sollte folgendes beachtet werden:

Nach dem Öffnen des lokalen Repos sollte zuerst der Befehl: git pull abgesetzt werden. Das stellt sicher, dass alle lokalen Dateien auf dem aktuellen Stand sind.
Es sollte in der Git-Konfiguration die Möglichkeit eines Rebases festgelegt werden. Dies geschieht mit dem Befehl: git config pull.rebase true. Wird beim Laden lokaler Änderungen in das Remote-Repo ein Konflikt angezeigt, wird nun zur Konfliklösung gleich ein Merge-Editor in MVSC angeboten. Anschließend kann die Änderung mit git commit -m "commit message" in das Remote Repo geladen werden.








