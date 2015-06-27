# Fundamentos de Git

[![Join the chat at https://gitter.im/csluesocc/taller-git](https://badges.gitter.im/Join%20Chat.svg)](https://gitter.im/csluesocc/taller-git?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)

## ¿Qué es Git?
Git es un software de control de versiones, diseñado por Linus Torvalds; pensado en la eficacia y la confiabilidad de que tiene para el mantenimiento de versiones de los proyectos en que se implementa esta herramienta.

## ¿Qué es Control de Versiones?
Es un sistema que permite registrar los cambios efectuados en un archivo o conjunto de archivos a lo largo del tiempo, para obtener una versión específica mas adelante.

### Ventajas
* Permite revertir archivos a un estado anterior.
* Permite comparar cambios a lo largo del tiempo.
* Si pierdes archivos, tienes la posibilidad de recuperarlos.
* Muestra quien modificó algo, cuando lo hizo y en que archivo.

### Desventajas
* Puede estresarte un poco cuando ocurre un error.
* En ocasiones es difícil trabajar con un solo archivo.

## Funcionamiento de Git

* **Cambios en los archivos**

Git guarda instantáneas y no una copia del archivo cuando éste es modificado y confirmado.

* **Casi cualquier operacion es local**

La mayoría de las operaciones sólo necesitan rchivos y recursos locales para operar.

* **Git tiene integridad**

Queriendo decir que todo en Git es verificado por una suma de comprobación antes de ser almacenado, esto significa que sería imposible hacer alguna modificación sin que Git se de cuenta.

* **Los tres estados**

Git maneja tres estados de archivos:

1. **Modificado:** Como su nombre lo dice, es cuando se le ha hecho alguna modificación y esta en el area de trabajo.
2. **Preparado:** Es cuando se ha agregado al área de preparación, para luego ser confirmado mediante un commit.
3. **Confirmado:** En este estado el archivo ya se encuentra guardado en la base de datos del repositorio.

## Instalación de Git

* **Para Debian, Ubuntu y derivados:**
```bash
$ sudo apt-get install git
```
* **Para Fedora, RedHat y derivados:**
```bash
$ sudo yum install git-core
```
* **Para ArchLinux y derivados:**
```bash
$ sudo pacman -S git
```

## Comandos de Git

```bash
$ git config --global user.name "CSHL"                  #Nombre de usuario
$ git config --global user.email hello@cshluesocc.org   #Email del usuario

$ git init                                              #Iniciar un proyecto
$ git clone https://url-del-repo                        #Clonar un repositorio

$ git status                                            #Ver el estado actual del repositorio
$ git add "archivo"                                     #Agregar un archivo a la zona de preparación
$ git reset "archivo"                                   #Quitar un archivo de la zona de preparación pero conservando sus cambios
$ git checkout -- "archivo"                             #Deshacer los cambios realizados a un archivo

$ git branch                                            #Listar las ramas del repositorio
$ git branch "nombre-rama"                              #Crear una rama
$ git checkout "nombre-rama"                            #Cambiar a la rama especificada
$ git checkout -b "nombre-rama"                         #Crear una rama y cambiar a esta
$ git merge "rama"                                      #Combinar ramas
$ git branch -d "nombre-rama"                           #Borrar una rama localmente
$ git push origin :nombre-rama                          #Borrar una rama de un repositorio remoto

$ git rm "archivo"                                      #Remover un archivo del proyecto
$ git mv "archivo" "archivo-renombrado"                 #Renombrar un archivo
$ git rm --cached "archivo"                             #Remover un archivo de git, pero conservandolo localmente

$ git log                                               #Mostrar el historial de commit
$ git commit -m "mensaje" -a                            #Hacer un commit
$ git reset "commit"                                    #Volver a un commit especifico
$ git reset --hard "commit"                             #Regresar a un commit especifico y borrar toda su historia
$ git fetch                                             #Obtener los cambios del proyecto
$ git pull "alias" "rama"                               #Combinar los cambios del proyecto
$ git push "alias" "rama"                               #Hacer cambios en el proyecto
```

* **Git Extras**

Comandos extras para git.

Repo del proyecto: https://github.com/tj/git-extras
Instalacion en GNU/Linux:
```bash

$ curl -sSL http://git.io/git-extras-setup | sudo bash /dev/stdin

```

## Participantes
