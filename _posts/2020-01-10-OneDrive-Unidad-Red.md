---
layout: post
title:  "Conectandonos a OneDrive usando unidades de red de Windows"
author: Luis A. Mass Noriega
date:   2015-08-11 14:32:55 -0500
categories: tutoriales
---
`Dificultad: Principiante`

## Cuentame un poco

Hoy en día una de los servicios de almacenamiento en la nube más populares es OneDrive. La plataforma de almacenamiento en línea por excelencia de Microsoft además de tener una compatibilidad sin precedentes con la suite de Microsoft Office tanto en su version de escritorio como su contraparte web.

En adición a lo anterior, una de las caracteristicas mas fuertes de OneDrive consiste en poder acceder y modificar los archivos de OneDrive sin necesidad la aplicación propiamente. Esto se logra mediante el uso de las unidades de red de Windows. Las unidades de red de Windows fueron diseñadas originalmente para obtener acceso a los recursos de información de una empresa o escuela sin necesidad de descargar fisicamente los archivos y en consecuencia ahorrar espacio en nuestro propio disco. Sin embargo eso no implica que no podamos convencer al Sistema de conectarnos a nuestros archivos *personales* como si se tratara de una empresa.

## Mucha charla, quiero ver la acción…

Antes de empezar, debemos entender que cada una de nuestras cuentas en OneDrive poseen una identificación que mas adelante es vital para asegurar la conectividad, normalmente este **id** viene como parametro de una **url** de OneDrive. Te mostramos:

<https://onedrive.live.com/>**id**=``B893A222D27A4720``%***215602***&**cid**=`B893A222D27A4720`

Aquí en un ejemplo diferenciamos dos partes:

- **ID**: En esta parte encontramos el id del propietario de la cuenta (Sombreado) mas el id de la carpeta a la que se navega en un momento dado(negrita en cursiva), estos separados por el símbolo porcentaje (%).
- **CID**: Representa el id del propietario de la cuenta (Sombreado).

He aquí el proceso:

01. Obtenemos el _id_ de nuestra cuenta: Para ello navega a cualquier carpeta en onedrive en la web y extrae el **CID** como mostramos anteriormente. En este caso usaremos: **B893A222D27A4720**

02. Ahora, navega a la sección Equipo (Windows 7/8.1) o Este Equipo (Windows 10). Ubica el boton de unidad de red. (Destacado en rojo)

    ![Network Button](../../../../../docs/assets/OneDrive_UnidadRed/network-button.png)

03. Presiona este boton. Aparecera un cuadro de dialogo. En este cuadro de dialogo, destacamos las siguientes opciones:

    ![Basic](../../../../../docs/assets/OneDrive_UnidadRed/drive-options.png)

    - ***Letra de unidad***: Puedes elegir la que desees, mientras no sea una letra reservada del Sistema, como **A:/** que normalmente se usa para unidades _Floppy_.

    - ***Opciones de conexión***: Podemos especificar que la unidad este disponible tan pronto iniciemos sesión en Windows o si deseamos usar otras credenciales. Para usuarios de Windows 7 esta opcion, es ***requerida***. en el caso de Windows 8.x/10, no lo será siempre y cuando se use una cuenta de Microsoft para iniciar sesión en Windows y esta cuenta **coincida** con aquella que se agrega en este tutorial. Dentro de otras consideraciones, si tienes activa la _verificación de dos pasos_. Deberás obtener una contraseña de aplicación aquí: [account.live.com/proofs](https://account.live.com/proofs)
    - ***Dirección de servidor***: Aquí colocaremos la ruta de la unidad de red de nuestro OneDrive de la siguiente forma: <https://d.docs.live.net/>`NuestroID`. En este caso quedaría así: <https://d.docs.live.net/>**B893A222D27A472**

04. Una vez hecho esto presionamos **Finalizar**. Dependiendo de las opciones seleccionadas en el literal 2 del item anterior podría aparecer un Segundo cuadro de dialogo solicitando nuestras **credenciales** de **inicio de sesión** en OneDrive.

05. Eso es todo. Tenemos nuestro OneDrive como una unidad de disco de red *(tal como se supone que es en la vida real)* y podemos accede a nuestros archivos de igual forma que en las aplicaciones.

### Consideraciones finales

Hemos conectado exitosamente nuestro OneDrive como una unidad de red. En consecuencia podemos hacer cualquier tipo de operación de archivos con sus contenidos. Sin embargo, al no estar los archivos fisicamente disponibles, algunas de las operaciones como mover, y copiar, pueden resultar en gastos considerables en banda ancha y tiempo en ver los cambios reflejados en la web.
