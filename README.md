# [![PrivateBin](https://cdn.rawgit.com/PrivateBin/assets/master/images/preview/logoSmall.png)](https://privatebin.info/)

*Current version: 1.7.4*

### ¿Qué es PrivateBin?

PrivateBin es una aplicación web que permite a las personas compartir texto o código de manera segura y privada. Es como un bloc de notas en línea, pero con una característica especial: todo lo que escribes se encripta antes de enviarse al servidor. Esto significa que ni siquiera los administradores del servidor pueden ver lo que has escrito.

### ¿Cómo funciona?

1. **Escribes tu texto**: Puedes escribir cualquier cosa, desde notas personales hasta fragmentos de código.
2. **Encriptación**: Antes de enviar tu texto al servidor, PrivateBin lo encripta en tu navegador usando un algoritmo de encriptación fuerte (AES de 256 bits).
3. **Envío al servidor**: El texto encriptado se envía al servidor.
4. **Compartir el enlace**: PrivateBin te da un enlace único que puedes compartir con otras personas. Este enlace contiene la clave de encriptación.
5. **Desencriptación**: Cuando alguien abre el enlace, el texto se desencripta en su navegador, permitiéndoles ver lo que escribiste.

### Características principales

1. **Seguridad**: Todo lo que escribes está encriptado, por lo que solo las personas con el enlace pueden verlo.
2. **Protección con contraseña**: Puedes añadir una contraseña adicional para mayor seguridad.
3. **Expiración**: Puedes configurar cuánto tiempo quieres que el texto esté disponible, desde "para siempre" hasta "borrar después de leer".
4. **Soporte de formato**: Puedes usar Markdown para formatear tu texto y también hay soporte para resaltado de sintaxis de código.
5. **Traducciones**: La aplicación puede detectar automáticamente el idioma de tu navegador y mostrar la interfaz en tu idioma.

### ¿Qué no hace?

1. **Confianza en el administrador**: Aunque el texto está encriptado, tienes que confiar en que el administrador del servidor no haya modificado el código de PrivateBin para hacer algo malicioso.
2. **Registros de acceso**: Los administradores del servidor pueden ser obligados a entregar registros de acceso a las autoridades, lo que podría revelar quién accedió a un texto específico.
3. **Seguridad del servidor**: Si el servidor es comprometido, un atacante podría modificar el código para capturar las claves de encriptación cuando alguien accede a un texto.

### Opciones adicionales

PrivateBin tiene varias opciones que puedes habilitar o deshabilitar en el archivo de configuración:

- Protección con contraseña
- Disusiones anónimas o con seudónimos
- Tiempos de expiración
- Soporte de Markdown
- Resaltado de sintaxis de código
- Soporte de subida de archivos
- Plantillas de diseño
- Traducciones automáticas
- Códigos QR para enlaces

### Resumen

PrivateBin es una herramienta muy útil para compartir texto o código de manera segura y privada. La encriptación asegura que solo las personas con el enlace puedan ver lo que has escrito, y hay muchas opciones adicionales para personalizar cómo funciona.

----

**PrivateBin** is a minimalist, open source online
[pastebin](https://en.wikipedia.org/wiki/Pastebin)
where the server has zero knowledge of pasted data.

Data is encrypted and decrypted in the browser using 256bit AES in
[Galois Counter mode](https://en.wikipedia.org/wiki/Galois/Counter_Mode).

This is a fork of ZeroBin, originally developed by
[Sébastien Sauvage](https://github.com/sebsauvage/ZeroBin). PrivateBin was
refactored to allow easier and cleaner extensions and has many additional
features. It is, however, still fully compatible to the original ZeroBin 0.19
data storage scheme. Therefore, such installations can be upgraded to PrivateBin
without losing any data.

## What PrivateBin provides

+ As a server administrator you don't have to worry if your users post content
  that is considered illegal in your country. You have plausible deniability of
  any of the pastes content. If requested or enforced, you can delete any paste
  from your system.

+ Pastebin-like system to store text documents, code samples, etc.

+ Encryption of data sent to server.

+ Possibility to set a password which is required to read the paste. It further
  protects a paste and prevents people stumbling upon your paste's link
  from being able to read it without the password.

## What it doesn't provide

- As a user you have to trust the server administrator not to inject any
  malicious code. For security, a PrivateBin installation *has to be used over*
  *HTTPS*! Otherwise you would also have to trust your internet provider, and
  any jurisdiction the traffic passes through. Additionally the instance should
  be secured by
  [HSTS](https://en.wikipedia.org/wiki/HTTP_Strict_Transport_Security). It can
  use traditional certificate authorities and/or use a
  [DNSSEC](https://en.wikipedia.org/wiki/Domain_Name_System_Security_Extensions)
  protected
  [DANE](https://en.wikipedia.org/wiki/DNS-based_Authentication_of_Named_Entities)
  record.

- The "key" used to encrypt the paste is part of the URL. If you publicly post
  the URL of a paste that is not password-protected, anyone can read it.
  Use a password if you want your paste to remain private. In that case, make
  sure to use a strong password and share it privately and end-to-end-encrypted.

- A server admin can be forced to hand over access logs to the authorities.
  PrivateBin encrypts your text and the discussion contents, but who accessed a
  paste (first) might still be disclosed via access logs.

- In case of a server breach your data is secure as it is only stored encrypted
  on the server. However, the server could be abused or the server admin could
  be legally forced into sending malicious code to their users, which logs
  the decryption key and sends it to a server when a user accesses a paste.
  Therefore, do not access any PrivateBin instance if you think it has been
  compromised. As long as no user accesses this instance with a previously
  generated URL, the content can't be decrypted.

## Options

Some features are optional and can be enabled or disabled in the [configuration
file](https://github.com/PrivateBin/PrivateBin/wiki/Configuration):

* Password protection

* Discussions, anonymous or with nicknames and IP based identicons or vizhashes

* Expiration times, including a "forever" and "burn after reading" option

* Markdown format support for HTML formatted pastes, including preview function

* Syntax highlighting for source code using prettify.js, including 4 prettify
  themes

* File upload support, image, media and PDF preview (disabled by default, size
  limit adjustable)

* Templates: By default there are bootstrap CSS, darkstrap and "classic ZeroBin"
  to choose from and it is easy to adapt these to your own websites layout or
  create your own.

* Translation system and automatic browser language detection (if enabled in
  browser)

* Language selection (disabled by default, as it uses a session cookie)

* QR code for paste URLs, to easily transfer them over to mobile devices

## Further resources

* [FAQ](https://github.com/PrivateBin/PrivateBin/wiki/FAQ)

* [Installation guide](https://github.com/PrivateBin/PrivateBin/blob/master/doc/Installation.md#installation)

* [Configuration guide](https://github.com/PrivateBin/PrivateBin/wiki/Configuration)

* [Templates](https://github.com/PrivateBin/PrivateBin/wiki/Templates)

* [Translation guide](https://github.com/PrivateBin/PrivateBin/wiki/Translation)

* [Developer guide](https://github.com/PrivateBin/PrivateBin/wiki/Development)

Run into any issues? Have ideas for further developments? Please
[report](https://github.com/PrivateBin/PrivateBin/issues) them!
