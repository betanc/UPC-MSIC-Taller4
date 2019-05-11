# UPC-MSIC-Taller4
Taller 4, monitoreo con splunk a base de datos

<b> Punto 1. Instalación de Splunk: </b>

Instalación:

![splunk1](https://user-images.githubusercontent.com/48939055/57562924-49dec600-735d-11e9-8b84-a5e7a98773f9.jpg)

Inicio de Splunk:

![splunk2](https://user-images.githubusercontent.com/48939055/57562925-49dec600-735d-11e9-80ba-c251e59fb859.jpg)

Interfaz y servicio arriba:

![splunk3](https://user-images.githubusercontent.com/48939055/57562982-f0c36200-735d-11e9-8803-a68bd4461345.jpg)

Acceso por interfaz web:

![inicio de sesion](https://user-images.githubusercontent.com/50051421/57562971-cd98b280-735d-11e9-97d7-d78775280612.PNG)

Acceso a la herramienta:

![splunk4](https://user-images.githubusercontent.com/48939055/57563016-33853a00-735e-11e9-87df-eb2af1ad6faf.jpg)


<b> Punto 2. Tutorial Splunk: </b>

Se ejecutaron los puntos 1 a 4 del tutorial Splunk y se conecto y cargó a la base de datos de prueba permitiendo realizar consultas, busquedas, etc sobre lo previamente cargado:

![splunk5](https://user-images.githubusercontent.com/48939055/57570050-64e42100-73c3-11e9-9abe-9759293536b1.jpg)

![splunk6](https://user-images.githubusercontent.com/48939055/57570043-644b8a80-73c3-11e9-9d01-641dc5a980bc.jpg)

![splunk7](https://user-images.githubusercontent.com/48939055/57570044-644b8a80-73c3-11e9-9aa1-e60f1a25b54f.jpg)

Resultados de la busqueda de exploradores en el host: 74.53.23.135

![splunk8](https://user-images.githubusercontent.com/48939055/57570045-644b8a80-73c3-11e9-97a8-3bd20479290b.jpg)

![Taller4_Resultado](https://user-images.githubusercontent.com/50051518/57570099-0e2b1700-73c4-11e9-9189-20a6b3e9e7b2.PNG)

Mozilla en diferentes versiones:
![Taller4_Resultado3](https://user-images.githubusercontent.com/50051518/57570100-0e2b1700-73c4-11e9-90e0-7d94fa6a64f6.PNG)


Busqueda Especifica de User-Agents utilizados en el activo con Direccionamiento IP 74.53.23.135

Search= 74.53.23.135 | stats count by useragent

![Taller4b](https://user-images.githubusercontent.com/50051493/57571058-b8a83780-73ce-11e9-9eb2-c7d27b60dc29.PNG)


<b> Punto 3. Se incia base de datos my sql, se configura splunk cargando addon o driver de conexión según corresponde, generando alertas y graficas de acuerdo a los riesgos a monitorear: </b>

Activación de logs en la base de datos para que sean posteriormente correlacionados por splunk:

![splunk9](https://user-images.githubusercontent.com/48939055/57570046-644b8a80-73c3-11e9-99d3-31c373b140a7.jpg)

Incio del servicio mysql y la bd:

![splunk10](https://user-images.githubusercontent.com/48939055/57570047-64e42100-73c3-11e9-88e3-5447f7e9c1dd.jpg)

Base de datos "employees" importanda al motor de base de datos local el cual sera monitoreado por splunk:

![splunk11](https://user-images.githubusercontent.com/48939055/57570048-64e42100-73c3-11e9-8a9f-140834554224.jpg)

Notificación del importe exitoso de la base de datos y creación de usuario para monitoreo "splunk":

![splunk12](https://user-images.githubusercontent.com/48939055/57570049-64e42100-73c3-11e9-97fb-a871f888161e.jpg)

Asignación de privilegios al usuario "splunk":

![splunk13](https://user-images.githubusercontent.com/48939055/57572002-e8f5d300-73da-11e9-9fa3-176ef1914e7d.jpg)

![splunk14](https://user-images.githubusercontent.com/48939055/57572003-e8f5d300-73da-11e9-83eb-4638a1e594b5.jpg)

![splunk15](https://user-images.githubusercontent.com/48939055/57572004-e98e6980-73da-11e9-9591-f75963284b5b.jpg)

![splunk16](https://user-images.githubusercontent.com/48939055/57572005-e98e6980-73da-11e9-9ed3-95c702472e78.jpg)

![splunk17](https://user-images.githubusercontent.com/48939055/57572006-e98e6980-73da-11e9-8238-9ca50f524854.jpg)

![splunk18](https://user-images.githubusercontent.com/48939055/57572007-e98e6980-73da-11e9-82f7-749fafae8796.jpg)

![splunk19](https://user-images.githubusercontent.com/48939055/57572008-e98e6980-73da-11e9-83fc-ac5915a68b72.jpg)

![splunk20](https://user-images.githubusercontent.com/48939055/57572009-e98e6980-73da-11e9-8572-4f66098740fb.jpg)

![splunk21](https://user-images.githubusercontent.com/48939055/57572154-2f97fd00-73dc-11e9-88a7-e79e6d75c8cb.jpg)

![splunk22](https://user-images.githubusercontent.com/48939055/57572219-e09e9780-73dc-11e9-924e-383e80a5a5df.jpg)

![splunk23](https://user-images.githubusercontent.com/48939055/57572220-e1372e00-73dc-11e9-9c50-dfbe40c6a87c.jpg)

<b>Punto 4. Configure splunk para detectar esos 2 riesgos</b>

1. RIESGO CREACION DE USUARIOS NO AUTORIZADA

![riesgo creacion de usuarios no autorizados](https://user-images.githubusercontent.com/50051421/57572390-19d80700-73df-11e9-8f5f-bb7f9f35b526.PNG)

Gráfico de la alerta.

![riesgo creacion de usuarios no autorizados imagen](https://user-images.githubusercontent.com/50051421/57572724-45112500-73e4-11e9-94a8-797cd48fd51e.PNG)

2. RIESGO ACCESO NO AUTORIZADO

Identificación de intentos de autenticación fallidos de usuarios desconocidos , posiblemente producto de un ataque de diccionario o
un ataque de fuerza bruta.
![Taller4_Riesgo1_24](https://user-images.githubusercontent.com/50051493/57575813-9a1a5e80-7417-11e9-843c-df5671b711bb.PNG)
![Taller4_Riesgo1_26](https://user-images.githubusercontent.com/50051493/57575810-91c22380-7417-11e9-97a6-d88372af0f30.PNG)
![Taller4_Riesgo1_19](https://user-images.githubusercontent.com/50051493/57575828-f1203380-7417-11e9-99b7-f015ca7d2e5a.PNG)
![Taller4_Riesgo1_23](https://user-images.githubusercontent.com/50051493/57575836-039a6d00-7418-11e9-8b04-674c3d640649.PNG)
![Taller4_Riesgo1_21](https://user-images.githubusercontent.com/50051493/57575833-ff6e4f80-7417-11e9-9f9d-8d7d35cce53b.PNG)

![Taller4_Riesgo1_22](https://user-images.githubusercontent.com/50051493/57575837-05643080-7418-11e9-8322-a2d54276302d.PNG)
![Taller4_Riesgo1_20](https://user-images.githubusercontent.com/50051518/57574236-e1462680-73fa-11e9-8c1b-e888557c5972.PNG)
