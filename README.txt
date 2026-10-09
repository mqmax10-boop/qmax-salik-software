Qmax & Salik Software — ملفات الموقع المتصلة بـ Supabase

مهم قبل النشر:
1) افتح index.html وadmin.html بمحرر نصوص.
2) ابحث في كل ملف عن PASTE_YOUR_SUPABASE_PUBLISHABLE_KEY_HERE واستبدل العبارة بمفتاح Publishable العام من Supabase → Project Settings → API Keys.
3) لا تستخدم secret key أو service_role key داخل ملفات الموقع إطلاقًا.
4) ارفع index.html وadmin.html إلى جذر مستودع GitHub نفسه واستبدل الملفات القديمة عند ظهور خيار الاستبدال، ثم Commit changes.
5) افتح admin.html وسجل الدخول بحساب المدير الذي أنشأته في Supabase Authentication.

قاعدة البيانات المتوقعة: public.models بالأعمدة:
id, name, category, description, flash_link, dump_link, loader_link, image_url, published, created_at.

الأمان:
- لا توقف RLS.
- يلزم وجود سياسة SELECT للزوار تسمح بقراءة الصفوف published = true.
- يلزم أن تكون سياسات INSERT/UPDATE/DELETE مقصورة على حساب المدير الذي سمحت له في Supabase.
- إذا ظهر خطأ عند الحفظ، لا تجعل الكتابة عامة؛ راجع سياسات RLS ودالة is_site_admin وتأكد من استبدال البريد التجريبي بالبريد الحقيقي للمدير.
