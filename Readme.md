<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
  <meta charset="UTF-8">
  <title>استبيان تقييم المستشفى</title>
  <script src="https://cdnjs.cloudflare.com/ajax/libs/xlsx/0.18.5/xlsx.full.min.js"></script>
  <style>
    body {
      font-family: 'Arial', sans-serif;
      margin: 40px;
      background-color: #f9f9f9;
      direction: rtl;
    }
    .logo {
      text-align: center;
      margin-bottom: 20px;
    }
    .logo img {
      max-width: 200px;
    }
    .section {
      display: none;
    }
    .section.active {
      display: block;
    }
    label {
      font-weight: bold;
    }
    .question {
      margin-bottom: 15px;
    }
    .buttons {
      margin-top: 20px;
      display: flex;
      justify-content: space-between;
    }
    button {
      padding: 10px 20px;
      font-size: 16px;
    }
  </style>
</head>
<body>

<div class="logo">
  <img src="F162D37E-8D06-4F16-8ACA-B79561F45679.jpeg" alt="شعار الهيئة">
</div>

<h2>هيئة اعتماد المؤسسات الصحية ومراقبتها</h2>
<h3>استبيان تقييم المستشفيات</h3>

<form id="surveyForm">
  <label>اسم المستشفى:</label><br>
  <input type="text" name="hospitalName" required><br><br>

  <label>تاريخ التقييم:</label><br>
  <input type="date" name="date" required><br><br>

  <label>اسم المقيم:</label><br>
  <input type="text" name="evaluator" required><br><br>

‎  <!-- الأقسام -->
  <div class="section active">
    <h4>القسم الأول: جودة الرعاية والسلامة</h4>
    <div class="question">1. مدى التزام الفريق الطبي ببروتوكولات السلامة.
      <select name="q1"><option>1</option><option>2</option><option>3</option><option>4</option><option>5</option></select>
    </div>
    <div class="question">2. سرعة الاستجابة في حالات الطوارئ.
      <select name="q2"><option>1</option><option>2</option><option>3</option><option>4</option><option>5</option></select>
    </div>
    <div class="question">3. وضوح إجراءات الإبلاغ عن الأخطاء الطبية.
      <select name="q3"><option>1</option><option>2</option><option>3</option><option>4</option><option>5</option></select>
    </div>
    <div class="question">4. فعالية إدارة العدوى داخل الأقسام.
      <select name="q4"><option>1</option><option>2</option><option>3</option><option>4</option><option>5</option></select>
    </div>
    <div class="question">5. مدى توفر الأدوية الأساسية بانتظام.
      <select name="q5"><option>1</option><option>2</option><option>3</option><option>4</option><option>5</option></select>
    </div>
  </div>

  <div class="section">
    <h4>القسم الثاني: كفاءة الكادر الطبي</h4>
‎    <!-- الأسئلة 6 إلى 10 -->
    <div class="question">6. مستوى مهارات الأطباء في التشخيص.
      <select name="q6"><option>1</option><option>2</option><option>3</option><option>4</option><option>5</option></select>
    </div>
    <div class="question">7. تعاون الفريق الطبي مع بعضه البعض.
      <select name="q7"><option>1</option><option>2</option><option>3</option><option>4</option><option>5</option></select>
    </div>
    <div class="question">8. احترام الطاقم الطبي لخصوصية المرضى.
      <select name="q8"><option>1</option><option>2</option><option>3</option><option>4</option><option>5</option></select>
    </div>
    <div class="question">9. توفر الأطباء المختصين على مدار 24 ساعة.
      <select name="q9"><option>1</option><option>2</option><option>3</option><option>4</option><option>5</option></select>
    </div>
    <div class="question">10. وضوح شرح الإجراءات الطبية للمريض.
      <select name="q10"><option>1</option><option>2</option><option>3</option><option>4</option><option>5</option></select>
    </div>
  </div>

  <div class="section">
    <h4>القسم الثالث: المرافق والتجهيزات</h4>
‎    <!-- الأسئلة 11 إلى 15 -->
    <div class="question">11. نظافة الغرف ومرافق الاستقبال.
      <select name="q11"><option>1</option><option>2</option><option>3</option><option>4</option><option>5</option></select>
    </div>
    <div class="question">12. جودة الأجهزة الطبية وتحديثها.
      <select name="q12"><option>1</option><option>2</option><option>3</option><option>4</option><option>5</option></select>
    </div>
    <div class="question">13. سهولة الوصول للمرافق.
      <select name="q13"><option>1</option><option>2</option><option>3</option><option>4</option><option>5</option></select>
    </div>
    <div class="question">14. توفر تجهيزات لذوي الاحتياجات الخاصة.
      <select name="q14"><option>1</option><option>2</option><option>3</option><option>4</option><option>5</option></select>
    </div>
    <div class="question">15. كفاية عدد الأسرة في الأقسام الحرجة.
      <select name="q15"><option>1</option><option>2</option><option>3</option><option>4</option><option>5</option></select>
    </div>
  </div>

  <div class="section">
    <h4>القسم الرابع: النظافة والتعقيم</h4>
