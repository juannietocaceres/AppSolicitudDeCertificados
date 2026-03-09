Solicitud de Certificados – UCC

Link del video explicativo: https://1drv.ms/v/c/8c46739721634d86/IQCWcWlT6ZO_R6IDHg5ZwIVMAXrE1Ran6qx30si9EVCvbtA?e=RReRCM

Aplicación móvil desarrollada en Android Studio (Java) para la gestión de solicitudes de certificados académicos en la Universidad Cooperativa de Colombia (UCC).

La aplicación permite a un estudiante ingresar sus datos, seleccionar certificados académicos, visualizar un resumen de la solicitud y finalmente generar un comprobante que puede ser compartido.

Integrante

Juan Diego Nieto Cáceres

Objetivo del proyecto

Desarrollar una aplicación Android que permita a un estudiante solicitar certificados académicos mediante una interfaz sencilla que incluya:

Registro de datos personales

Selección de programa académico

Selección de modalidad

Selección de certificados

Visualización de un resumen

Confirmación y generación de comprobante

Activities del proyecto

La aplicación está compuesta por tres Activities.

MainActivity

Pantalla principal donde el usuario ingresa la información.

Funciones:

Captura de datos del estudiante

Selección de certificados

Validación del formulario

Cálculo del costo total

Envío de información al resumen

SummaryActivity

Muestra un resumen completo de la solicitud antes de confirmarla.

Funciones:

Mostrar datos ingresados

Mostrar certificados seleccionados

Mostrar si el trámite es urgente

Mostrar el costo total

Permitir editar la solicitud

Confirmar solicitud

SubmitActivity

Pantalla final donde se muestra el comprobante de solicitud.

Funciones:

Mostrar resumen final

Permitir compartir la solicitud mediante Intent ACTION_SEND

Claves utilizadas en los Intent (Extras)

Para enviar información entre Activities se utilizaron las siguientes constantes:

EXTRA_ID
EXTRA_NOMBRE
EXTRA_PROGRAMA
EXTRA_MODALIDAD
EXTRA_CERTIFICADOS
EXTRA_URGENTE
EXTRA_COSTO_TOTAL

Tipos de datos utilizados:

Clave	Tipo
EXTRA_ID	String
EXTRA_NOMBRE	String
EXTRA_PROGRAMA	String
EXTRA_MODALIDAD	String
EXTRA_CERTIFICADOS	ArrayList
EXTRA_URGENTE	boolean
EXTRA_COSTO_TOTAL	int
Componentes de interfaz utilizados

En la aplicación se utilizaron los siguientes componentes de Android.

Entrada de datos:

EditText → Código estudiantil

EditText → Nombre completo

Selección de opciones:

Spinner → Programa académico

RadioGroup

RadioButton → Modalidad (Presencial / Virtual)

Selección múltiple:

CheckBox

Constancia de estudio

Notas

Paz y salvo

Matrícula

Promedio acumulado

Otros componentes:

Switch → Trámite urgente

Button

Ver resumen

Editar

Confirmar

Compartir solicitud

TextView → Mostrar resumen

ImageView → Mostrar iconos según modalidad o urgencia

Validaciones implementadas

Se implementaron validaciones para garantizar que la información ingresada sea correcta.

El código estudiantil no puede estar vacío.

El nombre no puede estar vacío.

Debe seleccionarse un programa académico.

Debe seleccionarse una modalidad.

Debe seleccionarse al menos un certificado.

En caso de error se muestra un mensaje utilizando:

Toast.makeText()
Cálculo del costo de certificados

Se implementó un sistema de cálculo automático del costo de la solicitud.

Reglas utilizadas:

Cada certificado cuesta $30.000 COP.

Si el trámite es urgente, se agregan $10.000 COP adicionales.

Ejemplo:

Certificados	Urgente	Costo
2	No	$60.000
2	Sí	$70.000
5	Sí	$160.000

El costo total se envía entre Activities mediante la clave:

EXTRA_COSTO_TOTAL
Extensiones implementadas

Se añadieron mejoras visuales y funcionales adicionales.

Fondo personalizado:
Se implementó un fondo con imagen de la Universidad Cooperativa de Colombia oscurecida mediante un overlay.

Interfaz mejorada:
Se modificó el color del texto para mejorar la visibilidad sobre el fondo.

Cálculo automático del costo:
El sistema calcula automáticamente el costo según los certificados seleccionados y si el trámite es urgente.

Compartir comprobante:
El usuario puede compartir el comprobante de solicitud mediante aplicaciones como WhatsApp, correo electrónico o mensajería, utilizando Intent.ACTION_SEND.

Tecnologías utilizadas

Android Studio

Java

XML (Layouts Android)

Intents

Material Components

Video demostración

El video muestra:

Validaciones del formulario

Selección de certificados

Visualización del resumen

Confirmación de solicitud

Compartir comprobante

Duración máxima: 2 minutos.

Conclusión

La aplicación cumple con los requerimientos del taller, implementando navegación entre Activities, validaciones de datos, transferencia de información mediante Intents y mejoras visuales para ofrecer una experiencia de usuario clara y funcional.