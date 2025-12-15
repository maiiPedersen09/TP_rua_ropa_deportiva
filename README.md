# TP_Rua_Ropa_Deportiva- Web 2 (2025)


## 1. El Proyecto y Dominio

Este es el Trabajo Práctico de Web 2, donde desarrollamos un sitio dinámico de **Ropa Deportiva** usando el patrón MVC.

El modelo de datos usa una relación **1 a N** para administrar:
1.  **Categorías** (el lado 1).
2.  **Productos / Ítems** (el lado N).

## 2. Base de Datos (`db_tienda_ropa`)

**Diagrama de Relación:**
**(AQUÍ VA LA IMAGEN DEL DIAGRAMA DE BASE DE DATOS)**

Las tablas son:

| Tabla | Contiene | Relación |
| :--- | :--- | :--- |
| `categoria` | Tipos de ropa (Ej: Running, Natación) | Lado **1** |
| `producto` | Los ítems específicos (Ej: Calzas Térmicas) | Lado **N** |

## 3. Requerimientos Cumplidos

### A. Acceso Público (Sin Login)

* Listado de todos los Productos.
* Detalle de cada Producto.
* Listado de Categorías.
* Ver Productos filtrados por Categoría.
* Importante: Cada Producto siempre muestra a qué Categoría pertenece.

### B. Acceso Administrador (Con Login)

* **Login** con usuario y contraseña.
* **Logout** (Cerrar sesión).
* **ABM de Productos** (Agregar/Borrar/Modificar Ítems).
    * Al agregar, la Categoría se elige con un `<select>`.
* **ABM de Categorías** (Agregar/Borrar/Modificar Categorías).

## 4. Despliegue

El sitio usa **MVC** y **URLs semánticas**.

1.  **Base de Datos:**
    * Crea la DB `db_tienda_ropa`.
    * Carga las tablas y datos usando el archivo `tienda_ropa.sql`.
2.  **Servidor (Apache):**
    * Es obligatorio tener habilitado el módulo **`mod_rewrite`** para que las URLs funcionen correctamente.
    * La URL base es configurada en `config.php`.

### Credenciales de Administrador

Para probar la sección privada (ABM):

| Rol | Usuario | Contraseña |
| :--- | :--- | :--- |
| **Administrador** | `webadmin` | `admin` |

---

