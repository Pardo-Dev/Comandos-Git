# Comandos Git 

`git --version` ➡️ Ver version de git actual.

`git help` ➡️ Explicacion comandos.

`git help <comando>` ➡️ Encontrar mas informacion sobre un comando.


## Configuracion de usuario

`git config --global -e` ➡️ Ver datos como de usuario, alias y etc...

`git config --global user.name "<Nombre>"` ➡️ Escoger nombre del usuario

`git config --global user.email "<email>"` ➡️ Escoger email del usuario

### Más configuraciones 
`git config --global init.defaultBranch <name>` ➡️ Define la rama inicial al inicializar un repositorio.

### Repositorios
`git init` ➡️ Inicializar un repositorio en la ruta actual.

`git status` ➡️ entregra informacion sobre estado del escenario.

`git status --short` ➡️ Muesta infomacion corta de los estados de archivos. 

`git add <archivo>` ➡️ Añadir un archivo al escenario.}

`git add .` ➡️ Añadir todo al escenario.

`git add <directorio>/` ➡️ Añade todos los archivos del directorio al escenario.

`git add *.extension` ➡️ Añadir todos los archivos de cierta extension al escenario.

`git reset <archivo>` ➡️ Quitar archivos del escenario.

`git commit -m "<nombre_commit>"` ➡️ Grabar el escenario, la -m es de message.

`git log` ➡️ Entrega informacion sobre los commits(hash, head, rama, autor y fecha)

### Viajes en el tiempo
`git checkout -- .` ➡️ Reconstruye el proyecto a como estaba en el ultimo commit.

`git reset --mixed <hash>` ➡️ Vuelve a un commit y saca los archivos que no estaban en el escenario y si guarda los cambios.

`git reset --hard <hash>` ➡️ Vuelve al commit pero borra todos los cambios.



### Archivos de git
.gitkeep ➡️ Para tener algo en una carpeta y que esta se pueda subit al escenario.

### Crear alias para comandos 
`git config --global alias.<alias> "Comandos a abreviar"`

### Ver cambios en archivos
`git diff <archivo>` ➡️ Muestra los cambios hechos en un archivo.

`git diff --staged <archivo> ` ➡️ Muestra los cambios hechos en un archivo en el escenario.

### Commits
`git commit --amend -m "mensaje"` ➡️ Cambia el nombre del ultimo commit.

`git reset --soft HEAD^<N° or hash>` ➡️ No elimina los cambios pero si el commit

`git reset --hard HEAD^<N° or hash>` ➡️ Destruccion de commits

`git reflog` ➡️ Muestra todo lo realizado(commit, reset y más)(Puedes volver a commits que hayas borrado con reset uwu)

### Comandos basicos 
`git mv <nombre_archivo> <nuevo_nombre>` ➡️ Renombrar archivos.

`git rm <nombre_archivo>` ➡️ Eliminar archivos. 

### Ramas
`git branch` ➡️ Ver rama actual.

`git branch -m <rama_actual> <nuevo_nombre>` ➡️ Modificar nombre de una rama.

`git branch "nombre_rama"` ➡️ Crear ramas.

`git checkout <nombre_rama>` ➡️ Moverse a otra rama.

`git branch -d <nombre-rama>` ➡️ Borra una rama.

`git branch -d <nombre-rama> -f` ➡️ Borra una rama forzada.

`git checkout -b <nombre-rama>` ➡️ Crea una rama y te mueve a ella.

### Uniones de ramas
Merge: fast-forward
	   ort : Automatico 
    
`git merge <nombre-rama>` ➡️ Unes una rama en la rama que estes.

### Etiquetas
Hacen referencia a un commit del como estaba en ese entonces el proyecto.

`git tag <tag>` ➡️ Deja una etiqueta en un commit actual.

`git tag` ➡️ Ver tags

`git tag -d <nombre_tag>` ➡️  Elimnar una etiqueta.

`git tag -a <nombre_etiqueta> <hash> -m "mensaje"` ➡️ Añadir una etiqueta a un commit especifico.

### GIT STASH
Stash: Guardar registros en una boveda.

`git stash` ➡️ Guarda los ultimos cambios en otro lugar y deshace lo avanzado hasta el ultimo commit.

`git stash list` ➡️ Mostrar listado de  stashes

`git stash pop` ➡️ Trae los cambios que mandamos al stash y elimina el mismo stash.

`git stash clear` ➡️ Borra todos los stash

`git stash apply stash@{num}` ➡️ Recuperar un stash en especifico.

`git stash drop stash@{num}` ➡️ Borra un stash en especifico.

`git stash show stash@{num}` ➡️ Mostrar el contenido de cada stash

`git stash save "nombreStash"` ➡️ Crear un stash con nombre.

### Ignorar archivos  

.gitignore ➡️ Este archivo hace que git ignore archivos para no darle seguimiento.

carpeta/

archivo

*.extension

### Posibles errores
Errores con CRLF
`git config core.autocrlf true`

### Alias
#### Log
`git config --global alias.lg "log --graph --abbrev-commit --decorate --format=format:'%C(bold blue)%h%C(reset) - %C(bold green)(%ar)%C(reset) %C(white)%s%C(reset) %C(dim white)- %an%C(reset)%C(bold yellow)%d%C(reset)' --all"`

#### Status
`git config --global alias.s status --short`

### Estados de archivos
Letra "U" --> Untracked: Sin seguimiento.

Letra "A" --> Add: Seguido.

Letra "M" --> Modify: Modificado.

Letra "D" --> Delete: Eliminado.

Letra "R" --> Rename: Renombrado.

### Notas

- ➡️ Abreviaciones.

-- ➡️ Palabra completa.
  
--global ➡️ Se usa para aplicar configuraciones globales a nivel local.

REAME.md ➡️ Notas del desarrollador

Formato Commits
`git commit -m "archivo.ex: mensaje"`
