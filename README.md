# Plataforma de Cumplimiento · Saving The Amazon

Sitio estático (HTML/CSS/JS sin build ni dependencias) con tres herramientas:

- **`index.html`** — página de inicio que enlaza las tres piezas.
- **`sistema-vinculacion-proveedores.html`** — datos institucionales, documentos con vigencia, ficha imprimible en PDF y seguimiento de solicitudes.
- **`plataforma-debida-diligencia.html`** — registro de contrapartes, verificación de listas restrictivas (Interpol en vivo + 9 fuentes guiadas) y constancia descargable.
- **`manual-vinculacion-proveedores.html`** — guía de uso del Sistema de Vinculación.

## Cómo funciona

Cada herramienta guarda sus datos en el `localStorage` del navegador de quien la usa — no hay backend ni base de datos. Para compartir información entre personas se usan los botones de descarga (ficha, constancia) dentro de cada herramienta.

La verificación de antecedentes consulta en vivo la API pública de Interpol (`ws-public.interpol.int`) directamente desde el navegador.

## Desarrollo local

No requiere instalación. Basta con servir la carpeta con cualquier servidor estático, por ejemplo:

```bash
python3 -m http.server 8000
```

y abrir `http://localhost:8000`.

## Despliegue

Publicado con GitHub Pages desde la rama `main`.
