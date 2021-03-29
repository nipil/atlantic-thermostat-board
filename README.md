# A propos

Suite à la panne d'un radiateur électrique Atlantic, j'ai dû réparer la carte thermostat. Même s'il ne s'agissait que d'un condensateur électrolytique 470uF 25v à remplacer, j'ai décidé de comprendre comment la carte fonctionne.

Le présent projet a pour but de consolider tout ce que j'ai analysé et compris au sujet de cette carte (j'ai 12 radiateurs de ce type dans la maison, tous de la même époque, je pense que ça vaut le temps investi !)

*Je partage ce travail ici uniquement pour que ça puisse servir à d'autres que moi-même, cependant je n'assurerai aucun support technique, ni ne répondrait aux questions concernant les éventuels problèmes de radiateur que vous pourriez rencontrer, que ça soit avec ce type de carte thermostat, une autre carte, ou autre.*

# La carte thermostat

Voici un aperçu de la carte thermostat :

![vue frontale](https://github.com/nipil/atlantic-thermostat-board/raw/master/Photo-pistes-composants/Apercu/overview-board-front-thumb.jpg)

![vue arrière](https://github.com/nipil/atlantic-thermostat-board/raw/master/Photo-pistes-composants/Apercu/overview-board-back-thumb.jpg)

# Analyse

Le fichier "[Photo-pistes-composants/atlantic-termostat-traces.xcf](https://github.com/nipil/atlantic-thermostat-board/raw/master/Photo-pistes-composants/atlantic-termostat-traces.xcf)" est une image faite avec [le logiciel gratuit GIMP](https://www.gimp.org/).

Cette image contient des calques, qui reprennent chacun soit une piste soit un ensemble de composant, l'ensemble me permettant d'identifier les différents circuits de la carte pour comprendre son fonctionnement.

Voici un aperçu du résultat (regardez le fichier GIMP pour naviguer dans les calques) :

![analyse des traces](https://github.com/nipil/atlantic-thermostat-board/raw/master/Photo-pistes-composants/atlantic-termostat-traces-thumb.png)

# Liste des composants

Shunts:

- L1 (!)
- ST1
- ST2
- ST3
- ST7

Résistances :

- R1: 13k 1%
- R2: 4.87k 1%
- R3: 6.49k 1%
- R4: 10k 1%
- R5: 475k 1%
- R6: 0.182k 1%
- R7: 1k (?) 1%
- R8: 1k (?) 1%
- R9: 100k 1%
- R10: 4.87k 1%
- R11: 1k (?) 1%
- R12: 100k 1%
- R13: 475k 1%
- R14: 100k 1%
- R15: 475k 1%
- R16: 30K 1%
- R17: 475k 1%
- R18: 5X-6-182LF 18k réseau de résistance **en serie entre les pin** !!
- R19: 5.11k 1%
- R20: 20k 5%
- R21: 20k 5% 
- R22: 20k 5%
- R23: non populé
- RP1: 18k 5%
- POT1: règlage "mode éco" 0-2.5k 2K65272
- POT2: règlage "mode confort" 0-2.5k 2K65212

Consensateur:

- C1: 470uF 25v électrolytique polarisé
- C2: 0.47uF 10% 100v
- C3: 4.7nF 10%
- C4: 100nF 10%
- C5: 4.7nF 10%
- C6: 4.7nF 10%
- C7: 4.7nF 10%
- C8: 4.7nF 10%
- C9: non populé
- C10: 4.7nF 10%
- C11: 4.7nF 10%
- C14: 4.7nF 10%

Inductances:

- L2: 100uH 10%
- L3: 100uH 10%

Diodes:

- DZ1: BZX 5V6 diode zener Vz=5.6v Vf=1v
- D1: 1N4007 (?) Vf=0.7v
- D2: 1N4007 (?) Vf=0.7v
- D3: 1N4007 (?) Vf=0.7v
- D4: 1N4007 (?) Vf=0.7v
- LD1: Vf=1.7v@10mA (3mm?) pour le mode éco
- LD2: Vf=1.7v@10mA (3mm?) pour le mode confort
- LD3: Vf=1.7v@10mA (3mm?) pour la chauffe

Puissance:

- TR1: BTB16-600SWRG

Contrôle:

- CCT1: OTTER H11 W#475 coupe-circuit de sécurité thermique à réponse rapide et réarmement automatique
- UC1: 60-MEC0 ou 60-MECO, 18 pin DIP package
- X1: résonateur céramique Murata CSTLS_G 4Mhz (?)
- COM1: commutateur (1 position off séparée + 4 positions hors-gel/prog/eco/confort à base commune)
