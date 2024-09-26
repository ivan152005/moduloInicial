# moduloInicial

Documentación del proceso de instalación de Odoo con docker compose.

Primeros pasos:
  1º Instalar la herramienta: docker desktop.
  2º Crearte una carpeta llamada "dockerCompose" donde guardaremos el proyecto.
  3º Creamos en la carpeta creada el archivo "docker-compose.yml" y las carpetas "config_odoo", "dev-addons" y "log". 
  4º Instalar Odoo con docker.
    4.1  Instalamos Postgress que será nuestro gestor de la BBDD con este comando: "docker run -d -e POSTGRES_USER=odoo -e POSTGRES_PASSWORD=odoo -e POSTGRES_DB=postgres --name db postgres".
    4.2  Instalamos Odoo enlazado a la BD con este comando: "docker run -p 8069:8069 --name odoo --link db:db -t odoo".
    4.3  Iniciamos los contenedores con este comando: "docker-compose up -d".
  5º Desde la terminal del docker desktop, abrimos la carpeta "dev-addons" y pondremos el comando "scaffold dam2".Todo lo que hay en el repositorio, irá a esta carpeta.  
  6º Para crear la base de datos, ponemos en el navegador "http://localhost:8069" y ponemos los datos necesarios.
  7º Una vez abierto, vamos a ajustes, herramientas del desarrollador, le damos a "activar modo desarrollador (primera opción).
  8º En aplicaciones, buscas el modulo creado y lo instalas.
