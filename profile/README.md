# API Shared - Manage Database via API (Java)

## English Version

### Project Overview
The **Shared API** project is designed to simplify the life of developers by allowing them to manage their databases via a REST API. Developers can easily register their plugins and automatically create databases and tables without worrying about the underlying infrastructure. The entire database management system is handled by the API, thus removing the need for manual database configurations.

### Key Features
- **Automatic Database Creation**: Developers can register their plugins on the platform, which automatically generates a dedicated database for them.
- **Table Management**: The API provides methods to create, update, and delete tables, hiding the complexity of SQL operations.
- **Database Sharing and Isolation**: Multiple developers can share the same infrastructure, with isolated access to their own databases.
- **No Direct Database Access**: All database operations are done via REST API calls, ensuring a streamlined and secure development process.

### Use Cases
- **Plugin Developers**: Easily manage database schemas and data for your plugin using just the API, without the need to interact with database servers.
- **Startups and Small Teams**: Focus on your core logic without worrying about database management.
- **Database Abstraction**: Developers can use high-level methods instead of direct SQL queries, saving time and reducing errors.

### Getting Started

#### 1. Register Your Plugin
Once a developer registers their plugin through a simple API call, a database is automatically created for them.

Example request:

```bash
POST /api/v1/plugin/register
{
  "pluginName": "MyAwesomePlugin",
  "developerId": "yourDeveloperId"
}
```

This creates a new database for the plugin.

#### 2. Create Tables via the API
You can create tables dynamically through API calls:

Example request:

```bash
POST /api/v1/plugin/createTable
{
  "pluginName": "MyAwesomePlugin",
  "tableName": "users",
  "columns": {
    "id": "INT PRIMARY KEY",
    "name": "VARCHAR(255)",
    "email": "VARCHAR(255)"
  }
}
```

The API will handle the SQL queries behind the scenes, creating the table in your plugin’s database.

#### 3. Access and Query Data via the API
Once the table is created, you can insert, update, and retrieve data through API methods.

### Technologies Used
- **Java**: Core API development
- **Python RESTful API**: For communication between client and server
- **SQL Databases**: Dynamically managed through the API

---

## Version Française

### Présentation du Projet
Le projet **Shared API** a pour objectif de simplifier la vie des développeurs en leur permettant de gérer leurs bases de données via une API REST. Les développeurs peuvent facilement enregistrer leurs plugins et créer automatiquement des bases de données et des tables sans avoir à se soucier de l'infrastructure sous-jacente. La gestion complète des bases de données est prise en charge par l'API, éliminant ainsi le besoin de configurations manuelles.

### Fonctionnalités Clés
- **Création Automatique de Base de Données** : Les développeurs peuvent enregistrer leurs plugins sur la plateforme, ce qui génère automatiquement une base de données dédiée.
- **Gestion des Tables** : L'API propose des méthodes pour créer, mettre à jour et supprimer des tables, en cachant la complexité des opérations SQL.
- **Partage et Isolation des Bases de Données** : Plusieurs développeurs peuvent partager la même infrastructure, avec un accès isolé à leurs propres bases de données.
- **Pas d'Accès Direct à la Base de Données** : Toutes les opérations sur la base de données sont effectuées via des appels API REST, garantissant un processus de développement simplifié et sécurisé.

### Cas d'Usage
- **Développeurs de Plugins** : Gérez facilement les schémas de base de données et les données de votre plugin en utilisant uniquement l'API, sans avoir besoin d'interagir avec les serveurs de base de données.
- **Startups et Petites Équipes** : Concentrez-vous sur votre logique métier sans vous soucier de la gestion des bases de données.
- **Abstraction des Bases de Données** : Les développeurs peuvent utiliser des méthodes de haut niveau au lieu d'effectuer des requêtes SQL directement, ce qui permet de gagner du temps et de réduire les erreurs.

### Démarrage

#### 1. Enregistrer Votre Plugin
Une fois qu’un développeur enregistre son plugin via un appel API, une base de données est automatiquement créée pour lui.

Exemple de requête :

```bash
POST /api/v1/plugin/register
{
  "pluginName": "MonSuperPlugin",
  "developerId": "votreIdentifiantDeveloppeur"
}
```

Cela crée une nouvelle base de données pour le plugin.

#### 2. Créer des Tables via l'API
Vous pouvez créer des tables dynamiquement via des appels API :

Exemple de requête :

```bash
POST /api/v1/plugin/createTable
{
  "pluginName": "MonSuperPlugin",
  "tableName": "utilisateurs",
  "columns": {
    "id": "INT PRIMARY KEY",
    "nom": "VARCHAR(255)",
    "email": "VARCHAR(255)"
  }
}
```

L'API s'occupe des requêtes SQL en arrière-plan et crée la table dans la base de données du plugin.

#### 3. Accéder et Interroger les Données via l'API
Une fois la table créée, vous pouvez insérer, mettre à jour et récupérer des données grâce aux méthodes de l'API.

### Technologies Utilisées
- **Java** : Développement du backend
- **Python API RESTful** : Pour la communication entre le client et le serveur
- **Bases de Données SQL** : Gérées dynamiquement via l'API
