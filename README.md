# Atelier-python
#!/usr/bin/python3
# --*-- coding: UTF-8 --*--

from ftplib import FTP
import os

#authentifcation
host=input('votre host')
user=input('votre identifiant')
password=input('votre mot de passe')
ftp=FTP(host)
ftp.login(user, password)
# Connexion

etat = ftp.getwelcome()
print ("Etat : ",etat)
#Changer le repertoir

chem=input('introduire le chemin de votre repertoire')
ftp.cwd(chem)

#action à faire

action=input('que souhaitez faire(choisir 1 a 7):\n 1: creation dossier \n 2: s$
 if action == 1:
        new_name=input('nom du nouveau dossier')
        ftp.mkd(new_name)
elif action == 2:
        name=input('nom du dossier a supprimer')
        ftp.rmd(name)
elif action==3
        name1=input('introduire dossier a renommer')
        name2=input('choisir le nouveau nom')
        ftp.rename(name1,name2)
elif action==4
        name1=input('introduire nom du fichier a renommer')
        name2=input('choisir le nouveau nom')
        ftp.rename(name1,name2)
elif action==5
        name=input('introduire nom du fichier a supprimer')
        ftp.delete(name)
elif action==6
        ftp.retlines('LIST', callback=None)
elif action==7
        name= input('nom du ficheir à envoyer')
        ftp.storbinary('STOR', name, blocksize=8192, callback=None, rest=None)
elif
        ftp.quit
