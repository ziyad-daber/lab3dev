# TP Android — HelloToast

## Objectif du TP
Réaliser une application Android simple permettant :
1. d’afficher un message **Bonjour!**,
2. d’implémenter un **compteur** qui s’incrémente à chaque clic.

## Description de l’application
L’application affiche :
- un texte qui montre la valeur actuelle du compteur,
- un bouton **Affiche un message** qui affiche un message,
- un bouton **incrementer compteur** qui augmente la valeur du compteur et met à jour l’écran.

## Interface (activity_main.xml)
L’interface est une `LinearLayout` verticale centrée avec un padding de 16dp :
- **TextView** `text_count` : affiche la valeur du compteur (taille 36sp).
- **Button** `button_toast` : affiche un "bonjour".
- **Button** `button_count` : incrémente le compteur.

## Fonctionnement (MainActivity.java)
- Une variable `count` est initialisée à 0.
- `textCount` est lié au `TextView` grâce à `findViewById`.
- Au clic sur **button_toast** :
  - affichage d’un "Bonjour!" avec `Toast.makeText(...)`.
- Au clic sur **button_count** :
  - `count++`
  - mise à jour du `TextView` avec `textCount.setText(String.valueOf(count))`.

## Ressources utilisées
Les textes affichés proviennent des ressources `strings.xml` :
- valeur initiale du compteur (`count_initial_value`)
- texte du bouton Toast
- texte du bouton d’incrémentation
- message du Toast (`hello_toast_text`)

## Résultat attendu
- En appuyant sur **Afficher un message**, un message s’affiche brièvement.
- En appuyant sur **incrementer le compteur**, le nombre affiché augmente de 1 à chaque clic.

## Technologies
- Java
- Android SDK
- Android Studio
