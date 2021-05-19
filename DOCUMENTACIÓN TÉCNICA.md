

DOCUMENTACIÓN TÉCNICA – PROYECTO 2

José Joab Romero Humba

Kevin Alexander Herrera Garcés

Manuela Zapata Giraldo

TÓPICOS ESPECIALES EN TELEMÁTICA

UNIVERSIDAD EAFIT

MEDELLÍN

2021-1





En el siguiente documento se presentarán los detalles del paso a paso que se realizo para el

despliegue de nuestra arquitectura de AWS.

[inserte aquí la arquitectura]

**Configuración del VPC**

Se crea una VPC con la dirección IP como se muestra a continuación

Después de esto se procede a crear las subredes de la VPC, ya que usaremos 2 zonas de

disponibilidad crearemos 4 subredes: 2 privadas y 2 públicas.

Después de esto se crea un Internet Gateway para la VPC que hemos creado

Una vez hecho lo anterior se procede a crear el grupo de seguridad de los NATs Instance de la

siguiente manera





Ahora se crearán las instancias NAT usando la imagen amzn-ami-vpc-nat-hvm-

2018.03.0.20181116-x86\_64-ebs, se creará en la VPC creada anteriormente y se usará la red

pública. Se creará una por cada zona de disponibilidad.

