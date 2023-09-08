# Laboratorio No. 7 - Networking, Background Processes & PID

#### Instrucciones:
Siga paso a paso los comandos en este documento y grabe un video de su servidor mientras realiza el laboratorio, suba su video a Youtube y entregue el link vía GES


### Background processes

1. Cree un nuevo archivo con el editor nano: ```nano file1.txt```
2. Para dejar el proceso de nano en segundo plano utilice ctrl+z. ¿puede ver el output que le despliega la consola?
3. Confirme que la instancia de nano que acaba de crear sigue corriendo en su servidor con el siguiente comando ```ps au | grep nano```
4. Cree otro archivo llamado ```file2.txt```
5. Corra el comando ```jobs``` y verifique los procesos que tiene actualmente en segundo plano en su servidor
6. Use el comando ```fg``` para regresar al proceso más reciente enviado a segundo plano.

### Networking

1. Corra el siguiente comando y ubique su dirección IP, su máscara de red y la interfaz de red: ```ip address show```
2. Corra el comando ```ip route show``` para poder ver la tabla de ruteo.
3. Con el comando ```netstat -r``` puede ver también información de la tabla de ruteo del Kernel. Corra el comando y compare el output con el comando del inciso anterior.
4. Corra el comando ```ip -6 address show``` para ver la información Ipv6 de su dispositivo.
5. Despliegue la dirección IP de cualquier nombre de dominio con el comando ```host www.example.com``` Usted puede ingresar cualquier página que desee. Este comando puede utilizarse también ingresando la ip para saber el nombre de dominio.
6. Corra el comando ```traceroute google.com``` y preste atención a la información que despliega el comando.

    Si no lo tiene instalado, puede descargarlo con el siguiente comando: ```sudo apt-get install inetutils-traceroute```

    Corra ahora el comando ```sudo traceroute -I google.com``` Este comando es para enviar paquetes ICMP en lugar de paquetes UDP
7. Corra el comando ```tracepath google.com``` y compare el output con el comando ```traceroute```
8. Corra el comando ```netstat -p``` para ver información relevante de todos los puertos de su servidor


    Corra el comando ```netstat -l``` para desplegar todos los puertos activos en su servidor.

    Corra el comando ```netstat -at``` para enlistar todos los puertos TCP

    Corra el comando ```netstat -au``` para enlistar todos los puertos UDP
  
    Corra el comando ```netstat -s``` para enlistar estadisticas por protocolos.
   
Nota: Puede ir alternando las banderas para ver más información de sus puertos, por ejemplo si quisiera ver todos los puertos TCP activos use el comando ```netstat -lt``` Para obtener más información del comando netstat puede utilizar el comando ```man```.


### PID

1. Corra el comando ```ps``` para enlistar los procesos que se encuentran actualmente corriendo en el equipo y su PID
2. Para saber el pid de vim corra el comando ```pidof vim```
3. Corra el comando ```ps aux``` para enlistar todos los procesos del sistema
4. corra el comando ```top``` en su consola e investigue cual es la diferencia principal entre “ps” y “top”
5. corra el comando ```htop``` y explore que información puede ver con este comando. Presione F1 para ver más ayuda de lo que visualiza el comando
6. con cualquiera de estos comandos busque cual es el PID de apache y guardelo en un archivo llamado ```pidapache.txt```
