# Catálogo de Productos con Filtrado y Generación de PDF

## Visión General
Este proyecto es una aplicación web interactiva que permite a los usuarios filtrar productos y generar un catálogo personalizado en PDF basado en sus selecciones.

## Estructura y Funcionalidad

### 2.1 HTML y CSS:
- La página incluye un encabezado fijo con el título "CATÁLOGO DE PRODUCTOS".
- Se implementan 10 filtros personalizables, cada uno como un elemento `<select>`.
- Dos filtros (FILTRO 4 y FILTRO 7) incluyen tooltips informativos.
- Se utilizan estilos CSS para crear un diseño responsive y atractivo.

### 2.2 JavaScript:

#### a) Datos y Estructuras:
- `products`: Objeto que contiene productos y su disponibilidad basada en 28 criterios.
- `filters`: Array con los IDs de los 10 filtros.
- `slideMatrix`: Objeto que mapea productos a números de diapositivas para el PDF.

#### b) Funciones Principales:
- `getFilterIndex(filterId)`: Mapea las selecciones de filtros a índices en el array de disponibilidad.
- `updateProducts()`: Actualiza la visualización de productos basada en los filtros seleccionados.
- `getAvailableProducts()`: Devuelve la lista de productos disponibles según los filtros actuales.
- `resetFilters()`: Reinicia todos los filtros a su estado inicial.
- `generatePDF()`: Genera un PDF personalizado basado en los productos filtrados.

#### c) Proceso de Generación de PDF:
1. Determina las diapositivas a incluir basándose en los productos filtrados.
2. Permite al usuario seleccionar un archivo PDF base.
3. Procesa el PDF seleccionado, extrayendo las diapositivas relevantes.
4. Crea un nuevo PDF con las diapositivas seleccionadas.
5. Guarda el nuevo PDF como "catalogo_productos.pdf".

## Características Clave:
- Filtrado dinámico de productos con actualización en tiempo real.
- Tooltips informativos para ciertos filtros.
- Generación de PDF personalizado basado en la selección del usuario.
- Diseño responsive que se adapta a diferentes tamaños de pantalla.

## Mejoras y Particularidades:
- Se incluye siempre la primera y la última diapositiva (7) en el PDF generado.
- El sistema de filtrado es flexible y puede adaptarse fácilmente a diferentes criterios.
- Se implementa manejo de errores y feedback visual durante la generación del PDF.

## Consideraciones Técnicas:
- Utiliza bibliotecas externas como pdf.js y jsPDF para el manejo de PDFs.
- El código está estructurado para facilitar futuras modificaciones o expansiones.

## Uso y Flujo de Trabajo:
1. El usuario selecciona criterios en los filtros.
2. La lista de productos se actualiza dinámicamente.
3. Al hacer clic en "Generar PDF", se solicita al usuario seleccionar un PDF base.
4. La aplicación procesa el PDF y genera un nuevo catálogo personalizado.
