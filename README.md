# MediaHub Android (Catálogo TMDB, IPTV/M3U, Web Sniffer & Modo Dormir OLED)

Projeto Android completo em **Kotlin + Clean Architecture + Jetpack Media3 (ExoPlayer) + Room Database**.

## Como Gerar o `.apk` Pronto para Instalar

### Opção 1: Pelo GitHub Actions (Sem precisar instalar Android Studio no PC)
1. Crie um repositório no seu GitHub (pode ser privado) e envie todos os arquivos deste pacote.
2. O arquivo `.github/workflows/build_apk.yml` já está configurado: na aba **Actions** do seu repositório, o GitHub compila o aplicativo automaticamente e disponibiliza o arquivo **`MediaHub-debug-apk` (`app-debug.apk`)** para download direto no celular.

### Opção 2: Pelo Android Studio / Linha de Comando Local
1. Extraia este arquivo `.zip` e abra a pasta no **Android Studio (Ladybug / Koala ou superior)**.
2. Opcional: No arquivo `app/build.gradle.kts`, substitua `SUA_CHAVE_TMDB_AQUI` pela sua chave da API v3 do TMDB (o app já conta com dados de demonstração funcionais e streams HLS de teste caso você compile sem chave).
3. Execute no terminal ou no menu **Build > Build Bundle(s) / APK(s) > Build APK(s)**:
   ```bash
   ./gradlew assembleDebug
   ```
4. O instalador estará em `app/build/outputs/apk/debug/app-debug.apk`.
