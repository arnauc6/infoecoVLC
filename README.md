# **infoecoVLC**
## **Asistente virtual para información económica municipal**
![Logo chatbot Telegram](https://github.com/arnauc6/infoecoVLC/blob/master/Imagenes/infoecoVLC_%20logo.jpg)

## Descripción


El proyecto surge para intentar solventar esta distancia entre ciudadanía y administración, acercando la información disponible en los portales de los ayuntamientos al bolsillo de la ciudadanía.

El **Asistente virtual para el acceso a información económica municipal**  es capaz de ofrecer la información a la ciudadanía mediante lenguaje común. De esta forma, el usuario o usuaria contactará con el asistente virtual y realizará preguntas como: ¿cuánto dinero se invierte en mi barrio? o ¿cuál es la deuda del ayuntamiento?; a partir de ahí, el asistente responderá con la información que obtiene de las páginas Web y portales de datos abiertos del ayuntamiento (Previamente guardados en una Base de Datos). Permitiendo, de esta manera, que los usuarios y usuarias adquieran información pública de forma fácil, rápida y confiable.

El desarrollo del asistente virtual es  modular y de código abierto para facilitar que sea fácilmente ampliable o exportable a cualquier ayuntamiento. Además, se está desarrollando utilizando el diseño centrado en la ciudadanía con el objetivo de que se adapte a sus necesidades reales. La estructura de módulos y relaciones es la siguiente:

![Diagrama módulos](https://github.com/arnauc6/infoecoVLC/blob/master/Imagenes/Diagrama-modulos-V2.png
)

- [Módulo 1: Integración con Telegram.](https://github.com/arnauc6/infoecoVLC_M1.A_Integracion_Telegram.git) El presente módulo se encarga de realizar toda la gestión interna de los mensajes recibidos. Cuenta con un mecanismo que se encarga de filtrar los mensajes, dejando pasar sólo aquellos que vienen en formato texto. Además, se encarga de gestionar las respuestas a los usuarios, realizando el direccionamiento de los mensajes con los módulos de procesamiento del lenguaje natural y el gestor de diálogo, hasta que se envía la respuesta al usuario.
- [Módulo 2: Procesamiento del lenguaje natural.](https://github.com/areahackerscivics/Chatbot_M3_Agente_Inteligente) Copia del agente inteligente creado en [Dialogflow](https://dialogflow.com/) para que pueda ser replicado.
- [Módulo 3: Gestor de diálogo.](https://github.com/arnauc6/infoecoVLC_M3_Gestor_dialogo.git) Servicio web que se encarga de recibir las preguntas ya clasificadas en *Intents* y, las *Entities* ya estructuradas y ordenadas. A partir de esta información realiza una consulta a la base de datos y construye la respuesta tal como la verá el usuario. Esta respuesta es mandada al gestor de Telegram para que a su vez se lo envíe al usuario correspondiente.
- [Módulo 4: Extracción, Transformación y Carga.](https://github.com/areahackerscivics/Chatbot_M1_Extraccion_y_Almacenamiento) Conjunto de scripts y procesos ETL (Extracción, transformación y carga) para recolectar la información de los distintos formatos que ofrece el ayuntamiento y estructurarlos en un base de datos MongoDB.
Este módulo está compuesto por ETL (Extracción, Transformación y Carga) que se encarga de recolectar la información y almacenarla en la base de datos que alimenta el gestor de respuestas.





## Guía de uso

Al tratarse de un proyecto modular puedes adoptar toda la estructura, algunos módulos sueltos, crear nuevos módulos o modificar los módulos existentes. Cada módulo contendrá la información de cómo ponerlo en funcionamiento y las entradas y salidas esperadas.

## Equipo

- Autores:
  - [Arnau Campos Albuixech](https://www.linkedin.com/in/arnau-campos-albuixech-759b23138)
  - [Valeria Alexandra Haro Valle](https://about.me/valexharo) | @ValeriaHaro
- Director del proyecto:
  - [Diego Álvarez](https://about.me/diegoalsan) | @diegoalsan


## Contexto del proyecto

El trabajo que contiene este repositorio se ha desarrollado en el [**Àrea Hackers cívics**](http://civichackers.cc). Un espacio de trabajo colaborativo formado por [hackers cívics](http://civichackers.webs.upv.es/conocenos/que-es-una-hacker-civicoa/) que buscamos y creamos soluciones a problemas que impiden que los ciudadanos y ciudadanas podamos influir en los asuntos que nos afectan y, así, construir una sociedad más justa. En definitiva, abordamos aquellos retos que limitan, dificultan o impiden nuestro [**empoderamiento**](http://civichackers.webs.upv.es/conocenos/una-aproximacion-al-concepto-de-empoderamiento/).

El [**Àrea Hackers cívics**](http://civichackers.cc) ha sido impulsada por la [**Cátedra Govern Obert**](http://www.upv.es/contenidos/CATGO/info/). Una iniciativa surgida de la colaboración entre la Concejalía de Transparencia, Gobierno Abierto y Cooperación del Ayuntamiento de València y la [Universitat Politècnica de València](http://www.upv.es).

  ![ÀHC](http://civichackers.webs.upv.es/wp-content/uploads/2017/02/Logo_CGO_web.png) ![ÀHC](http://civichackers.webs.upv.es/wp-content/uploads/2017/02/logo_AHC_web.png)


## Términos de uso

El contenido de este repositorio está sujeto a la licencia [GNU General Public License v3.0](https://www.gnu.org/licenses/gpl-3.0.en.html).

![](https://www.gnu.org/graphics/gplv3-127x51.png)
