#on definit les thermes principaux
import random
choix = ["ordinateur","vollant","telephone","souris","tableau","accident","incendie","parapluie","feuille","soleil","musique","stylo","chanteur","batiment","fenetre","lumiere","homeomorphisme","marshmallow","marcher","bonhomme","osteopathe","heure","cachalot","application","animation","qualiter","source","pessimiste","usage","carot","couverture","nounours","vegetarienne","canape","cabane","recompense"]
solution = random.choice(choix)
tentatives = 7
affichage = ""
lettres_trouvees = ""
#on affiche la premiere page 
for l in solution:
  affichage = affichage + "_ "

print(">> Let's go!!!! <<")

while tentatives > 0:
  print("Mot à deviner : ", affichage)
  proposition = input("proposez une lettre : ")
#ce qui se passe si une lettre est trouvé ou non
  if proposition in solution:
      lettres_trouvees = lettres_trouvees + proposition
      print("-> Moins une")
  else:
    tentatives = tentatives - 1
    print("-> Rater hahahaha\n")
    if tentatives==0:
        print(" ==========Y= ")
    if tentatives<=1:
        print(" ||/       |  ")
    if tentatives<=2:
        print(" ||        0  ")
    if tentatives<=3:
        print(" ||       /|\ ")
    if tentatives<=4:
        print(" ||       /|  ")
    if tentatives<=5:                    
        print("/||           ")
    if tentatives<=6:
        print("==============\n")
#l'affichage lorqu'une lettre est trouver ou pas
  affichage = ""
  for x in solution:
      if x in lettres_trouvees:
          affichage += x + " "
      else:
          affichage += "_ "
#lorsque le mot est trouve
  if "_" not in affichage:
      print(">>>C'est une win  <<<")
      break
 #petit plus ;)    
print("    * Revanche *    ")
