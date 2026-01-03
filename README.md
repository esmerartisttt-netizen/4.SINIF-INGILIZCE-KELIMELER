<!doctype html>
<html lang="tr">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>Gelişmiş İngilizce Kelime Kartları</title>
  <style>
    :root{
      --bg-start:#6a11cb;
      --bg-end:#2575fc;
      --accent:#6a11cb;
      --accent-2:#9C27B0;
      --muted:#666;
      --card-front:#f5f7fa;
      --card-back:#2E7D32;
      --success:#4CAF50;
      --danger:#f44336;
      --glass: rgba(255,255,255,0.95);
      --header-height:72px;
    }
    *{box-sizing:border-box;font-family:Inter, "Arial Rounded MT Bold", Arial, sans-serif}
    html,body{height:100%;margin:0}
    body{
      margin:0;
      display:flex;
      align-items:flex-start;
      justify-content:center;
      min-height:100vh;
      padding:20px;
      padding-top: calc(var(--header-height) + 20px); /* boşluk: sabit üst başlık için */
      background:linear-gradient(135deg,var(--bg-start) 0%,var(--bg-end) 100%);
      -webkit-font-smoothing:antialiased;
      -moz-osx-font-smoothing:grayscale;
    }

    /* ÜST SABİT BAŞLIK */
    header.app-header{
      position:fixed;
      top:0;
      left:0;
      right:0;
      height:var(--header-height);
      display:flex;
      align-items:center;
      justify-content:center;
      z-index:999;
      background: linear-gradient(90deg, rgba(255,255,255,0.05), rgba(255,255,255,0.02));
      backdrop-filter: blur(6px);
      border-bottom: 1px solid rgba(255,255,255,0.06);
      padding: 10px 18px;
    }
    .header-inner{
      width:100%;
      max-width:1100px;
      display:flex;
      gap:12px;
      align-items:center;
      justify-content:space-between;
    }
    .brand{
      display:flex;
      gap:12px;
      align-items:center;
    }
    .logo{
      width:46px;
      height:46px;
      border-radius:10px;
      display:flex;
      align-items:center;
      justify-content:center;
      background:linear-gradient(135deg,var(--accent),var(--accent-2));
      color:white;
      font-weight:800;
      font-size:18px;
      box-shadow:0 6px 18px rgba(0,0,0,0.18);
    }
    .site-title{
      color:white;
      font-weight:700;
      font-size:1rem;
    }
    .site-sub{
      color:rgba(255,255,255,0.85);
      font-size:0.85rem;
    }

    .header-actions{display:flex;gap:8px;align-items:center}
    .header-actions button{
      background:rgba(255,255,255,0.06);
      color:white;border:1px solid rgba(255,255,255,0.06);
      padding:8px 12px;border-radius:10px;cursor:pointer;font-weight:700;
    }
    .header-link{color:rgba(255,255,255,0.9);text-decoration:none;font-weight:700;padding:8px 12px;border-radius:8px;border:1px solid rgba(255,255,255,0.04)}

    /* UYGULAMA KUTUSU */
    .app{
      width:100%;
      max-width:980px;
      background:var(--glass);
      border-radius:16px;
      padding:18px;
      box-shadow:0 20px 50px rgba(0,0,0,0.25);
      display:grid;
      grid-template-columns: 320px 1fr;
      gap:18px;
      align-items:start;
    }

    /* Sidebar */
    .panel{
      background:white;
      border-radius:12px;
      padding:14px;
      box-shadow:0 8px 24px rgba(5,8,20,0.06);
    }

    h1{
      margin:0 0 8px;
      font-size:1.05rem;
      color:var(--accent-2);
    }
    .subtitle{color:var(--muted);font-size:0.9rem;margin-bottom:12px}

    label{display:block;font-size:0.85rem;color:#444;margin-top:10px;margin-bottom:6px}
    select,input,button,textarea{
      font-size:0.95rem;padding:10px;border-radius:8px;border:1px solid #e6e6e9;width:100%;
      outline:none;
    }

    .controls-row{display:flex;gap:8px}

    .category-list{
      max-height:220px;overflow:auto;margin-top:8px;padding-right:6px;
    }
    .category-item{
      display:flex;align-items:center;justify-content:space-between;padding:8px;border-radius:8px;
      cursor:pointer;margin-bottom:6px;border:1px solid transparent;
    }
    .category-item:hover{background:#fafafa;border-color:#f0f0f0}
    .category-item strong{font-size:0.95rem;color:#222}

    .small{font-size:0.85rem;color:var(--muted)}

    .settings{display:grid;gap:8px;margin-top:10px}

    .muted-box{
      background:#fbfbfd;border-radius:8px;padding:8px;font-size:0.9rem;color:#444;border:1px solid #f2f2f6
    }

    /* Main area */
    .main{
      display:flex;flex-direction:column;gap:12px;
    }

    .top-row{display:flex;align-items:center;justify-content:space-between;gap:12px}
    .title{
      font-size:1.1rem;color:#222;font-weight:700;
    }
    .status{
      text-align:right;color:var(--muted);font-size:0.9rem
    }

    .card-wrap{
      perspective:1200px;
      display:flex;align-items:center;justify-content:center;
      min-height:320px;
    }
    .card{
      width:100%;max-width:640px;height:320px;border-radius:14px;position:relative;cursor:pointer;
      box-shadow:0 18px 40px rgba(2,6,23,0.12);
      transition:transform 0.5s ease;
    }
    .card-inner{
      position:relative;width:100%;height:100%;transition:transform 0.7s;transform-style:preserve-3d;border-radius:14px;overflow:hidden;
    }
    .card.flipped .card-inner{transform:rotateY(180deg)}
    .face{
      position:absolute;inset:0;display:flex;align-items:center;justify-content:center;
      backface-visibility:hidden;padding:26px;font-weight:700;font-size:2.4rem;border-radius:14px;
    }
    .front{background:linear-gradient(135deg,var(--card-front),#d7def0);color:#222;border:4px solid var(--accent)}
    .back{background:linear-gradient(135deg,var(--card-back),#2b7a2d);color:white;transform:rotateY(180deg)}
    .word-small{font-size:1rem;color:rgba(0,0,0,0.6);position:absolute;left:18px;top:12px}

    .controls{
      display:flex;gap:10px;align-items:center;justify-content:center;flex-wrap:wrap;
    }
    button.btn{
      background:var(--accent);color:white;border:none;padding:10px 14px;border-radius:10px;cursor:pointer;font-weight:700;
      transition:all .18s;
    }
    button.btn.secondary{background:#FF9800}
    button.btn.ghost{background:transparent;color:#333;border:1px solid rgba(0,0,0,0.06)}
    button.btn.small{padding:8px 10px;font-size:0.9rem}

    .info-row{display:flex;align-items:center;justify-content:space-between;gap:10px}
    .progress{
      height:10px;background:#eee;border-radius:999px;overflow:hidden;width:60%;
    }
    .progress > i{display:block;height:100%;background:linear-gradient(90deg,var(--accent),var(--accent-2));width:0%}

    /* Quiz area */
    .quiz{
      display:none;padding:12px;border-radius:10px;background:#fff;border:1px solid #f2f2f6;
    }
    .quiz.show{display:block}
    .options{display:grid;grid-template-columns:repeat(2,1fr);gap:10px;margin-top:10px}
    .opt{padding:10px;border-radius:8px;background:#fafafa;border:1px solid #eee;cursor:pointer;font-weight:700}

    /* New: flashing styles for quiz options on correct/wrong answers */
    .opt.correct-flash{
      color: #fff !important;
      border-color: #00c853 !important;
      animation: correctFlash 0.6s ease-in-out 0s 4;
      background: linear-gradient(90deg,#00e676,#00c853) !important;
    }
    @keyframes correctFlash{
      0% { background: #00e676; }
      50% { background: #a5d6a7; }
      100% { background: #00e676; }
    }
    .opt.wrong-flash{
      color: #fff !important;
      border-color: #d50000 !important;
      animation: wrongFlash 0.6s ease-in-out 0s 4;
      background: linear-gradient(90deg,#ff5252,#d50000) !important;
    }
    @keyframes wrongFlash{
      0% { background: #ff5252; }
      50% { background: #ffc1c1; }
      100% { background: #ff5252; }
    }

    /* footer */
    .footer-row{display:flex;align-items:center;justify-content:space-between;gap:12px;margin-top:8px}
    .small-muted{font-size:0.85rem;color:var(--muted)}

    /* responsive */
    @media (max-width:900px){
      .app{grid-template-columns:1fr;max-width:720px;padding:12px}
      .card{height:260px}
      .card .face{font-size:1.8rem;padding:18px}
      body{padding-top: calc(var(--header-height) + 12px)}
      .header-inner{padding:0 8px}
    }
  </style>
</head>
<body>
  <!-- SABİT BAŞLIK -->
  <header class="app-header" role="banner" aria-label="Uygulama başlığı">
    <div class="header-inner">
      <div class="brand">
        <div class="logo" aria-hidden="true">SU</div>
        <div>
          <div class="site-title">Temel İngilizce Kelime Kartları</div>
          <div class="site-sub">Geliştirilmiş — Ses, Test, İlerleme</div>
        </div>
      </div>

      <div class="header-actions" role="navigation" aria-label="Başlık araçları">
        <a class="header-link" href="#" title="Ana sayfa" onclick="window.scrollTo({top:0,behavior:'smooth'});return false">Anasayfa</a>
        <button onclick="toggleTheme()" title="Tema değiştir">🌓 Tema</button>
        <a class="header-link" href="https://github.com/" target="_blank" rel="noopener">GitHub</a>
      </div>
    </div>
  </header>

  <!-- UYGULAMA -->
  <div class="app" role="application" aria-label="İngilizce kelime kartları uygulaması">
    <!-- SIDEBAR -->
    <aside class="panel" aria-label="Yan menü">
      <h1>📚 Kelime Kartları</h1>
      <div class="subtitle">Hızlı geliştirilmiş sürüm — ilerleme kaydetme, ses, test</div>

      <label for="categorySelect">Kategori</label>
      <select id="categorySelect" aria-label="Kategori seçici"></select>

      <div class="category-list" id="categoryList" aria-live="polite"></div>

      <label>Hızlı işlemler</label>
      <div class="controls-row">
        <button class="btn small" id="shuffleBtn" title="Kelime sırasını karıştır">🔀 Karıştır</button>
        <button class="btn small secondary" id="resetProgressBtn" title="İlerlemenizi sıfırla">♻️ Sıfırla</button>
      </div>

      <label>Ses Ayarları</label>
      <div class="muted-box">
        <label for="voiceSelect" class="small">Ses</label>
        <select id="voiceSelect"></select>
        <label class="small" for="rateRange">Hız: <span id="rateVal">0.9</span>x</label>
        <input type="range" id="rateRange" min="0.6" max="1.6" step="0.05" value="0.9">
        <div style="display:flex;gap:8px;margin-top:8px">
          <button class="btn ghost small" id="autoplayToggle">▶ Otomatik Oynatma: Kapalı</button>
          <button class="btn ghost small" id="speakBtn">🔊 Oku</button>
        </div>
      </div>

      <label>Kaydet / Dışa Aktar</label>
      <div style="display:flex;gap:8px;margin-top:6px">
        <button class="btn ghost small" id="exportBtn">⬇️ Dışa Aktar</button>
        <input type="file" id="importFile" accept=".json" style="display:none">
        <button class="btn ghost small" id="importBtn">⬆️ İçeri Aktar</button>
      </div>

      <label>Kart ekle</label>
      <input id="newEnglish" placeholder="İngilizce kelime/cümle">
      <input id="newTurkish" placeholder="Türkçe karşılığı" style="margin-top:6px">
      <div style="display:flex;gap:8px;margin-top:8px">
        <button class="btn small" id="addCardBtn">➕ Ekle</button>
        <button class="btn small ghost" id="removeKnownBtn">🗑️ Bilinenleri Sil</button>
      </div>

      <div class="settings">
        <div class="small-muted">Toplam kategoriler: <span id="catCount">0</span></div>
        <div class="small-muted">Geçerli kategori: <strong id="currentCatLabel">-</strong></div>
        <div class="small-muted">İlerleme kaydediliyor: <strong>LocalStorage</strong></div>
      </div>
    </aside>

    <!-- MAIN -->
    <main class="main" role="main">
      <div class="top-row">
        <div class="title">Temel İngilizce Kelimeler — Geliştirilmiş</div>
        <div class="status">
          <div id="modeIndicator" class="small-muted">🔤 İngilizce → Türkçe</div>
          <div id="counter" class="small-muted">0 / 0</div>
        </div>
      </div>

      <div class="card-wrap" aria-live="polite">
        <div id="card" class="card" role="button" tabindex="0" aria-pressed="false" aria-label="Kelime kartı">
          <div class="card-inner" id="cardInner">
            <div class="face front" id="frontFace">
              <div class="word-small" id="wordMeta"></div>
              <div id="frontText">Kategori seçin</div>
            </div>
            <div class="face back" id="backFace">
              <div id="backText">👆 Yukarıdan seçim yapın</div>
            </div>
          </div>
        </div>
      </div>

      <div class="controls" role="toolbar" aria-label="Kontroller">
        <button class="btn ghost small" id="prevBtn">◀ Önceki</button>
        <button class="btn small" id="flipBtn">🔄 Çevir (Boşluk)</button>
        <button class="btn ghost small" id="nextBtn">Sonraki ▶</button>

        <button class="btn secondary small" id="testModeBtn">📝 Test Modu</button>
        <button class="btn small" id="knowBtn">✅ Biliyorum</button>
      </div>

      <div class="quiz" id="quizArea" aria-hidden="true">
        <div class="small-muted">Test Modu: Türkçe gösterilecek, doğru İngilizceyi seçin.</div>
        <div id="quizPrompt" style="margin-top:10px;font-weight:800;font-size:1.1rem"></div>
        <div class="options" id="quizOptions"></div>
        <div style="margin-top:10px;display:flex;gap:8px;justify-content:flex-end">
          <div class="small-muted">Puan: <span id="quizScore">0</span></div>
          <button class="btn ghost small" id="quizNext">Atla</button>
        </div>
      </div>

      <div class="footer-row">
        <div class="small-muted">Hazırlayan: Selçuk UZUNAL</div>
        <div style="display:flex;gap:8px;align-items:center">
          <div class="small-muted">İlerleme</div>
          <div class="progress" role="progressbar" aria-valuemin="0" aria-valuemax="100">
            <i id="progressBar"></i>
          </div>
        </div>
      </div>
    </main>
  </div>

  <script>
    // Tema değiştirici (basit)
    function toggleTheme(){
      const body = document.body;
      if(body.dataset.theme === 'dark'){
        body.removeAttribute('data-theme');
      } else {
        body.dataset.theme = 'dark';
      }
    }

    // ---- Tam kelime veri tabanı (kullanıcının sağladığı tüm kategoriler) ----
    const wordSets = {
            "1. Zamirler (I, You, He, She)": [
                { english: "I", turkish: "Ben" },
                { english: "You", turkish: "Sen" },
                { english: "He", turkish: "O (erkek)" },
                { english: "She", turkish: "O (kadın)" },
                { english: "It", turkish: "O (cansız/hayvan)" },
                { english: "We", turkish: "Biz" },
                { english: "They", turkish: "Onlar" },
                { english: "My", turkish: "Benim" },
                { english: "Your", turkish: "Senin" },
                { english: "His", turkish: "Onun (erkek)" },
                { english: "Her", turkish: "Onun (kadın)" },
                { english: "Our", turkish: "Bizim" },
                { english: "Their", turkish: "Onların" }
            ],

            "2. Meslekler (Jobs)": [
                { english: "Teacher", turkish: "Öğretmen" },
                { english: "Doctor", turkish: "Doktor" },
                { english: "Nurse", turkish: "Hemşire" },
                { english: "Engineer", turkish: "Mühendis" },
                { english: "Police officer", turkish: "Polis" },
                { english: "Firefighter", turkish: "İtfaiyeci" },
                { english: "Chef", turkish: "Şef" },
                { english: "Driver", turkish: "Şoför" },
                { english: "Farmer", turkish: "Çiftçi" },
                { english: "Singer", turkish: "Şarkıcı" },
                { english: "Artist", turkish: "Sanatçı" },
                { english: "Student", turkish: "Öğrenci" }
            ],

            "3. Renkler (Colors)": [
                { english: "Red", turkish: "Kırmızı" },
                { english: "Blue", turkish: "Mavi" },
                { english: "Green", turkish: "Yeşil" },
                { english: "Yellow", turkish: "Sarı" },
                { english: "Black", turkish: "Siyah" },
                { english: "White", turkish: "Beyaz" },
                { english: "Orange", turkish: "Turuncu" },
                { english: "Purple", turkish: "Mor" },
                { english: "Pink", turkish: "Pembe" },
                { english: "Brown", turkish: "Kahverengi" },
                { english: "Gray", turkish: "Gri" },
                { english: "Gold", turkish: "Altın" },
                { english: "Silver", turkish: "Gümüş" }
            ],

            "4. Aile ve İlişkiler": [
                { english: "Mother", turkish: "Anne" },
                { english: "Father", turkish: "Baba" },
                { english: "Sister", turkish: "Kız kardeş" },
                { english: "Brother", turkish: "Erkek kardeş" },
                { english: "Grandmother", turkish: "Büyükanne" },
                { english: "Grandfather", turkish: "Büyükbaba" },
                { english: "Aunt", turkish: "Hala/Teyze" },
                { english: "Uncle", turkish: "Amca/Dayı" },
                { english: "Cousin", turkish: "Kuzen" },
                { english: "Friend", turkish: "Arkadaş" },
                { english: "Best friend", turkish: "En iyi arkadaş" },
                { english: "Family", turkish: "Aile" }
            ],

            "5. Meyve ve Sebzeler": [
                { english: "Apple", turkish: "Elma" },
                { english: "Banana", turkish: "Muz" },
                { english: "Orange", turkish: "Portakal" },
                { english: "Strawberry", turkish: "Çilek" },
                { english: "Grape", turkish: "Üzüm" },
                { english: "Watermelon", turkish: "Karpuz" },
                { english: "Tomato", turkish: "Domates" },
                { english: "Potato", turkish: "Patates" },
                { english: "Carrot", turkish: "Havuç" },
                { english: "Onion", turkish: "Soğan" },
                { english: "Lemon", turkish: "Limon" },
                { english: "Cherry", turkish: "Kiraz" }
            ],

            "6. Hayvanlar (Animals)": [
                { english: "Dog", turkish: "Köpek" },
                { english: "Cat", turkish: "Kedi" },
                { english: "Bird", turkish: "Kuş" },
                { english: "Fish", turkish: "Balık" },
                { english: "Horse", turkish: "At" },
                { english: "Cow", turkish: "İnek" },
                { english: "Sheep", turkish: "Koyun" },
                { english: "Lion", turkish: "Aslan" },
                { english: "Elephant", turkish: "Fil" },
                { english: "Monkey", turkish: "Maymun" },
                { english: "Rabbit", turkish: "Tavşan" },
                { english: "Butterfly", turkish: "Kelebek" }
            ],

            "7. Zaman Kavramları": [
                { english: "Today", turkish: "Bugün" },
                { english: "Yesterday", turkish: "Dün" },
                { english: "Tomorrow", turkish: "Yarın" },
                { english: "Now", turkish: "Şimdi" },
                { english: "Later", turkish: "Sonra" },
                { english: "Morning", turkish: "Sabah" },
                { english: "Afternoon", turkish: "Öğleden sonra" },
                { english: "Evening", turkish: "Akşam" },
                { english: "Night", turkish: "Gece" },
                { english: "Week", turkish: "Hafta" },
                { english: "Month", turkish: "Ay" },
                { english: "Year", turkish: "Yıl" },
                { english: "Always", turkish: "Her zaman" },
                { english: "Never", turkish: "Hiç" }
            ],

            "8. Soru Kelimeleri": [
                { english: "What", turkish: "Ne" },
                { english: "Who", turkish: "Kim" },
                { english: "Where", turkish: "Nerede" },
                { english: "When", turkish: "Ne zaman" },
                { english: "Why", turkish: "Neden" },
                { english: "How", turkish: "Nasıl" },
                { english: "Which", turkish: "Hangi" },
                { english: "How many", turkish: "Kaç tane" },
                { english: "How much", turkish: "Ne kadar" },
                { english: "How old", turkish: "Kaç yaşında" },
                { english: "What time", turkish: "Saat kaç" },
                { english: "Whose", turkish: "Kimin" }
            ],

            "9. Temel Fiiller": [
                { english: "To be", turkish: "Olmak" },
                { english: "To have", turkish: "Sahip olmak" },
                { english: "To do", turkish: "Yapmak" },
                { english: "To go", turkish: "Gitmek" },
                { english: "To come", turkish: "Gelmek" },
                { english: "To see", turkish: "Görmek" },
                { english: "To hear", turkish: "Duymak" },
                { english: "To speak", turkish: "Konuşmak" },
                { english: "To eat", turkish: "Yemek yemek" },
                { english: "To drink", turkish: "İçmek" },
                { english: "To sleep", turkish: "Uyumak" },
                { english: "To learn", turkish: "Öğrenmek" }
            ],

            "10. Okul ve Eğitim": [
                { english: "School", turkish: "Okul" },
                { english: "Book", turkish: "Kitap" },
                { english: "Pen", turkish: "Kalem" },
                { english: "Pencil", turkish: "Kurşun kalem" },
                { english: "Teacher", turkish: "Öğretmen" },
                { english: "Student", turkish: "Öğrenci" },
                { english: "Classroom", turkish: "Sınıf" },
                { english: "Homework", turkish: "Ev ödevi" },
                { english: "Exam", turkish: "Sınav" },
                { english: "Lesson", turkish: "Ders" },
                { english: "Learn", turkish: "Öğrenmek" },
                { english: "Study", turkish: "Çalışmak" }
            ],

            "11. Günlük Rutinler": [
                { english: "Go to the bathroom", turkish: "Tuvalete git" },
                { english: "Brush your teeth", turkish: "Dişlerini fırçala" },
                { english: "Wash your hands", turkish: "Ellerini yıka" },
                { english: "Wash your face", turkish: "Yüzünü yıka" },
                { english: "It's shower time", turkish: "Duş zamanı" },
                { english: "Put on your clothes", turkish: "Kıyafetlerini giy" },
                { english: "Put on your shoes", turkish: "Ayakkabılarını giy" },
                { english: "Don't forget your coat", turkish: "Montunu unutma" },
                { english: "Did you take your bag?", turkish: "Çantanı aldın mı?" },
                { english: "The food is ready", turkish: "Yemek hazır" },
                { english: "Are you done?", turkish: "Bitirdin mi?" },
                { english: "It's bedtime", turkish: "Yatma vakti" },
                { english: "Sweet dreams", turkish: "Tatlı rüyalar" },
                { english: "See you tomorrow", turkish: "Yarın görüşürüz" }
            ],

            "12. Sınıf Nesneleri": [
                { english: "Board", turkish: "Yazı tahtası" },
                { english: "Window", turkish: "Pencere" },
                { english: "Desk", turkish: "Sıra" },
                { english: "Table", turkish: "Masa" },
                { english: "Chair", turkish: "Sandalye" },
                { english: "Pen", turkish: "Kalem" },
                { english: "Pencil", turkish: "Kurşun kalem" },
                { english: "Ruler", turkish: "Cetvel" },
                { english: "Eraser", turkish: "Silgi" },
                { english: "Pencil case", turkish: "Kalemlik" },
                { english: "Pencil sharpener", turkish: "Kalemtıraş" },
                { english: "School bag", turkish: "Okul çantası" },
                { english: "Book", turkish: "Kitap" },
                { english: "Dictionary", turkish: "Sözlük" },
                { english: "Scissors", turkish: "Makas" },
                { english: "Crayons", turkish: "Pastel boyalar" }
            ],

            "13. Sınıf Komutları": [
                { english: "Sit down", turkish: "Otur" },
                { english: "Stand up", turkish: "Kalk" },
                { english: "Listen to me", turkish: "Beni dinle" },
                { english: "Look at", turkish: "Bak" },
                { english: "Turn around", turkish: "Arkanı dön" },
                { english: "Be quiet", turkish: "Sessiz ol" },
                { english: "Pay attention", turkish: "Dikkatini ver" },
                { english: "Raise your hand", turkish: "Elini kaldır" },
                { english: "Answer the question", turkish: "Soruyu cevapla" },
                { english: "Clean the board", turkish: "Tahtayı temizle" },
                { english: "Come in", turkish: "İçeri gir" },
                { english: "Go back to your place", turkish: "Yerine dön" },
                { english: "Turn on the light", turkish: "Işığı aç" },
                { english: "Turn off the light", turkish: "Işığı kapat" },
                { english: "Open the window", turkish: "Pencereyi aç" },
                { english: "Close the window", turkish: "Pencereyi kapat" }
            ],

            "14. Nezaket İfadeleri": [
                { english: "Excuse me", turkish: "Affedersiniz" },
                { english: "Please", turkish: "Lütfen" },
                { english: "Thank you", turkish: "Teşekkür ederim" },
                { english: "You're welcome", turkish: "Rica ederim" },
                { english: "Sorry", turkish: "Özür dilerim" },
                { english: "May I come in?", turkish: "İçeri girebilir miyim?" },
                { english: "Here you are", turkish: "Buyurun" },
                { english: "Give me", turkish: "Bana ver" },
                { english: "I'm sorry", turkish: "Üzgünüm" },
                { english: "Not right now", turkish: "Şu an olmaz" }
            ],

            "15. Fiziksel Eylemler": [
                { english: "Walk", turkish: "Yürümek" },
                { english: "Run", turkish: "Koşmak" },
                { english: "Jump", turkish: "Zıplamak" },
                { english: "Climb", turkish: "Tırmanmak" },
                { english: "Fly", turkish: "Uçmak" },
                { english: "Swim", turkish: "Yüzmek" },
                { english: "Dance", turkish: "Dans etmek" },
                { english: "Paint", turkish: "Boyamak" },
                { english: "Write", turkish: "Yazmak" },
                { english: "Read", turkish: "Okumak" },
                { english: "Listen", turkish: "Dinlemek" },
                { english: "Speak", turkish: "Konuşmak" }
            ],

            "16. Yetenekler (Can/Cant)": [
                { english: "I can play the piano", turkish: "Piyano çalabilirim" },
                { english: "I can drive a car", turkish: "Araba sürebilirim" },
                { english: "I can take pictures", turkish: "Fotoğraf çekebilirim" },
                { english: "I can ride a bike", turkish: "Bisiklete binebilirim" },
                { english: "I can swim", turkish: "Yüzebilirim" },
                { english: "I can speak English", turkish: "İngilizce konuşabilirim" },
                { english: "I can cook", turkish: "Yemek yapabilirim" },
                { english: "I can't drive a car", turkish: "Araba süremem" },
                { english: "I can't play the guitar", turkish: "Gitar çalamam" },
                { english: "I can't speak French", turkish: "Fransızca konuşamam" }
            ],

            "17. Ülkeler ve Milliyetler": [
                { english: "Turkey", turkish: "Türkiye" },
                { english: "Turkish", turkish: "Türk" },
                { english: "USA", turkish: "ABD" },
                { english: "American", turkish: "Amerikalı" },
                { english: "England", turkish: "İngiltere" },
                { english: "British", turkish: "Britanyalı" },
                { english: "Spain", turkish: "İspanya" },
                { english: "Spanish", turkish: "İspanyol" },
                { english: "France", turkish: "Fransa" },
                { english: "French", turkish: "Fransız" },
                { english: "Italy", turkish: "İtalya" },
                { english: "Italian", turkish: "İtalyan" },
                { english: "Germany", turkish: "Almanya" },
                { english: "German", turkish: "Alman" },
                { english: "Japan", turkish: "Japonya" },
                { english: "Japanese", turkish: "Japon" },
                { english: "China", turkish: "Çin" },
                { english: "Chinese", turkish: "Çinli" },
                { english: "Russia", turkish: "Rusya" },
                { english: "Russian", turkish: "Rus" },
                { english: "Australia", turkish: "Avustralya" },
                { english: "Australian", turkish: "Avustralyalı" },
                { english: "Pakistan", turkish: "Pakistan" },
                { english: "Pakistani", turkish: "Pakistanlı" },
                { english: "Egypt", turkish: "Mısır" },
                { english: "Egyptian", turkish: "Mısırlı" },
                { english: "Greece", turkish: "Yunanistan" },
                { english: "Greek", turkish: "Yunan" },
                { english: "Iran", turkish: "İran" },
                { english: "Iranian", turkish: "İranlı" },
                { english: "Iraq", turkish: "Irak" },
                { english: "Iraqi", turkish: "Iraklı" }
            ],

            "18. Spor ve Aktiviteler": [
                { english: "Play football", turkish: "Futbol oynamak" },
                { english: "Play tennis", turkish: "Tenis oynamak" },
                { english: "Play basketball", turkish: "Basketbol oynamak" },
                { english: "Ride a bike", turkish: "Bisiklete binmek" },
                { english: "Ride a horse", turkish: "Ata binmek" },
                { english: "Swim", turkish: "Yüzmek" },
                { english: "Run fast", turkish: "Hızlı koşmak" },
                { english: "Jump high", turkish: "Yükseğe zıplamak" },
                { english: "Fly a kite", turkish: "Uçurtma uçurmak" },
                { english: "Play the piano", turkish: "Piyano çalmak" },
                { english: "Play the drum", turkish: "Davul çalmak" },
                { english: "Dance", turkish: "Dans etmek" }
            ],

            "19. Yönler ve Renkler": [
                { english: "North", turkish: "Kuzey" },
                { english: "South", turkish: "Güney" },
                { english: "East", turkish: "Doğu" },
                { english: "West", turkish: "Batı" },
                { english: "Blue", turkish: "Mavi" },
                { english: "Red", turkish: "Kırmızı" },
                { english: "Green", turkish: "Yeşil" },
                { english: "Yellow", turkish: "Sarı" },
                { english: "White", turkish: "Beyaz" },
                { english: "Black", turkish: "Siyah" }
            ],

            "20. Oyun ve Sosyal İfadeler": [
                { english: "Let's play a game", turkish: "Oyun oynayalım" },
                { english: "Calm down", turkish: "Sakin ol" },
                { english: "It's your turn", turkish: "Senin sıran" },
                { english: "Good job", turkish: "Aferin" },
                { english: "Let's try again", turkish: "Tekrar deneyelim" },
                { english: "Take a break", turkish: "Mola ver" },
                { english: "Help people", turkish: "İnsanlara yardım et" },
                { english: "I think so", turkish: "Öyle düşünüyorum" },
                { english: "I don't think so", turkish: "Öyle düşünmüyorum" },
                { english: "Catch the ball", turkish: "Topu yakala" },
                { english: "Do puzzles", turkish: "Bulmaca çöz" }
            ],

           "21. Sayılar (0-1000)": [
                { english: "Zero", turkish: "Sıfır" },
                { english: "One", turkish: "Bir" },
                { english: "Two", turkish: "İki" },
                { english: "Three", turkish: "Üç" },
                { english: "Four", turkish: "Dört" },
                { english: "Five", turkish: "Beş" },
                { english: "Six", turkish: "Altı" },
                { english: "Seven", turkish: "Yedi" },
                { english: "Eight", turkish: "Sekiz" },
                { english: "Nine", turkish: "Dokuz" },
                { english: "Ten", turkish: "On" },
                { english: "Eleven", turkish: "On bir" },
                { english: "Twelve", turkish: "On iki" },
                { english: "Thirteen", turkish: "On üç" },
                { english: "Fourteen", turkish: "On dört" },
                { english: "Fifteen", turkish: "On beş" },
                { english: "Sixteen", turkish: "On altı" },
                { english: "Seventeen", turkish: "On yedi" },
                { english: "Eighteen", turkish: "On sekiz" },
                { english: "Nineteen", turkish: "On dokuz" },
                { english: "Twenty", turkish: "Yirmi" },
                { english: "Thirty", turkish: "Otuz" },
                { english: "Forty", turkish: "Kırk" },
                { english: "Fifty", turkish: "Elli" },
                { english: "Sixty", turkish: "Altmış" },
                { english: "Seventy", turkish: "Yetmiş" },
                { english: "Eighty", turkish: "Seksen" },
                { english: "Ninety", turkish: "Doksan" },
                { english: "One hundred", turkish: "Yüz" },
                { english: "Two hundred", turkish: "İki yüz" },
                { english: "Three hundred", turkish: "Üç yüz" },
                { english: "Four hundred", turkish: "Dört yüz" },
                { english: "Five hundred", turkish: "Beş yüz" },
                { english: "Six hundred", turkish: "Altı yüz" },
                { english: "Seven hundred", turkish: "Yedi yüz" },
                { english: "Eight hundred", turkish: "Sekiz yüz" },
                { english: "Nine hundred", turkish: "Dokuz yüz" },
                { english: "One thousand", turkish: "Bin" }
            ],

            "22. Vücut Bölümleri": [
                { english: "Head", turkish: "Baş" },
                { english: "Eye", turkish: "Göz" },
                { english: "Nose", turkish: "Burun" },
                { english: "Mouth", turkish: "Ağız" },
                { english: "Tongue", turkish: "Dil" },
                { english: "Lip", turkish: "Dudak" },
                { english: "Hand", turkish: "El" },
                { english: "Foot", turkish: "Ayak" }
            ],

            "23. Ek Kelimeler": [
                { english: "Board", turkish: "Tahta" },
                { english: "Book", turkish: "Kitap" },
                { english: "Chair", turkish: "Sandalye" },
                { english: "Crayon", turkish: "Pastel boya" },
                { english: "Desk", turkish: "Sıra" },
                { english: "Dictionary", turkish: "Sözlük" },
                { english: "Door", turkish: "Kapı" },
                { english: "Eraser / Rubber", turkish: "Silgi" },
                { english: "Glue", turkish: "Yapıştırıcı" },
                { english: "Map", turkish: "Harita" },
                { english: "Notebook", turkish: "Defter" },
                { english: "Pen", turkish: "Tükenmez kalem" },
                { english: "Pencil", turkish: "Kurşun kalem" },
                { english: "Pencil case", turkish: "Kalem kutusu" },
                { english: "Pencil sharpener", turkish: "Kalemtıraş" },
                { english: "Ruler", turkish: "Cetvel" },
                { english: "Scissors", turkish: "Makas" },
                { english: "Table", turkish: "Masa" },
                { english: "Window", turkish: "Pencere" },
                { english: "Ten", turkish: "On" },
                { english: "Twenty", turkish: "Yirmi" },
                { english: "Thirty", turkish: "Otuz" },
                { english: "Forty", turkish: "Kırk" },
                { english: "Fifty", turkish: "Elli" },
                { english: "Take", turkish: "Almak" },
                { english: "Excuse me", turkish: "Affedersiniz" },
                { english: "Give me", turkish: "Bana ver" },
                { english: "Please", turkish: "Lütfen" },
                { english: "Sure / Of course", turkish: "Tabii / Elbette" },
                { english: "Here you are", turkish: "Buyurun" },
                { english: "Thank you", turkish: "Teşekkür ederim" },
                { english: "You're welcome", turkish: "hoşgeldiniz" },
                { english: "Be quiet", turkish: "Sessiz olun" },
                { english: "Close the door", turkish: "Kapıyı kapat" },
                { english: "Open the window", turkish: "Pencereyi aç" },
                { english: "Come in", turkish: "İçeri gir" },
                { english: "Turn on the light", turkish: "Işığı aç" },
                { english: "Turn off the light", turkish: "Işığı kapat" },
                { english: "Listen to me", turkish: "Beni dinle" },
                { english: "Turn around", turkish: "Arkanı dön" },
                { english: "Sit down", turkish: "Otur" },
                { english: "Stand up", turkish: "Ayağa kalk" },
                { english: "Clean the board", turkish: "Tahtayı sil" },
                { english: "Answer the question", turkish: "Soruyu cevapla" },
                { english: "Cartoon", turkish: "Çizgi film" },
                { english: "Character", turkish: "Karakter" },
                { english: "Play the piano", turkish: "Piyano çalmak" },
                { english: "Play the drum", turkish: "Davul çalmak" },
                { english: "Sing a song", turkish: "Şarkı söylemek" },
                { english: "Fly", turkish: "Uçmak" },
                { english: "Dance", turkish: "Dans etmek" },
                { english: "Ride a horse", turkish: "Ata binmek" },
                { english: "Ride a bike", turkish: "Bisiklete binmek" },
                { english: "Take pictures / photos", turkish: "Fotoğraf çekmek" },
                { english: "Carry", turkish: "Taşımak" },
                { english: "Dive", turkish: "Dalış yapmak" },
                { english: "Play tennis", turkish: "Tenis oynamak" },
                { english: "Catch the ball", turkish: "Topu yakalamak" },
                { english: "Play football", turkish: "Futbol oynamak" },
                { english: "Swim", turkish: "Yüzmek" },
                { english: "Paint", turkish: "Boyamak" },
                { english: "Fly a kite", turkish: "Uçurtma uçurmak" },
                { english: "Read a book", turkish: "Kitap okumak" },
                { english: "Drive a car", turkish: "Araba sürmek" },
                { english: "Do puzzles", turkish: "Yapboz yapmak" },
                { english: "Change shape", turkish: "Şekil değiştirmek" },
                { english: "Be invisible", turkish: "Görünmez olmak" },
                { english: "Jump high", turkish: "Yükseğe zıplamak" },
                { english: "Cook", turkish: "Yemek pişirmek" },
                { english: "Climb", turkish: "Tırmanmak" },
                { english: "Turn green", turkish: "Yeşile dönmek" },
                { english: "Run fast", turkish: "Hızlı koşmak" },
                { english: "Help people", turkish: "İnsanlara yardım etmek" },
                { english: "Save people", turkish: "İnsanları kurtarmak" },
                { english: "Walk", turkish: "Yürümek" },
                { english: "Whose", turkish: "Kimin" },
                { english: "My", turkish: "Benim" },
                { english: "Your", turkish: "Senin / Sizin" },
                { english: "His", turkish: "Onun (erkek)" },
                { english: "Her", turkish: "Onun (kadın)" },
                { english: "And", turkish: "Ve" },
                { english: "But", turkish: "Ama" },
                { english: "Swimming", turkish: "Yüzme" },
                { english: "Riding a bike", turkish: "Bisiklete binme" },
                { english: "Playing football", turkish: "Futbol oynama" },
                { english: "Reading a book", turkish: "Kitap okuma" },
                { english: "Sliding", turkish: "Kayma" },
                { english: "Swinging", turkish: "Sallanma" },
                { english: "Playing tennis", turkish: "Tenis oynama" },
                { english: "Singing a song", turkish: "Şarkı söyleme" },
                { english: "Watching cartoons", turkish: "Çizgi film izleme" },
                { english: "Painting", turkish: "Resim yapma" },
                { english: "Flying a kite", turkish: "Uçurtma uçurma" },
                { english: "Running", turkish: "Koşma" },
                { english: "Cooking", turkish: "Yemek pişirme" },
                { english: "Drawing pictures", turkish: "Resim çizme" },
                { english: "Skipping rope", turkish: "İp atlama" },
                { english: "Playing basketball", turkish: "Basketbol oynama" },
                { english: "Dancing", turkish: "Dans etme" },
                { english: "Doing puzzles", turkish: "Yapboz yapma" },
                { english: "Skating", turkish: "Paten kayma" },
                { english: "Listening to music", turkish: "Müzik dinleme" },
                { english: "Driving a car", turkish: "Araba sürme" },
                { english: "Playing chess", turkish: "Satranç oynama" },
                { english: "Like", turkish: "Sevmek" },
                { english: "Love", turkish: "Çok sevmek" },
                { english: "Dislike / Don't like", turkish: "Sevmemek" },
                { english: "Not much", turkish: "Pek değil" },
                { english: "Pardon me", turkish: "Affedersiniz" },
                { english: "Say that again, please", turkish: "Tekrar söyler misiniz?" },
                { english: "Slowly, please", turkish: "Yavaşça lütfen" },
                { english: "Repeat, please", turkish: "Tekrar eder misiniz?" }
            ]
        };

    // ---- DOM ----
    const categorySelect = document.getElementById('categorySelect');
    const categoryList = document.getElementById('categoryList');
    const catCount = document.getElementById('catCount');
    const currentCatLabel = document.getElementById('currentCatLabel');

    const card = document.getElementById('card');
    const cardInner = document.getElementById('cardInner');
    const frontFace = document.getElementById('frontFace');
    const backFace = document.getElementById('backFace');
    const frontText = document.getElementById('frontText');
    const backText = document.getElementById('backText');
    const wordMeta = document.getElementById('wordMeta');

    const prevBtn = document.getElementById('prevBtn');
    const nextBtn = document.getElementById('nextBtn');
    const flipBtn = document.getElementById('flipBtn');
    const knowBtn = document.getElementById('knowBtn');

    const shuffleBtn = document.getElementById('shuffleBtn');
    const resetProgressBtn = document.getElementById('resetProgressBtn');

    const voiceSelect = document.getElementById('voiceSelect');
    const rateRange = document.getElementById('rateRange');
    const rateVal = document.getElementById('rateVal');
    const speakBtn = document.getElementById('speakBtn');
    const autoplayToggle = document.getElementById('autoplayToggle');

    const exportBtn = document.getElementById('exportBtn');
    const importBtn = document.getElementById('importBtn');
    const importFile = document.getElementById('importFile');

    const newEnglish = document.getElementById('newEnglish');
    const newTurkish = document.getElementById('newTurkish');
    const addCardBtn = document.getElementById('addCardBtn');
    const removeKnownBtn = document.getElementById('removeKnownBtn');

    const modeIndicator = document.getElementById('modeIndicator');
    const counter = document.getElementById('counter');
    const progressBar = document.getElementById('progressBar');

    const testModeBtn = document.getElementById('testModeBtn');
    const quizArea = document.getElementById('quizArea');
    const quizPrompt = document.getElementById('quizPrompt');
    const quizOptions = document.getElementById('quizOptions');
    const quizScoreEl = document.getElementById('quizScore');
    const quizNext = document.getElementById('quizNext');

    const currentCatKey = 'flashcards_v2_state';

    // ---- State ----
    let currentCategory = null;
    let currentWords = [];
    let order = []; // index order array
    let currentIndex = 0;
    let autoplay = false;
    let testMode = false;
    let quizScore = 0;

    // Persisted state structure in localStorage:
    // { categoryName: { order: [...], index: n, known: [indexes] }, ... }
    let persisted = loadState();

    // ---- Helpers ----
    function saveState(){
      localStorage.setItem(currentCatKey, JSON.stringify(persisted));
    }
    function loadState(){
      try{
        const raw = localStorage.getItem(currentCatKey);
        return raw ? JSON.parse(raw) : {};
      }catch(e){
        console.warn('State load error', e);
        return {};
      }
    }

    function populateCategories(){
      categorySelect.innerHTML = '';
      const emptyOpt = document.createElement('option');
      emptyOpt.value = '';
      emptyOpt.textContent = 'Kategori Seçin';
      categorySelect.appendChild(emptyOpt);

      catCount.textContent = Object.keys(wordSets).length;
      categoryList.innerHTML = '';
      for(const cat of Object.keys(wordSets)){
        const opt = document.createElement('option');
        opt.value = cat;
        opt.textContent = cat;
        categorySelect.appendChild(opt);

        // sidebar quick list
        const div = document.createElement('div');
        div.className = 'category-item';
        div.innerHTML = `<strong>${cat}</strong><span class="small">${wordSets[cat].length} kelime</span>`;
        div.addEventListener('click', ()=> {
          categorySelect.value = cat;
          selectCategory(cat);
          // scroll to top of app for visibility
          window.scrollTo({ top: 0, behavior: 'smooth' });
        });
        categoryList.appendChild(div);
      }
    }

    function initCategoryState(cat){
      if(!persisted[cat]){
        persisted[cat] = {
          order: wordSets[cat].map((_,i)=>i),
          index: 0,
          known: []
        };
        saveState();
      }
    }

    function loadCategory(cat){
      currentCategory = cat;
      currentCatLabel.textContent = cat || '-';
      if(!cat){
        currentWords = [];
        order = [];
        currentIndex = 0;
        renderEmpty();
        return;
      }
      initCategoryState(cat);
      // apply saved order
      order = persisted[cat].order.slice();
      // filter out known indexes if present
      const known = new Set(persisted[cat].known || []);
      if(known.size){
        order = order.filter(i=>!known.has(i));
      }
      currentWords = order.map(i=>wordSets[cat][i]);
      currentIndex = Math.min(Math.max(0, persisted[cat].index || 0), Math.max(0, currentWords.length-1));
      updateUI();
    }

    function selectCategory(cat){
      // reset UI
      loadCategory(cat);
      saveProgressToPersist();
      updateUI();
    }

    function renderEmpty(){
      frontText.textContent = 'Kategori Seçin';
      backText.textContent = '👆 Yukarıdan seçim yapın';
      wordMeta.textContent = '';
      counter.textContent = '0 / 0';
      progressBar.style.width = '0%';
      // ensure reveal state cleared
      frontFace.dataset.revealed = 'false';
      card.classList.remove('flipped');
    }

    function updateUI(){
      // reset any front reveal when updating card
      frontFace.dataset.revealed = 'false';
      card.classList.remove('flipped');

      if(!currentCategory || currentWords.length===0){
        renderEmpty();
        return;
      }
      const w = currentWords[currentIndex];
      // mode: English -> Turkish (default). If testMode then reverse.
      if(testMode){
        frontText.textContent = w.turkish || '';
        backText.textContent = w.english || '';
        modeIndicator.textContent = '🔤 Türkçe → İngilizce (Test)';
        quizArea.classList.add('show');
        quizArea.setAttribute('aria-hidden','false');
      }else{
        frontText.textContent = w.english || '';
        backText.textContent = w.turkish || '';
        modeIndicator.textContent = '🔤 İngilizce → Türkçe';
        quizArea.classList.remove('show');
        quizArea.setAttribute('aria-hidden','true');
      }
      wordMeta.textContent = `${currentIndex+1}/${currentWords.length}`;
      counter.textContent = `${currentIndex+1} / ${currentWords.length}`;
      // progress
      const total = (wordSets[currentCategory] || []).length;
      const removed = (persisted[currentCategory] && persisted[currentCategory].known)? persisted[currentCategory].known.length : 0;
      const ratio = Math.round( ((currentIndex+1 + removed) / total) * 100 );
      progressBar.style.width = Math.min(100, ratio) + '%';
      // save index
      saveProgressToPersist();
      // speak if autoplay
      if(autoplay && !card.classList.contains('flipped') && !testMode){
        speakCurrent();
      }
    }

    function saveProgressToPersist(){
      if(!currentCategory) return;
      persisted[currentCategory] = persisted[currentCategory] || {};
      persisted[currentCategory].index = currentIndex;
      saveState();
    }

    function shuffleCurrent(){
      if(!currentCategory) return;
      // shuffle persisted[cat].order and re-generate currentWords excluding known
      const arr = persisted[currentCategory].order.slice();
      for(let i=arr.length-1;i>0;i--){
        const j = Math.floor(Math.random()*(i+1));
        [arr[i],arr[j]]=[arr[j],arr[i]];
      }
      persisted[currentCategory].order = arr;
      // update visible order excluding known
      const known = new Set(persisted[currentCategory].known || []);
      order = arr.filter(i=>!known.has(i));
      currentWords = order.map(i=>wordSets[currentCategory][i]);
      currentIndex = 0;
      saveState();
      updateUI();
    }

    function nextCard(){
      // clear any reveal when moving
      frontFace.dataset.revealed = 'false';
      card.classList.remove('flipped');

      if(!currentWords.length) return;
      if(currentIndex < currentWords.length-1){
        currentIndex++;
        updateUI();
      }else{
        // end reached
        currentIndex = currentWords.length-1;
        updateUI();
        // small notice
        alert('Bu kategori sonuna ulaştınız. Karıştır düğmesiyle yeniden başlayabilirsiniz veya bilinenleri kaldırabilirsiniz.');
      }
    }
    function prevCard(){
      // clear any reveal when moving
      frontFace.dataset.revealed = 'false';
      card.classList.remove('flipped');

      if(!currentWords.length) return;
      if(currentIndex > 0){
        currentIndex--;
        updateUI();
      }
    }

    function flipCard(){
      if(!currentWords.length) return;
      // when flipping, also clear the "front reveal" flag so we don't mix modes
      frontFace.dataset.revealed = 'false';
      card.classList.toggle('flipped');
      // if flipped to back and autoplay enabled in test mode, speak the back (english)
      if(card.classList.contains('flipped')){
        if(testMode){
          // speak english (back)
          speakText(currentWords[currentIndex].english);
        } else {
          // nothing by default
        }
      } else {
        // flipped back to front
        if(autoplay && !testMode){
          speakCurrent();
        }
      }
    }

    function markKnownAndAdvance(){
      if(!currentCategory || !currentWords.length) return;
      const originalIndex = order[currentIndex]; // index in original array
      persisted[currentCategory].known = persisted[currentCategory].known || [];
      if(!persisted[currentCategory].known.includes(originalIndex)){
        persisted[currentCategory].known.push(originalIndex);
      }
      // remove from visible arrays
      order.splice(currentIndex,1);
      currentWords.splice(currentIndex,1);
      if(currentIndex >= currentWords.length) currentIndex = Math.max(0, currentWords.length-1);
      saveState();
      updateUI();
    }

    function removeKnowns(){
      if(!currentCategory) return;
      if(!persisted[currentCategory] || !persisted[currentCategory].known || persisted[currentCategory].known.length===0){
        alert('Bilinen kart yok.');
        return;
      }
      const confirmed = confirm('Bu kategori için işaretlenmiş "bilinen" kartlar kalıcı olarak silinecek. Devam edilsin mi?');
      if(!confirmed) return;
      // remove known from original array
      const knownSet = new Set(persisted[currentCategory].known);
      const orig = wordSets[currentCategory];
      const filtered = orig.filter((_,i)=>!knownSet.has(i));
      wordSets[currentCategory] = filtered;
      // rebuild persisted order for this category
      persisted[currentCategory].order = filtered.map((_,i)=>i);
      persisted[currentCategory].known = [];
      saveState();
      // reload category UI
      loadCategory(currentCategory);
      updateUI();
      alert('Bilinen kartlar silindi ve kategori güncellendi.');
    }

    // ---- Speech ----
    let voices = [];
    function populateVoices(){
      voices = speechSynthesis.getVoices() || [];
      voiceSelect.innerHTML = '';
      const def = document.createElement('option'); def.value=''; def.textContent = 'Varsayılan (tarayıcı)';
      voiceSelect.appendChild(def);
      voices.forEach(v=>{
        const o = document.createElement('option');
        o.value = v.name;
        o.textContent = `${v.name} — ${v.lang}`;
        voiceSelect.appendChild(o);
      });
    }
    function ensureVoices(){
      if(typeof speechSynthesis !== 'undefined'){
        populateVoices();
        speechSynthesis.onvoiceschanged = populateVoices;
      }
    }

    function speakText(text, lang='en-US'){
      if(!('speechSynthesis' in window)) { alert('Tarayıcı ses özelliğini desteklemiyor.'); return; }
      speechSynthesis.cancel();
      const u = new SpeechSynthesisUtterance(text);
      u.lang = lang;
      u.rate = parseFloat(rateRange.value) || 0.9;
      const chosen = voiceSelect.value;
      if(chosen){
        const v = voices.find(x=>x.name===chosen);
        if(v) u.voice = v;
      }else{
        // prefer en- voices when speaking english
        const preferred = voices.find(v => v.lang && v.lang.startsWith('en'));
        if(preferred) u.voice = preferred;
      }
      u.onend = ()=>{ speakBtn.textContent='🔊 Oku'; speakBtn.style.background=''; };
      u.onerror = ()=>{ speakBtn.textContent='🔊 Oku'; speakBtn.style.background=''; };
      speakBtn.textContent='🔊 Oynatılıyor...';
      speakBtn.style.background='#FF9800';
      speechSynthesis.speak(u);
    }

    function speakCurrent(){
      if(!currentWords.length) return;
      if(testMode){
        // in test mode front is Turkish, don't autoplay
        return;
      }else{
        speakText(currentWords[currentIndex].english || '', 'en-US');
      }
    }

    // ---- Reveal behavior: click on the front English word to show Turkish on the front (toggle) ----
    frontFace.addEventListener('click', (e) => {
      // prevent outer card click (flip) from firing when we click specifically the front word
      e.stopPropagation();
      if(!currentWords.length) return;
      if(testMode) return; // in test mode front is Turkish already
      const revealed = frontFace.dataset.revealed === 'true';
      if(!revealed){
        // show Turkish meaning on front
        frontText.textContent = currentWords[currentIndex].turkish || '';
        frontFace.dataset.revealed = 'true';
      } else {
        // restore English
        frontText.textContent = currentWords[currentIndex].english || '';
        frontFace.dataset.revealed = 'false';
      }
    });

    // ---- Quiz (çoktan seçmeli) ----
    function startQuiz(){
      quizScore = 0;
      quizScoreEl.textContent = '0';
      nextQuizQuestion();
    }
    function nextQuizQuestion(){
      if(!currentWords.length) return;
      // pick random target from currentWords
      const targetIdx = Math.floor(Math.random()*currentWords.length);
      const target = currentWords[targetIdx];
      quizPrompt.textContent = target.turkish;
      // create 3 wrong options from entire category (not equal to target)
      const options = new Set([target.english]);
      const pool = (wordSets[currentCategory] || []).map(w=>w.english).filter(e=>e!==target.english);
      while(options.size < 4 && pool.length){
        const pick = pool.splice(Math.floor(Math.random()*pool.length),1)[0];
        options.add(pick);
      }
      const arr = shuffleArray(Array.from(options)).slice(0,4);
      quizOptions.innerHTML = '';
      arr.forEach(opt => {
        const btn = document.createElement('button');
        btn.className = 'opt';
        btn.textContent = opt;
        btn.disabled = false;
        btn.addEventListener('click', ()=>{
          // disable all options to prevent multiple clicks
          Array.from(quizOptions.children).forEach(c => c.disabled = true);

          if(opt === target.english){
            // correct: add flashing green class
            btn.classList.add('correct-flash');
            quizScore++;
            quizScoreEl.textContent = quizScore;
            speakText(opt,'en-US');
            // wait for the flash animation to complete (approx animationDuration * iterations)
            setTimeout(nextQuizQuestion, 1200);
          }else{
            // wrong: flash the clicked button red and highlight correct one as green-flash
            btn.classList.add('wrong-flash');
            Array.from(quizOptions.children).forEach(c=> {
              if(c.textContent === target.english) c.classList.add('correct-flash');
            });
            setTimeout(nextQuizQuestion, 1200);
          }
        });
        quizOptions.appendChild(btn);
      });
    }

    // ---- Utilities ----
    function shuffleArray(a){ for(let i=a.length-1;i>0;i--){ const j=Math.floor(Math.random()*(i+1)); [a[i],a[j]]=[a[j],a[i]] } return a }

    // ---- Events ----
    categorySelect.addEventListener('change', e=>{
      const cat = e.target.value;
      if(cat) selectCategory(cat);
    });

    prevBtn.addEventListener('click', ()=>{ prevCard(); });
    nextBtn.addEventListener('click', ()=>{ nextCard(); });
    flipBtn.addEventListener('click', flipCard);
    card.addEventListener('click', flipCard);
    card.addEventListener('keydown', (e)=>{ if(e.code==='Space'){ e.preventDefault(); flipCard(); } });

    knowBtn.addEventListener('click', ()=>{ markKnownAndAdvance(); });

    shuffleBtn.addEventListener('click', ()=>{ if(!currentCategory){ alert('Önce kategori seçin.'); return;} shuffleCurrent(); });
    resetProgressBtn.addEventListener('click', ()=>{
      if(!currentCategory){ alert('Önce kategori seçin.'); return;}
      const ok = confirm('Bu kategorinin ilerlemesi sıfırlansın mı? (bilinenler korunur)');
      if(!ok) return;
      if(persisted[currentCategory]){
        persisted[currentCategory].index = 0;
        // restore order to original sequence
        persisted[currentCategory].order = wordSets[currentCategory].map((_,i)=>i);
        saveState();
        loadCategory(currentCategory);
        updateUI();
      }
    });

    rateRange.addEventListener('input', ()=>{ rateVal.textContent = rateRange.value });

    speakBtn.addEventListener('click', ()=>{ if(!currentWords.length){ alert('Önce kategori seçin!'); return;} speakCurrent(); });

    autoplayToggle.addEventListener('click', ()=>{
      autoplay = !autoplay;
      autoplayToggle.textContent = autoplay ? '▶ Otomatik Oynatma: Açık' : '▶ Otomatik Oynatma: Kapalı';
    });

    exportBtn.addEventListener('click', ()=>{
      const data = {wordSets, persisted};
      const blob = new Blob([JSON.stringify(data, null, 2)], {type:'application/json'});
      const url = URL.createObjectURL(blob);
      const a = document.createElement('a');
      a.href = url; a.download = 'flashcards-export.json'; a.click();
      URL.revokeObjectURL(url);
    });

    importBtn.addEventListener('click', ()=> importFile.click());
    importFile.addEventListener('change', (e)=>{
      const f = e.target.files[0];
      if(!f) return;
      const reader = new FileReader();
      reader.onload = function(){ try{
        const parsed = JSON.parse(reader.result);
        if(parsed.wordSets) {
          // merge (simple)
          for(const k in parsed.wordSets){
            if(!wordSets[k]) wordSets[k] = parsed.wordSets[k];
            else {
              // append those not present by english+turkish key
              const existSet = new Set(wordSets[k].map(x=>x.english+'||'+x.turkish));
              parsed.wordSets[k].forEach(item => {
                const key = item.english + '||' + item.turkish;
                if(!existSet.has(key)) wordSets[k].push(item);
              });
            }
          }
        }
        if(parsed.persisted) {
          // merge persisted
          persisted = Object.assign({}, persisted, parsed.persisted);
          saveState();
        }
        // refresh UI
        categoryList.innerHTML = '';
        populateCategories();
        alert('İçeri aktarma tamamlandı.');
      }catch(err){ alert('Dosya okunamadı veya geçersiz JSON.'); } };
      reader.readAsText(f);
    });

    addCardBtn.addEventListener('click', ()=>{
      const en = newEnglish.value.trim();
      const tr = newTurkish.value.trim();
      if(!en || !tr){ alert('Hem İngilizce hem Türkçe alanını doldurun.'); return; }
      if(!currentCategory){ alert('Önce kategori seçin. Yeni kart seçili kategoriye eklenecek.'); return; }
      wordSets[currentCategory].push({english:en,turkish:tr});
      // update persisted order to include new index
      const idx = wordSets[currentCategory].length - 1;
      persisted[currentCategory] = persisted[currentCategory] || {order:[],index:0,known:[]};
      persisted[currentCategory].order.push(idx);
      saveState();
      // reload
      loadCategory(currentCategory);
      updateUI();
      newEnglish.value=''; newTurkish.value='';
      alert('Kart eklendi.');
    });

    removeKnownBtn.addEventListener('click', ()=>{
      removeKnowns();
    });

    // test mode (toggle)
    testModeBtn.addEventListener('click', ()=>{
      testMode = !testMode;
      testModeBtn.textContent = testMode ? '🔤 Normal Moda Dön' : '📝 Test Modu';
      if(testMode){
        startQuiz();
      }else{
        quizArea.classList.remove('show');
      }
      updateUI();
    });

    quizNext.addEventListener('click', ()=> nextQuizQuestion());

    // keyboard shortcuts
    document.addEventListener('keydown',(e)=>{
      if(e.target.tagName === 'INPUT' || e.target.tagName === 'TEXTAREA') return;
      if(e.code==='ArrowRight') nextCard();
      if(e.code==='ArrowLeft') prevCard();
      if(e.code==='Space') { e.preventDefault(); flipCard(); }
      if(e.code==='KeyS') speakBtn.click();
      if(e.code==='KeyK') markKnownAndAdvance();
      if(e.code==='KeyT') testModeBtn.click();
    });

    // swipe gestures for mobile
    (function addSwipe(){
      let startX=0,startY=0;
      card.addEventListener('touchstart', e=>{
        const t=e.touches[0]; startX=t.clientX; startY=t.clientY;
      }, {passive:true});
      card.addEventListener('touchend', e=>{
        const t = e.changedTouches[0];
        const dx = t.clientX - startX; const dy = t.clientY - startY;
        if(Math.abs(dx)>60 && Math.abs(dx)>Math.abs(dy)){
          if(dx<0) nextCard(); else prevCard();
        }
      }, {passive:true});
    })();

    // init
    function init(){
      populateCategories();
      ensureVoices();
      // auto-select first category if any
      const first = Object.keys(wordSets)[0];
      if(first){
        categorySelect.value = first;
        selectCategory(first);
      }
      rateVal.textContent = rateRange.value;
    }

    // initial run
    init();

    // Safety: save on unload
    window.addEventListener('beforeunload', ()=> saveState());
  </script>
</body>
</html>
