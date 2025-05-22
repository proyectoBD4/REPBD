# 📚 Proyecto de Base de Datos para <Nombre del Proyecto>  

Este repositorio contiene el diseño y los archivos relacionados con la base de datos usada en el proyecto **Proyecto BD**. La base está diseñada para <explica brevemente el propósito: por ejemplo, gestionar libros en una biblioteca, registrar ventas, controlar usuarios, etc.>.

---

## 🧱 Estructura de la Base de Datos

La base de datos contiene las siguientes tablas principales:

- `usuarios`: almacena los datos de los usuarios del sistema.
- `libros`: contiene información sobre los libros disponibles.
- `prestamos`: registra cuándo un usuario toma prestado un libro.

Puedes revisar el archivo `schema.sql` para ver la estructura completa (CREATE TABLE, claves primarias y foráneas).

---

## 📂 Archivos incluidos

| Archivo           | Descripción |
|-------------------|-------------|
| `schema.sql`      | Script con la estructura de las tablas (esquema de la base de datos). |
| `datos_iniciales.sql` o `datos.csv` | Datos de ejemplo para poblar la base. |
| `conexion.py` o `conexion.js` | Código de ejemplo que muestra cómo conectarse a la base. |
| `README.md`        | Este archivo de explicación. |

---

## 🧪 ¿Cómo probar esta base?

1. Abre tu gestor de base de datos (como pgAdmin, MySQL Workbench, Supabase SQL Editor, etc.).
2. Ejecuta el archivo `schema.sql` para crear las tablas.
3. (Opcional) Carga el archivo de datos para tener información de prueba.
4. Usa el código de conexión si quieres conectarla con una app o hacer consultas.

---

## 🔗 Vinculación con GitHub

La base fue vinculada a GitHub para:

- Tener un respaldo del diseño y los datos.
- Permitir control de versiones.
- Compartir fácilmente con compañeros y profesores.
- Integrarse con plataformas como Supabase o Appsmith.

---

Este repositorio me permite mantener organizado mi proyecto de base de datos. Aquí se puede ver el diseño, los datos de ejemplo y el código que demuestra cómo conectarla a una aplicación.

---

## 📅 Autor y Fecha

- Autor: <Tu nombre>
- Fecha: <Fecha de entrega o creación>


---

## 🧪 Ejemplos de consultas a la base de datos (Supabase)

### 📄 Tabla: `libros`

| id | titulo                 | autor           | disponible |
|----|------------------------|------------------|------------|
| 1  | Cien Años de Soledad   | Gabriel García Márquez | true       |
| 2  | El Principito          | Antoine de Saint-Exupéry | false     |
| 3  | Rayuela                | Julio Cortázar   | true       |

**Consulta SQL para ver todos los libros:**
```sql
SELECT * FROM libros;
SELECT libros.titulo, usuarios.nombre
FROM prestamos
JOIN libros ON libros.id = prestamos.id_libro
JOIN usuarios ON usuarios.id = prestamos.id_usuario;

#**Agrego ejemplos de datos y consultas SQL para demostrar la base**

Tablas:
- libros
- usuarios
- prestamos

libros:
| id | titulo               | autor                  | disponible |
|----|----------------------|------------------------|------------|
| 1  | Cien Años de Soledad | Gabriel García Márquez | true       |
| 2  | El Principito        | Antoine de Saint-Exupéry | false     |
| 3  | Rayuela              | Julio Cortázar         | true       |

usuarios:
| id | nombre     | correo              |
|----|------------|---------------------|
| 1  | Ana Torres | ana@gmail.com       |
| 2  | Luis Pérez | luisp@hotmail.com   |
| 3  | Marta Díaz | marta@gmail.com     |

prestamos:
| id | id_usuario | id_libro | fecha     |
|----|------------|----------|-----------|
| 1  | 1          | 2        | 2025-05-21 |
| 2  | 2          | 1        | 2025-05-20 |
