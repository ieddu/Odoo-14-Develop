INSTALACION
------------

Clona el repositorio: git clone git@github.com:ieddu/Odoo-14-Develop.git

Crear las siguientes carpetas en la rais: 

data-db-14/
data-log-14/
data-odoo-14/
extra-addons/
src/

Actualmente este repositorio fue configurado con la version 14 de Odoo, 
si deseas utilizar la ultima version de Odoo, debes de eliminar todos
los archivos de la carpeta /src/ y clonar la ultima version de Odoo de la
siguiente forma:

cd Odoo-14-Develop/
cd src/
git clone https://github.com/odoo/odoo.git --branch master --depth 1 --single-branch .

Copia el archivo .odoorc que se encuentra en la carpeta config/ 
debes de pegar el archivo en src/

cp config/.odoorc src/

Genera la imagen de odoo de la siguiente forma e inicia el contenedor
de la siguiente forma:

docker build -t image_odoo_14 .
docker-compose up -d

Ingresa al ambiente local de desarrollo: http://localhost:8069