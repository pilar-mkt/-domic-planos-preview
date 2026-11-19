# DOMIC Experiences · Landing para subir planos

Landing minimalista para que los clientes de DOMIC suban sus planos y estos lleguen al equipo por email. Sigue el estilo visual de domicexperiences.com: tipografía Inter, paleta oscura y crema, botón bronce.

## Archivos

| Archivo | Para qué es |
|---|---|
| `index.html` | Vista previa para presentar. Incluye selector English / Español y una zona de subida de muestra (no envía nada). Se publica con GitHub Pages. |
| `ghl/domic-plans-en.html` | Versión final en inglés para pegar en un elemento **Custom Code** de GoHighLevel. |
| `ghl/domic-plans-es.html` | Versión final en español, igual que la anterior. |

## Configuración en GoHighLevel

1. **Formulario por idioma** (Sites > Forms): uno en inglés y otro en español, con un campo **File Upload** (varios archivos, PDF, DWG, JPG, PNG). Estilo sugerido: fondo `#eeece5`, botón `#73583b` con texto blanco.
2. **Embed**: en *Integrate*, copiar el ID del formulario y reemplazar `FORM_ID_EN` o `FORM_ID_ES` en el archivo correspondiente (aparece 4 veces).
3. **Workflow**: disparador *Form Submitted* (los dos formularios) y acción *Send Internal Notification > Email* al mail de DOMIC, incluyendo el campo de archivos.

Nota: GHL envía los archivos como links de descarga, no como adjuntos. Además, sin un campo de email o teléfono el envío no queda asociado a un contacto, así que conviene probar un envío real antes de publicar.
