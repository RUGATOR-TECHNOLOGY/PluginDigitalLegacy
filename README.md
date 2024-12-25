# 💾 **Plugin Digital Legacy**

¡Bienvenido al proyecto Plugin Digital Legacy! 🌐 Este plugin está diseñado para facilitar la gestión de legados digitales, permitiendo a los usuarios configurar y automatizar el manejo de sus datos digitales en caso de eventos futuros.

![Status](https://img.shields.io/badge/Estado-En%20Desarrollo-yellow?style=flat-square)
![GitHub license](https://img.shields.io/github/license/RUGATOR-TECHNOLOGY/PluginDigitalLegacy?style=flat-square)
![GitHub version](https://img.shields.io/github/v/tag/RUGATOR-TECHNOLOGY/PluginDigitalLegacy?label=versión&style=flat-square)
![GitHub repo size](https://img.shields.io/github/repo-size/RUGATOR-TECHNOLOGY/PluginDigitalLegacy?style=flat-square)
![GitHub Repo stars](https://img.shields.io/github/stars/RUGATOR-TECHNOLOGY/PluginDigitalLegacy?style=social)

![GitHub issues](https://img.shields.io/github/issues/RUGATOR-TECHNOLOGY/PluginDigitalLegacy?style=flat-square)
![GitHub forks](https://img.shields.io/github/forks/RUGATOR-TECHNOLOGY/PluginDigitalLegacy?style=flat-square)
![GitHub last commit](https://img.shields.io/github/last-commit/RUGATOR-TECHNOLOGY/PluginDigitalLegacy?style=flat-square)
![GitHub Workflow Status](https://img.shields.io/github/actions/workflow/status/RUGATOR-TECHNOLOGY/PluginDigitalLegacy/main.yml?style=flat-square)


> [!NOTE]
> **Versión actual:** 1.0.0  
> **Plataforma WordPress:** v5.8^  
> **Compatibilidad PHP:** v8.0

> [!WARNING]
> Proyecto fase desarrollo.

---

## 📋 Indíce
- [Características](#-características)
- [Estructura](#-estructura)
- [Guía de uso](#-guía-de-uso)
- [Desarrollo](#-desarrollo)
- [Ejemplos de uso](#-ejemplos-de-uso)
- [Contribuciones](#-contribuciones)
- [Próximas mejoras](#-próximas-mejoras)
- [Créditos](#-créditos)
- [Licencia](#-licencia)

---

## 🌟 **Características**

✅ **Gestión del legado digital**: Configuración personalizada para delegar acceso o eliminar datos digitales.

✅ **Automatización**: Programación de acciones basadas en fechas específicas o triggers externos.

✅ **Seguridad**: Uso de claves de acceso y cifrado para proteger datos sensibles.

✅ **Notificaciones**: Sistema de alertas configurables para mantener a los usuarios informados.

✅ **Integración**: Compatible con WordPress y fácil de extender con otros plugins.

---

## 📂 **Estructura**

```plaintext
plugin-digital-legacy/
├── assets/            # Recursos estáticos como imágenes, CSS y JS
├── includes/          # Funcionalidades principales del plugin
│   ├── admin/         # Archivos relacionados con la configuración en el panel de administración
│   ├── public/        # Funciones accesibles desde la interfaz pública
│   └── utils/         # Utilidades y helpers
├── templates/         # Plantillas para vistas del plugin
├── languages/         # Archivos de traducción
├── tests/             # Pruebas unitarias y funcionales
├── plugin-digital-legacy.php  # Archivo principal del plugin
├── readme.txt         # Descripción para el repositorio de WordPress
└── README.md          # Este archivo
```
---

## 🚀 **Guía de instalación**
### 1. Requisitos previos
- WordPress >= 5.8
- PHP >= 8.0

### 2. Instalación
🔹Descargar el repositorio o el archivo ***.ZIP** del plugin.
🔹Accede a tu escritorio de administración de WordPress:

```
Plugins > Añadir Nuevo > Subir Plugin
```
🔹Selecciona el archivo ***.ZIP** y haz clic en "Instalar Ahora".
🔹Activa el plugin desde la lista de plugins instalados.

---

## 🛠️ **Desarrollo**
### Scripts útiles
- Formatear código:

```
bash dev-tools/format.sh
```

- Ejecución de pruebas:

```
bash dev-tools/test.sh
```

### Requisitos de desarrollo
🔹Instala las dependencias de desarrollo:
```
composer install
npm install
```

## 🛠️ **Ejemplos de uso**
### 🛡️Configuración Básica
1. Accede a la página de configuración del plugin:
```
Ajustes > Digital Legacy
```
2. Configura el destino de los datos en caso de activación.
3. Guarda los cambios y prueba el sistema con datos de ejemplo.

---

- ``url``: URL inicial para comenzar el rastreo.
- ``max_webs``: Número máximo de páginas a rastrear.
- ``output-folder``: Carpeta destino para los archivos JSON.

---

#### 📇 Indexer
Construye un índice invertido a partir de los archivos JSON generados por el Crawler:

```
python -m src.indexer.app --input-folder ./etc/webpages --output-name ./etc/indexes/inverted_index.bin
```
**Parámetros:**
- ``--input-folder``: Carpeta con los archivos JSON generados por el Crawler.
- ``--output-name``: Archivo donde se almacenará el índice invertido.

---

#### 🔍 Retriever
Resuelve consultas utilizando el índice invertido:
```
python -m src.retriever.app --index-file ./etc/indexes/inverted_index.bin --query "grado AND NOT master OR docencia"
```

**Parámetros:**
- ``--index-file``: Ruta al índice invertido generado por el Indexer.
- ``--query``: Consulta a resolver.

---

#### 🛠️ Desarrollo
**Scripts Útiles**
- Formatear Código:
```
bash dev-tools/format.sh
```
- Análisis Estático:
```
bash dev-tools/lint.sh
```
**Requisitos de Desarrollo**
Instala las dependencias adicionales para desarrollo:
```
pip install -r dev-requirements.txt
```

---

#### 🧪 Ejemplos de Consultas
| Consulta | Descripción |
|:----------|:-------------|
| ``grado AND NOT master`` | Recupera páginas con "grado" y sin "master". |
| ``docencia OR investigación``	| Recupera páginas con cualquiera de las palabras. |
| ``universidad AND europea``	| Recupera páginas que contienen ambas palabras. |

---

## 🗂️ Contribuciones
### 🤝 ¿Quieres colaborar? ¡Eres bienvenido! Sigue estos pasos:

🔹1. Haz un fork de este repositorio.

Haz clic en el botón **Fork** en la parte superior derecha de la página para crear una copia de este repositorio en tu cuenta.

Clona tu copia del repositorio a tu máquina local:
```bash
git clone https://github.com/RubenGamezTorrijos/NOMBRE_REPOSITORIO.git
cd NOMBRE_REPOSITORIO
```
🔹2. Crea un branch para tu funcionalidad:
```
git checkout -b mi-rama
```
Haz los cambios en el código o añade nuevas funcionalidades según sea necesario. Asegúrate de seguir las guías de estilo del proyecto.
🔹3. Haz un commit con tus cambios:
```
git add .
git commit -m "Descripción clara de los cambios realizados"
```
🔹4. Sube tus cambios:
```
git push origin mi-rama.
```
🔹5. Abre un pull request en este repositorio.
- Ve al repositorio original del proyecto.
- Haz clic en la pestaña Pull Requests.
- Haz clic en New Pull Request.
- Selecciona tu rama desde el repositorio forkeado y compárala con la rama principal (main o master) del repositorio original.
- Describe brevemente los cambios realizados y envía la solicitud.

> [!NOTE]:
>  Los cambios en el main o master, deberán ser aprobados por el propietario.
---

## 🤖 Próximas Mejoras
- Implementar ranking de resultados basado en relevancia (TF-IDF).
- Ampliar soporte para búsqueda en documentos PDF.
- Optimizar el tiempo de rastreo con paralelización del Crawler.

---

## ✨ Créditos
Este proyecto no sería posible sin la dedicación de sus integrantes:

- **Luca 🕷️** - Implementación del módulo Crawler
- **Sergio 📇** - Implementación del módulo Indexer
- **Rubén 🔍** - Implementación del módulo Retriever
Agradecemos también a la Universidad Europea por inspirar este proyecto académico. 🙌

---

## 📝 Licencia
Este proyecto está bajo la licencia Apache 2.0. ¡Siéntete libre de usarlo, modificarlo y compartirlo!

