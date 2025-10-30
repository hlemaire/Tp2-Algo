### CC2 Maison
* Hugo Lemaire 1A2

---

### Échelle de difficulté

1. x - trivial (0.4 point).
2. x x - facile (0.8 point).
3. x x x - moyen (1.2 point).
4. x x x x - difficile (1.6 point).
5. x x x x x - challenge (2 points).

---

### Récapitulatif

* Max 8 exercices
* Actuel 3 exo = 4.0p
* 0 de x x - facile (0.8 point).
* 2 de x x x - moyen (1.2 point).
* 1 de x x x x - difficile (1.6 point).
* 0 de x x x x x - challenge (2 points).

---

### Chapitre 4

* 4 Activité – Recherche dans un tableau trié . . . . . . . . . . . . . . 74
* 18 Exercice – x x x Existe . . . . . . . . . . . . . . . . . . . . . . . . . 74
* 19 Exercice – x x x Compter . . . . . . . . . . . . . . . . . . . . . . . . 74
* 20 Exercice – x x x x Recherche de bornes dans un tableau . . . . . . . 74
* 21 Exercice – x x x Tableau trié ? . . . . . . . . . . . . . . . . . . . . . 75
* 22 Exercice – x x x x Trier un tableau . . . . . . . . . . . . . . . . . . . 75
* 23 Exercice – x x x x Calcul de médiane . . . . . . . . . . . . . . . . . 75
* 24 Exercice – x x x Tables de multiplications . . . . . . . . . . . . . . 75
* 25 Exercice – x x x x x Suite de Fibonacci généralisée . . . . . . . . . . 75

---

### Chapitre 5

* 5 Activité – Calcul bloquant . . . . . . . . . . . . . . . . . . . . . . . 84
* 26 Exercice – x x Parité . . . . . . . . . . . . . . . . . . . . . . . . . . 84
* 27 Exercice – x x x Puissance . . . . . . . . . . . . . . . . . . . . . . . 84
* 28 Exercice – x x Diviseur . . . . . . . . . . . . . . . . . . . . . . . . . 84
* 29 Exercice – x x x Crible d’Ératosthène . . . . . . . . . . . . . . . . . 84
* 30 Exercice – x x x Factorielle . . . . . . . . . . . . . . . . . . . . . . . 85
* 31 Exercice – x x x x Racine carré méthode de Newton . . . . . . . . . 85
* 32 Exercice – x x x x Appliquer des fonctions à un tableau . . . . . . . 85

---

### Exercice choisis : [19, 20, 21, 22, 23, 25, 31, 32]

---

### Exercice 19 (x x x Compter). = 1.2p
Écrire un algorithme qui affiche tous les indices où un élément est présent dans
un tableau et renvoie son nombre d’occurrences.

```
1. données : "←"
   1 | entrée : liste : tableau de n éléments
   2 | entrée : valeur : élément
   3 | sortie : occurrences : entier
2. variables :
   1 | i : entier
   2 | occurrences : entier
3. début
   1 | occurrences ← 0
   2 | pour i ← 0 à |liste| − 1 faire
   3 |     si liste[i] = valeur alors
   4 |         affiche(valeur, " trouvé à l’indice ", i)
   5 |         occurrences ← occurrences + 1
   6 |     fin si
   7 | fin pour
   8 | affiche("Nombre total d'occurrences : ", occurrences)
4. fin
```

---

### Exercice 20 (x x x x Recherche de bornes dans un tableau). = 1.6p
Alice souhaite déterminer une méthode automatique (...). Écrire un programme qui prend
en entrée un entier naturel n, demande à l’utilisateur de saisir n nombres et affiche
le maximum et le minimum de cette suite de valeurs. Par exemple pour n = 5,
nous pourrions avoir la sortie suivante :

* Entrez 5 valeurs : 2 3 1 5 4
* Le minimum de 2, 3, 1, 5, 4 est 1.
* Le maximum de 2, 3, 1, 5, 4 est 5.

```
1. données : "←"
    1 | entrée : n : entier
    2 | sortie : min, max : entiers
2. variables :
    1 | liste : tableau de n nombres
    2 | i : entier
    3 | visualisation : chaîne de caractères
3. début
    1 | affiche("Entrez ", n, " valeurs : ")
    2 | visualisation ← ""
    3 | pour i ← 0 à n − 1 faire
    4 |     lire liste[i]
    5 |     si i = 0 ∨ liste[i] > max alors
    6 |         max ← liste[i]
    7 |     fin si
    8 |     si i = 0 ∨ liste[i] < min alors
    9 |         min ← liste[i]
   10 |     fin si
   11 |     si i ≠ 0 alors
   12 |         visualisation ← visualisation · ", "
   13 |     fin si
   14 |     visualisation ← visualisation · liste[i]
   15 | fin pour
   16 | affiche("Le minimum de ", visualisation, " est ", min, ".")
   17 | affiche("Le maximum de ", visualisation, " est ", max, ".")
4. fin
```

---

### Exercice 21 (x x x Tableau trié ?). = 1.2p
Écrire un algorithme qui vérifie si un tableau est trié.

```
1. données : "←"
    1 | entrée : liste : tableau de n éléments
    2 | sortie : trié : booléen
2. variables :
    1 | i : entier
    2 | croissant : booléen
    3 | décroissant : booléen
3. début
    1 | croissant ← Vrai
    2 | décroissant ← Vrai
    3 | pour i de 1 à |liste| - 1 faire
    4 |     si liste[i] < liste[i - 1] alors
    5 |         croissant ← faux
    6 |     fin si
    7 |     si liste[i] > liste[i - 1] alors
    8 |         décroissant ← faux
    9 |     fin si
   10 | fin pour
   11 | trié ← croissant \/ décroissant
   12 | affiche(trié)
4. fin
```

---

### Exercice 22 (x x x x Trier un tableau). = 1.6p
Écrire un algorithme de tri d’un tableau (reprendre par exemple la méthode proposée en activité introductive).

```
1. données :
    1 | entrée : liste : tableau de n éléments
    2 | sortie : liste : tableau de n éléments triés (ordre croissant)
2. variables :
    1 | i, j : entiers
    2 | tmp : élément
3. début
    1 | pour i ← 0 à |liste| − 2 faire
    2 |     pour j ← i + 1 à |liste| − 1 faire
    3 |         si liste[j] < liste[i] alors
    4 |             tmp ← liste[i]
    5 |             liste[i] ← liste[j]
    6 |             liste[j] ← tmp
    7 |         fin si
    8 |     fin pour
    9 | fin pour
4. fin
```



