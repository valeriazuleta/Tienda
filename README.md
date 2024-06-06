# Tienda
Este código en Java implementa una aplicación para gestionar una base de datos de productos. A continuación, se describe cada componente del código:

### Clase `App`
- **Método `main`**:
  - Crea una instancia de `Scanner` para leer la entrada del usuario.
  - Crea una instancia de `BaseDeDatosProducto` para gestionar la base de datos de productos.
  - Agrega una serie de productos a la base de datos con el método `agregarProducto`.
  - Lee el número de casos (operaciones) que se van a ejecutar desde la entrada del usuario.
  - Itera a través de los casos, leyendo la operación y los datos del producto desde la entrada del usuario, y realiza la operación solicitada (`agregar`, `actualizar` o `borrar`) en la base de datos.
  - Calcula y muestra las estadísticas de la base de datos después de ejecutar todas las operaciones.

### Clase `BaseDeDatosProducto`
- **Atributos**:
  - `listaProductos`: Un mapa (`HashMap`) que almacena los productos, utilizando el código del producto como clave.

- **Métodos**:
  - `agregarProducto(int codigo, String nombre, double precio, int inventario)`: Agrega un nuevo producto a la base de datos si el código no existe ya en la base de datos. Muestra un error si el producto ya existe.
  - `actualizarProducto(int codigo, String nombre, double precio, int inventario)`: Actualiza un producto existente en la base de datos. Muestra un error si el producto no existe.
  - `borrarProducto(int codigo)`: Elimina un producto de la base de datos si el código existe. Muestra un error si el producto no existe.
  - `realizarOperacion(String operacion, int codigo, String nombre, double precio, int inventario)`: Realiza la operación indicada (`agregar`, `actualizar` o `borrar`) en la base de datos.
  - `calcularEstadisticas()`: Calcula y muestra las siguientes estadísticas:
    - Nombre del producto con el precio mayor.
    - Nombre del producto con el precio menor.
    - Promedio de los precios de todos los productos.
    - Valor total del inventario (precio de cada producto multiplicado por su inventario y sumado para todos los productos).

### Clase `Producto`
- **Atributos**:
  - `codigo`: Código único del producto.
  - `nombre`: Nombre del producto.
  - `precio`: Precio del producto.
  - `inventario`: Cantidad de productos en inventario.

- **Constructor**:
  - Inicializa los atributos del producto con los valores proporcionados.

- **Métodos `get` y `set`**:
  - Métodos para obtener y establecer los valores de los atributos del producto.

### Flujo del Programa
1. Se crean instancias necesarias (`Scanner` y `BaseDeDatosProducto`).
2. Se agregan productos predefinidos a la base de datos.
3. Se leen las operaciones a realizar (número de casos).
4. Para cada operación, se lee la operación específica (`agregar`, `actualizar`, `borrar`) y los datos del producto, y se realiza la operación correspondiente.
5. Finalmente, se calculan y muestran las estadísticas de la base de datos.

Este código ofrece una estructura básica para la gestión de una base de datos de productos, permitiendo agregar, actualizar y eliminar productos, además de calcular estadísticas relevantes.
