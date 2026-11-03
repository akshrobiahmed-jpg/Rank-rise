# Build RANKRISE APK on GitHub (phone-friendly)

1. Create a new **private** repository on https://github.com/new.
2. Upload the contents of this folder to the repository's `main` branch (not the outer folder itself).
3. Open the repository's **Actions** tab and select **Build RANKRISE APK**.
4. Tap **Run workflow**. Wait for the workflow to finish successfully.
5. Open the completed workflow run. Under **Artifacts**, download `RANKRISE-debug-APK`.
6. Extract the artifact ZIP and install the APK on your Android phone. If prompted, allow your browser or file manager to install unknown apps.

Notes:
- This workflow builds a debug APK for testing. It is not a Play Store release build.
- The project needs credentials/configuration for optional online services such as Gemini/Firebase. Do not commit API keys or `.env` files to a public repository.
- The workflow creates a temporary debug signing key for each run. Rebuilding may produce an APK that cannot update an earlier install; uninstall the old debug build first if Android reports a signature conflict.
