# Gestion de matériel - LyonPalme

![readme_logo__1_](https://github.com/user-attachments/assets/74bc75c4-f87c-448b-85c0-c5637abc7e5b)

# Sommaire

- [Description](#description)
- [Technologies Utilisées](#technologies-utilisées)
- [Diagramme de cas d'utilisation](#diagramme-de-cas-dutilisation)
- [Prérequis](#prérequis)
- [Installation](#installation)
- [Utilisation](#utilisation)
- [Dépendances](#dépendances)



## Description

Le club "LyonPalme" est une association sportive de natation avec palmes : monopalme ou bi-palmes. Il compte une quarantaine d'adhérents et son siège est à Saint-Fons. L'application de gestion matériel permet de gérer le matériel du club. Ce site est destiné au responsable du matériel qui pourra après s’être connecter, voir le stock et ajouter du matériel au stock, voir les prêt en affichant les emprunts que les nageurs ont faits à l’association et ainsi ajouter et retirer un prêt et donné son état de retour.
Elle permet également de « tracer » le matériel c’est-à-dire pour un matériel, connaitre toutes les personnes à qui il a été prêté. Ceci permet de retrouver la personne responsable en cas de détérioration du matériel.


## Technologies Utilisées


| **Nom** | **Description** |
| ------- | ------------- |
| ![C#](https://img.shields.io/badge/c%23-%23239120.svg?style=for-the-badge&logo=c-sharp&logoColor=white) | Langage de programmation orienté objet. |
| ![MicrosoftSQLServer](https://img.shields.io/badge/Microsoft%20SQL%20Server-CC2927?style=for-the-badge&logo=microsoft%20sql%20server&logoColor=white) | Base de données. |
| ![.Net](https://img.shields.io/badge/.NET-5C2D91?style=for-the-badge&logo=.net&logoColor=white) | Framework .Net `6.0`. |
| ![Windows](https://img.shields.io/badge/Windows-0078D6?style=for-the-badge&logo=windows&logoColor=white) | Interface utilisateur avec Windows Forms |
| ![Git](https://img.shields.io/badge/git-%23F05033.svg?style=for-the-badge&logo=git&logoColor=white) | Contrôle de version. |

## Diagramme de cas d'utilisation

![Diagramme de cas GM](https://github.com/user-attachments/assets/d1d36bf9-df61-42b5-bf2b-079f1df7ee6b)

## Prérequis
Pour exécuter ce projet, vous devez avoir Windows, Visual Studio, Microsoft SQL Server, le Framework .Net 6.0 et Git. Assurez-vous d'être connecté au réseau de l'établissement ou utiliser openVPN.

## Installation
Tout d'abord, vous devez cloner le projet :
```xml
git clone https://github.com/Lilly-22/gestion_materiel_.git
```

Ouvrez le projet dans votre environnement de développement intégré (IDE).

Créez un nouveau fichier `App.config` dans le répertoire racine du projet.

Dans le fichier `App.config`, ajoutez le code nécessaire pour configurer l'accès à la base de données.  Voici un exemple de ce à quoi pourrait ressembler votre fichier `App.config` :
```xml
<configuration>
	<startup>
		<supportedRuntime version="v4.0" sku=".NETFramework,Version=v4.7.2" />
	</startup>
	<connectionStrings>
		<add name="sqlserver_lyonpalme" connectionString="Data Source=192.168.100.236;Initial Catalog=user_de_bdd;User ID=User_lp;Password=MDP-lp"
			 providerName="System.Data.SqlClient" />
	</connectionStrings>

</configuration>
```

 - Une fois ses modifications effectuées, l'utilisateur devra se diriger dans le dossier suivant \bin\Debug où il trouvera l'exécutable.
 

Voici donc l'utilisateur admin pour se connecter à l'application lorsque vous l'avez executer :

| **Login** | **Mot de passe** |
| ------- | ------------- |
| jdupont | MonSuperMotDePasse |


## Utilisation
Pour utiliser l'application, il faut tout d'abord s'y connecter et seul l'administrateur le peut. L'utilisateur sera ensuite redirigé vers une page où il aura le choix entre visualiser le stock et voir les matériels qui sont en train d'être prêtés.
 
- Page pour visualiser le stock : Au sein de cette page, l'utilisateur peut ajouter du matériel à son stock et aussi ajouter un nouveau prêt.

- Page où l'on voit les prêts en cours : Au sein de cette page, l'utilisateur pourra récupérer les prêts en cours.

## Dépendances
 
L'application dépend d'une base de données (SQL Serveur). Si nous ne sommes pas connectés au réseau de l'établissement (ou a un vpn) , l'application ne fonctionnera pas.
 




