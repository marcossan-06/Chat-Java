# Chat en Java Documentado (Cliente-Servidor)

Este es un proyecto de un **chat de consola** en Java 11 que permite la comunicación entre múltiples usuarios a través de un servidor central. Los usuarios se conectan al servidor utilizando un socket y pueden mandar
y recibir mensajes en tiempo real. He tratado de documentar aclarando que hace cada bloque de código.
¡Espero que te sirve para aprender y divertirte!😁

### **IMPORTANTE**
  - El proyecto sirve para redes locales, está configurado en **localhost** por defecto. Para conectarse desde diferentes dispositivos, asegúrate de usar la dirección IP local del servidor.

    Seguramente necesitarás activar una nueva regla de entrada en el Firewall para el puerto TCP que usamos en la aplicación (51000 en mi caso).
    Para obtener la IP local del servidor tienes el comando "ipconfig" (Windows). Si estas en Linux o Mac usa "ip a" o "ifconfig".
    
    Ejemplo de regla del Firewall en Windows 10:
    
    ![image](https://github.com/user-attachments/assets/06f5a926-9301-43ac-ae53-f2b17d38cbba)
    
  - He integrado en el código soporte para emojis utilizando Unicode, pero es importante que en las terminales activas ejecutes el comando "chcp 65001" antes de ejecutar el chat,
    y que soporten Unicode, evidentemente.
    Más que nada es para que la consola se vea más atractiva con los emoticonos.

### ¿Cómo se usa?

Para usar el chat simplemente ejecuta el servidor en una terminal y se mostrará el mensaje de "Servidor iniciado...",
esto quiere decir que el servidor está escuchando constantemente los mensajes de los clientes por el puerto que le hayamos especificado.

Luego ejecuta la clase de ChatCliente en otras terminales o PCs y ya simplemente te queda escribir mensajes,
estos llegarán al PC Servidor el cuál los reenviará a todos los clientes conectados,
puedes tener más de 2 clientes comunicándose como si fuera un grupo de Whatsapp en la consola.

En el servidor simplemente se mostrará lo que va ocurriendo en terminos generales (Servidor iniciado...; Pepito se ha conectado; Pepito se ha desconectado)

Luego ya si quieres hacerlo funcionar con redes externas tendrás que configurar el mapeo de puertos en el router.

    
