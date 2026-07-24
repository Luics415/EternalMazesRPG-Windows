# Eternal Mazes RPG Windows

Eternal Mazes RPG Windows es un proyecto de videojuego de rol (RPG) orientado a Windows, desarrollado con una estructura basada en un motor de escritorio web y un conjunto de assets completos para exploración, progresión, diálogo y combate por turnos.

El proyecto presenta una identidad clara de aventura de fantasía, con mapas, personajes, eventos, inventario, habilidades, enemigo, estados y una lógica de juego que combina narrativa, exploración y resolución de encuentros.

## Descripción general

Este repositorio contiene la base completa del videojuego, incluyendo:

- la interfaz y flujo principal del juego,
- los archivos de datos del sistema,
- los mapas y eventos del mundo,
- los actores, clases, enemigos, habilidades, objetos y armaduras,
- los recursos visuales y de audio,
- la estructura de empaquetado para ejecución en Windows.

La intención del proyecto es presentar una experiencia de RPG clásica con una estética de aventura de mazmorras y exploración, donde el jugador puede avanzar a través de mapas, interactuar con eventos, obtener progreso y enfrentarse a enemigos en batallas dinámicas.

## Qué es lo que se encuentra dentro del videojuego

El proyecto está compuesto por una gran cantidad de contenidos funcionales y artísticos. Dentro de la estructura del juego se pueden identificar estos componentes:

### 1. Sistema principal del juego

El núcleo del juego está alojado en la carpeta `www/`, donde se encuentran los scripts, datos y recursos de la aplicación.

Entre ellos destacan:

- `www/index.html`: punto de entrada de la aplicación.
- `www/js/`: scripts del motor y del flujo del juego.
- `www/data/`: archivos JSON que contienen el contenido del sistema.
- `www/img/`: gráficos y sprites del juego.
- `www/audio/`: música, sonidos y efectos.
- `www/fonts/`: tipografías utilizadas por la interfaz.
- `www/icon/`: iconos del proyecto.

### 2. Datos y contenido de juego

La carpeta `www/data/` concentra la mayor parte de la lógica de contenido del videojuego.

Se incluyen archivos para:

- `Actors.json`: personajes jugables.
- `Classes.json`: clases y progresión de los personajes.
- `Skills.json`: habilidades activas y pasivas.
- `Items.json`: objetos y consumibles.
- `Weapons.json`: armas.
- `Armors.json`: armaduras y accesorios.
- `Enemies.json`: criaturas y enemigos.
- `Troops.json`: formaciones de batalla.
- `States.json`: estados alterados del combate.
- `System.json`: configuración global de la partida.
- `Map001.json` a `Map071.json`: varios mapas del mundo del juego.
- `MapInfos.json`: metadatos de los mapas.
- `CommonEvents.json`: eventos compartidos y lógica reutilizable.

Esto permite construir una experiencia completa de RPG con personalidad propia, con datos que definen el comportamiento de personajes, enemigos, habilidades, diálogo y progresión.

### 3. Visuales

La carpeta `www/img/` almacena capas de arte que definen:

- personajes,
- enemigos,
- fondos de batalla,
- tilesets,
- animaciones,
- iconos y decoraciones.

Las imágenes forman el apartado visual principal del juego, aportando la estética del mundo y el estilo del combate.

### 4. Audio

La carpeta `www/audio/` contiene los elementos sonoros:

- música de fondo,
- efectos de sonido,
- música de batalla,
- sonidos de menús, confirmaciones y eventos.

Esto ayuda a reforzar la inmersión del jugador en distintos contextos dentro del juego.

### 5. Localización

La carpeta `locales/` contiene recursos de localización y textos traducidos para distintas regiones. Esto muestra que el proyecto tiene una intención de soporte multilenguaje.

## Dinámica del videojuego

La dinámica del proyecto se centra en una estructura típica de RPG con una fuerte presencia de exploración y combate.

### Exploración del mundo

El jugador se mueve por mapas, interactúa con personajes no jugables, descubre puntos de interés, abre cofres, atraviesa zonas del mapa y activa sucesos de juego mediante eventos.

En varios mapas se observan transiciones, encuentros, mensajes narrativos y elementos interactivos. La presencia de eventos en las tablas de datos permite que la aventura avance de manera guiada.

### Progresión del personaje

La progresión se define a través de:

- actores,
- clases,
- niveles,
- habilidades,
- equipos,
- estados,
- estadísticas base.

El sistema permite que los personajes asciendan en poder, utilicen equipo y desarrollen capacidades específicas conforme avanza la aventura.

### Combate por turnos

El sistema de batalla se apoya en una estructura por turnos, con soporte para:

- ataque físico,
- magia elemental,
- habilidades especiales,
- uso de objetos,
- estados de daño o mejora,
- selección de objetivos,
- defensa y evasión.

La presencia de habilidades como ataque, defensa, curación, fuego, hielo, agua, veneno, confusión, reanimación y otras técnicas muestra una mecánica de combate flexible y variada.

### Estados y condición de personajes

Los archivos de `States.json` y `Skills.json` muestran que el juego incorpora mecánicas de condiciones, como:

- daño sobre tiempo,
- debilitamiento,
- paralización,
- ceguera,
- sueño,
- veneno,
- confusión,
- curación,
- fortalecimiento.

