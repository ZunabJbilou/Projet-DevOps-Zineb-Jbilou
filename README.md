# Projet DevOps - Amal Chegdali

## Description

Ce projet démontre l'utilisation pratique des outils DevOps pour créer, gérer et déployer une application Java/Maven.

## Structure du projet

```
Projet-DevOps-AmalChegdali/
├── demo-app/              # Application principale
│   ├── src/              # Code source
│   ├── pom.xml           # Configuration Maven
│   ├── Dockerfile        # Configuration Docker
│   └── Jenkinsfile       # Pipeline Jenkins
├── .github/
│   └── workflows/
│       └── ci.yml         # Workflow GitHub Actions
└── README.md             # Ce fichier
```

## Technologies utilisées

- **Java 17** : Langage de programmation
- **Maven** : Gestionnaire de dépendances et build
- **Docker** : Conteneurisation
- **Jenkins** : CI/CD
- **GitHub Actions** : Intégration continue
- **Slack** : Notifications

## Fonctionnalités

- Application Java simple affichant un message de bienvenue
- Tests unitaires avec JUnit 5
- Pipeline CI/CD avec Jenkins
- Workflow GitHub Actions pour tests et build
- Notifications Slack pour les builds

## Installation et exécution

### Prérequis

- Java 17
- Maven 3.9+
- Docker (optionnel)

### Build local

```bash
cd demo-app
mvn clean package
java -jar target/demo-app-1.0-SNAPSHOT.jar
```

### Build avec Docker

```bash
cd demo-app
docker build -t demo-app .
docker run demo-app
```

## Pipeline Jenkins

Le pipeline Jenkins (`PipeLine-AmalChegdali`) exécute les étapes suivantes :

1. **Checkout** : Récupération du code depuis GitHub
2. **Build** : Compilation avec Maven
3. **Test** : Exécution des tests unitaires
4. **Archive** : Archivage des artefacts
5. **Deploy** : Déploiement (optionnel)
6. **Notify Slack** : Envoi de notifications Slack

## GitHub Actions

Le workflow GitHub Actions se déclenche sur :
- Push vers les branches `main` et `dev`
- Pull Requests vers `main`

Il exécute :
- Tests avec Maven
- Build de l'application
- Upload des artefacts

## Auteur

**Amal Chegdali**
