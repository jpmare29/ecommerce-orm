# ecommerce-orm

[Video Demonstration](https://drive.google.com/file/d/1sPzjUx3zMG_68jJsp-KhwmvNKKjo0XBR/view)

This project contains a functioning backend, the database is initialized via the schema.sql
file in the /db directory. The sequelize.sync function is run once with the force: true
argument to synce the tables in the specified database, that was previously initialized,
with the models. The models specify all of the information about the columns in the 
tables in the database and the index specifies the relation between them so that 
sequelize can perform the necessary joins when queried. The tables in the database are
seeded with the information in the seed files for the sake of demonstration. The routes are 
specified using express and RESTful practices so that data can be retrieved from and populated
into the database via the ORM. The get routes either return the whole table, and any related
tables, or one row/object as specified in the url parameters. The post routes create a new
row from the passed object in the json body of the request. The put routes update information
in the database and the delete routes remove rows, both specified in the url parameters.
Once the server begins listening on the specified port it can handle all of the respective
route requests. The dotenv package from npm is used to protect sensitive data that needs to
be passed to sequelize to connect to the database.