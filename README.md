# HamzaPost (Flutter Web/Mobile)

تطبيق Flutter بسيط يجمع عناوين أخبار المغرب من Google News RSS ويعرضها كبطاقات مع دعم العربية RTL والفرنسية والإنجليزية.

## التشغيل محليًا
```bash
flutter pub get
flutter config --enable-web
flutter run -d chrome
```

## البناء للويب
```bash
flutter build web --release
```
سيتولد مجلد `build/web` يمكن نشره على Netlify أو Vercel (سحب وإفلات).

## النشر عبر GitHub Pages (بدون تثبيت Flutter)
1. ارفع هذا المشروع إلى GitHub على فرع `main`.
2. اذهب إلى Settings → Pages واجعل المصدر `gh-pages` بعد أول نشر.
3. كل Push على `main` سيبني تلقائيًا موقع Flutter Web وينشره على:
`https://<username>.github.io/<repo-name>/`

## تعديل المصادر
روابط RSS في `assets/feeds.json`. أضِف/عدّل حسب الحاجة.

## ملاحظات
- على الويب: المقالات تُفتح في تبويب جديد.
- على الهاتف: تُفتح داخل WebView (تحتاج إضافة إعدادات المنصات إن أردت بناء APK).