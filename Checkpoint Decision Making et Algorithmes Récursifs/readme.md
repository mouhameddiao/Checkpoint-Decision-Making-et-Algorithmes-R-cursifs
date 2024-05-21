function estAnneeBissextile(annee):
if (annee % 4 == 0 and annee % 100 != 0) or (annee % 400 == 0):
return True
else:
return False

// Exemple d'utilisation
annee = input("Entrez une année: ")
if estAnneeBissextile(annee):
print(annee + " est une année bissextile.")
else:
print(annee + " n'est pas une année bissextile.")

function prixBillet(age):
if age <= 12:
return 10
else if age >= 13 and age <= 17:
return 15
else:
return 20

// Exemple d'utilisation
age = input("Entrez votre âge: ")
prix = prixBillet(age)
print("Le prix du billet est de $" + prix + ".")

function conseillerVetements(temperature, pleut):
if pleut:
if temperature < 10:
return "Portez un manteau chaud et un parapluie."
else if temperature < 20:
return "Portez une veste légère et un parapluie."
else:
return "Portez des vêtements légers et un parapluie."
else:
if temperature < 10:
return "Portez un manteau chaud."
else if temperature < 20:
return "Portez une veste légère."
else:
return "Portez des vêtements légers."

// Exemple d'utilisation
temperature = input("Entrez la température actuelle: ")
pleut = input("Est-ce qu'il pleut (oui/non)? ") == 'oui'
conseil = conseillerVetements(temperature, pleut)
print(conseil)

function fibonacci(n):
if n <= 0:
return 0
else if n == 1:
return 1
else:
return fibonacci(n-1) + fibonacci(n-2)

// Exemple d'utilisation
n = input("Entrez un nombre: ")
print("Le " + n + "ème nombre de Fibonacci est " + fibonacci(n) + ".")

function estPalindrome(chaine):
// Enlever les espaces, la ponctuation et convertir en minuscules
chaine = enleverEspacesEtPonctuation(chaine).toLowerCase()
return estPalindromeRecursive(chaine)

function estPalindromeRecursive(chaine):
if longueur(chaine) <= 1:
return True
else if chaine[0] != chaine[longueur(chaine) - 1]:
return False
else:
return estPalindromeRecursive(sousChaine(chaine, 1, longueur(chaine) - 2))

function enleverEspacesEtPonctuation(chaine):
// Implémenter la fonction pour enlever les espaces et ponctuations
nouvelleChaine = ""
for caractère in chaine:
if caractère est alphanumérique:
nouvelleChaine += caractère
return nouvelleChaine

// Exemple d'utilisation
chaine = input("Entrez une chaîne: ")
if estPalindrome(chaine):
print("La chaîne est un palindrome.")
else:
print("La chaîne n'est pas un palindrome.")

function puissance(base, exponent):
if exponent == 0:
return 1
else:
return base \* puissance(base, exponent - 1)

// Exemple d'utilisation
base = input("Entrez la base: ")
exponent = input("Entrez l'exposant: ")
print(base + " à la puissance " + exponent + " est " + puissance(base, exponent) + ".")
