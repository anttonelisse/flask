# flask
installer les packages suivants :  

pip install flask flask_sqlalchemy flask_login flask_bcrypt flask_wtf wtforms email_validator  


$env:FLASK_APP = './app.py'  
$env:WEBAPP_DB = './databse.sql'  

pour gérer la database, une fois créée, utiliser la commande :  

from app import sql   

# ici de temps en temps cela me renvoit un erreur comme quoi il ne trouve pas flask alors qu'il est bien installé (cf commande ci-dessus)

sql.create_all() #pour créer les tables  


pour vérifier que les tables ont été créées :   

sqlite3 database.sql  

sqlite> .tables  

# normalement ici cela devrait me retourner les tables présentes dans database.sql et ça ne me retourne rien. 
