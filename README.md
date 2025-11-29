Générateur de Mots de Passe Sécurisés
Description du Projet
Ce projet est un générateur de mots de passe simple et efficace, développé en HTML, CSS et JavaScript pur.

Il permet aux utilisateurs de créer rapidement des mots de passe robustes et aléatoires en choisissant divers critères :

La longueur du mot de passe (entre 4 et 30 caractères).

L'inclusion de minuscules, majuscules, chiffres et symboles.

L'objectif est de fournir un outil accessible directement via un navigateur web pour générer un mots de passe d'une manière automatique.

Technologies Utilisées:
HTML5: Structure de base de la page web et des éléments de formulaire.
CSS: Stylisation de l'interface utilisateur, gestion du design (couleurs, polices, centrage) et responsivité de base.
JavaScript:	Logique principale de l'application : génération aléatoire du mot de passe, gestion des options et fonctionnalité de copie.
Fonctionnalités Principales
Génération Aléatoire : Crée un mot de passe basé sur des critères de longueur et de types de caractères sélectionnés.

Options Flexibles : Permet à l'utilisateur de choisir l'inclusion de minuscules, majuscules, chiffres et symboles.

Contrôle de la Longueur : L'utilisateur peut spécifier la longueur désirée du mot de passe.

Fonctionnalité "Copier" : Un bouton dédié permet de copier instantanément le mot de passe généré dans le presse-papiers.

Alerte Utilisateur : Un message s'affiche si l'utilisateur tente de générer un mot de passe sans avoir sélectionné au moins un type de caractère.
Lien vers la Page GitHub Pages (Rendu Final)
[CLIQUEZ ICI pour accéder au Générateur de Mots de Passe]https://github.com/yosra-coder/test_github.git 

Nouveautés Explorées
Gestion des Options de Caractères : J'ai renforcé ma compréhension de la construction dynamique d'une chaîne de caractères (chars) en JavaScript basée sur l'état des cases à cocher (checkboxes). Cela garantit que la génération utilise uniquement les jeux de caractères souhaités par l'utilisateur.

Fonction de Copie avec document.execCommand('copy') : J'ai implémenté la méthode de copie de texte dans le presse-papiers via l'API du navigateur et géré l'affichage d'un message de confirmation temporaire à l'aide de setTimeout()
Difficultés Rencontrées
Difficulté Conceptuelle (Sécurité) : S'assurer que le mot de passe généré utilise au moins un caractère de chaque type sélectionné. La version actuelle garantit que tous les types peuvent être utilisés, mais pour une sécurité maximale, il faudrait garantir la présence d'au moins un caractère de chaque type coché (par exemple, si Majuscules est coché, s'assurer qu'au moins une majuscule est incluse). Pour ce projet, j'ai privilégié la simplicité de la génération purement aléatoire à partir de l'ensemble combiné des caractères.
Solutions Apportées
Gestion des Erreurs (Critères Vides) : J'ai ajouté une vérification simple en début de la fonction generatePassword() : si la chaîne chars est vide, j'affiche un message d'erreur clair ("Choisissez au moins un critère !") et j'arrête l'exécution de la fonction avec return.

Design Amélioré : J'ai utilisé des transitions CSS (transition: 0.2s ease et transform: scale(1.05)) sur les boutons Générer et Copier pour fournir un retour visuel moderne et interactif à l'utilisateur lors du survol et du clic.

Amélioration de la Copie : Pour la fonctionnalité de copie, j'ai enveloppé le code dans une fonction fléchée ajoutée à l'écouteur d'événement du bouton copyBtn, ce qui permet d'exécuter la sélection, la copie et la gestion du message temporaire de manière fluide et synchrone
