# HAMIDOU AI — Android starter project

واجهة Android عربية تعمل عبر WebView وتضم ملفات HTML/CSS/JavaScript محلياً.

## هيكلة المشروع

- `settings.gradle`: إعداد وحدات Gradle والمستودعات.
- `build.gradle`: إصدارات إضافات Android وKotlin.
- `gradle.properties`: إعدادات Gradle وAndroidX.
- `app/build.gradle`: إعداد تطبيق Android.
- `app/src/main/AndroidManifest.xml`: تعريف التطبيق والصلاحيات.
- `app/src/main/java/com/hamidou/ai/MainActivity.kt`: شاشة WebView.
- `app/src/main/assets/web/`: ملفات الواجهة `index.html` و`style.css` و`app.js`.
- `.github/workflows/android.yml`: بناء APK تلقائياً باستخدام GitHub Actions.

## إنشاء APK من الهاتف عبر GitHub

1. فك ضغط الملف ZIP.
2. أنشئ مستودعاً جديداً على GitHub وارفع **محتويات** المجلد إلى الفرع `main` (لا ترفع ملف ZIP وحده).
3. افتح تبويب **Actions** في المستودع.
4. اختر **Build HAMIDOU AI APK** ثم **Run workflow**، أو انتظر البناء بعد رفع الملفات.
5. بعد نجاح العملية، افتح نتيجة التشغيل ونزّل Artifact باسم `HAMIDOU-AI-APK`.
6. فك ضغط Artifact لتحصل على `app-debug.apk` وثبّته على هاتف Android.

## المتطلبات

- Android Gradle Plugin 8.7.3
- Kotlin Android plugin 2.0.21
- Gradle 8.9
- JDK 17
- Android SDK 35

## حدود النسخة

هذه نسخة بداية قابلة للبناء كتطبيق Android. الواجهة تُنشئ وصفاً منظماً للفيديو وتنسخه؛ **لا تولّد فيديو MP4 فعلياً**. التوليد الحقيقي يتطلب ربط Backend بخدمة توليد فيديو خارجية، مع حفظ مفاتيح API على الخادم وعدم وضعها داخل التطبيق.
