

# Instalación y Configuración de APACHE
Pasos para instalar y configurar un servidor apache en windows

## Descarga
1. Vaya al sitio oficial de **Apache [aquí](http://httpd.apache.org/)**
2. Clic en el link **["Download"](http://httpd.apache.org/download.cgi)** que le *permitirá descargar la ultima versión* estable de **Apache**
3. Clic en el link **["Files for Microsoft Windows"]**(http://httpd.apache.org/docs/current/platform/windows.html#down)
4. Seleccione uno de los sitios que cuentan con los archivos binarios para windows de **Apache** (Nosotros optamos por **[Apache Lounge]**(https://www.apachelounge.com/download/))
5. Seleccione el link con la *distribución adecuada para su computadora* (Apache version Win64 o pache version Win32)
6. **Extraiga** el archivo descargado en el *directorio raiz que se adapte a sus necesidades* (Nosotros usamos el directorio **C:/**)

## Instalación
Tenga en cuenta que debe tener instalada en su computadora ***Visual C++ Redistributable [aquí](https://support.microsoft.com/es-co/help/2977003/the-latest-supported-visual-c-downloads) o [aquí](https://www.apachelounge.com/download/)***
1. Abra una *linea de comandos como administrador*
2. Ubiquese en el directorio **C:/Apache24/bin**
3. Ejecute el comando `httpd.exe -k install -n "Apache HTTP Server"`
4. **En el navegador web** navegue a la url `localhost` para verificar que **Apache** este funcionando. Se debe ver el mensaje **It works!**

## Configuración Básica
Abra el archivo de configuración de apache **`httpd.conf`** ubicado en el directorio **`A:\Apache24\conf\httpd.conf`**, busque y modifique las siguientes configuraciones de **Apache**.
1. Indique donde está ubicado el servidor:
    Por defecto es: **`Define SRVROOT "c:/Apache24"`**
2. Indique el puerto por donde debe escuchar **Apache**
Por defecto es: **`Listen 80`**
3. Indique el email del administrador del servidor:
Por defecto es: **`ServerAdmin admin@example.com`**
4. Indique el directorio donde serán ubicadas las paginas web:
Por defecto es: *htdocs*
**`DocumentRoot "${SRVROOT}/htdocs"`**
**`<Directory "${SRVROOT}/htdocs">`**

[**Ver cómo configurar PHP**](https://github.com/bitcubico/php-install-config-win/blob/master/README.md)
