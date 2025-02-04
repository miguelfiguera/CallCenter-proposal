# Propuesta de optimizacion de call-center para VictorySun:

Esta propuesta contempla dos opciones de acuerdo a las necesidades previstas y conversadas. Su objetivo principal es reducir el tiempo de marcado de los agentes y facilitar la asignación diaria de cada uno, automatizando parte del proceso y permitiendo de esta forma que los agentes y los supervisores se concentren en concretar citas.

Sumado a esto, ambas propuestas incluyen el sistema para las campañas de sms, como filtro para landlines y para convertir cold leads en hot leads en manos de los agentes con mayor índice de éxito.

## SMS Campaign system:

Una campaña de mensajes de texto, es un mensaje generado en automático que espera una respuesta precisa para filtrar personas interesadas y landlines (telefonos de casa). El resultado es que aquellos interesados pueden ser abordados de forma rápida por los agentes con mejores resultados y los landlines se anotan para ser trabajados en horarios adecuados.

Se puede hacer un barrido diario de aproximadamente 720 numeros por cada linea dedicada a sms, desde las 8 am hasta las 8pm. Esto debido a que las lineas, para evitar ser marcadas como spam, pueden enviar un total de 60 mensajes por hora, en alguno proveedores varia.

De lunes a jueves da un total de 2880 numeros semanales por linea, incluso más en algunos casos.

Dependiendo del proveedor de servicios (telnyx,twilio,zadarma,etc) el precio puede variar de $15 a $30, semanales en mensajes de texto para cubrir los 2880 mensajes.

Las respuestas de los mensajes enviados serán grabadas en una base de datos para sortear aquellas positivas y asignarlas a los agentes en tiempo real.

Ejemplo de mensaje:

"Nuestra empresa de paneles solares se está expandiendo en tu zona, deseas saber más?

Responde Si y serás contactado por uno de nuestros agentes."

### App para SMS:

Usando Ruby on Rails + React, se desarrollará una aplicación que permita al usuario encargado gestionar las lineas que se usan para los SMS, crear campañas a partir de listas de clientes en formato .csv (comma separated values) y gestionar los resultados en tiempo real, permitiendo la asignación de citas a sus mejores vendedores.

Esta app debe ser alojada en un servidor de digital ocean, que suele tener de costo un aproximado de $18 a $36.

## Opcion A - Callcenter + CRM - Open Source:

1. Open-source Asterisk PBX.
2. Requiere alojamiento en Digital Ocean
3. Tarda mas tiempo en configurar, pero reduce costos.
4. Puede integrarse a un CRM para que los datos esten en un solo lugar.
5. Existen versiones pagas con la empresa sangoma y que eliminan el tiempo de configuracion.

[Web oficial de Asterisk]

## Opcion B - Callcenter + CRM - 3cx:

1. 3cx licencia profesional que incluye el hosting ($545 anuales) / Sin hosting son $295, sin embargo el costo del hosting con otra empresa puede variar de $24 mensuales a $58 y agrega horas de configuracion.
2. Integrar con un CRM para que toda la data este cuidada en un solo lugar.
3. Existe una versión gratuita si desean probarlo primero.
4. Se pueden usar lineas existentes que tengan compradas bajo protocolos VOIP (llamas por internet) o Troncales SIP (lineas virtuales).
5. Permite usar el protocolo click2call (llamar con un click) dentro del crm escogido. Recomendado hubspot, zohocrm, sugar, vtiger.
6. Incluye operadora automatica.
7. Para las llamadas entrantes puede hacer un queue (lista de llamadas en espera).

Links de referencia:

- [Intro a 3cx](https://www.youtube.com/watch?v=cPtyu6QRWNY)
- [Ventajas de 3cx](https://www.youtube.com/watch?v=k-UXmJ-e_0c)

## Opcion C - Custom CRM:

El sistema que se hará para manejar las campañas de SMS, puede ser extendido en codigo para que funcione como CRM con funcionalidad limitada a las necesidades del callcenter.

## Precio:

### Costos variables dependiendo de la opcion:

- Lineas telnyx: desde $1 a $10
- Saldo de telnyx: a gusto del cliente.
- Version paga de 3cx $545
- Servidor de Digital Ocean para 3cx / Asterisk: $40 mensuales.
- Dominio con nombre de la empresa: victorySun.net tiene un precio que ronda los $60 por 2 años.
- Configuracion de email con dominio, ejemplo@victorysun.net: costo variable por proveedor:
  google $15 mensuales.
  Zoho varia entre gratis por menos de 5 correos y $12 al año por correo una vez superadas las licencias.

### Opciones

1. ### A:

- Honorarios: $1200

2. ### B:

- Honorarios $900

3. ### C:

- Honorarios $1200

### Tiempo estimado de desarrollo: 8 semanas.

### Que incluye el servicio:

1. Configuración del PBX.
2. Desarrollo web (de ser requerido).
3. Compra y configuración de lineas para el PBX.
4. Configuracion del CRM de su eleccion.
5. Servicio técnico.
6. Administración de servidores y bases de datos.
7. Entrenamiento del personal.
8. Configuracion del dominio para correo electrónico.
