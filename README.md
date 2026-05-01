🎨 DataDesign DP - Panel de Análisis de Tráfico (Vanilla Edition)

¡Bienvenido al proyecto DataDesign DP!

Si estás leyendo este documento, es porque te diste cuenta de que llevar el seguimiento de cientos de flyers, carruseles, campañas y ajustes (que piden para "ayer") en un Excel gigante no era vida para nadie. Este proyecto nació de la necesidad de sacar a la luz la verdadera carga laboral del equipo de diseño, ver quién nos está pidiendo más cosas de la cuenta y, sobre todo, saber si estamos entregando a tiempo.

🚀 ¿Qué es este engendro hermoso?

Es un Dashboard interactivo 100% portátil. No usa bases de datos complejas, no requiere servidores, ni instalaciones raras que le den dolores de cabeza al equipo de IT. Es un único archivo index.html que contiene toda la estructura (HTML), el diseño bonito (Tailwind CSS) y el motor de procesamiento (JavaScript puro y duro).

Literalmente: le das doble clic, se abre en tu navegador (Chrome, Edge, Safari, el que sea) y ya estás analizando datos. Nivel Dios de la practicidad.

⚙️ ¿Qué superpoderes tiene?

El aplicativo está dividido en 4 módulos que hacen el trabajo sucio por ti:

📊 General (Dashboard): La vista panorámica. Te escupe en la cara los números reales: cuántas cosas se han pedido, cuántas salieron a tiempo, cuántos retrasos dolorosos llevamos y cuántas cosas siguen flotando en el limbo.

🔍 Buscador Universal: Se acabó el suplicio de usar Ctrl+B en Excel. Escribes cualquier cosa ("flyer", "Pipo", "Karen") y filtra la tabla en tiempo real.

👨‍🎨 Diseñadores: La hora de la verdad para el equipo. Muestra una barra de progreso de cada diseñador. Aquí vas a ver visualmente quién está camellando duro, quién tiene un cuello de botella (las barritas rojas de retraso) y quién es el rey de los "Pendientes".

🏢 Solicitantes (El Muro de los Lamentos): El top de clientes internos. Te enlista de mayor a menor quiénes son los que más carga laboral le tiran al equipo de diseño y cómo les estamos respondiendo. Ideal para cuando necesites justificar que X persona los tiene reventados a punta de correos.

⚠️ LA CRUDA VERDAD (Aviso Legal sobre los Datos)

Atención a quien vaya a mantener o auditar este dashboard: El sistema es brutalmente honesto y solo es tan bueno como los datos que le metes.

La lógica matemática del sistema funciona así: Toma la fecha solicitada de entrega y la compara con la fecha entrega final.

Si la diferencia es de 0 días o menos: A Tiempo.

Si la diferencia es mayor a 0: Con Retraso.

EL GRAN PROBLEMA: Si en el Excel original el equipo o el coordinador se olvida de anotar la fecha en la que se entregó la pieza (como pasó en casi todo el mes de mayo de 2026), el sistema no va a adivinar, simplemente lo va a marcar como Pendiente / Sin dato.

Si ves que las métricas están llenas de "Pendientes", no vengas a echarle la culpa al código. Tienen que ir a apretarle las tuercas al equipo para que sean juiciosos llenando el Excel original apenas manden el correo con el diseño final.

🛠️ ¿Cómo actualizar los datos? (Modo Manual)

Como esta es una versión "Vanilla" (sin un backend conectado a la nube), si quieres meter los datos de junio, julio o diciembre, vas a tener que ensuciarte un poquito las manos:

Abre el archivo index.html con un editor de texto (el Bloc de notas sirve, aunque te recomiendo algo decente como VS Code).

Ve casi al final del archivo, a la línea donde empieza la etiqueta <script> y busca una variable gigante llamada const rawData = [ ... ];.

Ese bloque contiene la información en formato JSON. Vas a tener que exportar tus nuevas filas de Excel a ese mismo formato.

Tip de vida: Si no sabes programar, copia tus filas nuevas de Excel, pégalas en ChatGPT o en Gemini y dile: "Conviérteme esta tabla de Excel a un array de objetos en JavaScript con las llaves: solicitud, solicitante, diseñador, fecha_solicitada, fecha_entrega".

Pegas los nuevos datos ahí adentro, guardas el archivo index.html y refrescas el navegador.

¡Boom! Datos actualizados.

Desarrollado con mucha paciencia, algo de sarcasmo y café cargado. Que la fuerza del diseño los acompañe.