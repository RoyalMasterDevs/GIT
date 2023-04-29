# Una vez creaste el repositorio en GITHUB Copia el codigo SSH, esto va a darle a tu equipo la direccion a donde apuntara el proyecto en github.

### git remote add origin "aqui va el enlace de ssh de github que copiaste"

## Secuencia de inicio para todo proyecto desde consola  

### git init

#### Inicializa git en tu proyecto

### git branch master -M main 

#### cambia el nombre de la rama de master a main, importante en github

### git add .

#### agrega todos los cambios a la etapa de working directory en git

### git commit "primer commit"

#### Agrega la descripcion de los cambios y coloca los archivos en la staging area

#### estos ultimos dos puedes sustituirlos con git commit -am "Texto del commit"

### git push --set-upstream origin main

#### Establece la rama a donde se enviaran los archivos, este comando solo se hace la primera vez que haces un push. En la siguiente vez que subas algun cambio solo basta que hagas 

### git push

# Algunos comandos adicionales que debes conocer

## Regresar Cambios

### git reset --soft "numero de commit"

#### Revierte los cambios al commit dado a la estapa stage, para poder seguir editando.

### git reset --hard "numero de commit"

#### Revierte los cambios al commit dado eliminando todos los cambios commiteados a partir del numero de commit dado.

#### Tanto git reset --hard como --soft se aplican antes de mandar al repositorio remoto los cambios (git push).

#### Para revertir cambios una vez se enviaron al repositorio remoto (se hizo un push) se usa git revert

### git revert "numero de commit"

#### Realiza "commit" revertido, es decir nos regresa a un punto anterior en la rama pero conservando los cambios realizados. 



# COMBINAR RAMAS
#### Las diferentes formas de combinar tus ramas de desarrollo en la rama principal. Supongamos que tienes una rama principal llamada "main" y una rama que estas desarrollando tu, que llamaremos "feature".

### git merge

#### combina tu rama "feature" y la rama principal "main" del proyecto, conservando el arbol completo del proceso, es decir todas las ramas las puedes ver si haces --git-log-oneline

![image info](./Screenshot%20from%202023-04-28%2018-36-17.png)

### git squash

#### Combina tu rama "feature" y la rama principal "main" del proyecto, de una manera mas "destructiva" no dejando rastro del proyecto y haciendo que la nueva rama principal pierda el historial, al hacer un squash el ultimo commit que hagas sera tu nuevo HEAD en la rama "main".

![image info2](./Screenshot%20from%202023-04-28%2018-41-00.png)

### git rebase 

####  Combina tu rama "feature" y la rama principal "main" sin generar ramas adicionales o mezclar el codigo en un solo commit, rebase pone hasta adelante de tu rama principal los commits de la rama "feature" que vayas creando.

![image info3](./Screenshot%20from%202023-04-28%2018-47-46.png)

# INFORMACION DE RAMAS

### git log 

#### Muestra el historial del proyecto completa

### git log --oneline

#### Muestra el historial del proyecto de una forma resumida.

### git log --oneline --graph

#### Muestra un diagrama del historial del proyecto.