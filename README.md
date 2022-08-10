# PruebaGt
En la línea de comandos, navega al directorio raíz de tu proyecto.

Inicializar el directorio local como un repositorio de Git.

git init -b main
Probar y confirmar todos los archivos en tu proyecto

git add . && git commit -m "initial commit"
Para crear un repositorio para tu proyecto en GitHub, utiliza el subcomando gh repo create. Cuando se te solicite, selecciona Subir un repositorio local existente a GitHub e ingresa el nombre que quieras ponerle a tu repositorio. Si quieres que tu proyecto pertenezca a una organización en vez de a tu cuenta de usuario, especifica el nombre de la organización y del proyecto con organization-name/project-name.

Sigue los mensajes interactivos. Para agregar el remoto y subir el repositorio, confirma con "Sí" cuando se te pida agregar el remoto y subir las confirmaciones a la rama actual.

Como alternativa, para saltarte todos los mensajes, proporciona la ruta del repositorio con el marcador --source y pasa un marcador de visibilidad (--public, --private o --internal). Por ejemplo, gh repo create --source=. --public. Especifica un remoto con el marcador --remote. Para subir tus confirmaciones, pasa el marcador --push. Para obtener más información sobre los argumentos posibles, consulta el manual del CLI de GitHub.

Agregar un repositorio local a GitHub utilizando Git
Crear un repositorio nuevo en GitHub.com. Para evitar errores, no inicialices el nuevo repositorio con archivos README licencia o gitingnore. Puedes agregar estos archivos después de que tu proyecto se haya subido a GitHub.
Desplegable Create New Repository (Crear nuevo repositorio)
Abre la Git Bash.
Cambiar el directorio de trabajo actual en tu proyecto local.
Inicializar el directorio local como un repositorio de Git.
$ git init -b main
Agregar los archivos a tu nuevo repositorio local. Esto representa la primera confirmación.
$ git add .
# Agrega el archivo en el repositorio local y lo presenta para la confirmación. Para deshacer un archivo, usa 'git reset HEAD YOUR-FILE'.
Confirmar los archivos que has preparado en tu repositorio local.
$ git commit -m "First commit"
# Commits the tracked changes and prepares them to be pushed to a remote repository. Para eliminar esta confirmación y modificar el archivo, usa 'git reset --soft HEAD~1' y confirma y agrega nuevamente el archivo.
En la parte superior de tu repositorio en la página de configuración rápida de GitHub.com, haz clic en  para copiar la URL del repositorio remoto.
Copiar el campo de URL de repositorio remoto
En la indicación Command (Comando), agrega la URL para el repositorio remoto donde se subirá tu repositorio local.
$ git remote add origin  <REMOTE_URL> 
# Sets the new remote
$ git remote -v
# Verifies the new remote URL
Sube los cambios en tu repositorio local a GitHub.com.
$ git push origin main
# Pushes the changes in your local repository up to the remote repository you specified as the
