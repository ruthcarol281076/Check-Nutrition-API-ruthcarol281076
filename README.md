# Check-Nutrition-API-ruthcarol281076
Proyecto PreWork AI Engineering Introduction - Automatización Verificar Nutrición

## Automatización 
Se automatiza con un flujo de n8n, se adjunta archivo JSON de la automatización. 
  . Nombre de archivo: 
El flujo se ha representado en un diagrama adjunto en esta carpeta. 
  . Nombre de archivo: DiagramaExcalidrawProyectoNutricionSnack_06sep2026.png

## Como funciona
ESte proyecto de automatización en n8n, es una API que realiza la evaluación nutricional de un snack, usando el código de barras del producto para indicar al cliente si el snack es 'saludable' o 'no saludable'.

## Configuración / Instalación
No requiere instalación, solo el uso de plataformas como https://hoppscotch.io/, para lanzar una petición y obtener una respuesta. Igualmente vincular esta API con su aplicativo para enviar el código de barra y recibir la respuesta.

## Uso
### Petición 
Realizar petición a las siguientes URLs
  . Test: https://ruthcarol2810.app.n8n.cloud/webhook-test/nutrition-check
  . Production: 
JSON de Entrada - Ejemplo:
{ "barcode": "8480000239266" }

### Respuesta Salida exitosa
Se responde un texto estructurado en secciones con el resultado de la evaluación nutricional del snack y sugerencias sobre su consumo.

### Respuesta Salida con fallo
JSON de Salida - Ejemplo:
{
  "message": "Check Nutrition API",
  "version": "1.0",
  "respond": "Disculpe las molestias. El código de barras debe estar presente y contener únicamente dígitos numéricos. Por favor, inténtelo de nuevo con un código de barras válido. Si el problema persiste, póngase en contacto con nuestro servicio de soporte para recibir asistencia.",
  "usage": {
    "endpoint": "POST a esta URL de webhook",
    "required": {
      "barcode": "Código de barras (ej., 3017620422003)"
    },
    "example1": {
      "barcode": "3017620422003"
    },
    "example2": {
      "barcode": "8480000168832"
    }
  }
}

## Limitaciones 

## License

[MIT](https://choosealicense.com/licenses/mit/)
