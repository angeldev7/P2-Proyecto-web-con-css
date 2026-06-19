# FastMenu ESPE - Sistema de Pedidos Inteligente

## Descripción
**FastMenu ESPE** es una aplicación web responsiva diseñada para simular un sistema de pedidos y compra de alimentos en el patio de comidas de la Universidad de las Fuerzas Armadas ESPE (Sede Santo Domingo). Su objetivo principal es evitar que los estudiantes hagan largas filas en el campus universitario para adquirir su almuerzo, snacks o bebidas, permitiéndoles reservar y ver el progreso de su comida desde una interfaz intuitiva y adaptable.

## Objetivo
Integrar estilos CSS externos estructurados junto con componentes personalizados de Bootstrap 5 para crear una interfaz con enfoque "mobile-first". Asimismo, establecer representaciones formales de los datos principales del menú del proyecto mediante los formatos JSON y XML en un entorno simulado local.

## Tecnologías Utilizadas
- **HTML5:** Marcado estructurado semántico.
- **CSS3:** Estilos personalizados, efectos hover, transiciones suaves, diseño flexible (Flexbox y Grid) y adaptabilidad responsiva con Media Queries.
- **Bootstrap 5.3.3:** Framework de CSS utilizado para agilizar el diseño adaptable e incorporar componentes avanzados (carruseles, barras de progreso, acordeones, modales y navegación colapsable).
- **FontAwesome 6.5.0:** Iconografía del sistema.
- **JSON y XML:** Formatos de intercambio de datos para representar y simular los productos del catálogo de alimentos.

## Estructura de Carpetas
```
P2Proyecto/
│
├── index.html               # Página de inicio de sesión (Login)
│
├── pages/
│   ├── principal.html       # Panel principal del estudiante (Menú, Carrusel y Horarios)
│   ├── pedido.html          # Resumen de compra, barra de progreso y mapa de retiro
│   ├── nosotros.html        # Misión, visión e historia de FastMenu ESPE
│   ├── contacto.html        # Formulario de buzón de sugerencias y reclamos
│   └── registro.html        # Formulario de registro de nuevos usuarios
│
├── css/
│   ├── general.css          # Estilos globales y personalización de Bootstrap 5
│   ├── index.css            # Estilos específicos del Login
│   ├── principal.css        # Estilos específicos del dashboard, carrusel y acordeón
│   ├── pedido.css           # Estilos de la tabla de carrito y barra de progreso
│   ├── contacto.css         # Estilos del formulario de contacto
│   ├── nosotros.css         # Estilos de la historia institucional
│   └── registro.css         # Estilos del formulario de registro
│
├── data/
│   ├── datos.json           # Catálogo de alimentos estructurado en formato JSON
│   └── datos.xml            # Catálogo de alimentos estructurado en formato XML
│
├── imagenes/                # Recursos gráficos del proyecto (logos, productos)
│
└── README.md                # Documentación del proyecto (este archivo)
```

## Páginas Disponibles
1. **Inicio de Sesión (Login):** Ubicado en `index.html`. Permite acceder al panel mediante un usuario o correo institucional de la ESPE.
2. **Registro de Cuenta:** Ubicado en `pages/registro.html`. Formulario mobile-first para nuevos usuarios.
3. **Inicio / Dashboard:** Ubicado en `pages/principal.html`. Contiene el menú categorizado, carrusel de promociones del día y horarios de atención.
4. **Mi pedido / Carrito:** Ubicado en `pages/pedido.html`. Muestra el resumen de compra, el progreso animado de la preparación de la comida y enlace al mapa físico de retiro.
5. **Nosotros:** Ubicado en `pages/nosotros.html`. Presenta la historia escolar, visión y misión del proyecto.
6. **Contacto:** Ubicado en `pages/contacto.html`. Buzón de sugerencias que permite a los estudiantes enviar comentarios.

## Componentes Bootstrap Utilizados y Adaptación Visual
Para evitar la apariencia predeterminada de Bootstrap y reflejar la identidad visual de la ESPE, se personalizaron los siguientes componentes en `general.css`, `principal.css` y `pedido.css`:
- **Navbar (Navegación):** Rediseñado con color carbón (`#2d2d2d`), textos blancos y efectos hover en amarillo ESPE (`#ffcc00`) que se colapsa en un menú hamburguesa responsivo.
- **Carousel (Carrusel de Promociones):** Incorporado en el dashboard para rotar combos y platos destacados. Se adaptaron los fondos con alertas suaves (amarillo, rojo y verde claros) y tipografías personalizadas.
- **Cards (Tarjetas de Alimentos):** Utilizado para diagramar de manera uniforme los productos. Se le aplicaron efectos hover con elevación en el eje Y y sombras más marcadas.
- **Accordion (Acordeón de FAQ):** Utilizado en las preguntas frecuentes para optimizar el espacio móvil. Se personalizó la cabecera activa en rojo ESPE (`#8b0000`) y con fondos semitransparentes.
- **Progress Bar (Barra de progreso):** Usado en la simulación de preparación del pedido. Se adaptó con un color rojo vivo, efecto a rayas y animación de carga.
- **Modales:** Integrados para ventanas emergentes al añadir productos, enviar mensajes de contacto y confirmar registros. Se rediseñó el header en color rojo institucional con botones redondeados.

## Representación de Datos y Relación con la Interfaz (JSON / XML)
Los archivos `data/datos.json` y `data/datos.xml` simulan cómo se recibirían los datos de los alimentos si el proyecto se conectara a un servidor o una API REST en una entrega posterior.

### Relación entre Interfaz y Datos (Mapeo):
| Elemento Visual en la Interfaz | Campo en datos.json | Etiqueta en datos.xml | Descripción / Ejemplo |
| :--- | :--- | :--- | :--- |
| **Nombre del producto** | `nombre` | `<nombre>` | El título principal del alimento (Ej: "Arroz con camarón") |
| **Descripción** | `descripcion` | `<descripcion>` | Detalles del platillo (Ej: "Con porción especial de ensalada") |
| **Precio unitario** | `precio` | `<precio>` | Valor decimal del producto (Ej: `2.50`) |
| **Imagen del producto** | `imagen` | `<imagen>` | Ruta relativa al archivo gráfico (Ej: `imagenes/...`) |
| **Cantidad disponible** | `stock` | `<stock>` | Límite disponible en cocina (Ej: `15`) |
| **Categoría** | `categoria` | `<categoria>` | Agrupación del menú (Ej: "Almuerzos", "Bebidas", "Snacks") |

## Instrucciones para Ejecutar el Proyecto
Dado que es un proyecto de fundamentos sin backend, se puede ejecutar de forma local de la siguiente manera:
1. Clonar o descargar el repositorio.
2. Abrir la carpeta raíz del proyecto en un editor como **VS Code**.
3. Ejecutar el archivo raíz `index.html` utilizando la extensión **Live Server** (esto desplegará el proyecto en el puerto local, típicamente `http://localhost:5500` o similar).
4. Navegar entre las páginas desde la barra de menús.
5. Presionar los botones "Añadir al carrito", "Confirmar Pago" o "Enviar Mensaje" para visualizar la interacción con los componentes modales de Bootstrap.

## Autor
- **Estudiante de Fundamentos de Programación Web**
- Universidad de las Fuerzas Armadas ESPE
- Año: 2026
