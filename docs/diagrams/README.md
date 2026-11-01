# فهرس المخططات وحالة الإنجاز

مراجعة 1 نوفمبر 2026. جميع المخططات تصف التصميم المستهدف؛ لا تثبت تنفيذ منصة .NET أو تكامل GitHub فعلي.

مراجعة المراجع والمواءمة الأكاديمية: [ملاحظات UML وISO والقالب المرفق](../ACADEMIC_DESIGN_REVIEW.md). طبقت تعديلات علاقات Use Case وحراسات Activity ومعرفات الحالات. نجاح التصيير لا يثبت اكتمال التوثيق أو المطابقة الأكاديمية.

المراجعة الأخيرة للمحتوى والتصحيحات وما بقي: [تقرير المراجعة](../DESIGN_CONTENT_REVIEW_2026-11-01.md). وتشمل [ملاحظات حماية المنصة](../SECURITY_DESIGN_NOTES.md) ما تأكد من حديث المشرف عن CIA والأصالة والتشفير والتهشير.

تفصيل إجراءات كل دور وسحب الوصول: [مصفوفة الصلاحيات المعتمدة](../ACCESS_CONTROL_MATRIX.md). حالة البنود التالية وحدود WIP في [سياسة Kanban ومراجع العمل](../KANBAN.md).

## ترتيب الملفات

```text
diagrams/
  context/       مخطط السياق ومصدره ووصفه
  use-cases/     مناظر حالات الاستخدام ومصدرها ووصفها
  activity/      مسارات الحالات، بملفات PlantUML ومعاينات PNG
  architecture/  المعمارية العامة ومصدرها ووصفها
  legacy/        نسخ قديمة محفوظة محليًا
```

المعاينة بجانب مصدرها داخل مجلد نوع المخطط؛ لا توجد صور منفردة في جذر الحزمة. ملفات `legacy` ليست النسخة الحالية ولا تدخل حزمة الرفع الجديدة.

## الرسومات الحالية

| المخطط | المصدر القابل للتعديل | المعاينة الحالية |
|---|---|---|
| سياق النظام | [PlantUML](context/01-system-context.puml) | [PNG](context/01-system-context.png) |
| حالات استخدام المسؤول | [PlantUML — ثلاثة مناظر](use-cases/02-use-cases.puml) | [PNG](use-cases/02-use-cases-admin.png) |
| حالات استخدام المقيّم | الملف السابق نفسه | [PNG](use-cases/02-use-cases-evaluator.png) |
| حالات استخدام المراجع | الملف السابق نفسه | [PNG](use-cases/02-use-cases-reviewer.png) |
| تشغيل التقييم UC05 | [PlantUML](activity/03-run-assessment-activity.puml) | [PNG](activity/03-run-assessment-activity.png) |
| طلب خطة إصلاح UC07 | [PlantUML](activity/04-request-repair-activity.puml) | [PNG](activity/04-request-repair-activity.png) |
| إعادة التحقق UC08 | [PlantUML](activity/05-reverify-activity.puml) | [PNG](activity/05-reverify-activity.png) |
| المعمارية العامة Container | [PlantUML](architecture/06-container-architecture.puml) | [PNG](architecture/06-container-architecture.png) |
| ربط اتصال GitHub — UC02 | [PlantUML — الربط والفصل](activity/07-github-connection-activity.puml) | [PNG](activity/07-github-connection-activity.png) |
| فصل اتصال GitHub محليًا — UC02 | الملف السابق نفسه | [PNG](activity/07-github-disconnect-activity.png) |
| ضبط السياسة وأهداف الأطراف — UC03 | [PlantUML](activity/08-policy-and-objectives-activity.puml) | [PNG](activity/08-policy-and-objectives-activity.png) |
| تحديد نطاق التقييم — UC04 | [PlantUML](activity/09-assessment-scope-activity.puml) | [PNG](activity/09-assessment-scope-activity.png) |
| متابعة معالجة المخالفات — UC06 | [PlantUML](activity/10-finding-follow-up-activity.puml) | [PNG](activity/10-finding-follow-up-activity.png) |
| مراجعة النتائج والأدلة والتاريخ — UC09 | [PlantUML](activity/11-review-results-activity.puml) | [PNG](activity/11-review-results-activity.png) |
| عرض التقارير وطباعتها — UC10 | [PlantUML](activity/12-view-print-reports-activity.puml) | [PNG](activity/12-view-print-reports-activity.png) |
| إدارة العضويات والأدوار — UC01 | [PlantUML](activity/13-manage-memberships-activity.puml) | [PNG](activity/13-manage-memberships-activity.png) |

المجموع: 13 ملفًا من PlantUML تنتج 16 رسمًا. الرسومات الثلاثة لحالات الاستخدام مناظر للنظام نفسه وتكرر الوظائف المشتركة بين الأدوار دون إنشاء وظائف جديدة. UC02 له رسمان لتمييز الربط عن الفصل المحلي.

## وصف حالات الاستخدام

