# Tip Time

Application Android de calcul de pourboire (Kotlin + Jetpack Compose), réalisée
d'après le **Chapitre 8 – Interagir avec l'interface utilisateur et l'état**
(cours de développement d'applications mobiles), **jusqu'au slide 82/199**.

## Ce qui est implémenté (slides 1 → 82)

| Slides | Notion | Où dans le code |
|---|---|---|
| 14-16 | Code de démarrage : `strings.xml`, `TipTimeLayout()`, `calculateTip()`, Spacer | `MainActivity.kt`, `res/values/strings.xml` |
| 20-25 | Composable `TextField` via `EditNumberField()` | `MainActivity.kt` |
| 26-42 | État, composition / recomposition, `MutableState` | `MainActivity.kt` |
| 43-50 | `remember { mutableStateOf("") }` avec délégué `by` | `TipTimeLayout()` |
| 56-63 | Libellé, `singleLine`, clavier numérique | `EditNumberField()` |
| 64-69 | `toDoubleOrNull() ?: 0.0`, `calculateTip()`, affichage du pourboire | `TipTimeLayout()` |
| 70-82 | **Hissage d'état** : `EditNumberField` sans état (`value` / `onValueChange`) | `MainActivity.kt` |

Le pourcentage de pourboire reste fixé à 15 % (slide 11) ; sa personnalisation
fait partie de la suite du cours.

## Lancer le projet

1. Android Studio : **File > Open** et sélectionner ce dossier.
2. Laisser la synchronisation Gradle se terminer (JDK 17 requis).
3. Exécuter sur un émulateur ou un appareil (minSdk 24).
