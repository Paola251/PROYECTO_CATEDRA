# Sistema de Control de Notas Académicas

Aplicación de escritorio desarrollada en **C# (Windows Forms)** y **SQL Server** para la gestión, cálculo y consulta centralizada de calificaciones académicas.

---
###  Integrantes del Equipo
| Apellidos y Nombres | Carnet |
| :--- | :---: |
| Batres Pérez, Daniel Armando | `260703` |
| Cruz Vásquez, Paola Esmeralda | `261105` |
| Hernández López, Allison Michelle | `260600` |

---

##  Características Principales
* **Pantalla de Presentación (`FormAutores`):** Muestra la información institucional y los autores del proyecto antes de iniciar sesión.
* **Autenticación de Docentes (`FormLogin`):** Validación de credenciales (`Usuario` y `Contraseña`) contra la tabla `Docente` en SQL Server.
* **Gestión de Calificaciones (`FormNotas`):** Filtrado por curso/carga académica, visualización de estudiantes en `DataGridView`, captura de `Nota_1`, `Nota_2` y `Examen`, y cálculo automático de `Promedio` y `Estado` (`Aprobado` / `Reprobado`).

---

## Tecnologías Utilizadas
* **Lenguaje:** C# (.NET / Windows Forms)
* **IDE:** Visual Studio
* **Base de Datos:** Microsoft SQL Server / SQL Server Management Studio (SSMS)
* **ORM / Acceso a Datos:** Entity Framework Core
* **Control de Versiones:** Git & GitHub

---

##  Estructura de la Base de Datos (`ESCUELA`)
El sistema utiliza una base de datos relacional llamada **`ESCUELA`** compuesta por 5 tablas principales:

1. **`Estudiantes`:** Almacena `Id_Estudiante` (PK), `Nombres`, `Apellidos` y `Grupo_Seccion`.
2. **`Docente`:** Almacena `Id_Docente` (PK), `Nombre_D`, `Apellido_D`, `Usuario` y `Contrasena`.
3. **`Materia`:** Almacena `Id_Materia` (PK) y `Nombre_Materia`.
4. **`Carga_Academica`:** Tabla intermedia que vincula `Id_Docente` (FK) y `Id_Materia` (FK) con su respectivo `Grupo_Seccion`.
5. **`Calificaciones`:** Registra `Id_Estudiante` (FK), `Id_Carga` (FK), `Nota_1`, `Nota_2`, `Examen`, `Promedio` y `Estado`.
