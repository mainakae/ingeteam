# ingeteam
Domotica con el inversor Ingeteam ISS 1Play para instalaciones solares fotovoltaicas

Mirad este video para más información:

[![Video Youtube](https://img.youtube.com/vi/6LML5U0NqVU/0.jpg)](https://www.youtube.com/watch?v=6LML5U0NqVU)

## Como aplicarlo a vuestro inversor

Previo a todo, necesitareis tener una instalación de Node-Red funcionando. Es bastante fácil, hay mucha documentación en la red. Si ya habéis instalado Home Assistant en casa, podeis instalar Node-Red directamente desde el Supervisor de HA. Si queréis instalar Home Assistant en una Raspberry Pi, [tengo un video explicando como hacerlo aquí](https://youtu.be/ZFrOirWBZqk).

1. Pon la IP de tu inversor en el nodo de configuración de conexión Modbus de los nodos *Ingeteam IRs* y *Gavazzi IRs* (haz doble click sobre estos nodos, y luego pulsa el icono del lapiz donde pone "Server")
2. Configura las salidas que desees: puedes utilizar el nodo de debug para recuperar los datos, introducir nuevos nodos de MQTT e incluso utilizar los ejemplos que he dejado de InfluxDB (tanto la versión 1 como la versión 2)

Si quereis recuperar los mapas de memoria de MODBUS actualizados desde el inversor, deberéis configurar la ip del inversor en el nodo *inverter map*, así como activar el ``Use authentication`` y rellenar los campos de ``Username`` y ``Password`` con el usuario de la aplicación web de vuestro inversor (¡no la app web de ingeconsun!). Os recomiendo crear un usuario específico para node-red en el inversor, que solo tenga permisos básicos. Lo podéis hacer desde la web del inversor (si entrais como instalador, no se si avanzado también vale) en ``Comms->Users``