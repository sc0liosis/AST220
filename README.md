Este proyecto realiza una simulación numérica de la órbita de la Tierra alrededor del Sol, junto con partículas ubicadas cerca de los puntos de Lagrange L4 y L5, usando la librería `rebound` para la simulación de sistemas gravitacionales.

###Funcionalidad
1. Creación de la simulación:
Se utiliza rebound.Simulation() para crear una simulación de un sistema gravitacional donde las unidades están definidas en unidades astronómicas (AU), años (yr) y masas solares (Msun).
Se añade el Sol en el origen y la Tierra orbitando alrededor de él con una velocidad inicial calculada para una órbita circular.

2. Añadir partículas alrededor de los puntos L4 y L5:
Se añaden partículas en posiciones cercanas a los puntos Lagrange L4 y L5 (ubicados en un triángulo equilátero con respecto al Sol y la Tierra).
Las partículas se colocan con una pequeña variación aleatoria en torno a los puntos exactos de L4 y L5 y se les asignan velocidades correspondientes a las de estos puntos.

3. Integración temporal:
El sistema se integra durante los años que se requieran con el número de pasos temporales necesarios para que la animación se vea correctamente. Mientras más años se introduzcan, más pasos requiere. Estos parámetros se pueden modificar en la línea "times",
donde el segundo parámetro son los años y el tercer parámetro el número de pasos. Durante la integración, se registran las posiciones del Sol, la Tierra y las partículas en L4 y L5.

4. Visualización:
Se utiliza matplotlib para graficar la trayectoria de las partículas, la Tierra y el Sol en un sistema de referencia centrado en el Sol.
Se genera una animación que muestra las trayectorias de las partículas en L4 y L5, así como la órbita de la Tierra.
La animación se guarda como un archivo MP4 y se muestra en formato HTML.

###Archivos generados
trayectoria_L4_L5_moviendose_con_tierra.mp4: Archivo de video que muestra la animación de las trayectorias de las partículas en los puntos de Lagrange L4 y L5 en relación con la órbita de la Tierra.


###Cómo ejecutar el código
Clona este repositorio o descarga el archivo.
Asegúrese de tener instaladas las dependencias listadas en la sección Dependencias.
Ejecuta el script en un entorno de Jupyter Notebook o cualquier IDE compatible con Python. En este caso, es mucho más recomendable usar Google Colab para simplificar el proceso de instalación de `rebound`.

La animación incluye:
El Sol (en amarillo).
La Tierra (en verde), orbitando alrededor del Sol.
Partículas alrededor de los puntos L4 (en azul) y L5 (en cian).

###Notas adicionales
Los puntos de Lagrange L4 y L5 son posiciones donde los objetos pequeños pueden mantener una posición estable respecto a dos cuerpos masivos, como el Sol y la Tierra.
Se puede ajustar el número de partículas (num_particles) y la variación en torno a L4 y L5 (spread) para experimentar con diferentes configuraciones. Si la variación es muy grande, es posible que algunas partículas se salgan de 
órbita, ya que el sistema es estable ante pequeñas perturbaciones.
