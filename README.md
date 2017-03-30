# Curso Git desde cero
Sistema de control de versiones para el mantenimiento eficiente y confiable de archivos.

## Zonas de Git
1. Directorio de trabajo
2. Área de preparación
3. Directorio Git

## Flujo de trabajo básico en Git

1. Modificas una serie de archivos en tu directorio de trabajo.
2. Preparas los archivos añadiéndolos a tu área de preparación.
3. Confirmas los cambios, lo que toma los archivos tal y como están en el área de preparación y almacena esa copia instantánea de manera permanente en tu directorio de Git.

## Configurando Git por primera vez
```
git config --global user.name "Noé Ramírez"
git config --global user.email "noeramirezset@gmail.com"
git config --global core.editor sublime
git config --list
```

## Configuración SSH en windows
Usando Git Bash seguimos los siguientes pasos:
1. Creamos una carpeta llamada `llaves-ssh` en el disco `C` para evitar problemas de rutas.
2. Ejecutamos el comando `ssh-keygen -t rsa -C "micorreo@algo.com"`.
El email debe ser el mismo con el que nos registramos en Github para evitar posibles problemas.
Dejamos el passphrase vacío y damos enter.
Cuando nos pida la ruta escribimos `/c/llaves-ssh/github_rsa`.
3. Iniciamos ssh-agent en background ejecutando el comando `eval "$(ssh-agent -s)"`.
4. Agregamos la llave ssh generada a ssh-agent ejecutando el comando `ssh-add /c/llaves-ssh/github_rsa`.
5. Desde ahora podemos hacer pull y push sin que Github pida datos de acceso.