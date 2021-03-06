# U1_A2.- Instalación de MySQL Server en Ubuntu Server 20.04 LTS

### 1.-Instalar el Ubuntu Server 20.04 LTS

Descargamos la ISO y configuramos una MV con una instalación normal de Ubuntu Server.

![](img/001.png)

![](img/002.png)

![](img/003.png)

![](img/004.png)

![](img/005.png)

![](img/006.png)

![](img/007.png)

![](img/008.png)

![](img/009.png)

Configuramos que nuestra MV se llame `ade-robert`.

![](img/010.png)

Instalamos el servicio `SSH`.

![](img/011.png)

![](img/012.png)

![](img/013.png)

![](img/014.png)

![](img/015.png)

#### 1.1 Instalación de escritorio.

- Actualizamos los repositorios

![](img/016.png)

- Ejecutamos `sudo apt-get install xubuntu-desktop`.

![](img/017.png)

![](img/018.png)

### 2.- Instalar MySQL Server

![](img/019.png)

![](img/020.png)

### 3.- Comprobación de version estable

![](img/021.png)

![](img/022.png)

![](img/023.png)

### 4.- Parar el demonio y reiniciar (init.d)

![](img/024.png)

![](img/026.png)

### 5.- Configuración de la seguridad post-instalación.

![](img/055.png)

Configuramos el script de este modo:

- Comprueba que el usuario root tiene una contraseña.

![](img/056.png)

- Permite eliminar los usuarios anónimos.

- Elimina la cuenta root remota.

- Elimina la base test de pruebas.

![](img/057.png)

- Permite recargar los privilegios.


![](img/058.png)

Ejecuta esta consulta: `select user, host, plugin from mysql.user;`

![](img/059.png)

### 6.- Modificar BD MySQL

El usuario root nos denegaba la password y tenemos que implementar una nueva.

![](img/027.png)

![](img/029.png)

![](img/030.png)

### 7.- Instalar MYSQL Workbench

![](img/031.png)

![](img/032.png)

![](img/033.png)

![](img/034.png)

![](img/035.png)

- Comprobamos el funcionamiento del `Workbench` añadiendo una `SQL`.

![](img/037.png)

### 8.- Instalar  Adminer sobre Apache

- Instalamos el `Adminer` siguiendo los pasos del PDF que nos ofrece la profesora.

![](img/038.png)

![](img/039.png)

![](img/040.png)

![](img/041.png)

> Hemos generado el archivo `adminer-4.7.8.php`.

![](img/042.png)

![](img/045.png)

![](img/046.png)

![](img/047.png)

### 8.2 Instalar PHPMyAdmin

![](img/052.png)

![](img/048.png)

![](img/049.png)

![](img/050.png)

![](img/051.png)

![](img/053.png)

![](img/054.png)

### 9.- Preguntas

![](img/060.png)

#### 9.1 Directorio de instalación base

Se encuentra dentro de `/usr/bin`, filtraremos por "mysql"

![](img/061.png)

Si ejecutamos el comando `sudo mysqladmin -u root -p shutdown`, apagaremos el servicio para iniciar como usuario root en mysql.

![](img/062.png)

Para revocar esta accion ejecutamos el comando `/etc/init.d/mysql start`.

![](img/063.png)

![](img/064.png)

#### 9.2 Directorio del servicio

Esto se encuentra en `init.d` como comprobamos en apartados anteriores cuando apagamos y encendemos el servicio.

![](img/065.png)

![](img/066.png)

#### 9.3 Directorio de los datos

Este directorio se encuentra en `/var/lib` dentro de `mysql`.

![](img/067.png)

#### 9.4 Fichero de configuracion del servidor

Dentro de `/etc/mysql` esta el archivo `my.cnf`.

![](img/068.png)

![](img/069.png)
