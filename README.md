# TFDocker

## Anleitung zur Bearbeitung mit Docker CE auf Ubuntu:

Das verwendete Image herunterladen
```bash
sudo docker pull tensorflow/tensorflow:latest-devel-py3
```
Den Container starten (ohne --rm falls er nach dem Beenden weiter existieren soll) 
```bash
sudo docker run -it -p 8888:8888 --rm --name myWorkstation1 tensorflow/tensorflow:latest-devel-py3 jupyter notebook --allow-root
```
>Den Link der erstellt wurde kopieren und im Browser aufrufen  

>Eine neue Konsole öffnen  

Dieses Repository herunterladen  
```bash
sudo docker exec -it myWorkstation1 bash
git clone https://github.com/gAIt-Project/gAIt.git
cd gait/
git config --global user.email "<you@example.com>"
git config --global user.name "<Your Name>"
```
Falls nach dem clone Änderungen eintreten und der aktuellste Zustand heruntergeladen werden muss  
```bash
git pull
```
>Projekt bearbeiten  

Lokalen Zustand auf Github laden  
```bash
git add .
git commit -m “<Commit Beschreibung>”
git push
```  
#### Nützliche Befehle:
Informationen über den Zustend des Lokalen Repositories  
```bash
git status
```
Alle Container auflisten  
```bash
sudo docker ps -a 
```
Alle Images auflisten  
```bash
sudo docker images
```
