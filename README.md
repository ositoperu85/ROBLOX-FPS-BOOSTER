# ROBLOX FPS BOOSTER — prototipo Android

Proyecto inicial para Android Studio. `minSdk = 26` (Android 8.0).

## Qué hace esta versión
- Muestra una ventana flotante que se puede arrastrar.
- Detecta y muestra la frecuencia de refresco de la pantalla en Hz.
- Mantiene el indicador mediante un servicio en primer plano.

## Limitación importante
Esta versión **no mide los FPS reales de Roblox**. Una app Android normal no puede consultar directamente los FPS de otro proceso/juego. Los Hz de la pantalla no son lo mismo que los FPS que Roblox está renderizando. El indicador está etiquetado como `PANTALLA: xx Hz` para no presentar datos falsos.

Tampoco fuerza Roblox a 60/120 FPS ni modifica sus archivos. El resultado depende del dispositivo, la pantalla, Android y los límites del propio juego.

## Compilar APK
1. Instala Android Studio en una PC.
2. Abre esta carpeta como proyecto.
3. Deja que Gradle sincronice y descargue los componentes solicitados.
4. Ve a **Build > Build Bundle(s) / APK(s) > Build APK(s)**.
5. El APK de prueba aparecerá en `app/build/outputs/apk/debug/app-debug.apk`.

## Prueba
- Instala el APK en un dispositivo Android 8 o superior.
- Abre la app y pulsa **ACTIVAR MEDIDOR FLOTANTE**.
- Concede el permiso de “Mostrar sobre otras aplicaciones”.
- Arrastra el indicador a una esquina y abre Roblox.
- Toca el indicador para cerrarlo; también puedes detenerlo desde la app.

Este es un prototipo de desarrollo y debe probarse en distintos fabricantes/versiones de Android antes de distribuirlo.
