# PostgreSQL Data Retrieval Project

## Description
Ce projet consiste à se connecter à une base de données PostgreSQL, récupérer des données à partir d'une table spécifique et les afficher dans un environnement Python.

## Prérequis
- **PostgreSQL** doit être installé et configuré.
- **pgAdmin** ou un autre outil de gestion de bases de données pour gérer PostgreSQL.
- Python 3 avec les bibliothèques suivantes :
  - `psycopg2` pour se connecter à PostgreSQL
  - `pandas` (optionnel) pour manipuler et afficher les données sous forme de tableau

### Bibliothèques à installer

```bash
pip install psycopg2 pandas python-dotenv
Fichier .env de configuration
Voici un exemple de fichier .env à utiliser pour vos paramètres de connexion :

### Fichier `.env` de configuration

Voici un exemple de fichier `.env` à utiliser pour vos paramètres de connexion :

```env
DB_HOST='your_local_host'
DB_PORT=your_port
DB_NAME='your_dataBaseName'
DB_USER='your_Username'
DB_PASSWORD='your_Password'
````

### Test de connexion à PostgreSQL en Python

Le code suivant vous permet de tester la connexion à une base de données PostgreSQL en utilisant la bibliothèque `psycopg2` :

```python

try:
    # Connexion à la base de données PostgreSQL
    connection = psycopg2.connect(
        host="your_local_host",
        port="your_port",
        database="your_database_name",
        user="your_username",
        password="your_password"
    )
    
    print("Connexion réussie à PostgreSQL")

except psycopg2.Error as e:
    print(f"Erreur de connexion : {e}")
    
finally:
    if connection:
        connection.close()
        print("Connexion fermée")
```

### Conclusion

Ce projet constitue une base solide pour la connexion à une base de données PostgreSQL en Python. Il peut être étendu pour inclure des fonctionnalités supplémentaires telles que la manipulation des données, l'optimisation des requêtes, ou encore l'intégration dans des applications , l'objectif est de realiser la data ingestion d'un fichier en Base et de recuperer cette data Sur Tableau sowftware
