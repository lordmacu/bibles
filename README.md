# Bible Versions Repository

Este repositorio contiene versiones encriptadas de la Biblia en formato SQLite para la aplicación Biblia IPUC.

## 📋 Contenido

- `versions.json` - Índice de todas las versiones disponibles con metadata
- `*.dat` - Archivos ZIP encriptados con las bases de datos SQLite
- `index.html` - Página simple para servir los archivos

## 🔐 Seguridad

Todos los archivos de base de datos están encriptados usando AES-256-GCM con:
- **Algoritmo**: AES-256-GCM
- **KDF**: PBKDF2-HMAC-SHA256
- **Iteraciones**: 200,000
- **Salt y Nonce únicos** por versión

## 📚 Versiones Disponibles

- **RVR1960** - Reina Valera 1960
- **NVI** - Nueva Versión Internacional 1999
- **RVC** - Reina Valera Contemporánea
- **PDT** - Palabra de Dios para Todos
- **RVG** - Reina Valera Gómez 2010
- **BLS** - Biblia en Lenguaje Sencillo
- **NTV** - Nueva Traducción Viviente

## 🌐 GitHub Pages

Este repositorio está configurado para GitHub Pages para servir los archivos a través de:

```
https://lordmacu.github.io/bibles/versions.json
https://lordmacu.github.io/bibles/<version>.dat
```

## 📱 Uso en la App

La aplicación Biblia IPUC descarga estas versiones encriptadas, las desencripta localmente y las indexa con FTS5 para búsqueda de texto completo.

## 🔧 Scripts

- `scripts/encrypt_versions.py` - Encripta las versiones de la Biblia
- Otros scripts de procesamiento

## ⚠️ Notas

- Los archivos no encriptados (`.sqlite`, `.zip`) no están en el repositorio
- Solo los `.dat` encriptados son públicos
- El `index.html` incluye meta tags `noindex` para evitar indexación por buscadores
