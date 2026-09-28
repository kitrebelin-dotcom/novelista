# Novelista para Android (APK)

Contiene la app (`www/index.html`) ya envuelta con Capacitor. Hay dos caminos para obtener el APK.

## Camino A: sin instalar nada (GitHub, gratis)
1. Crea una cuenta en github.com y un repositorio nuevo (privado o público).
2. Sube TODO el contenido de esta carpeta (incluida la carpeta oculta `.github`).
3. Ve a la pestaña **Actions** > "Construir APK" > **Run workflow**.
4. En ~5-10 minutos aparece el archivo **Novelista-APK** al final de la ejecución. Descárgalo, descomprímelo.
5. Pasa `app-debug.apk` al celular, ábrelo y acepta "instalar apps de origen desconocido".

## Camino B: en tu computadora
Requiere Node 18+, Java 17 y Android Studio (SDK).
    npm install
    npx cap add android
    npx cap sync android
    cd android && ./gradlew assembleDebug
El APK queda en `android/app/build/outputs/apk/debug/app-debug.apk`.

## Notas
- Es un APK de prueba ("debug"): sirve para instalar en tu celular, no para subir a Google Play.
- Todo se guarda dentro del teléfono. Exportar abre el menú de compartir/guardar de Android.
- Para modificar la app, edita `www/index.html` y repite los pasos.
