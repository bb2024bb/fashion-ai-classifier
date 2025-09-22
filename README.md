# 🧠 نظام تصنيف صور الملابس بالذكاء الاصطناعي 
## Fashion Image Classification using AI 

---

<p align="center">✍️ عمل الطلاب:<b>بلال محمد صالح الشامي <b>حمزه أحمد محمد يفوز</b> و 
 و <b> بكر مهيوب التبعي </b>
<br><br>✍️ Work of the students:  Bilal Mohammed Saleh Al-Shami, Hamza Ahmed Mohammed Yafouz, and  Bakr Mahyoub Al-Tabie </br></p>
 </br></p>


---

## 📖 نظرة عامة | Overview 

<div dir="rtl" style="text-align: right;">
تم تطوير نظام ذكي يعتمد على <b>الشبكات العصبية التلافيفية (CNN)</b> لتصنيف صور الملابس إلى <b>10 فئات مختلفة</b> باستخدام قاعدة بيانات <b>Fashion MNIST</b>.<br>
حقق النموذج دقة وصلت إلى <b>93.3%</b> عند اختباره على بيانات مخصصة لذلك.
</div>

<div dir="ltr" style="text-align: left;">
This AI system leverages <b>Convolutional Neural Networks (CNNs)</b> to classify fashion images into <b>10 categories</b> using the <b>Fashion MNIST</b> dataset.<br>
The model achieved <b>93.3% accuracy</b> on the test set.
</div>

---

## 🎯 الاستخدامات العملية | Practical Use Cases 

<div dir="rtl" style="text-align: right;">
- 🛒 تصنيف المنتجات تلقائيًا في المتاجر الإلكترونية.<br>
- 📱 تحسين تجربة المستخدم عبر عرض التصنيفات بشكل منظم.<br>
- ⏳ تقليل الوقت والجهد المبذول في التصنيف اليدوي.
</div>

<div dir="ltr" style="text-align: left;">
- 🛒 Automating product categorization in e-commerce platforms.<br>
- 📱 Enhancing user experience with organized classification.<br>
- ⏳ Reducing time and effort compared to manual labeling.
</div>

---

## 📊 مجموعة البيانات | Dataset 

<div dir="rtl" style="text-align: right;">
- <b>المصدر:</b> Fashion MNIST<br>
- <b>عدد الصور:</b> 70,000 صورة (60,000 للتدريب + 10,000 للاختبار)<br>
- <b>الأبعاد:</b> 28×28 بكسل (أبيض وأسود)<br>
- <b>عدد الفئات:</b> 10 أصناف ملابس وأحذية
</div>

<div dir="ltr" style="text-align: left;">
- <b>Source:</b> Fashion MNIST<br>
- <b>Number of images:</b> 70,000 (60,000 training + 10,000 test)<br>
- <b>Dimensions:</b> 28×28 pixels (grayscale)<br>
- <b>Number of classes:</b> 10 types of clothing and shoes
</div>

**Classes / الفئات:** 
0. T-shirt / Top → تيشيرت / قميص 
1. Trouser → بنطال 
2. Pullover → بلوفر 
3. Dress → فستان 
4. Coat → معطف 
5. Sandal → صندل 
6. Shirt → قميص 
7. Sneaker → حذاء رياضي 
8. Bag → حقيبة 
9. Ankle Boot → حذاء قصير 

---

## ⚙️ فكرة عمل المشروع | How it Works 

<div dir="rtl" style="text-align: right;">
1. <b>📥 إدخال البيانات:</b> المستخدم يرفع صورة قطعة ملابس.<br>
2. <b>🧠 معالجة الصورة:</b> تغيير حجمها إلى 28×28 بكسل، تحويلها لتدرج رمادي، وتطبيع القيم.<br>
3. <b>🔎 استخراج المميزات:</b> تمرير الصورة عبر طبقات Conv2D + Pooling لاستخراج الخصائص المهمة.<br>
4. <b>📊 التصنيف:</b> طبقات Dense لتحديد الفئة النهائية.<br>
5. <b>📤 الإخراج:</b> عرض الفئة المتوقعة في واجهة Streamlit أو عبر FastAPI.
</div>

