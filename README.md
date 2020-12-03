# Examen primer trimestre


## Actividad 1: Comparativa de SGBD
Indica las ventajas e inconvenientes de cada uno de ellos, así como las  características principales que hace que se diferencien los unos de los otros.

### ORACLE
#### Ventajas
Buen soporte, estabilidad, escalabilidad. Intuitivo para los usuarios. Controlado por navegador, facilita el uso desde cualquier SO
#### Inconvenientes
Aunque cuenta con una versión gratuita, su principal desventaja es el precio. La licencia es cara y la dificultad de instalar y configurar el sistema requiere de personal altamente competente y con sueldo acorde.
### SQL SERVER 
#### Ventajas
Sistema propietario de Microsoft con el consiguiente soporte. Interfaz gráfica intuitiva, acceso a numerosos scripts prefabricados, escalabilidad atractiva para empresas pequeñas.

#### Inconvenientes
Precio para opciones avanzadas, problemas de retrocompatibilidad, alto consumo de memoria.

### MYSQL 
#### Ventajas
Versión gratuita muy completa. Fácil de instalar. Buen rendimiento en diferentes tamaños de bases de datos salvo las más pesadas. Multiplataforma. Soportado en contenedor docker. 
#### Inconvenientes
El rendimiento decae rápidamente en bases de datos muy grandes.
### POSTGRESQL 
#### Ventajas
Open Source. Flexibilidad de programación, muy personalizable si se tienen conocimientos. Dispone de una interfaz de programación con la que se puede integrar su aplicación con terceros.

#### Inconvenientes
Interfaz muy particular. Requiere trabajo de personalización para maximizar el rendimiento, por defecto tiene menor rendimiento que MySQL por ejemplo.
### MONGODB 
#### Ventajas
- Indexación y replicación
- Balanceo de carga
- Almacenamiento en ficheros
- Consultas ad hoc (Permiten incluir variables, de tal forma que la misma operación puede dar resultados diferentes)
- Escalabilidad horizontal (Funciona bien con varios servidores actuando como un todo)
- Open Source
- Gran agilidad con bases de datos pequeñas

#### Inconvenientes

MongoDB no es un SGBD adecuado para realizar transacciones complejas.

------------


## Actividad 2: Actividad instalacion MYSQL

### Instalando MySQL en docker
#### Lanzando contenedor con persistencia de datos
```bash
docker run -d --name mysql -e MYSQL_ROOT_PASSWORD=root -p 3306:3306 -v /home/asgbd/mysql_data:/var/lib/mysql mysql:8.0.22
```
##### ¿Y qué significa todo esto?
```bash
-d --name -e -p -v 
```
#### Usar docker como usuario. La variable coge nuestro usuario actual.
```bash
sudo usermod -aG docker $USER
```

#### Algunos comandos útiles
`sudo systemctl status docker` Comprueba que docker este activo.
`sudo systemctl start docker` Arranca docker.
`sudo systemctl stop docker` Detiene docker.
`sudo systemctl restart docker` Arranca docker.
`docker ps -a` Muestra los contenedores. -a muestra los ocultos.
`docker start nombre_contenedor` Arranca el contenedor.
`docker stop nombre_contenedor` Detiene el contenedor.
`docker restart nombre_contenedor`Reinicia el contenedor.

### Instalando MySQL Workbench
#### Bajamos desde el repositorio.
`wget https://dev.mysql.com/get/mysql-apt-config_0.8.15-1_all.deb`
#### Instalamos lo descargado. Ya tenemos la configuración preparada
`sudo apt install ./mysql-apt-config_0.8.15-1_all.deb`
#### Ahora sí, instalamos MySQL Workbench
`sudo apt install mysql-workbench-community.`
#### Para hacer nuestras tareas, nos aseguramos de que poder ver las tablas ocultas.
![Tablas](https://i.imgur.com/ZUfCPKd.png "Tablas")
#### Referencias:
https://www.how2shout.com/how-to/how-to-install-mysql-workbench-on-ubuntu-20-04-lts.html

------------

## Actividad 3: Actividad configuración MYSQL

### 1. El fichero de configuración

### 2. Variables del servidor

### 3. Variables de estado

### 4. Variables dinámicas

### 5. Parámetros de configuración comunes

### 6. my-large

### 7. Modificando la configuración





------------


## Actividad 4: Actividad ficheros logs


------------