<!doctype html>

<html lang="fa" dir="rtl">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>Pooyan — Links</title>
  <meta name="description" content="Official links of Pooyan Shahmohamady" />
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Vazirmatn:wght@400;600;700&family=Inter:wght@400;600;700&display=swap" rel="stylesheet">
  <style>
    :root{--bg:#0f1724;--card:#0b1220;--accent:#06b6d4;--text:#e6eef6}
    *{box-sizing:border-box}
    html,body{margin:0;padding:0}
    body{min-height:100svh;font-family:'Inter',system-ui,-apple-system,'Segoe UI',Roboto,'Helvetica Neue',Arial;background:linear-gradient(180deg,#031024 0%, #071428 100%);color:var(--text)}
    html[dir="rtl"] body{font-family:'Vazirmatn','Inter',system-ui,-apple-system,'Segoe UI',Roboto,'Helvetica Neue',Arial}
    .wrap{max-width:920px;margin:16px auto 40px;border-radius:16px;background:linear-gradient(180deg,rgba(255,255,255,0.02),rgba(255,255,255,0.01));box-shadow:0 6px 30px rgba(2,6,23,0.6)}/* Header */
.header{position:sticky;top:0;z-index:10;backdrop-filter:blur(6px);background:linear-gradient(180deg,rgba(3,16,36,0.9),rgba(7,20,40,0.85));border-top-left-radius:16px;border-top-right-radius:16px;border-bottom:1px solid rgba(255,255,255,0.06)}
.header-inner{display:flex;flex-wrap:wrap;align-items:center;justify-content:space-between;gap:16px;padding:14px 16px}
.brand{display:flex;gap:16px;align-items:center}
.avatar{width:56px;height:56px;border-radius:14px;background:linear-gradient(135deg,var(--accent),#7c3aed);display:flex;align-items:center;justify-content:center;font-weight:700;color:#001}
h1{margin:0;font-size:18px}
.sub{margin:2px 0 0;color:rgba(230,238,246,0.75);font-size:13px}

/* Lang switcher */
.lang{display:flex;align-items:center;gap:8px}
.select{appearance:none;background:rgba(255,255,255,0.06);border:1px solid rgba(255,255,255,0.12);color:var(--text);padding:8px 12px;border-radius:10px;cursor:pointer}

/* Content */
.section{padding:18px 16px}
.links{display:grid;grid-template-columns:repeat(2,1fr);gap:12px}
@media (max-width:600px){.links{grid-template-columns:1fr}}
.btn{display:flex;align-items:center;gap:12px;padding:12px 14px;border-radius:12px;background:rgba(255,255,255,0.02);text-decoration:none;color:var(--text);border:1px solid rgba(255,255,255,0.06);transition:transform .12s ease,background .12s, border-color .12s}
.btn:hover{transform:translateY(-3px);background:linear-gradient(90deg,rgba(255,255,255,0.03),rgba(255,255,255,0.05));border-color:rgba(255,255,255,0.16)}
.icon{width:28px;height:28px;display:inline-flex;align-items:center;justify-content:center}
.small{font-size:13px;color:rgba(230,238,246,0.8)}

.footer{margin-top:8px;padding:12px 16px;color:rgba(230,238,246,0.7);font-size:12px;border-top:1px solid rgba(255,255,255,0.06);border-bottom-left-radius:16px;border-bottom-right-radius:16px}

  </style>
</head>
<body>
  <main class="wrap">
    <div class="header">
      <div class="header-inner">
        <div class="brand">
          <div class="avatar">P</div>
          <div>
            <h1 id="title">Pooyan Shahmohamady</h1>
            <p class="sub" id="subtitle">Official links</p>
          </div>
        </div>
        <div class="lang">
          <label class="small" id="langLabel" for="langSel">زبان:</label>
          <select id="langSel" class="select" aria-label="Language">
            <option value="fa">فارسی</option>
            <option value="en">English</option>
            <option value="ru">Русский</option>
          </select>
        </div>
      </div>
    </div><div class="section">
  <div class="links" id="links"></div>
</div>

<div class="footer">
  <span id="copyright">© Pooyan Shahmohamady</span>
</div>

  </main>  <script>
    const $ = (s)=>document.querySelector(s);
    const links = [
      { id:'instagram', href:'https://instagram.com/pooyanshahmohamady', icon:'🎯', small:{fa:'@pooyanshahmohamady', en:'@pooyanshahmohamady', ru:'@pooyanshahmohamady'} },
      { id:'tg_ir', href:'https://t.me/pooyanshahmohamady', icon:'✈️', small:{fa:'@pooyanshahmohamady', en:'@pooyanshahmohamady', ru:'@pooyanshahmohamady'} },
      { id:'tg_us', href:'https://t.me/pooyanshahmohamadyus', icon:'✈️', small:{fa:'@pooyanshahmohamadyus', en:'@pooyanshahmohamadyus', ru:'@pooyanshahmohamadyus'} },
      { id:'wa_ir', href:'https://whatsapp.com/+989109514970', icon:'📱', small:{fa:'+98 910 951 4970', en:'+98 910 951 4970', ru:'+98 910 951 4970'} },
      { id:'wa_us', href:'https://whatsapp.com/+18452750508', icon:'📱', small:{fa:'+1 845 275 0508', en:'+1 845 275 0508', ru:'+1 845 275 0508'} },
      { id:'call_ir', href:'tel:+989109514970', icon:'📞', small:{fa:'+98 910 951 4970', en:'+98 910 951 4970', ru:'+98 910 951 4970'} },
      { id:'call_us', href:'tel:+18452750508', icon:'📞', small:{fa:'+1 845 275 0508', en:'+1 845 275 0508', ru:'+1 845 275 0508'} },
      { id:'email', href:'mailto:info@shahmohamady.ir', icon:'✉️', small:{fa:'info@shahmohamady.ir', en:'info@shahmohamady.ir', ru:'info@shahmohamady.ir'} },
      { id:'tiktok', href:'https://tiktok.com/@pooyanshahmohamady', icon:'🎵', small:{fa:'@pooyanshahmohamady', en:'@pooyanshahmohamady', ru:'@pooyanshahmohamady'} },
      { id:'facebook', href:'https://facebook.com/pooyanshahmohamady', icon:'📘', small:{fa:'facebook.com/pooyanshahmohamady', en:'facebook.com/pooyanshahmohamady', ru:'facebook.com/pooyanshahmohamady'} },
      { id:'x', href:'https://twitter.com/pooyanshahmo1', icon:'✖️', small:{fa:'@pooyanshahmo1', en:'@pooyanshahmo1', ru:'@pooyanshahmo1'} },
      { id:'pinterest', href:'https://pinterest.com/pooyanshahmohamady', icon:'📌', small:{fa:'pinterest.com/pooyanshahmohamady', en:'pinterest.com/pooyanshahmohamady', ru:'pinterest.com/pooyanshahmohamady'} },
      { id:'vk', href:'https://vk.com/pooyanshahmohamady', icon:'🌀', small:{fa:'vk.com/pooyanshahmohamady', en:'vk.com/pooyanshahmohamady', ru:'vk.com/pooyanshahmohamady'} },
      { id:'threads', href:'https://www.threads.net/@pooyanshahmohamady', icon:'#️⃣', small:{fa:'@pooyanshahmohamady', en:'@pooyanshahmohamady', ru:'@pooyanshahmohamady'} },
      { id:'youtube', href:'https://youtube.com/pooyanshahmohamady', icon:'▶️', small:{fa:'youtube.com/pooyanshahmohamady', en:'youtube.com/pooyanshahmohamady', ru:'youtube.com/pooyanshahmohamady'} },
      { id:'site', href:'https://www.shahmohamady.ir/', icon:'🌐', small:{fa:'shahmohamady.ir', en:'shahmohamady.ir', ru:'shahmohamady.ir'} },
      { id:'gh1', href:'https://pooyanshahmohamady.github.io/', icon:'📄', small:{fa:'GitHub Pages', en:'GitHub Pages', ru:'GitHub Pages'} },
      { id:'gh2', href:'https://github.com/Pooyanshahmohamady/Pooyanshahmohamady', icon:'💻', small:{fa:'Repository', en:'Repository', ru:'Репозиторий'} }
    ];

    const i18n = {
      fa: {
        dir: 'rtl',
        title: 'پویان شاه محمدی',
        subtitle: 'لینک‌های رسمی',
        langLabel: 'زبان:',
        labels: {
          instagram:'اینستاگرام', tg_ir:'تلگرام (ایران)', tg_us:'تلگرام (آمریکا)', wa_ir:'واتساپ (ایران)', wa_us:'واتساپ (آمریکا)', call_ir:'تماس (ایران)', call_us:'تماس (آمریکا)', email:'ایمیل', tiktok:'تیک‌تاک', facebook:'فیس‌بوک', x:'ایکس (توییتر)', pinterest:'پینترست', vk:'وی‌کی', threads:'تریدز', youtube:'یوتیوب', site:'وب‌سایت', gh1:'گیت‌هاب یک', gh2:'گیت‌هاب دو'
        }
      },
      en: {
        dir: 'ltr',
        title: 'Pooyan Shahmohamady',
        subtitle: 'Official links',
        langLabel: 'Language:',
        labels: {
          instagram:'Instagram', tg_ir:'Telegram (Iran)', tg_us:'Telegram (USA)', wa_ir:'WhatsApp (Iran)', wa_us:'WhatsApp (USA)', call_ir:'Call (Iran)', call_us:'Call (USA)', email:'Email', tiktok:'TikTok', facebook:'Facebook', x:'X (Twitter)', pinterest:'Pinterest', vk:'VK', threads:'Threads', youtube:'YouTube', site:'Website', gh1:'GitHub One', gh2:'GitHub Two'
        }
      },
      ru: {
        dir: 'ltr',
        title: 'Пуян Шахмохамади',
        subtitle: 'Официальные ссылки',
        langLabel: 'Язык:',
        labels: {
          instagram:'Инстаграм', tg_ir:'Телеграм (Иран)', tg_us:'Телеграм (США)', wa_ir:'WhatsApp (Иран)', wa_us:'WhatsApp (США)', call_ir:'Звонок (Иран)', call_us:'Звонок (США)', email:'E-mail', tiktok:'TikTok', facebook:'Facebook', x:'X (Твиттер)', pinterest:'Pinterest', vk:'VK', threads:'Threads', youtube:'YouTube', site:'Сайт', gh1:'GitHub 1', gh2:'GitHub 2'
        }
      }
    };

    function render(lang){
      const t = i18n[lang] || i18n.fa;
      document.documentElement.lang = lang;
      document.documentElement.dir = t.dir;
      document.body.style.fontFamily = (t.dir === 'rtl') ? "Vazirmatn, Inter, system-ui, -apple-system, 'Segoe UI', Roboto, 'Helvetica Neue', Arial" : "Inter, system-ui, -apple-system, 'Segoe UI', Roboto, 'Helvetica Neue', Arial";
      $('#title').textContent = t.title;
      $('#subtitle').textContent = t.subtitle;
      $('#langLabel').textContent = t.langLabel;

      const grid = $('#links');
      grid.innerHTML = '';
      links.forEach(item=>{
        const a = document.createElement('a');
        a.className='btn';
        a.href=item.href; a.target='_blank'; a.rel='noopener';
        a.innerHTML = `<span class=\"icon\">${item.icon}</span>
          <div><div>${t.labels[item.id]||item.id}</div>
          <div class=\"small\">${item.small[lang]||''}</div></div>`;
        grid.appendChild(a);
      });

      localStorage.setItem('lang', lang);
    }

    const sel = $('#langSel');
    sel.addEventListener('change', e=> render(e.target.value));

    const userLang = (navigator.language||'fa').toLowerCase();
    let saved = localStorage.getItem('lang');
    if(!saved){ saved = userLang.startsWith('fa') ? 'fa' : userLang.startsWith('ru') ? 'ru' : 'en'; }
    sel.value = saved;
    render(sel.value);
  </script></body>
</html>
