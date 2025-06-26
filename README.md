# HR FIRST LINE CORE - نظام إدارة الموارد البشرية

نظام متطور لإدارة الموارد البشرية مصمم خصيصاً لشركة FIRST LINE LOGISTICS مع دعم كامل للغة العربية والذكاء الاصطناعي.

## 🌟 الميزات الرئيسية

### 📊 إدارة شاملة للموظفين
- إدارة بيانات الموظفين مع ربط قوى العاملة
- تتبع الوظائف والأقسام والرواتب
- إدارة العقود والوثائق

### 🔐 نظام التحقق الآمن
- تحقق ثنائي عبر SMS و WhatsApp
- نظام أذونات متقدم
- حماية البيانات الحساسة

### 🤖 الذكاء الاصطناعي
- تحليل تلقائي للمشاعر في التعليقات
- توليد التقارير الذكية
- اقتراحات تحسين الأداء

### 📱 إشعارات فورية
- إشعارات WhatsApp للأحداث المهمة
- رسائل SMS للتحقق
- تنبيهات في الوقت الفعلي

### 🎨 واجهة عربية احترافية
- دعم كامل للاتجاه من اليمين لليسار (RTL)
- تصميم متجاوب لجميع الأجهزة
- ألوان وهوية FIRST LINE LOGISTICS

## 🛠️ التقنيات المستخدمة

### Frontend
- **React 18** - مكتبة JavaScript للواجهات
- **TypeScript** - للبرمجة الآمنة
- **Tailwind CSS** - للتصميم المتقدم
- **Shadcn/UI** - مكونات واجهة المستخدم
- **TanStack Query** - لإدارة البيانات
- **Wouter** - للتوجيه

### Backend
- **Node.js** - بيئة تشغيل JavaScript
- **Express.js** - إطار عمل الخادم
- **TypeScript** - للبرمجة الآمنة
- **Drizzle ORM** - لإدارة قاعدة البيانات
- **PostgreSQL** - قاعدة البيانات الرئيسية

### خدمات خارجية
- **OpenAI GPT-4o** - للذكاء الاصطناعي
- **Twilio** - للرسائل النصية و WhatsApp
- **Neon Database** - قاعدة بيانات PostgreSQL سحابية

## 🚀 التثبيت والتشغيل

### متطلبات النظام
- Node.js 20 أو أحدث
- npm أو yarn
- PostgreSQL 16

### خطوات التثبيت

1. **نسخ المشروع**
```bash
git clone <repository-url>
cd hr-first-line-core
```

2. **تثبيت الحزم**
```bash
npm install
```

3. **إعداد البيئة**
```bash
cp .env.example .env
```

4. **تحديث متغيرات البيئة**
```env
DATABASE_URL="your-postgresql-connection-string"
OPENAI_API_KEY="your-openai-api-key"
TWILIO_ACCOUNT_SID="your-twilio-account-sid"
TWILIO_AUTH_TOKEN="your-twilio-auth-token"
TWILIO_PHONE_NUMBER="your-twilio-phone-number"
TWILIO_WHATSAPP_NUMBER="your-twilio-whatsapp-number"
```

5. **إعداد قاعدة البيانات**
```bash
npm run db:push
```

6. **تشغيل المشروع**
```bash
npm run dev
```

## 📁 هيكل المشروع

```
hr-first-line-core/
├── client/                 # تطبيق React Frontend
│   ├── src/
│   │   ├── components/     # مكونات واجهة المستخدم
│   │   ├── pages/          # صفحات التطبيق
│   │   ├── hooks/          # React Hooks مخصصة
│   │   └── lib/           # مكتبات مساعدة
│   └── index.html
├── server/                 # خادم Express Backend
│   ├── services/          # خدمات خارجية
│   ├── routes.ts          # مسارات API
│   ├── storage.ts         # إدارة البيانات
│   └── index.ts           # نقطة دخول الخادم
├── shared/                # أكواد مشتركة
│   ├── schema.ts          # نموذج قاعدة البيانات
│   └── hr-schema.ts       # نموذج HR المحدث
└── package.json
```

## 🔧 الأوامر المتاحة

```bash
# تشغيل المشروع في وضع التطوير
npm run dev

# بناء المشروع للإنتاج
npm run build

# تشغيل المشروع في وضع الإنتاج
npm run start

# تحديث قاعدة البيانات
npm run db:push

# فتح استوديو إدارة قاعدة البيانات
npm run db:studio
```

## 🔐 الأمان والخصوصية

- جميع كلمات المرور مشفرة باستخدام bcrypt
- التحقق الثنائي عبر SMS/WhatsApp
- حماية البيانات الحساسة
- جلسات آمنة ومشفرة
- التحقق من الأذونات على جميع المستويات

## 🌐 النشر

المشروع جاهز للنشر على منصات متعددة:

### Replit (الحالي)
- النشر التلقائي عند الحفظ
- قاعدة بيانات PostgreSQL مدمجة
- متغيرات البيئة آمنة

### Vercel
```bash
npm run build
vercel deploy
```

### Heroku
```bash
git push heroku main
```

## 📊 مخطط قاعدة البيانات

### الجداول الرئيسية

#### employees (الموظفين)
- معلومات شخصية ووظيفية كاملة
- ربط مع قوى العاملة (qiwa_id)
- تتبع الراتب والعقود

#### users (المستخدمين)
- حسابات النظام والأذونات
- التحقق عبر الهاتف
- إدارة الجلسات

#### customer_feedback (تعليقات العملاء)
- تعليقات مع تحليل ذكي للمشاعر
- ربط بالموظفين والمشاريع
- حالة المعالجة والأولوية

#### internal_comments (التعليقات الداخلية)
- نقاشات الفريق حول التعليقات
- تتبع المساهمين

#### activities (الأنشطة)
- سجل جميع إجراءات النظام
- تتبع التغييرات والأحداث

#### notifications (الإشعارات)
- إشعارات للمستخدمين
- حالة القراءة والنوع

## 🤝 المساهمة

نرحب بالمساهمات! يرجى اتباع الإرشادات التالية:

1. انشئ Fork للمشروع
2. انشئ فرع للميزة الجديدة (`git checkout -b feature/AmazingFeature`)
3. قم بتأكيد التغييرات (`git commit -m 'Add some AmazingFeature'`)
4. ادفع للفرع (`git push origin feature/AmazingFeature`)
5. افتح Pull Request

## 📝 الترخيص

هذا المشروع مخصص لشركة FIRST LINE LOGISTICS - جميع الحقوق محفوظة.

## 📞 التواصل والدعم

لأي استفسارات أو دعم تقني:
- إنشاء Issue في GitHub
- التواصل مع فريق التطوير

## 🔄 سجل التحديثات

### الإصدار 1.0.0 (يونيو 2025)
- إطلاق النسخة الأولى
- نظام إدارة الموظفين الكامل
- تكامل الذكاء الاصطناعي
- واجهة عربية احترافية
- نظام الإشعارات والتحقق

---

**تم تطويره بواسطة فريق التقنية - FIRST LINE LOGISTICS**