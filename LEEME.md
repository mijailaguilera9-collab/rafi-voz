# Lectura en voz alta · prototipo (paso 1)

Una sola página (`index.html`), sin servidor, sin cuentas y **sin guardar nada**. Sirve para comprobar, con Chromebooks y estudiantes reales, qué tan bien funciona el reconocimiento de voz midiendo palabras correctas por minuto.

## Cómo publicarla para probarla (GitHub Pages, gratis)
1. Crea una cuenta en github.com (puede ser la personal) y un repositorio **público** nuevo, por ejemplo `rafi-voz`.
2. «Add file → Upload files» y sube `index.html` a la raíz.
3. «Settings → Pages → Build and deployment»: Source «Deploy from a branch», rama `main`, carpeta `/ (root)`, Save.
4. En uno o dos minutos la página queda en `https://TU-USUARIO.github.io/rafi-voz/`. Ábrela en el Chromebook (Chrome).

Importante: el repositorio es público, así que cualquiera con el enlace puede abrir la página. Este prototipo solo contiene 12 textos de muestra de tu banco de Dominio Lector y no guarda datos de nadie. Si prefieres no exponer esos textos, dime y los cambio por otros.

## Cómo probarla
1. Abre la página en un Chromebook y elige curso y texto. «Probar micrófono» debe mover la barra.
2. «Empezar a leer»: cuenta regresiva de 3 y un minuto de lectura. Chrome pedirá permiso de micrófono la primera vez.
3. En el resultado, toca las palabras rojas que sí se leyeron bien (y las que se marcaron bien siendo un error). Así medimos cuánto se equivoca el reconocedor.
4. «Copiar datos de la prueba» y pégalos en el chat. No llevan nombre ni audio.

Haz la prueba con 3 o 4 estudiantes de distintos cursos (3° a 8°), idealmente uno con lectura vacilante, con audífonos con micrófono y sin ellos.

## Pruebas rápidas
- `?dur=10` al final de la dirección acorta la lectura a 10 segundos (solo para ensayar).
- «Opciones avanzadas» permite cambiar el idioma del reconocimiento (es-CL, es-419, es-ES, es-MX) para comparar.

## Qué mide y cómo
- Compara lo que oyó con el texto, ignorando tildes, mayúsculas y puntuación, y tratando como iguales sonidos del español (b/v, s/z/c, ll/y, h muda).
- Tolera repeticiones, palabras que el reconocedor une o parte, y ruido.
- Las palabras casi iguales (una letra de diferencia) quedan «dudosas» y cuentan como bien leídas hasta que se revisen.
- Palabras correctas por minuto = (palabras leídas − errores) × 60 / segundos, igual que el panel 2, con las mismas categorías por curso.
- El resultado automático es un borrador: la revisión humana manda.

## Privacidad
No se graba ni guarda audio. Chrome envía el sonido a Google en el momento para convertirlo en texto. Eso hay que informarlo y acordarlo con el colegio antes de usarlo con estudiantes de forma regular.
