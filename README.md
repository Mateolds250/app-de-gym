# Mi Gym — app Android

App de entrenamiento (plan de 8 semanas, temporizador de descanso, progresión de peso,
recuperación muscular, recordatorios nativos). Hecha con HTML/JS + Capacitor.

## Compilar el APK sin instalar nada (GitHub Actions)
1. Crea un repositorio en GitHub (público o privado) y sube TODO el contenido de esta carpeta.
2. Ve a la pestaña **Actions** → "Compilar APK de Mi Gym" → **Run workflow** (o simplemente haz push a `main`).
3. Cuando termine (5–8 min), abre la ejecución y descarga el artefacto **MiGym-APK** → dentro está `app-debug.apk`.
4. Pásalo por WhatsApp/Drive. En Android: abrir el archivo → permitir "instalar apps de esta fuente" → Instalar.

## Compilar local (Android Studio)
    npm install
    npx cap sync android
    npx cap open android      # Build > Build APK(s)

## Editar la app
Todo el código está en `www/index.html`. Después de cambiarlo: `npx cap sync android` y vuelve a compilar.

## Publicar en Google Play (opcional)
Requiere cuenta de desarrollador (pago único de US$25), un APK/AAB firmado con tu llave
(`./gradlew bundleRelease`) e íconos/capturas. El `applicationId` es `com.mateocardenas.migym`.
