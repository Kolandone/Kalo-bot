# ربات کلو - ربات تلگرام هوشمند

## معرفی
ربات کلو یک ربات تلگرام برای پاسخ‌گویی هوشمند به زبان فارسی است که با API جمینای کار می‌کند و روی کلادفلر ورکرز اجرا می‌شود.

## قابلیت‌ها
- پاسخ‌گویی در چت خصوصی به تمام پیام‌ها.
- پاسخ‌گویی در گروه‌ها فقط در صورت ذکر نام (مانند ، `کلو` یا `kalobot`) یا ریپلای.
- تشخیص سؤال درباره نام و پاسخ غیرمستقیم
- فیلتر پیام‌های غیرمرتبط برای بهینه‌سازی عملکرد.
- پشتیبانی از زبان فارسی با لحن دوستانه.
- مدیریت خطاها در ارسال پیام.

## پیش‌نیازها
- حساب کلادفلر.
- توکن ربات تلگرام (از `@BotFather`).
- کلید API جمینای (از گوگل).
- آیدی عددی ربات.

## مراحل نصب
### 1. ساخت ربات در تلگرام
1. به `@BotFather` پیام دهید و دستور `/newbot` را وارد کنید.
2. نام (مثلاً `Kaloobot`) و نام کاربری انتخاب کنید.
3. توکن ربات را کپی کنید.

### 2. دیپلوی روی کلادفلر
1. به [dash.cloudflare.com](https://dash.cloudflare.com/) بروید.
2. یک ورکر ایجاد کنید.
3. کد را از `worker.js` کپی و در ورکر پیست کنید.
4. متغیرهای محیطی را تنظیم کنید:
   - `BOT_TOKEN`: توکن ربات.
   - `GEMINI_API_KEY`: کلید API جمینای.
   - `BOT_ID`: آیدی عددی ربات.
5. روی **Save and Deploy** کلیک کنید.

### 3. تنظیم Webhook
1. درخواست زیر را ارسال کنید:
https://api.telegram.org/bot<BOT_TOKEN>/setWebhook?url=https://ورکرتون.workers.dev/

### 4. تنظیمات حریم خصوصی
1. به `@BotFather` پیام دهید.
2. با دستور `/setprivacy`، گزینه **Disable** را برای ربات انتخاب کنید.

### 5. دسترسی در گروه
1. ربات را به گروه اضافه کنید.
2. ربات را ادمین کنید

### 6. تست
- در چت خصوصی: پیام (مثلاً "سلام") بفرستید.
- در گروه: ربات را صدا کنید (مثلاً "کلو چطوری؟").
- درباره نام بپرسید (مثلاً "اسمت چیه؟").

