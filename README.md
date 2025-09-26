<p align="center"><a href="https://laravel.com" target="_blank"><img src="https://raw.githubusercontent.com/laravel/art/master/logo-lockup/5%20SVG/2%20CMYK/1%20Full%20Color/laravel-logolockup-cmyk-red.svg" width="400" alt="Laravel Logo"></a></p>

<p align="center">
<a href="https://github.com/laravel/framework/actions"><img src="https://github.com/laravel/framework/workflows/tests/badge.svg" alt="Build Status"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://img.shields.io/packagist/dt/laravel/framework" alt="Total Downloads"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://img.shields.io/packagist/v/laravel/framework" alt="Latest Stable Version"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://img.shields.io/packagist/l/laravel/framework" alt="License"></a>
</p>

# Laboratorio: Implementación del Login en Laravel

**Curso:** Ingeniería Web — Unidad I: MVC  
**Instructor:** Ing. Irina Fong  
**Fecha de ejecución:** 25/09/2025
**Estudiante:** Jose Bustamante 8-1011-1717 — jose.bustamante2@utp.ac.pa 

---

## 1. Descripción del proyecto
Este repositorio contiene la implementación del módulo de autenticación (login/registro) en Laravel.  
El laboratorio demuestra el uso de la arquitectura **MVC (Modelo — Vista — Controlador)**, la configuración de entornos locales y la integración de un kit de autenticación.  

---

## 2. Requisitos previos
- PHP ≥ 8.0  
- Composer (última versión)  
- Node.js y npm  
- Servidor local (XAMPP / WampServer / Laragon) con MySQL/MariaDB  
- Visual Studio Code (recomendado)  
- Git  

---

## 3. Instalación y configuración
1. Clonar repositorio:
 ```bash
   git clone https://github.com/TUUSUARIO/TUREPO.git
   cd TUREPO
```

2. Instalar las dependencias de PHP y node.js:
 ```bash
  composer install
  npm install
```

3. Configurar el archivo .enp:
 ```bash
  cp .env.example .env
```

 3.1 Generar la clave de aplicación:
 ```bash
  php artisan key:generate
```
 3.2 Configurar las variables de conexión a Bases de datos:
 ```bash
DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=lab_login
DB_USERNAME=root
DB_PASSWORD=tu_password
```
4. Ejecutar migraciones
 ```bash
  php artisan migrate
```
5. Compilar assets
 ```bash
  npm run dev
```
6. Levantar Servidor local
 ```bash
  php artisan serve
# Abrir en el navegador http://127.0.0.1:8000
```
---
## 4. Comandos usados para autenticación
- Opción A: Laravel Breeze (recomendado, moderno con Tailwind)
```bash
 composer require laravel/breeze --dev
php artisan breeze:install
npm install && npm run dev
php artisan migrate
```
- Opción B: Laravel UI (clásico con Bootstrap)
```bash
 composer require laravel/ui
php artisan ui bootstrap --auth
npm install && npm run dev
php artisan migrate
```
---
## 5. Bases de Datos y Respaldos
- Motor: MySQL
- Nombre de la BD: lablaravellogin7

Para generar el respaldo:
```bash
 ```
---
## 6. Estructura del Repositorio
```bash
 /app
/bootstrap
/config
/database
  /backups
/public
/resources
  /views
  /screenshots
/routes
README.md
```
---
## 7. Evidencias de Capturas
Las capturas se encuentran enn la carpeta \screenshots
- Login
- Registro
- Home
---
## 8. Dificultades encontradas y Soluciones
- **No instalación de node.js y npm**
- Solución: Descargar e instalar los archivos necesarios y enrutarlos en las variables de 
entorno.

- **Tabla ya existente en base de datos MySQL al usar el comando php artisan 
migrate**
- Solución: ejecutar php artisan migrate:fresh.

- **Problemas con la seguridad en Powershell**
- Solución: Al correr los comandos en powershell pueden no funcionar y mostrar un error, 
por lo cual puede utilizarse el cmd de la computadora para proseguir instalando.

- **No aparecen vistas de login**
- Solución: instalar correctamente Breeze o Laravel UI según versión de Laravel.
---
## 9. Referencias
- Instrucciones del laboratorio (documento entregado por la docente).
- Laravel - the PHP framework for web artisans. (n.d.). Retrieved September 26, 2025, from Laravel.com website: https://laravel.com/
- MySQLdump y su poder ¿Qué es y cómo usarlo? [Web log post]. (2024, October 24). Retrieved September 26, 2025, from NebulaCloud.es - Blog - Hosting, Cloud VPS, Dedicados website: https://nebulacloud.es/blog/como-hacer-un-dump-en-mysql-mysqldump/

---
<br>
<p align="center">
    Desarrollado por el estudiante de la Universidad Tecnológica de Panamá:
<br>
Nombre: Jose Bustamante 8-1011-1717
<br>
Correo: jose.bustamante2@utp.ac.pa
<br>
Curso: Ingeniería Web - Unidad I: MVC
<br>
Instructor del Laboratorio: Ing. Irina Fong.
<br><br>
</p>


## License

The Laravel framework is open-sourced software licensed under the [MIT license](https://opensource.org/licenses/MIT).
