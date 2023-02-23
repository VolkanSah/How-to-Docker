# How to Docker

Dieses Repository enthält eine Sammlung von Anleitungen und Beispielen für die Verwendung von Docker. Sie können Docker verwenden, um Anwendungen schnell und einfach in Containern zu erstellen, auszuführen und zu verwalten. Die Anleitungen und Beispiele in diesem Repository sind darauf ausgelegt, Ihnen den Einstieg in die Verwendung von Docker zu erleichtern.

Folgen Sie den Anweisungen unten, um zu beginnen.

## Systemanforderungen

Bevor Sie Docker installieren, sollten Sie sicherstellen, dass Ihr System die folgenden Anforderungen erfüllt:

- Ein 64-Bit-Betriebssystem
- Mindestens 4 GB RAM
- Mindestens 5 GB freier Festplattenspeicher
- Eine CPU, die Virtualisierung unterstützt

Es ist wichtig, dass diese Anforderungen erfüllt sind, da Docker intensive Ressourcen nutzt und eine Virtualisierungsumgebung benötigt, um Container zu erstellen und auszuführen. Wenn Sie nicht über ausreichend Ressourcen verfügen, kann dies zu Problemen bei der Nutzung von Docker führen.

## Installation von Docker

Um Docker auf verschiedenen Betriebssystemen zu installieren, müssen Sie verschiedene Schritte ausführen. Im Folgenden finden Sie Anleitungen für Ubuntu und Debian.

### Ubuntu

1. Aktualisiere die Liste der verfügbaren Pakete:
`bash sudo apt update `

2. Installiere die benötigten Pakete, um das Docker-Repository hinzuzufügen:
sudo apt install apt-transport-https ca-certificates curl software-properties-common

3. Füge das Docker-Repository hinzu:
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable"

4. Aktualisiere die Liste der verfügbaren Pakete erneut:
sudo apt update

5. Installiere Docker:
sudo apt install docker-ce

6. Starte den Docker-Dienst:
sudo systemctl start docker

7. Verifiziere, dass Docker ordnungsgemäß installiert wurde, indem du den folgenden Befehl ausführst, der eine Begrüßungsnachricht von Docker anzeigen sollte:
sudo docker run hello-world

### Debian

1. Aktualisiere die Liste der verfügbaren Pakete:
sudo apt update

2. Installiere die benötigten Pakete, um das Docker-Repository hinzuzufügen:
sudo apt-get install apt-transport-https ca-certificates curl gnupg2 software-properties-common

3. Füge das Docker-Repository hinzu:
curl -fsSL https://download.docker.com/linux/debian/gpg | sudo apt-key add -
sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/debian $(lsb_release -cs) stable"

4. Aktualisiere die Liste der verfügbaren Pakete erneut:
sudo apt update

5. Installiere Docker:
sudo apt install docker-ce

6. Starte den Docker-Dienst:
sudo systemctl start docker

7. Verifiziere, dass Docker ordnungsgemäß installiert wurde, indem du den folgenden Befehl ausführst, der eine Begrüßungsnachricht von Docker anzeigen sollte:
sudo docker run hello-world

### Arch-Linux

1. Aktualisieren Sie die Liste der verfügbaren Pakete:
sudo pacman -Syu

2. Installieren Sie Docker:
sudo pacman -S docker

3. Starten Sie den Docker-Dienst:
sudo systemctl start docker

4. Aktivieren Sie den Docker-Dienst, damit Docker bei jedem Systemstart automatisch gestartet wird:
sudo systemctl enable docker

5. Verifizieren Sie, dass Docker ordnungsgemäß installiert wurde, indem Sie den folgenden Befehl ausführen, der eine Begrüßungsnachricht von Docker anzeigen sollte:
sudo docker run hello-world

### FreeBSD

1. Installieren Sie die notwendigen Pakete:
sudo pkg install docker

2. Starten Sie den Docker-Dienst:
sudo service docker start

3. Aktivieren Sie den Docker-Dienst, damit Docker bei jedem Systemstart automatisch gestartet wird:
sudo sysrc docker_enable=YES

4. Fügen Sie Ihren Benutzer zur Docker-Gruppe hinzu:
sudo pw groupmod docker -m <Benutzername>

5. Verifizieren Sie, dass Docker ordnungsgemäß installiert wurde, indem Sie den folgenden Befehl ausführen, der eine Begrüßungsnachricht von Docker anzeigen sollte:
sudo docker run hello-world

Bitte beachten Sie, dass es auch von der genauen BSD-Variante abhängt, welche Schritte zur Installation von Docker notwendig sind. Die obige Anleitung gilt speziell für FreeBSD, andere BSD-Varianten erfordern möglicherweise unterschiedliche Schritte oder Paketnamen.

  ### Windows
  
  Für die Installation von Docker auf Windows gibt es verschiedene Schritte, die je nach verwendetem Betriebssystem und Version unterschiedlich sein können. Hier sind jedoch einige allgemeine Schritte, die für die Installation von Docker auf Windows erforderlich sind:

Überprüfen Sie, ob Ihr Windows-System die Systemanforderungen von Docker erfüllt. Docker Desktop for Windows erfordert mindestens Windows 10 64-Bit: Pro, Enterprise oder Education Edition (Version 16299 oder höher) mit mindestens 4 GB RAM.

Laden Sie Docker Desktop for Windows herunter und installieren Sie es. Sie können es von der offiziellen Docker-Website herunterladen: https://www.docker.com/products/docker-desktop

Stellen Sie sicher, dass die virtuelle Maschine (VM) in Docker Desktop for Windows aktiviert ist. Docker Desktop for Windows verwendet Hyper-V, um eine VM bereitzustellen, die die Docker-Container ausführt. Gehen Sie wie folgt vor, um sicherzustellen, dass Hyper-V auf Ihrem System aktiviert ist:

Drücken Sie die Windows-Taste, um das Startmenü zu öffnen.
Geben Sie "Windows-Features" ein und wählen Sie "Windows-Features aktivieren oder deaktivieren".
Suchen Sie nach der Option "Hyper-V" und aktivieren Sie sie.
Starten Sie Docker Desktop for Windows und warten Sie, bis die VM gestartet wurde. Sie sollten dann das Docker-Symbol im Benachrichtigungsbereich des Taskleistes sehen.

Verifizieren Sie, dass Docker ordnungsgemäß installiert wurde, indem Sie den folgenden Befehl in einer Eingabeaufforderung oder PowerShell-Shell ausführen:

docker run hello-world
  
Das Beispiel zeigt einen allgemeinen Überblick darüber, wie Sie Docker auf Windows installieren können. Bitte beachten Sie, dass je nach Ihrer spezifischen Konfiguration möglicherweise weitere Schritte erforderlich sind oder andere Anweisungen gelten können. Bitte lesen Sie die offizielle Docker-Dokumentation und stellen Sie sicher, dass Sie die neueste Version von Docker verwenden.

## Vorteile von Container Systemen

Plattformunabhängigkeit: Mit Docker können Anwendungen in Containern ausgeführt werden, die auf verschiedenen Betriebssystemen und Hardware-Plattformen funktionieren, was eine höhere Portabilität und Interoperabilität ermöglicht.

Leichtgewichtig und skalierbar: Docker-Container sind leichtgewichtig und starten sehr schnell, wodurch sie eine skalierbare Lösung für die Bereitstellung von Anwendungen bieten.

Isolierung und Sicherheit: Durch die Isolierung von Containern voneinander und vom Hostsystem ermöglicht Docker eine höhere Sicherheit und verhindert, dass Anwendungen sich gegenseitig beeinflussen oder das Hostsystem gefährden können.

Einfache Verwaltung und Automatisierung: Docker bietet eine einfache Möglichkeit, Anwendungen in Containern zu verwalten und zu automatisieren, was die Bereitstellung von Anwendungen erleichtert und beschleunigt.

Ökosystem und Community: Docker hat ein großes Ökosystem von Werkzeugen und Services, die auf Docker aufbauen, sowie eine aktive Community, die sich engagiert und Probleme löst.

## Nachteile von Container Systemen

Komplexität: Docker kann aufgrund seiner Komplexität und der vielen verfügbaren Funktionen schwierig zu erlernen und zu verwenden sein. Es kann eine gewisse Einarbeitungszeit erfordern, um Docker effektiv nutzen zu können.

Größe von Containern: Docker-Container können aufgrund der benötigten Abhängigkeiten und Bibliotheken relativ groß werden, was zu längeren Startzeiten und höherem Speicherbedarf führen kann.

Keine nativen GUIs: Docker verfügt nicht über nativen Support für grafische Benutzeroberflächen (GUIs). Entwickler müssen daher spezielle Tools verwenden, um Docker-Container zu verwalten und zu überwachen.

Sicherheitsrisiken: Obwohl Docker Sicherheitsfunktionen wie Container-Isolierung und -Begrenzung bietet, kann es immer noch zu Sicherheitslücken und Angriffen kommen, insbesondere wenn Container unsachgemäß konfiguriert oder verwaltet werden.

Eingeschränkte Unterstützung von Windows: Docker unterstützt Windows-Container nur auf bestimmten Windows-Versionen (Windows 10 Pro oder Enterprise 64-Bit) und erfordert die Verwendung von Hyper-V, was zu zusätzlicher Komplexität und höheren Anforderungen an die Hardware führen kann.

Es ist wichtig zu beachten, dass diese Vor- & Nachteile je nach spezifischem Anwendungsfall unterschiedlich schwerwiegend sein können. Es ist daher ratsam, die Vor- und Nachteile von Docker sorgfältig abzuwägen und zu entscheiden, ob Docker die richtige Lösung für Ihre spezifischen Anforderungen ist.

















