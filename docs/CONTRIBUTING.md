Repris de https://github.com/team-gsri/.github/blob/main/CONTRIBUTING_FR.md

Tout est à reprendre pour être adapté.

# Guide de contribution standard

Cette documentation offre des lignes directrices et des procédures standard pour contribuer à nos projets. Il s'agit d'une documentation générique susceptible d'être remplacée au niveau de chaque projet. Merci de vérifier le fichier `docs\CONTRIBUTING.md` du projet concerné pour davantage d'instructions.

## Possibilités de contribution aux projets

Il existe deux manières de contribuer à nos projets :

1. Suggérer des idées, donner un retour d'expérience
2. Contribuer au code source

**Note :** afin de contribuer au code source vous devez posséder un compte _github.com_.

## Comment transmettre des idées et retours d'expérience

La meilleure manière de procéder est d'ouvrir une `issue` sur le dépôt Github concerné.
Pour cela, rendez-vous sur le dépôt en question, et cliquez sur l'onglet `issues` en dessous du nom du dépôt.
Cliquez ensuite sur le bouton vert indiquant `New issue`, qui vous donnera accès au formulaire de création.

Avant d'envoyer votre `issue`, vérifiez que vous avez indiqué les éléments suivants :
* un titre éloquent
* une description détaillée
* un label `bug` (incident) ou `enhancement` (amélioration)


## Contribution ponctuelle au code source

**Note :** *cette procédure s'adresse aux contributeurs ponctuels. En tant que tel, vous n'êtes pas autorisé à écrire directement dans le dépôt, mais vous pouvez soumettre une `pull request` depuis un `fork` de notre dépôt.*

### Fork le dépôt

La première étape pour contribuer est de réaliser un `fork` du dépôt. Cela signifie concrètement que vous créez votre propre copie de notre dépôt. Pour faire cela, cliquez simplement sur le bouton `Fork` en haut à droite de l'interface.

C'est tout.

### Cloner le dépôt