<div dir="ltr" style="text-align: left;">
1. <b>📥 Input:</b> The user uploads a clothing image.<br>
2. <b>🧠 Preprocessing:</b> Resize to 28×28 pixels, convert to grayscale, normalize values.<br>
3. <b>🔎 Feature Extraction:</b> Pass the image through Conv2D + Pooling layers to extract important features.<br>
4. <b>📊 Classification:</b> Dense layers determine the final class.<br>
5. <b>📤 Output:</b> Display the predicted class via Streamlit interface or FastAPI.
</div>

---

## 🏗️ بنية النموذج | Model Architecture 

<div dir="rtl" style="text-align: right;">
- Conv2D لاستخلاص المميزات البصرية.<br>
- Batch Normalization لتسريع الاستقرار أثناء التدريب.<br>
- Dropout لتقليل فرط التعلّم.<br>
- Dense للتصنيف النهائي.<br>
- إجمالي المعاملات القابلة للتدريب: <b>3,462,790</b>
</div>

<div dir="ltr" style="text-align: left;">
- Conv2D layers for feature extraction.<br>
- Batch Normalization to stabilize training.<br>
- Dropout to prevent overfitting.<br>
- Dense layers for final classification.<br>
- Total trainable parameters: <b>3,462,790</b>
</div>

---

## 📈 النتائج | Results 

<div dir="rtl" style="text-align: right;">
- دقة التدريب: 94.7%<br>
- دقة الاختبار: 93.3%<br>
- خسارة الاختبار: 0.21
</div>

<div dir="ltr" style="text-align: left;">
- Training Accuracy: 94.7%<br>
- Test Accuracy: 93.3%<br>
- Test Loss: 0.21
</div>

---

## 🚀 التشغيل | How to Run 

<div dir="rtl" style="text-align: right;">
1. تثبيت المتطلبات: <code>pip install -r requirements.txt</code><br>
2. لتشغيل واجهة Streamlit: <code>streamlit run app.py</code><br>
3. لتشغيل واجهة API: <code>uvicorn main:app --reload</code>
</div>

<div dir="ltr" style="text-align: left;">
1. Install requirements: <code>pip install -r requirements.txt</code><br>
2. Run Streamlit interface: <code>streamlit run app.py</code><br>
3. Run API interface: <code>uvicorn main:app --reload</code>
</div>

---

## 📌 تحسينات مستقبلية | Future Improvements 

<div dir="rtl" style="text-align: right;">
- دعم الصور الملونة.<br>
- إضافة فئات جديدة من الملابس.<br>
- استخدام نماذج متقدمة مثل ResNet أو EfficientNet.<br>
- دمج النظام مع منصات التجارة الإلكترونية.
</div>

<div dir="ltr" style="text-align: left;">
- Support RGB images.<br>
- Add new clothing categories.<br>
- Use advanced models like ResNet or EfficientNet.<br>
- Integrate the system with e-commerce platforms.
</div>

---

## ✨ المساهمة | Contribution 

<div dir="rtl" style="text-align: right;">
مرحب بالمساهمات لتحسين المشروع:<br>
- تحسين بنية الشبكة العصبية.<br>
- دعم أنواع بيانات إضافية.<br>
- تطوير واجهة المستخدم.
</div>

<div dir="ltr" style="text-align: left;">
Contributions are welcome to improve the project:<br>
- Enhance neural network architecture.<br>
- Support additional data types.<br>
- Improve user interface.
</div>

---

## 📝 الترخيص | License 

<div dir="rtl" style="text-align: right;">
المشروع مفتوح المصدر للأغراض التعليمية والبحثية.
</div>

<div dir="ltr" style="text-align: left;">
This project is open-source for educational and research purposes.
</div>
