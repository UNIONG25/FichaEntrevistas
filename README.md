# 📄 Sistema de Gestión Documental con Recorte CamScan & OCR (V4_MultiOCRbeta)

**Aplicación web de escaneo inteligente, recorte perspectivo y extracción de datos mediante OCR.**

Desarrollado por: **Antonio Altuna** | **Año:** 2026  
📞 0412-7294298 | ✉️ altuna.g1@gmail.com

---

## 📖 Descripción

**V4_MultiOCRbeta** es una herramienta web standalone diseñada para digitalizar, procesar y estructurar documentos físicos. Combina un **recorte perspectivo inteligente (estilo CamScanner)** con un motor **OCR (Reconocimiento Óptico de Caracteres)** altamente configurable. 

La aplicación permite extraer información literal, estructurar fichas de identificación (Cédula/RIF) y digitalizar tablas contables directamente desde el navegador, sin necesidad de servidores externos.

---

## ✨ Características Principales

- ✂️ **Recorte Perspectivo Inteligente:** Sistema de 4 puntos de control (círculos verdes) para recortar, enderezar y eliminar el fondo de cualquier documento.
- 🔍 **Motor OCR Multilenguaje:** Soporte para Español, Inglés y combinaciones.
- ⚙️ **Configuración Adaptativa:** Ajuste de OCR según el tipo de papel (Térmico/Químico, Foto de celular, PDF nítido) y disposición del texto.
- 💾 **Base de Datos Local:** Almacenamiento persistente en el navegador (LocalStorage) para fichas y documentos.
- 📄 **Exportación a PDF:** Generación de reportes y fichas en formato A4 (Horizontal/Vertical) listos para imprimir.
- 📱 **100% Responsive:** Funciona en PC, Tablets y Smartphones (aprovecha la cámara nativa del dispositivo).

---

## 🚀 Modos de Escaneo

La aplicación cuenta con 4 motores de extracción especializados:

### 1. 🧾 Factura / Pago / POS
Diseñado para comprobantes fiscales, tickets térmicos y cierres POS.
- **Extracción literal:** Fecha, Emisor, RIF, Nro. Factura/Control.
- **Cálculos monetarios:** Base Imponible, Exento, IVA, Total en Bolívares (Bs) y Total en Divisas (USD).

### 2. 🪪 ID - Identificación (Cédula / RIF)
Especializado en documentos de identidad y comprobantes del SENIAT.
- Recorta automáticamente el formato de carnet.
- Genera una **Ficha Estructurada** editable con: N° Cédula/RIF, Apellidos, Nombres/Razón Social, Estado Civil, Fechas (Nacimiento, Expedición, Vencimiento) y Domicilio Fiscal.

### 3. 📄 Documento Normal
Para cartas, oficios, certificados y documentos legales generales.
- Extracción de texto continuo con preservación de párrafos.
- Ideal para archivos digitales y respaldos legales.

### 4. 📊 Tabla / Documento Contable
Para estados financieros, balances de comprobación y reportes tabulares.
- Detecta columnas y filas automáticamente.
- Estructura la data en formato contable: **Concepto | Referencia | Debe | Haber**.
- Permite agregar o editar filas manualmente antes de guardar.

---

## 🛠️ Cómo Usar

### Paso 1: Captura
Selecciona el modo de escaneo y toma una foto con la cámara de tu dispositivo o sube una imagen desde la galería.

### Paso 2: Recorte CamScan
Se activará la herramienta de recorte. **Arrastra los 4 círculos verdes** hacia las esquinas exactas de tu documento. El sistema enderezará la perspectiva y eliminará el fondo automáticamente.

### Paso 3: Extracción OCR
Haz clic en **"EXTRAER DATOS"**. El motor procesará la imagen según la configuración de idioma y tipo de papel seleccionada.

### Paso 4: Edición y Validación
Revisa los campos extraídos. Todos los campos son **100% editables** para corregir cualquier error de lectura del OCR. Puedes re-analizar el texto crudo si es necesario.

### Paso 5: Guardar y Exportar
- Haz clic en **"GUARDAR EN BASE DE DATOS"** para almacenar la ficha en tu navegador.
- Usa la **"Vista Previa"** para descargar el documento final en **PDF**.

---

## 💻 Tecnologías Utilizadas

- **Frontend:** HTML5, CSS3, JavaScript (ES6+).
- **Motor OCR:** [Tesseract.js](https://github.com/naptha/tesseract.js) (Procesamiento de imagen y texto en el lado del cliente).
- **Almacenamiento:** Web LocalStorage / IndexedDB.
- **Gráficos:** Canvas API (para el warp perspectivo y manipulación de imágenes).

---

## 📦 Instalación y Despliegue

Esta aplicación es **100% del lado del cliente (Client-Side)**, lo que significa que no requiere instalación de servidores, bases de datos SQL ni dependencias de backend.

1. Descarga o clona el archivo `V4_MultiOCRbeta.html`.
2. Ábrelo directamente en cualquier navegador moderno (Chrome, Edge, Firefox, Safari).
3. *Opcional:* Para usar la cámara en dispositivos móviles, sirvelo a través de un servidor local (ej. `Live Server` en VS Code) o súbelo a un hosting estático (GitHub Pages, Netlify) con certificado **HTTPS** (requisito de los navegadores para acceder a la cámara).

---

## 📂 Estructura del Proyecto

```text
V4_MultiOCRbeta/
│
├── V4_MultiOCRbeta.html   # Archivo principal (Contiene HTML, CSS y JS)
├── README.md              # Documentación del proyecto
└── assets/                # (Opcional) Logos o recursos estáticos