Vous devez utiliser un client git afin de télécharger et synchroniser votre travail avec le dépôt. Si vous n'êtes pas coutumier de git, nous vous recommandons l'usage de [Github Desktop](https://desktop.github.com/).

Une fois votre client git installé, rendez-vous sur la page de votre `fork` sur github.com, et cliquez sur le bouton vert `Clone or download` sur la droite de la page, puis cliquez sur `Open in Desktop` dans l'encart. Github Desktop démarrera alors et vous demandera où télécharger le code source. Sélectionner le dossier de votre choix puis cliquez sur `Clone` ; Github Desktop téléchargera les sources sur votre ordinateur.

### Modifier les sources

Vous pouvez alors travailler sur les sources à l'aide de votre éditeur favori. Si vous n'en avez pas encore, nous vous conseillons vim.

Git dispose de trois différentes fonctions de suivi des changements :

* `git stage` signifie que vous considérez la version actuelle d'un fichier *prêt pour le commit*. C'est une façon efficace d'ajouter ou retirer des changements au commit en cours.

* `git commit` signifie que vos modifications en mode `stage` sont stockées **localement**. Chaque commit est associé à votre identité et vous pouvez ajouter une petite description résumant ce que vous avez modifié et pourquoi. Si vous n'avez rien mis en `stage`, git placera en mode `stage` tous les changements détectés et créera le commit en les incluant tous.

* `git push` permet d'envoyer vos *commits* vers Github. Toutes les modifications restent locales jusqu'à l'utilisation de la commande `push`. D'autres utilisateurs peuvent alors accéder à vos modifications depuis leur dépôt. Vous pouvez également récupérer le code `pushed` par d'autres personnes sur Github en utilisant la commande `fetch`.

### Conserver les dépôts synchronisés

Assurez-vous fréquemment que vous ne travaillez pas sur une version obsolète des sources. Vérifiez que votre branche n'a aucun commit *behind* (en retard) relativement à notre branche `main`. Si votre branche n'est pas à jour avec `upstream/main`, l'ouverture d'une `pull request` sera refusée par notre équipe.

Si vous avez besoin de mettre à jour, vous devriez synchroniser les changements de notre dépôt vers le votre. Cette opération se nomme *intégration*. Durant l'intégration, des conflits peuvent apparaître, par exemple si vous avez modifié une entité qui a été par ailleurs supprimée de notre dépôt par un autre développeur.

La résolution des conflits doit être effectuée sur votre branche de travail, car cela facilite les tests visant à s'assurer que le processus d'intégration n'a rien cassé. Une fois satisfait de la fusion, vérifiez que votre version du code source fonctionne toujours avant d'ouvrir une `pull request`. Cette technique est nommée *ping-pong merging*.

### Ouvrir une pull request vers upstream

Lorsque vous êtes satisfait de votre travail et que vous souhaitez nous le soumettre, vous pouvez ouvrir une `pull request` pour intégrer vos modifications *upstream*.

Ouvrez la `pull request` en sélectionnant `Branch` / `Create pull request` dans Github Desktop. Cela ouvrira dans votre navigateur un formulaire à remplir. Assurez-vous que la branche source est votre branche de travail, et que la branche destination est `develop` sur notre propre dépôt. Une fois prêt, cliquez sur `Open pull request`.

 **Note : toutes les PR vers d'autres branches que `develop` seront refusées.**

Les administrateurs du projet effectueront une revue de votre code avant de fusionner votre travail. Selon le type de projet, des tests et autres opérations automatisées pourront être mises en place afin de s'assurer de la robustesse de votre production. Si un problème apparait, ou si nous remarquons un détail à modifier, vous pourrez ajouter des commits sur votre propre branche de travail afin d'effectuer les corrections nécessaires : elles seront automatiquement ajoutées à votre `pull request`.

## Contribution régulière au code source

**Note :** cette procédure s'adresse aux contributeurs réguliers identifiés. Ils·elles sont autorisés à contribuer directement dans notre dépôt afin d'éviter la prolifération des forks. Si vous n'êtes pas autorisés à contribuer directement au dépôt, référez-vous aux instructions de la section *Contribution ponctuelle au code source* plus haut dans ce document.

### Obtenir le droit d'écriture sur le dépôt

Votre première étape pour les contributions directes est d'obtenir les droits d'accès sur notre dépôt. Prenez contact avec nous sur Discord et nous étudierons votre demande.

### Cloner le dépôt

Si vous êtes un contributeur régulier, vous pouvez contribuer directement au dépôt. Vous n'avez pas besoin de créer de fork de notre dépôt : vous pouvez cloner directement le dépôt qui vous intéresse.

### Créer une nouvelle branche

**Note : cette étape est obligatoire.** Y circonvenir vous permettra de créer des commits sur main **localement**, mais toute tentative de `push` vers Github sera automatiquement refusée.

Afin de créer une branche, sélectionnez `Branch` / `New branch ...` dans le menu. Github Desktop demandera un nom de branche. Entrez le nom souhaité : pseudo, fonctionnalité... Dans le doute, demandez-nous si le nom choisi est pertinent. Assurez-vous que la branche source est `main`. Une fois créée, publiez la branche sur Github en cliquant sur le bouton dans la barre en haut de Github Desktop.

Les autres opérations sont similaires à celles décrites dans la procédure ci-dessus.

### Garder votre branche à jour avec main

Il est recommandé de vérifier régulièrement que vous ne travaillez pas sur une version obsolète des sources. Vérifiez que votre branche n'a aucun commit *behind* (en retard) relativement à notre branche `main`. Si votre branche n'est pas à jour avec `main`, l'ouverture d'une `pull request` sera refusée par notre équipe. Si des changements ont eu lieu sur la branche `main`, vous pouvez utiliser la fonction `Branch` / `Update from main` de Github Desktop afin de rattraper le retard. La résolution des conflits doit être faite sur votre branche de travail.

### Ouvrir une pull request vers main

Cette procédure est également la même que pour les contributeurs occasionnels. Votre dépôt doit être à jour avec `main`, sans quoi votre `pull request` sera refusée. Des tests et autres opérations automatisées pourront également être menées pour s'assurer de la robustesse de votre production. Les fusions sont ensuite faites par l'équipe de maintenance du GSRI. Vous pouvez ajouter des commit à votre branche de travail : ils seront automatiquement ajoutés à la PR en cours.

## Quelques conseils

* Débutez toujours votre travail en effectuant les actions `Fetch from Github` et `Update from main`.
* Travaillez toujours sur votre propre branche, n'ouvrez de `pull request` que vers `main`.
* Créez des commits petits et dotés de descriptions représentatives de vos changements.
* Créez des commits fréquemment, il s'agit d'un proche équivalent du raccourci `Ctrl + S` pour un document.
* Effectuez un `push` au moins quotidiennement, même si votre code ne fonctionne pas (mieux vaut inachevé que perdu).
* Le mode Fenêtré sans bordures sur ArmA 3 permet une transition plus aisée entre le jeu et le bureau.
