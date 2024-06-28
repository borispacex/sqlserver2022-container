# Creacion de un contenedor de SQL SERVER 2022
## Comandos
- Creacion de Volumen
``` 
docker volume create BU_UC_VOL_DB_SQLSERVER_COL
``` 
- Descargamos la imagen sql server
``` 
docker pull mcr.microsoft.com/mssql/server:2022-latest
``` 
- Ejecutamos el contendor
``` 
docker compose up -d
``` 
- Verificamos la conexion
``` 
docker exec -t BU_UC_CON_DB_SQLSERVER_COL cat /car/opt/mssql/log/errorLog | grep connection
``` 
- Ingresamos al bash del contendor
``` 
docker exec -it BU_UC_CON_DB_SQLSERVER_COL "bash"
``` 
- Ingresamos a la consola de SQLSERVER
``` 
/opt/mssql-tools/bin/sqlcmd -S localhost -U SA -P ".sysDBA99."
``` 
- Creamos una base de datos
``` 
CREATE DATABASE db_test;
GO
``` 
- Ahora realizamos la conexion
![Descripción de la imagen](/images/01conexion.png)