Esto añade profundidad al sistema de combate y a la estrategia del jugador.

### Interacciones narrativas

El contenido de `Map001.json` y otros mapas revela que el juego no se centra solo en la exploración, sino también en interacción con personajes y secuencias de diálogo. Se observan eventos con texto narrativo, preguntas, comercio y referencias a tramas y misiones.

## Estructura técnica del proyecto

Este repositorio está organizado como un proyecto de videojuego de escritorio con una base web ejecutada por un entorno de paquetes Windows.

### Archivo principal

El archivo `package.json` define la configuración de la aplicación y establece el arranque principal hacia la interfaz web interna:

- `main`: `www/index.html`
- `window`: configuración de ventana y acceso a iconos.

Esto indica que el juego se ejecuta como una aplicación de escritorio con una interfaz basada en navegador y recursos locales.

<img width="1550" height="874" alt="image" src="https://github.com/user-attachments/assets/4d8eefeb-b34d-4836-aa52-f6320d08f028" />


### Motor y dependencias

La estructura usa bibliotecas y recursos propios del estilo de RPG Maker/engine de scriptado web, con archivos como:

- `www/js/rpg_core.js`
- `www/js/rpg_managers.js`
- `www/js/rpg_objects.js`
- `www/js/rpg_scenes.js`
- `www/js/rpg_sprites.js`
- `www/js/rpg_windows.js`

El uso de plugins y scripts especializados sugiere una construcción con un sistema de jugabilidad avanzada, reenfocada en menús, batalla, eventos, guards, save/load y pantallas de juego típicas del género.

## Cómo se desarrolló el proyecto

El proyecto se desarrolló sobre una base de contenido estructurado en formato de datos JSON para el diseño del juego. La idea principal es separar:

1. la lógica del juego,
2. los datos de contenido,
3. los recursos visuales y sonoros,
4. y la interfaz ejecutable.

Esto hace que el proyecto sea fácilmente ampliable, modificable y reutilizable. En lugar de estar todo inmerso en un único archivo, cada sistema del juego se organiza por tipo de recurso:

- mapas,
- actores,
- clases,
- habilidades,
- eventos,
- enemigos,
- interfaz,
- recursos de audio y arte.

Ese modelo de desarrollo es muy típico en RPGs modernos y permite ampliar el contenido sin depender de un único bloque monolítico de código.

## Qué representa este repositorio

Este repositorio representa una compilación completa de contenido y estructura de un videojuego tipo RPG de aventura. El proyecto combina:

- diseño de mapas,
- lógica de eventos,
- ayuda de combate,
- personajes y clases,
- recursos gráficos y de audio,
- persistencia de progresos,
- configuración de la aplicación como juego de escritorio.

En resumen, el proyecto no es solo una colección de archivos, sino una base completa de un juego jugable y ampliable.

## Cómo ejecutar el proyecto en Windows

Dependiendo de cómo esté compilado el proyecto en tu entorno, puedes ejecutarlo de dos maneras:

### Opción 1: ejecutar el archivo de juego empaquetado

Si el proyecto ya viene empaquetado para Windows, basta con abrir el ejecutable en la raíz del repositorio.

### Opción 2: ejecutar como proyecto de aplicación web/desktop

Desde la raíz del proyecto, puedes lanzar la aplicación siguiendo la estructura de `package.json` y el punto de entrada `www/index.html`.

## Requisitos básicos

- Sistema operativo Windows
- Un entorno capaz de ejecutar la aplicación empaquetada o la base web del proyecto
- Los recursos del juego localizados en los directorios `www/` y `locales/`

## Estado del proyecto

Este repositorio se encuentra como una base de juego completa, lista para ser revisada, modificada, extendida o subida a GitHub para su distribución o seguimiento de desarrollo.

## Licencia

Este proyecto se distribuye bajo la licencia MIT, con el siguiente propósito:

- permitir el uso, copia, modificación y distribución del proyecto,
- mantener la atribución al autor principal,
- y facilitar la publicación del juego en repositorios públicos o privados.

La licencia completa está disponible en el archivo [LICENSE](LICENSE).

> Nota importante: aunque este repositorio se comparte bajo una licencia abierta, el juego puede incluir recursos, librerías o motores de terceros con sus propias condiciones. La licencia principal aplicada aquí cubre la organización del repositorio, el contenido original y la documentación asociada.

## Créditos

### Autor principal

- Luics415

### Proyecto

Eternal Mazes RPG Windows es un videojuego de estilo RPG desarrollado como proyecto personal, con foco en una experiencia de exploración, diálogo, progresión y combate por turnos.

### Créditos del desarrollo

- Dirección, estructura y organización del proyecto: Luics415
- Diseño de contenido y desarrollo del sistema base del juego: Luics415
- Documentación y publicación del repositorio: Luics415

### Agradecimientos

Este proyecto incorpora una base técnica y de contenido orientada a RPG clásico, con una organización basada en datos, recursos visuales, audio y lógica de juego. Gracias a la comunidad, a los motores de referencia y a la estructura de desarrollo del género, este juego puede seguir creciendo y ampliándose con nuevas mecánicas y contenidos.


