# Arquitectura de Software - Laboratorio 1 
## Hablemos de MAVEN  
![image](https://github.com/user-attachments/assets/b9c07ede-af78-4df8-b351-3ab0a21c4d4a)

### ¿Qué es MAVEN?  
**Maven** es una **herramienta de automatización de compilación** y gestión de proyectos, especialmente usada en proyectos Java.  
Apache **Maven** es un sistema que ayuda a:

- Compilar código fuente
- Ejecutar pruebas automáticas
- Empaquetar aplicaciones (.jar, .war)
- Administrar dependencias externas
- Generar documentación
- Automatizar despliegues
### ¿Para qué sirve Maven?
#### 1. Gestión de dependencias
Maven descarga automáticamente librerías externas desde un repositorio central.  
#### 2. Estandarización del proyecto  
Estructura típica de un proyecto Maven  
![image](https://github.com/user-attachments/assets/d807bf56-5a25-4f2d-83e2-704c5703b0ce)  
#### 3. Automatización de tareas comunes  
Comandos útiles:  
![image](https://github.com/user-attachments/assets/3dfa67b6-7147-401f-93d1-ec6ac437b18b)  
#### 4. Ideal para integración continua (CI/CD)  
Funciona bien con herramientas como Jenkins, GitHub Actions, etc.  
#### 5. Gestión del ciclo de vida del proyecto  
Incluye fases como:  
- Validación  
- Compilación  
- Test  
- Empaquetado  
- Instalación  
- Despliegue  
### Algunas ventajas de usar Maven  
- Manejo automático de dependencias  
- Estandarización de proyectos  
- Automatización de tareas  
- Integración con herramientas de desarrollo y CI/CD  
- Comunidad activa y muchos recursos  
## Hablemos de GitHub  
![image](https://github.com/user-attachments/assets/9d6e4853-bb47-45fb-87d3-5c718f5ec8f6)

### ¿Qué es GitHub?

**GitHub** es una plataforma de desarrollo colaborativo basada en la web, que permite almacenar, gestionar y controlar versiones de proyectos de software utilizando **Git**.  
GitHub combina el sistema de control de versiones **Git** con una interfaz web para:

- Alojar código fuente
- Gestionar cambios en los archivos
- Colaborar entre múltiples desarrolladores
- Automatizar flujos de trabajo con CI/CD

### ¿Para qué sirve GitHub?

#### 1. Control de versiones

GitHub permite llevar un historial completo de los cambios en un proyecto, lo que facilita:

- Volver a versiones anteriores
- Comparar modificaciones
- Rastrear errores


#### 2. Trabajo colaborativo

Funciona muy bien para equipos de desarrollo. Puedes:

- Crear ramas (`branches`) para desarrollar nuevas funcionalidades sin afectar el código principal
- Hacer revisiones de código (`pull requests`)
- Comentar y aprobar cambios entre colaboradores


#### 3. Gestión de proyectos

GitHub incluye herramientas para organizar el trabajo:

- Issues (problemas o tareas)
- Proyectos (tableros tipo Kanban)
- Wiki (documentación del proyecto)


#### 4. Automatización (CI/CD)

Con **GitHub Actions**, puedes automatizar tareas como:

- Compilar y testear tu código al hacer un push
- Desplegar aplicaciones automáticamente
- Ejecutar scripts y flujos personalizados

#### 5. Portafolio y comunidad

GitHub también sirve como:

- Portafolio para mostrar tus proyectos personales
- Medio para contribuir a proyectos de código abierto
- Plataforma para seguir desarrolladores o proyectos interesantes


### ¿Qué contiene un repositorio GitHub?

Un repositorio puede incluir:

- Archivos de código (`.java`, `.py`, `.js`, etc.)
- `README.md`: documento principal con la descripción del proyecto
- `LICENSE`: licencia del proyecto
- `.gitignore`: define qué archivos no se deben subir
- Carpetas organizadas por módulos, pruebas, documentación, etc.


### Ventajas de usar GitHub

- Gratuito para proyectos públicos y privados
- Colaboración en tiempo real
- Historial de cambios confiable
- Integración con IDEs, servicios de CI/CD, y más
- Comunidad activa de desarrolladores


## Empecemos con el laboratorio  
En este laboratorio se recordará todo lo relacionado con maven y GitHub, tanto la creación de archivos y proyectos como la ejecución de estos y el manejo en el repositorio de GitHub.  

Lo primero será crear la carpeta en local la cual será la que conectamos con GitHub, y configuraremos el usuario y el correo para que al hacer un commit se sepa quién lo hizo, usaremos los comandos user.name y user.email  
![image](https://github.com/user-attachments/assets/8fd75c5f-396f-447a-9716-e0cd863505e3)  
Luego debemos crear el proyecto con el comando dado en el laboratorio, esto nos creará la carpeta mi-primera-app con las carpetas necesarias para maven, acto seguido debemos ver el árbol creado en la carpeta, pero para poder ver el archivo pom, debemos ejecutar "tree /F".  
![image](https://github.com/user-attachments/assets/f00ae657-d1f2-47a3-95d2-3baa0ec43349)  
Ahora ingresamos al archivo App.java y verificamos lo que aparece en el laboratorio.  
![image](https://github.com/user-attachments/assets/0f38b92e-6a91-47b2-8291-eabb0bdbae4a)  
Seguido de esto ejecutamos mvn package para empaquetar el proyecto  
![image](https://github.com/user-attachments/assets/69d8b51d-430f-40d2-aedc-a07bdc3ff295)  
Procedemos a ejecutarlo, dando como resultado.  
![image](https://github.com/user-attachments/assets/18b15ce3-84e8-43c2-afc0-f68fdbd363a2)  
Ahora es importante agregar el plugin de javadoc, para esto se modifica el pom de la siguiente manera.  
![image](https://github.com/user-attachments/assets/4eb759b5-b21e-4570-91ee-8b14df739139)  
Contamos con varios comandos que sirven para generar el javadoc, estos son.  
![image](https://github.com/user-attachments/assets/67ab8624-1b16-4e68-81a0-d242c4cca631)  
Esto nos permite crear los javadoc y empaquetarlos con el .jar  
Para cada arquitectura, se deben definir mínimo los siguientes parámetros.  
![image](https://github.com/user-attachments/assets/979669fb-1069-4bb4-938d-7370d505675e)  
Por ejemplo en nuestro pom.  
![image](https://github.com/user-attachments/assets/a56473ca-e0ee-4c5e-b8ad-ef9ae7816c6f)  
Recordemos que Maven primero busca en su directorio local y luego en su repositorio remoto para obtener las dependencias y la mayoría de librerías open source están disponibles en el repositorio por defecto, hay que saber las coordenadas de la librería en le repositorio.  

Algunos comandos útiles de GitHub son: 
- git init (Inicializa la carpeta para que sepa que se usará con GitHub)
- git add . (Agrega los cambios que se realizaron en los archivos)
- git commit -m "(mensaje)" (Deja un mensaje junto con los cambios)
- git push (Envía cambios locales a repositorio remoto)
- git pull (Trae el repositorio remoto al repositorio local)
- git clone <(URL del repositorio)> (Clona un repositorio remoto en una carpeta local)

Aparte, creamos el README.txt, el .gitignore (Le agregamos la carpeta target para que la ignore) y la licencia dada en el laboratorio. Para subir los cambios y que quede guardado en el repositorio, usamos.  
![image](https://github.com/user-attachments/assets/99088bb7-cf31-4f11-ae0e-73347ffdcb18)  
Desde la línea de comandos.  
Al trabajar con Maven no es necesario crear la carpeta src, pero de tener que hacerlo, usamos el comando.  
![image](https://github.com/user-attachments/assets/d1400dae-d4f6-4d9c-acb7-af2c02ba6b7a)  

Hasta acá el informe.
# GRACIAS
