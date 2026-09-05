# CHRONOS · El archivo de las cinco curvas

Escape room cooperativo para interpretar gráficas del movimiento en Bachillerato General Unificado (BGU).

- **Abrir el recurso:** https://mguerreroz-rgb.github.io/chronos/
- **Guía docente:** https://mguerreroz-rgb.github.io/chronos/guia-docente.html
- **Windows y archivos de la publicación:** https://github.com/mguerreroz-rgb/chronos/releases

Cuatro participantes comparten una partida de veinte desafíos en cuatro misiones. La experiencia incluye turnos rotativos, preguntas socráticas, puntuación colectiva, opciones de accesibilidad, reporte final y diplomas.

## Autoría del recurso

Marcos Guerrero Zambrano · Bryan Valarezo Chamba · Leonor Sánchez Alvarado.

El recurso original identifica su licencia como **Creative Commons BY-NC-SA**, sin indicar versión. Esta adaptación conserva esa atribución; no atribuye una versión de licencia, afiliación institucional o DOI que no figure en los archivos entregados. Las bibliotecas incluidas mantienen sus avisos originales.

## Qué contiene esta publicación

La entrega recibida como versión 5.2 incluye un export compilado de HTML, CSS y JavaScript. No contiene el proyecto de edición original de React. Se conserva el juego, sus preguntas y sus recursos, y se añade una portada, una guía docente y un arranque estático independiente del enrutador del export original.

Las importaciones de PDF conservan rutas relativas. La partida y las preferencias se guardan en el navegador; si el almacenamiento está bloqueado, se utiliza memoria de sesión y se muestra un aviso. No hay una base de datos del proyecto ni sincronización entre dispositivos.

## Ejecutar la edición web

Se necesita Node.js 22 o superior para estos comandos. No hay dependencias que instalar.

```sh
node scripts/build.mjs
node scripts/check.mjs
node scripts/serve.mjs --dist
```

Abrir `http://127.0.0.1:4173/chronos/`. El servidor local reproduce la subcarpeta de GitHub Pages y admite solicitudes parciales de audio.

- `src/`: portada, guía y aplicación web.
- `scripts/`: preparación, comprobaciones y servidor de desarrollo.
- `dist/`: archivos estáticos generados para publicar.
- `verification.json`: identidad de la entrega original y huella del banco de preguntas.

El archivo `CHRONOS-web-fuentes.zip` de la versión publicada contiene estos archivos de edición completos. GitHub Actions comprueba su SHA-256, ejecuta las comprobaciones y publica únicamente `dist/` en Pages. El ejecutable Windows se distribuye como archivo de la versión, separado de la web.

## Límites de la verificación

Se comprueban sintaxis JavaScript, integridad del banco de preguntas, permutación de respuestas, recursos y rutas internas, metadatos y tolerancia a fallos de almacenamiento. Estas comprobaciones no sustituyen una sesión manual completa en cada navegador ni verifican el ejecutable Windows.

La versión web necesita conexión para cargar los recursos. La síntesis de voz depende de las voces del sistema. Se recomienda una pantalla amplia y un dispositivo compartido por equipo. Los diplomas documentan participación y no certifican dominio permanente.
