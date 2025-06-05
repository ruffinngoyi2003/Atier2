# Atier2

Projet : Création d'un installateur avec script SQL complet et intégration au portfolio

Sommaire
1. Contexte
2. Mission globale
3. Déroulement du projet
4. Suivi via Kanban GitHub
5. Objectifs atteints
6. Bilan final

1. Contexte
Dans le cadre de ma formation en BTS SIO (Services Informatiques aux Organisations), nous avons réalisé un projet visant à mettre en pratique plusieurs compétences techniques : création de base de données, gestion de projet avec GitHub, rédaction de documentation et création d’un fichier d'installation. Le tout devait être présenté dans notre portfolio en ligne.
2. Mission globale
La mission à réaliser comportait plusieurs étapes clés :
- Créer un fichier d’installation pour déployer l’application sur un autre poste.
- Générer un script SQL complet (create + insert) avec création d’un utilisateur.
- Rédiger un compte rendu d’activité avec sommaire automatique et captures.
- Intégrer une page dans le portfolio avec lien vers GitHub, le PDF et la vidéo de démo.
3. Déroulement du projet
J’ai commencé par créer les tables nécessaires avec MySQL Workbench. Voici un extrait du script utilisé :
CREATE DATABASE IF NOT EXISTS mon_application;
USE mon_application;

CREATE TABLE utilisateurs (
    id INT AUTO_INCREMENT PRIMARY KEY,
    nom VARCHAR(50),
    prenom VARCHAR(50),
    email VARCHAR(100),
    mot_de_passe VARCHAR(255)
);

INSERT INTO utilisateurs (nom, prenom, email, mot_de_passe)
VALUES ('Doe', 'John', 'john.doe@example.com', 'azerty123');

CREATE USER IF NOT EXISTS 'user_app'@'localhost' IDENTIFIED BY 'MotDePasse123!';
GRANT ALL PRIVILEGES ON mon_application.* TO 'user_app'@'localhost';
FLUSH PRIVILEGES;
Ensuite, j’ai utilisé le logiciel Inno Setup pour créer un installateur simple de l’application avec le script SQL inclus.
4. Suivi via Kanban GitHub
J’ai utilisé le tableau Kanban dans GitHub Projects pour suivre chaque tâche. Voici l'organisation :
- To Do : Analyse, script SQL
- In Progress : Installateur

6. Bilan final
Ce projet m’a permis de mieux comprendre le lien entre le développement, la base de données et la mise à disposition d’une application. J’ai pris en main les outils comme GitHub, Inno Setup et les bases de SQL pour créer un livrable complet et professionnel. Ce travail m’a donné plus de confiance pour documenter mes projets et les présenter dans mon portfolio en ligne.