| الحالة | مستوى التوثيق الحالي |
|---|---|
| UC01 إدارة العضويات والأدوار | [وصف مفصل](../use-cases/UC01-manage-memberships.md) ومخطط Activity |
| UC02 إدارة اتصال GitHub | [وصف مفصل](../use-cases/UC02-github-connection.md) ومخططا Activity للربط والفصل |
| UC03 السياسة وأهداف الأطراف | [وصف مفصل](../use-cases/UC03-configure-policy.md) ومخطط Activity |
| UC04 تحديد نطاق التقييم | [وصف مفصل](../use-cases/UC04-define-assessment-scope.md) ومخطط Activity |
| UC05 تشغيل التقييم | [وصف مفصل](../use-cases/UC05-run-assessment.md) ومخطط Activity |
| UC06 متابعة معالجة المخالفات | [وصف مفصل](../use-cases/UC06-follow-up-findings.md) ومخطط Activity |
| UC07 طلب خطة إصلاح | [وصف مفصل](../use-cases/UC07-request-repair.md) ومخطط Activity |
| UC08 إعادة التحقق | [وصف مفصل](../use-cases/UC08-reverify.md) ومخطط Activity |
| UC09 مراجعة النتائج والأدلة والتاريخ | [وصف مفصل](../use-cases/UC09-review-results-evidence.md) ومخطط Activity |
| UC10 عرض التقارير | [وصف مفصل](../use-cases/UC10-view-print-reports.md) ومخطط Activity |

الحالات العشر الحالية كلها موصوفة تفصيليًا، وليست إثبات اكتمال SRS أو مصفوفة الصلاحيات. لدينا 28 متطلبًا وظيفيًا رئيسيًا؛ الحالات تجمع هذه المتطلبات ولا تساوي عددها. الفحوص الـ24 تفصيل لمتطلب تنفيذ الفحوص FR-11، ولا تجمع مع الـ28 جمعًا مكررًا. المصادقة والتفويض والتدقيق متطلبات مشتركة موثقة في [حصر المتطلبات](../FUNCTIONAL_REQUIREMENTS_INVENTORY.md).

## ما لم يُعدّ بعد

- Component Diagram وتفصيل حدود الوحدات وعقود استدعائها.
- Domain Model وERD.
- Sequence Diagrams.
- State Diagrams للمهمة والمخالفة، والمخطط التفصيلي لخوارزمية الإصلاح.
- تدفق البيانات وحدود الثقة الأمنية، وDeployment Diagram.
- المخططات الأولية للواجهات، وربط المتطلبات بالتحقق، وتثبيت مسودة الصلاحيات ثم تنفيذها واختبارها.
- تفصيل تهيئة المؤسسة والمسؤول الأول واسترداد الوصول ضمن تصميم المصادقة قبل التنفيذ.

مكتبة تنفيذ المهام والاستضافة لم تُحددا بعد. Container Diagram يبين التصميم العام ومسار المهام المحفوظة، ولا يثبت اختيار مكتبة طوابير أو بيئة نشر.

## الخط والنسخ القديمة

وُحد الخط في المصادر الحالية إلى **Dubai** المتوفر محليًا، مع تكبير النصوص والتسميات الصغيرة. إعادة التصدير على جهاز آخر تتطلب توفر الخط؛ المعاينات النقطية تحتفظ بالمظهر المعروض.

المرجع الحالي هو ملفات PlantUML الثلاثة عشر والمعاينات الست عشرة المرتبطة أعلاه. النسخ السابقة، ومنها السياق القديم والرسم المجمع لحالات الاستخدام، محفوظة في `legacy`.

شملت المراجعة تحديث الخط والترميز، وتفصيل حالات الاتصال والسياسة والنطاق والتقييم والمعالجة والمراجعة والتقارير، ثم UC01 لإدارة العضويات والأدوار. أصبحت الحالات العشر موصوفة تفصيليًا؛ تبقى المناظير والقرارات المذكورة أعلاه لاستكمال التصميم. لم تتضمن تشغيل منصة .NET أو اختبار GitHub حيًا، ولم تضف حالات اختبار برمجية.

أعيدت مراجعة محتوى الرسوم، وصححت فروع الحفظ والإلغاء والتحقق والوصول والطباعة، ثم أعيد تنظيم الملفات. يبين تقرير المراجعة التعديلات وحدودها؛ لا يعني إكمال الحالات العشر اكتمال SRS.

## إعادة تصدير المعاينات

توفر Java وملف [PlantUML](https://plantuml.com/download) والخط Dubai محليًا، ثم شغّل من جذر المشروع في PowerShell:

```powershell
$sources = (Get-ChildItem docs/diagrams -Recurse -Filter '*.puml').FullName
java -jar C:/Tools/plantuml.jar -charset UTF-8 -tpng @sources
```

استبدل مسار JAR بموقعه لديك. يحفظ التصدير الصور بجوار المصادر؛ لا يحتاج العرض إلى تعديل ملفات المصدر.
