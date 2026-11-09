# Código MEDIR: escape del consultorio

Actividad para el segundo parcial de **Teoría de la Medida** (Licenciatura en Psicología Clínica, Universidad de Guanajuato).

Escape room educativo para jugar **por parejas** (un celular o laptop por pareja, aprox. 60 min). La pareja queda encerrada en el consultorio de la Dra. Escala y debe abrir 5 salas; cada sala entrega una letra de la palabra final:

1. **El archivero de las técnicas**: pruebas proyectivas vs. psicométricas.
2. **La línea de ensamblaje**: pasos para desarrollar una prueba.
3. **El mapa del constructo**: dimensiones, subtemas e indicadores.
4. **El taller de ítems**: redacción de ítems.
5. **La puerta Likert**: escala Likert y redacción de un ítem propio.

Al final se genera una **Constancia de escape** (nombres, grupo, fecha, tiempo, puntaje, pistas usadas, el ítem Likert redactado y referencias APA 7) que se puede imprimir/guardar en PDF o capturar.

## Reglas de puntaje
- 20 puntos por sala (100 en total).
- −1 por cada «Comprobar» incorrecto; −3 por cada pista (3 pistas por partida).
- Mínimo 5 puntos por sala completada.

## Archivos
| Archivo | Para qué sirve |
|---|---|
| `index.html` | Página de la actividad. |
| `css/estilos.css` | Diseño (consultorio nocturno, dorados UG). |
| `js/contenido.js` | **Todo el contenido editable**: historia, retos, respuestas, pistas, retroalimentación y referencias. |
| `js/app.js` | Lógica del juego (no es necesario tocarla para cambiar textos). |
| `img/dra-escala.jpg` | Retrato de la Dra. Escala. |

Sin frameworks, sin dependencias externas ni cuentas. El avance se guarda en el navegador de cada dispositivo (botón **Reiniciar** para otra pareja).

## Modo docente
Permite revisar todas las salas sin resolverlas: abre cualquier sala, salta entre retos, muestra las pistas sin costo y tiene un botón **Mostrar respuesta**. También permite probar la puerta final y ver una constancia de ejemplo. No cuenta puntos ni modifica el avance guardado en el dispositivo.

- **Entrar:** en la pantalla de inicio, «Acceso docente», o agregando `#docente` al final de la dirección (sirve aunque una pareja ya haya empezado en ese dispositivo).
- **Salir:** botón «Salir» de la franja morada, o recargar la página.
- **Clave:** en `js/contenido.js` solo se guarda su versión cifrada (hash SHA-256 con sal), nunca la clave. Para cambiarla: dentro del modo docente, «Cambiar la clave docente», y reemplaza el bloque `docente` de `js/contenido.js` con el código que genera.
- **Límite:** al ser una página estática (sin servidor), la clave evita el acceso casual, pero no es una protección fuerte: las respuestas están en `js/contenido.js`, que cualquier persona con conocimientos técnicos puede leer desde el navegador.

## Publicar con GitHub Pages
**Settings → Pages → Build and deployment**: *Source* = **Deploy from a branch**, *Branch* = **main**, carpeta **/(root)** → **Save**. En uno o dos minutos estará en `https://psicmarcorl.github.io/Escape-Room-teoria-de-la-medida/`.

## Referencias
Meneses, J., Barrios, M., Bonillo, A., Cosculluela, A., Lozano, L. M., Turbany, J., & Valero, S. (2013). *Psicometría*. Editorial UOC.
