# iceTaskTwo — Android + Auth + Biometric + Backend

This package includes:
- **Android** app (Kotlin) with **Google Sign-In (Firebase Auth)** and **BiometricPrompt** login.
- **Retrofit** client communicating with your MemeStream REST API.
- **Backend** from Task One located at `MemeStream/01-RestfulAPI`.

## Android Setup
1. Open the `Android/` folder in Android Studio (Giraffe+).
2. Add your **Firebase configuration**:
   - Place `google-services.json` from Firebase Console into `Android/app/`.
   - Enable **Google** authentication in Firebase Authentication settings.
   - Add the **Web client ID** to `strings.xml` as `default_web_client_id` (create it if missing).
3. Update the API base URL in `ApiClient.kt` if your backend is deployed elsewhere.
4. Run the app: first log in with Google, then optionally enable biometrics for quicker access.

## Backend Setup
- Node/Express API is under `MemeStream/01-RestfulAPI`.
- Run `npm install`, set your `.env` file, then start with `npm start`.
- On the Android emulator, use `http://10.0.2.2:8080/` to access the backend.

## Notes
- Minimum SDK version: 23; uses `androidx.biometric`.
- Replace placeholders, icons, or strings as needed.
