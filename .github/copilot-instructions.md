# Copilot Instructions for con_fuego_aprendo

## Overview
Este proyecto es un simulador educativo web para enseñar el uso de extintores y la identificación de tipos de fuego. Está orientado a niños y pensado para funcionar en pantallas grandes (TV) y dispositivos móviles. La experiencia incluye tarjetas informativas y un simulador interactivo.

## Estructura principal
- `index.html`: Pantalla principal, contiene tarjetas educativas, navegación tipo slider y guía por voz.
- `simulador.html`: Simulador interactivo donde el usuario responde preguntas o realiza acciones.
- Imágenes y recursos: Todos los assets (PNG, JPG, GLB, MP3) están en la raíz para fácil acceso.

## Convenciones y patrones
- **Diseño responsivo**: Usa unidades relativas (`vw`, `rem`) y media queries para adaptar a TV y móvil.
- **Interactividad**: La navegación entre tarjetas se realiza con botones y eventos `onclick`. La guía usa `SpeechSynthesis` para voz.
- **QR fijo**: Se muestra un QR en la pantalla para acceso móvil, usando un servicio externo.
- **Simulador**: El avance depende de la respuesta del usuario; si el juego no avanza, revisar la lógica JS en `simulador.html`.

## Flujos clave
- No hay build ni test automatizados; los cambios se ven directamente en el navegador.
- Para depurar, usar las herramientas de desarrollador del navegador (F12).
- Para agregar nuevas tarjetas, copiar la estructura de las existentes en `index.html`.
- Para modificar preguntas/respuestas del simulador, editar directamente en `simulador.html`.

## Integraciones
- El simulador puede integrarse en Bitrix24 mediante iframe/widget.
- El QR usa `api.qrserver.com` para generar el código.

## Ejemplo de patrón de tarjeta
```html
<div class="card" onclick="hablar('Clase A. Papel, cartón, madera y tela. Se apagan con agua o espuma.')">
  <img src="oficina_papelera.png" alt="Clase A">
  <h3>Clase A - Materiales sólidos</h3>
  <p>Incluyen papel, cartón, madera y telas.</p>
  <p>Se apagan con <strong>agua</strong> o <strong>espuma</strong>.</p>
</div>
```

## Recomendaciones para agentes
- Mantener la experiencia simple y visual, evitando sobrecargar de texto o elementos.
- Priorizar la accesibilidad y legibilidad en todos los cambios.
- Documentar nuevas preguntas/respuestas en el README para revisión pedagógica.

---
¿Falta algún flujo, integración o convención importante? Indica si necesitas que se detalle alguna sección o patrón específico.
