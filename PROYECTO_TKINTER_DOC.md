# Documentación del Proyecto - Aplicación Demo (tkinter)

**Autor:** Equipo de desarrollo  
**Fecha:** 2025-09-26

---

## 1. Resumen del proyecto
Este proyecto es una aplicación demo escrita en **Python** utilizando la librería **tkinter**.  
Funciona como un **MVP (Minimum Viable Product)** que contiene una pantalla principal con acceso a distintas ventanas que ejemplifican funcionalidades comunes en interfaces gráficas:

- **Home / Bienvenida**
- **Formulario**
- **Lista (CRUD básico)**
- **Tabla (Treeview con CSV)**
- **Canvas (Dibujo)**

El propósito es mostrar cómo crear ventanas modulares con `tkinter` y organizar un proyecto en varios archivos.

---

## 2. Estructura del proyecto

```
proyecto_demo/
│
├── main.py                # Ventana principal con menú
├── app/
│   ├── win_home.py        # Ventana de bienvenida
│   ├── win_form.py        # Ventana de formulario con validación y guardado en archivo
│   ├── win_list.py        # Ventana con CRUD básico sobre una lista
│   ├── win_table.py       # Ventana que carga datos desde un CSV en un Treeview
│   ├── win_canvas.py      # Ventana con un canvas y dibujos de ejemplo
│
└── data/
    └── sample.csv         # Archivo CSV de ejemplo para la tabla (esperado)
```

---

## 3. Explicación de cada archivo

### `main.py`
- Punto de entrada de la aplicación.
- Crea la ventana principal (`root`) con botones que abren cada una de las ventanas secundarias.
- Incluye un botón **Salir** para cerrar la aplicación.

### `win_home.py`
- Muestra una pantalla de bienvenida con un mensaje introductorio.
- Tiene un botón que despliega un `messagebox` con un aviso de confirmación.

### `win_form.py`
- Ventana de formulario con dos campos: **Nombre** y **Edad**.
- Valida que el nombre no esté vacío y que la edad sea numérica.
- Permite guardar los datos en un archivo `.txt` usando `filedialog`.
- Muestra mensajes de error o confirmación con `messagebox`.

### `win_list.py`
- Ventana que implementa operaciones básicas de **CRUD** sobre un `Listbox`:
  - **Agregar**: Inserta un nuevo ítem.
  - **Eliminar seleccionado**: Elimina el ítem marcado.
  - **Limpiar**: Vacía toda la lista.
- Se asegura de mostrar advertencias si no se ingresa texto al intentar agregar.

### `win_table.py`
- Carga datos desde un archivo `CSV` ubicado en la carpeta `data/sample.csv`.
- Usa `Treeview` para mostrar los registros en formato tabular.
- Si el archivo no existe, muestra una advertencia.
- Se espera que el CSV tenga al menos tres columnas: `nombre`, `valor1`, `valor2`.

### `win_canvas.py`
- Ejemplo de uso de `Canvas` en tkinter.
- Dibuja varias figuras: rectángulo, óvalo, línea y texto.
- Útil para aplicaciones gráficas o educativas.

---

## 4. Requisitos e instalación
- **Python 3.8+**
- Librerías estándar: `tkinter`, `csv`, `pathlib`  
(No se requieren librerías externas).

Para ejecutar la aplicación:

```bash
python main.py
```

---

## 5. Mejoras recomendadas
- Implementar un sistema de **persistencia de datos** (ej. JSON o base de datos SQLite).
- Mejorar la estética con estilos de `ttk` personalizados o temas externos.
- Agregar validaciones más robustas en el formulario (ej. rango de edad).
- Incluir un archivo `sample.csv` de ejemplo dentro del repositorio.
- Internacionalización (traducciones en varios idiomas).

---

## 6. Casos de uso
- Ejemplo educativo para aprender `tkinter`.
- Plantilla base para proyectos más grandes.
- Demostración de CRUD simple y manejo de archivos.

---

## 7. Licencia
Este proyecto puede distribuirse libremente con fines educativos o de aprendizaje.  
Se recomienda incluir una licencia oficial (ej. MIT, GPL, Apache 2.0) si se publica en GitHub.
