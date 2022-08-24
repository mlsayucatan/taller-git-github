# Crea un repositorio utilizando Git Bash

## Carpeta del repositorio
Crea una carpeta con el nombre de tu nuevo repositorio. Da clic izquierdo y selecciona la opcion *Git Bash Here*.

![Carpeta del repositorio](1)

Al abrir la terminal, asegurate de estar en la dirección correcta.
![Dirección de la carpeta](2)

## Configuración incial de tu entorno de trabajo
El historial de versionas nos ayuda a conocer todos los cambios que se han realizado en la historia del código, por ello, es muy importante hacer esta configuración inicial para llevar un seguimiento de quién y cuándo ha hecho modificaciones.
```bash
git config --global user.name TuNombre

git config --global user.email TuCorreo
```
Si deseas comprobar que la configuración inicial se realizó correctamente, utiliza el comando
```bash
git config --list
```
Al final de la salida, debes poder observar el nombre y correo que ingresaste.
![Salida git config --list](3)

**Nota:** Si tu terminal se ve de esta manera, presiona **"q"** para salir.
![Caso opcional config --list](4)

## Crear un repositorio local
Una vez hecha la configuración inicial, ya puedas crear tu repositorio.
```bash
git init
```
Al ejercutar el comando, observarás en la terminal el mensaje "Initialized empty Git repository in [Dirección de la carpeta]". También podrás observar que se agregó la palabra **Main** o **Master**.
![Main](5)

## Realizar modificaciones
En la carpeta de tu repositorio, crea dos nuevos archivos de texto. Después, escribe en la terminal lo siguiente.
```bash
git status
```
El comando ```git status``` nos permite conocer si existen archivos recién agregados o modificados, a los que aún no se les ha hecho **commit**. En este caso te aparecerá en rojo los archivo de texto recién añadidos.

![git status con cambios](6)

Para enviar los nuevos cambios al [staging area](https://stackoverflow.com/questions/49228209/whats-the-use-of-the-staging-area-in-git), utilizaremos
```bash
# Envía un archivo a la vez
git add archivo.extensión
# Envía todos los archivos modificados
git add -A
```
Si nuevamente ejecutamos ```git status```, observaremos que el nombre de los archivos estan en color verde.

![git status sin cambios](7)

## Eliminar un cambio
Si por error añadimos o necesitamos modificar un archivo que ya se encuentra en el *staging area*, podemos utilizar el siguiente comando para removerlo.
```bash
git rm --cached archivo.extensión
```
![Archivo removido](8)

Si deseamos comprobar que el archivo se eliminó del *staging area*, utilizamos nuevamente ```git status```. Deberá aparecer en rojo los archivos eliminados.
![Comprobación archivo removido](9)

## Enviar commit
Una vez añadidos los archivos y si no hay más modificaciones pendientes, es momento de enviarlos al repositorio local.
```bash
git commit -m "Descipción"
```
![Primer commit](10)

**Nota:** Si deseamos conocer todos los commits que se han realizado en el programa, utilizamos ```git log```.

## Sube tu repositorio a GitHub
Hasta el momento solo hemos trabajado con nuestro proyecto de manera local, sin embargo, si deseamos que otras personas también trabajen en nuestro programa o si queremos contribuir en el trabajo de otras personas, es importante subir nuestras aportaciones a GitHub.

Para subir este trabajo, es necesario crear un repositorio en [GitHub](https://github.com).
![Repo en GitHub](11)

Una vez creado nos dirigiremos a la sección *…or push an existing repository from the command line*, y ejecutaremos los tres comandos que allí aparecen.
```bash
git remote add origin https://github.com/tu-usuario/tu-repositorio.git
git branch -M main
git push -u origin main
```
Si al momento de crear tu repositorio, seleccionaste la opción de añadir archivo *README.md*, la vista será diferente.
![Repo con readme](12)

Sin embargo, el procedimiento es el mismo. Solamente necesitaras la URL de tu repositorio. Ésta la encontrarás en el recuadro verde con el texto *"Code"*.
![Code](13)

Una vez enviado tu repositorio local, vuelve a cargar la página de tu repositorio en GitHub y deberás observar que se añadieron nuevos archivos.
![Resultado final](14)

---
**Última actualización:** Agosto, 24.