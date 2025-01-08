# MeinProjekt

**Dokumentation der durchgeführten Schritte**

### Einrichtung des GitHub-Repositorys "MeinProjekt"

1. Ich habe mich auf der GitHub-Website (www.github.com) mit meinem Benutzerkonto angemeldet. Da ich noch kein Repository hatte, habe ich ein neues Repository mit dem Namen "MeinProjekt" erstellt.
2. Nach dem Erstellen des Repositories habe ich die URL des Repositories notiert, da ich diese für den weiteren Workflow benötigte.



### Erstellen eines SSH-Schlüssels

1. Zunächst habe ich in meinem Terminal überprüft, ob ich bereits einen SSH-Schlüssel hatte, indem ich den folgenden Befehl ausgeführt habe:
   ls ~/.ssh/

2. Da keine Dateien wie `id_rsa` oder `id_rsa.pub` angezeigt wurden, habe ich einen neuen SSH-Schlüssel erstellt:
   ssh-keygen -t rsa -b 4096 -C "o.schulczynski@gmail.com"

3. Ich habe den Standard-Speicherort für den SSH-Schlüssel akzeptiert und optional ein Passwort gesetzt.


### Lokales Klonen des Repositorys, Konfiguration von Git und Erstellen der initialen Commits

1. Im Terminal habe ich in das Verzeichnis navigiert, in dem ich mein lokales Git-Repository erstellen möchte.

2. Anschließend habe ich das GitHub-Repository "MeinProjekt" mit dem folgenden Befehl geklont:
   git clone git@github.com:aTTiCuZ-CodingPage/MeinProjekt.git

3. Nach dem Klonen bin ich in das geklonte Verzeichnis gewechselt:
   cd MeinProjekt

4. Ich habe Git mit meinem Namen und meiner E-Mail-Adresse konfiguriert:
   git config user.name "aTTiCuZ-CodingPage"
   git config user.email "o.schulczynski@gmail.com"

5. Um eine erste Datei hinzuzufügen, habe ich die Datei `main.py` erstellt und die Änderungen wie folgt committed:
   git add main.py
   git commit -m "Initialer Commit"


### Erstellen des "feature"-Branches, Hinzufügen neuer Dateien und Committen der Änderungen

1. Ich habe einen neuen Branch mit dem Namen "feature" erstellt und bin zu diesem gewechselt:
   git checkout -b feature

2. Danach habe ich eine neue Datei `utils/database.py` hinzugefügt und die Änderungen committed:
   git add utils/database.py
   git commit -m "Neue Funktion hinzugefügt"

3. Ich habe die Datei `main.py` bearbeitet und erneut die Änderungen committed:
   git add main.py
   git commit -m "Hauptdatei aktualisiert"


### Mergen des "feature"-Branches in den "master"-Branch und Beheben eines Merge-Konflikts

1. Ich bin zurück zum "master"-Branch gewechselt:
   git checkout master

2. Danach habe ich die Datei `main.py` im "master"-Branch bearbeitet und die Änderungen committed:
   git add main.py
   git commit -m "Hauptdatei aktualisiert"

3. Anschließend habe ich versucht, den "feature"-Branch in den "master"-Branch zu mergen:
   git merge feature

4. Da ein Merge-Konflikt auftrat, habe ich die betroffenen Dateien überprüft und den Konflikt manuell in Visual Studio Code gelöst. Ich habe anschließen einen "Commit" ebenfalls in VSC getätigt.

5. Anschließend habe ich Mein Projekt ins Remote Repository hochgeladen:
   git push origin main 




### Fazit

Durch die oben genannten Schritte habe ich erfolgreich ein GitHub-Repository eingerichtet, lokale Änderungen verwaltet und Branches genutzt, um parallele Entwicklungsarbeiten durchzuführen.