‎    <!-- الأسئلة 16 إلى 20 -->
    <div class="question">16. نظافة دورات المياه والممرات.
      <select name="q16"><option>1</option><option>2</option><option>3</option><option>4</option><option>5</option></select>
    </div>
    <div class="question">17. التخلص الآمن من النفايات الطبية.
      <select name="q17"><option>1</option><option>2</option><option>3</option><option>4</option><option>5</option></select>
    </div>
    <div class="question">18. تعقيم الأدوات قبل الاستخدام.
      <select name="q18"><option>1</option><option>2</option><option>3</option><option>4</option><option>5</option></select>
    </div>
    <div class="question">19. خلو البيئة من الروائح الكريهة.
      <select name="q19"><option>1</option><option>2</option><option>3</option><option>4</option><option>5</option></select>
    </div>
    <div class="question">20. نظافة أغطية الأسرة والأدوات الشخصية.
      <select name="q20"><option>1</option><option>2</option><option>3</option><option>4</option><option>5</option></select>
    </div>
  </div>

  <div class="section">
    <h4>القسم الخامس: الخدمات الإدارية</h4>
‎    <!-- الأسئلة 21 إلى 25 -->
    <div class="question">21. سرعة إجراءات القبول والاستقبال.
      <select name="q21"><option>1</option><option>2</option><option>3</option><option>4</option><option>5</option></select>
    </div>
    <div class="question">22. وضوح سياسات الدفع والتأمين.
      <select name="q22"><option>1</option><option>2</option><option>3</option><option>4</option><option>5</option></select>
    </div>
    <div class="question">23. سرعة معالجة الشكاوى والاقتراحات.
      <select name="q23"><option>1</option><option>2</option><option>3</option><option>4</option><option>5</option></select>
    </div>
    <div class="question">24. مرونة أوقات الزيارة.
      <select name="q24"><option>1</option><option>2</option><option>3</option><option>4</option><option>5</option></select>
    </div>
    <div class="question">25. توفر معلومات عن حقوق المريض.
      <select name="q25"><option>1</option><option>2</option><option>3</option><option>4</option><option>5</option></select>
    </div>
  </div>

  <div class="section">
    <h4>القسم السادس: الرعاية الشاملة</h4>
‎    <!-- الأسئلة 26 إلى 30 -->
    <div class="question">26. دقة التعليمات المقدمة عند الخروج.
      <select name="q26"><option>1</option><option>2</option><option>3</option><option>4</option><option>5</option></select>
    </div>
    <div class="question">27. متابعة الحالة بعد الخروج.
      <select name="q27"><option>1</option><option>2</option><option>3</option><option>4</option><option>5</option></select>
    </div>
    <div class="question">28. مراعاة الجوانب النفسية للمريض.
      <select name="q28"><option>1</option><option>2</option><option>3</option><option>4</option><option>5</option></select>
    </div>
    <div class="question">29. توفر برامج توعية صحية.
      <select name="q29"><option>1</option><option>2</option><option>3</option><option>4</option><option>5</option></select>
    </div>
    <div class="question">30. تقييمك العام لخدمات المستشفى.
      <select name="q30"><option>1</option><option>2</option><option>3</option><option>4</option><option>5</option></select>
    </div>
  </div>

  <div class="buttons">
    <button type="button" onclick="prevSection()">السابقة</button>
    <button type="button" onclick="nextSection()">التالي</button>
  </div>

  <br><br>
  <button type="button" onclick="submitForm()">إرسال</button>
</form>

<script>
  let current = 0;
  const sections = document.querySelectorAll(".section");
  function showSection(index) {
    sections.forEach((sec, i) => {
      sec.classList.toggle("active", i === index);
    });
  }
  function nextSection() {
    if (current < sections.length - 1) {
      current++;
      showSection(current);
    }
  }
  function prevSection() {
    if (current > 0) {
      current--;
      showSection(current);
    }
  }

  function submitForm() {
    const form = document.forms["surveyForm"];
    const data = {};
    for (let element of form.elements) {
      if (element.name) {
        data[element.name] = element.value;
      }
    }

    const worksheet = XLSX.utils.json_to_sheet([data]);
    const workbook = XLSX.utils.book_new();
    XLSX.utils.book_append_sheet(workbook, worksheet, "تقييم المستشفى");
    XLSX.writeFile(workbook, "hospital_survey_results.xlsx");
    alert("تم تحميل الملف بنجاح!");
  }
</script>

</body>
</html>