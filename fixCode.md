
# classe GameRunner

- eviter les do while qui ne sont pas aisés pour la lecture : préferer (while(notAWinner))
- mettre les variables static en Majuscules
- utiliser des listes plutot que des int[] ou des boolean[] pour éviter les erreurs d'accès

# classe GAME
- respecter l'indentation, les espaces entre les "+" ex ligne 154

- respecter les "{}" pour les if pour une meilleur lecture du code

- fonction add qui retourne toujours "true", elle devrait retourner void
 
- éviter les expressions négatives ligne 163

- éviter les forêts de if (ligne 100 à 108) : créer 3 fonctions => isPopQuestion, isScienceQuestion, isSportQuestion

- donner des noms propres aux fonctions: "ex addPlayer au lieu de add"

- commenter sommairement ce que fais chaque fonction

- la fonction isPlayable peut être écrite en une seule fois; (return players.size() >= 2), 
de même pour rockQuestions.addLast(createRockQuestion(i));

- utiliser des listes plutôt que des int[] pour éviter les erreurs d'accès.

- regrouper les classes privés et publiques ensembles

- utiliser  les String.format pour afficher les logs

- préferer l'utilisation des loggers (log4j, Sl4j)

- tests manquants, le retour des fonctions importantes n'est pas vérifié

-  "for (int i = 0; i < 50; i++) {" on ne sait pas combien de questions seront posés, cela peut dépasser 50 car les joeurs peuvent reculer.
   il faut en ajouter dynamiquement.

- scienceQuestions.removeFirst() : on ne vérifies pas si la liste contient encore des élements

- vérifier que le joeur ne dépasse pas la taille du plateau.

# réusinage des classes:

- créer une classe Player avec champs:
name : String // nom du joueur
order : Integer // ordre de passage
  
- créer un enum QuestionTypeEnum pour les differents types de question
- créer une classe AbstractQuestion avec les champs (type: QuestionTypeEnum , questionToAsk)
- créer une classe SportQuestion qui étend de AbstractQuestion, le champ type sera par défaut à QuestionTypeEnum.sport"
- idem pour (science, sport, rock, pop)
