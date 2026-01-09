# Projet DevOps - Manal Qachri
Présentation du projet

Ce mini-projet a pour objectif de mettre en œuvre les principes fondamentaux du DevOps à travers la mise en place d’une chaîne d’intégration continue (CI). Le projet s’appuie sur un dépôt GitHub, des workflows GitHub Actions et un pipeline Jenkins afin d’automatiser le cycle de vie d’une application Java simple.

L’application développée sert de support pédagogique pour illustrer l’automatisation du build, l’exécution des tests, la génération d’artefacts et la notification des résultats du pipeline.

Objectifs pédagogiques

Comprendre les principes de l’intégration continue (CI)

Mettre en place un dépôt Git structuré avec GitHub

Automatiser les builds et tests avec GitHub Actions

Configurer un pipeline Jenkins pour la compilation et l’archivage des artefacts

Assurer la traçabilité des changements via les commits et les Pull Requests

Mettre en place des notifications du pipeline via Slack

Architecture générale

Le projet repose sur l’architecture suivante :

Dépôt GitHub pour la gestion du code source

Application Java basée sur Maven

GitHub Actions pour l’intégration continue côté GitHub

Jenkins pour l’orchestration du pipeline CI

Slack pour les notifications automatiques du pipeline

Technologies et outils utilisés

Git et GitHub

GitHub Actions

Jenkins

Java 17

Maven

Docker

Slack (Incoming Webhooks)

Structure du projet
Projet-DevOps-ManalQachri
│
├── hello-devops
│   ├── pom.xml
│   └── src
│       ├── main
│       │   └── java
│       │       └── com
│       │           └── devops
│       │               └── App.java
│       └── test
│           └── java
│               └── com
│                   └── devops
│                       └── AppTest.java
│
├── .github
│   └── workflows
│       └── ci.yml
│
└── README.md

Gestion du code source

Le code source est géré via Git et hébergé sur GitHub. Le projet utilise deux branches principales :

main : branche principale contenant la version stable du projet

dev : branche de développement utilisée pour les évolutions

Les modifications sont intégrées dans la branche principale via des Pull Requests, permettant de valider le code avant fusion.

Intégration continue avec GitHub Actions

GitHub Actions est utilisé pour automatiser le processus d’intégration continue lors des pushs et des pull requests.

Fonctionnement du workflow

Le workflow défini dans le fichier ci.yml effectue les étapes suivantes :

Récupération du code source

Configuration de l’environnement Java 17

Compilation du projet avec Maven

Exécution des tests unitaires

Génération du package JAR

Ce workflow garantit que chaque modification du code est automatiquement testée et validée.

Pipeline Jenkins

Un pipeline Jenkins a été mis en place afin de compléter la chaîne CI et de centraliser l’exécution des builds.

Étapes du pipeline

Le pipeline Jenkins est composé des étapes suivantes :

Checkout : récupération du code source depuis GitHub

Build & Test : compilation et exécution des tests avec Maven

Archive : archivage de l’artefact généré

À la fin de l’exécution, Jenkins génère un fichier JAR qui est conservé comme artefact du build.

Gestion des artefacts

L’artefact généré par le pipeline Jenkins est un fichier JAR correspondant à l’application Java compilée. Cet artefact est automatiquement archivé par Jenkins et accessible depuis l’interface du job.

Notifications Slack

Une intégration Slack a été mise en place afin de notifier automatiquement l’état du pipeline Jenkins. À chaque exécution, un message est envoyé dans un canal Slack dédié indiquant si le build s’est terminé avec succès ou en échec.

Cette fonctionnalité permet un suivi en temps réel du pipeline et améliore la communication autour du projet.

Résultats obtenus

Mise en place réussie d’une chaîne d’intégration continue

Exécution automatique des builds et tests

Génération et archivage d’un artefact exploitable

Notifications automatiques du pipeline via Slack

Traçabilité complète des modifications via GitHub

Améliorations possibles

Plusieurs améliorations peuvent être envisagées pour étendre ce projet :

Ajout d’un déploiement continu (CD)

Utilisation de Docker Compose pour le déploiement

Mise en place de tests plus avancés

Sécurisation des accès Jenkins et GitHub

Ajout de métriques et de monitoring

Conclusion

Ce mini-projet DevOps a permis d’appliquer concrètement les concepts d’intégration continue à travers l’utilisation conjointe de GitHub Actions et Jenkins. Il démontre l’importance de l’automatisation dans le cycle de développement logiciel et constitue une base solide pour des projets DevOps plus avancés.
