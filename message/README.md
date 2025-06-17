# Fichier textes

## Hierarchie

Chaque répertoire contient les fichier texte de différentes partie du jeu.
Voilà ce que j'en ai compris :

- mes_4th_dlc : DLC du 4ème survivant
- mes_cf : Sous titres de différentes cutscene in game
- mes_conv : D'autres sous-titres
- mes_ev : Encore d'autres sous-titres
- mes_file : Les différents documents qu'on trouve dans le jeu
- mes_item : Noms et description des objets
- mes_other_dlc : La descriptions des différentes tenus DLC je crois
- mes_rogue_dlc : Du texte en rapport avec les missions de survivant en DLC
- mes_stg : Ca ressemble à des ID de trigger de certains trucs, vaut mieux pas y toucher.
- mes_sys : Tout ce qui est lié à l'interface (menu, tutoriel, etc...)

## Syntaxe

Une bonne ressource pour la syntaxe est ce [post sur le forum de modding RE](https://residentevilmodding.boards.net/thread/11743/game-message-syntaxes-codes-documentation)

Pour résumer :

- Chaque ligne qui commence par `<string>` est une entrée dans le fichier. Pour les documents, ça correspond à une page (a priori limité à 11 entrées, je sais pas ce que ça fait si on surrpime ou ajoute une entrée). Pour les objets ou l'interface, ça correspond à une entrée spécifique -> **Attention à l'ordre des entrées pour ces cas là, sinon on risque de casser des trucs**
- Pour les documents, il y a la possibilité de mettre des retours à la ligne avec la balise `<lf>`. Un retour à la ligne automatique existe si la ligne est trop grande, donc on est pas trop obligé de se prendre la tête.
- Il est possible de changer la couleur du texte avec la balise `<COLOR>` en spécifiant le code hexa de la couleur, ou d'utiliser des couleurs prédéfinies (exemple : `<COLOR FF0000>` ou `<COL RED>` pour du rouge)
- Pour les documents, la balise `<END>` indique la fin du fichier.
