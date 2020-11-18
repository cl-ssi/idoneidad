## Instalación Sistema de Idoneidad SSI
=======

### Programas

- Instalar PHP >= 7.3
- Instalar Composer
- Instalar Git
- (opcional) Instalar MySql

#### Configurar

- Agregar todos los programas al PATH
- En php.ini habilitar (descomentar) extención gd2, mbstring, pdo_sqlite, fileinfo, ssl y no me acuerdo cual mas.

### Ejecutar en interprete de comandos

- $ git clone https://github.com/cl-ssi/idoneidad
- $ cd idoneidad
- $ cp .env.example .env (copy en vez de cp en windows)
- $ composer install
- $ php artisan key:generate

### Base de datos
- Editar archivo .env

#### Opción 2. MySql editar
- Configurar en .env los campos de base de datos, empiezan con DB_


### Ejecutar los siguientes comandos
- $ php artisan migrate --seed   ( Para cargar la base de datos )
- $ php artisan serve    ( Para iniciar el servidor web )

### Abrir en navegador
- http://localhost:8000
- usuario: sistemas.ssi@redsalud.gob.cl
- clave: admin

## Para mantener actualizado el sistema
- $ git pull
- $ composer install
- $ php artisan migrate


## Para consultas e información sobre actualizaciones del sistema
- http://monitor-esmeralda.slack.com
- esmeralda.ssi@redsalud.gob.cl

## Otros comandos
- $ php artisan migrate:fresh --seed  ( Restaura al base de datos al punto de partida )

## Si presenta algún error en archivos Seeder
- $ composer dump-autoload

## Contribución
- El sistema está abierto a quien quiera colaborar. :)

