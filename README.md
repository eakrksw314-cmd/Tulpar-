<!DOCTYPE html>
<html lang="tr">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1, viewport-fit=cover">
<title>Tulpar Akıllı Bileklik</title>
<meta name="theme-color" content="#0e3b43">
<meta name="apple-mobile-web-app-capable" content="yes">
<meta name="mobile-web-app-capable" content="yes">
<meta name="apple-mobile-web-app-title" content="Tulpar">
<meta name="apple-mobile-web-app-status-bar-style" content="black-translucent">
<script>
/* PWA: ikon ve manifest kodla üretilir */
(function () {
  function icon(s) {
    var c = document.createElement('canvas'); c.width = c.height = s; var x = c.getContext('2d');
    x.fillStyle = '#0e3b43'; x.fillRect(0, 0, s, s);
    x.strokeStyle = '#f2a65a'; x.lineWidth = s * 0.045; x.lineJoin = x.lineCap = 'round';
    x.beginPath(); var m = [[.14,.55],[.34,.55],[.42,.3],[.54,.78],[.63,.5],[.7,.55],[.86,.55]];
    m.forEach(function (p, i) { i ? x.lineTo(p[0]*s, p[1]*s) : x.moveTo(p[0]*s, p[1]*s); }); x.stroke();
    return c.toDataURL('image/png');
  }
  var a = icon(192), b = icon(512), base = location.href.split('#')[0].split('?')[0];
  var man = { name: 'Tulpar Akıllı Bileklik', short_name: 'Tulpar', start_url: base,
    scope: base.replace(/[^\/]*$/, ''), display: 'standalone', orientation: 'portrait',
    background_color: '#eef3f1', theme_color: '#0e3b43', lang: 'tr',
    icons: [{ src: a, sizes: '192x192', type: 'image/png', purpose: 'any' },
            { src: b, sizes: '512x512', type: 'image/png', purpose: 'any' },
            { src: b, sizes: '512x512', type: 'image/png', purpose: 'maskable' }] };
  var l = document.createElement('link'); l.rel = 'manifest';
  l.href = URL.createObjectURL(new Blob([JSON.stringify(man)], { type: 'application/manifest+json' }));
  document.head.appendChild(l);
  var t = document.createElement('link'); t.rel = 'apple-touch-icon'; t.href = a; document.head.appendChild(t);
})();
</script>
<style>
:root{--ink:#0e3b43;--ink2:#4b6b70;--bg:#eef3f1;--card:#fff;--line:#d5e0dd;--hr:#d9482b;--ox:#1b6fa8;--tp:#c98512;--ok:#2c8a5b;--warn:#c98512;--bad:#c4311f;--acc:#f2a65a}
*{box-sizing:border-box;margin:0}
body{font:15px/1.45 "Avenir Next","Segoe UI",system-ui,sans-serif;background:var(--bg);color:var(--ink);padding-bottom:env(safe-area-inset-bottom)}
button,input,select,textarea{font:inherit;color:inherit}
button{cursor:pointer;border:1px solid var(--line);background:var(--card);border-radius:10px;padding:9px 14px;font-weight:600}
button:active{transform:scale(.97)}
:focus-visible{outline:3px solid var(--acc);outline-offset:2px}
header{background:var(--ink);color:#fff;padding:calc(10px + env(safe-area-inset-top)) 16px 10px;display:flex;align-items:center;justify-content:space-between;gap:10px;position:sticky;top:0;z-index:20}
header b{font-size:18px;letter-spacing:.5px}
header small{display:block;opacity:.7;font-size:12px}
header button{background:transparent;color:#fff;border-color:#ffffff44;padding:6px 10px;font-size:13px}
main{max-width:760px;margin:0 auto;padding:14px;display:grid;gap:14px}
.card{background:var(--card);border:1px solid var(--line);border-radius:14px;padding:16px}
h2{font-size:16px;margin-bottom:4px}
.sub{color:var(--ink2);font-size:13px}
.chips{display:flex;gap:8px;overflow-x:auto;padding-bottom:2px}
.chip{flex:0 0 auto;text-align:left;border-radius:12px;padding:10px 12px;min-width:150px}
.chip.on{background:var(--ink);color:#fff;border-color:var(--ink)}
.chip small{display:block;font-weight:400;opacity:.75}
.tag{display:inline-block;font-size:12px;font-weight:700;padding:2px 9px;border-radius:99px;border:1px solid}
.s-Stabil{color:var(--ok)}.s-Gözlem{color:var(--warn)}.s-Kritik{color:var(--bad)}
.trace{background:var(--ink);border-radius:14px;padding:14px 14px 10px;color:#fff;position:relative}
canvas{width:100%;height:120px;display:block}
.nums{display:grid;grid-template-columns:repeat(3,1fr);gap:8px;margin-top:8px}
.nums div{border-top:2px solid;padding-top:6px}
.nums span{display:block;font-size:12px;opacity:.8}
.nums b{font-size:30px;line-height:1.1;font-variant-numeric:tabular-nums}
.nums em{font-style:normal;font-size:12px;opacity:.85}
.n1{border-color:var(--hr)!important}.n2{border-color:#6cb6e8!important}.n3{border-color:var(--acc)!important}
.live{position:absolute;right:14px;top:12px;font-size:12px;display:flex;align-items:center;gap:6px;opacity:.85}
.live i{width:8px;height:8px;border-radius:50%;background:#5be09a;animation:b 1.4s infinite}
@keyframes b{50%{opacity:.25}}
@media (prefers-reduced-motion:reduce){.live i{animation:none}}
.row{display:flex;gap:8px;flex-wrap:wrap;align-items:center;justify-content:space-between}
.docs{display:grid;gap:8px;margin-top:10px}
.doc{display:flex;justify-content:space-between;align-items:center;border-radius:10px;padding:10px 12px;text-align:left}
.doc.on{border-color:var(--ox);background:#e7f1f9;color:#12527d}
.btn-p{background:var(--ink);color:#fff;border-color:var(--ink)}
.btn-ok{background:#e4f4ec;color:var(--ok);border-color:#b9dfca}
.btn-no{background:#fbe7e3;color:var(--bad);border-color:#efc2ba}
textarea,input,select{width:100%;border:1px solid var(--line);border-radius:10px;padding:10px;background:#fbfdfc}
textarea{resize:vertical;min-height:84px;margin:10px 0}
.quick{display:flex;gap:6px;flex-wrap:wrap;margin-top:8px}
.quick button{font-size:12px;font-weight:500;padding:5px 10px;border-radius:99px}
.rec{border-left:4px solid var(--ox);padding:10px 12px;background:#f6faf9;border-radius:0 10px 10px 0;margin-top:10px}
.rec small{color:var(--ink2)}
.rec p{margin:4px 0}
.rec .v{font-size:12px;font-weight:600}
.lock{text-align:center;color:var(--ink2);padding:18px 6px}
#login{position:fixed;inset:0;background:var(--ink);z-index:50;display:grid;place-items:center;padding:20px}
#login .card{width:100%;max-width:360px;display:grid;gap:10px}
#toast{position:fixed;left:50%;bottom:calc(20px + env(safe-area-inset-bottom));transform:translateX(-50%);background:var(--ink);color:#fff;padding:11px 16px;border-radius:12px;font-size:14px;z-index:99;max-width:90vw;text-align:center;display:none}
.hide{display:none!important}
.mic.rec-on{background:#fbe7e3;color:var(--bad);border-color:var(--bad)}
</style>

<!-- Firebase SDK (Modüler Sürüm) -->
<script type="module">
  import { initializeApp } from "https://www.gstatic.com/firebasejs/10.8.0/firebase-app.js";
  import { getFirestore, collection, addDoc, onSnapshot, query, orderBy, serverTimestamp, deleteDoc, doc } from "https://www.gstatic.com/firebasejs/10.8.0/firebase-firestore.js";

  const firebaseConfig = {
    apiKey: "AIzaSyC6MVQi6I03lYQ6_P72jWtOAEPvxKbDW_0",
    authDomain: "tulpar-70d30.firebaseapp.com",
    projectId: "tulpar-70d30",
    storageBucket: "tulpar-70d30.firebasestorage.app",
    messagingSenderId: "793549326312",
    appId: "1:793549326312:web:a2e7795fef3590b883c65d",
    measurementId: "G-FMP57GY7W6"
  };

  const app = initializeApp(firebaseConfig);
  const db = getFirestore(app);

  // Global alana taşıyoruz ki arayüz fonksiyonları rahatça erişebilsin
  window.db = db;
  window.firebaseModules = { collection, addDoc, onSnapshot, query, orderBy, serverTimestamp, deleteDoc, doc };
  window.dispatchEvent(new Event('firebase-ready'));
</script>
</head>
<body>

<div id="login">
  <div class="card">
    <h2 style="font-size:22px">Tulpar</h2>
    <p class="sub">Yetkili sağlık personeli girişi</p>
    <select id="lu" aria-label="Kullanıcı"></select>
    <input id="lp" type="password" inputmode="numeric" maxlength="4" placeholder="4 haneli PIN" aria-label="PIN">
    <button class="btn-p" onclick="login()">Giriş yap</button>
    <p class="sub">Demo PIN: Dr. Selin Kaya 1234, Dr. Murat Aksoy 5678, Hemşire Canan 0000</p>
  </div>
</div>

<header>
  <div><b>Tulpar</b><small id="who"></small></div>
  <div style="display:flex;gap:8px">
    <button id="install" class="hide" onclick="installApp()">Uygulamayı yükle</button>
    <button onclick="scan()" id="scanbtn">Bileklik okut</button>
    <button onclick="logout()">Çıkış</button>
  </div>
</header>

<main>
  <section class="card">
    <h2>Hastalar</h2>
    <div class="chips" id="plist" style="margin-top:8px"></div>
  </section>

  <section class="card">
    <div class="row">
      <div><h2 id="pname" style="font-size:20px"></h2><p class="sub" id="pmeta"></p></div>
      <span class="tag" id="pstat"></span>
    </div>
  </section>

  <section class="trace" aria-label="Canlı vital bulgular">
    <div class="live"><i></i><span>Bileklik bağlı (Bulut Senkronize)</span></div>
    <canvas id="cv" width="700" height="120"></canvas>
    <div class="nums">
      <div class="n1"><span>Nabız</span><b id="vb">--</b><em id="nb"></em></div>
      <div class="n2"><span>SpO2</span><b id="vo">--</b><em id="no"></em></div>
      <div class="n3"><span>Sıcaklık</span><b id="vt">--</b><em id="nt"></em></div>
    </div>
  </section>

  <section class="card">
    <div class="row">
      <div><h2>Hasta onayı ve doktor yetkisi</h2>
      <p class="sub">Onay olmadan veriler gizli kalır. Kayıt ekleme ve silme yalnızca hastanın yetkilendirdiği doktorlara açıktır. Değişiklik için hasta PIN'i gerekir (bileklik ID'sinin son 4 hanesi).</p></div>
      <button id="cbtn" onclick="toggleConsent()"></button>
    </div>
    <div class="docs" id="docs"></div>
  </section>

  <section class="card">
    <h2>Sesli rapor ve Tıbbi Not</h2>
    <p class="sub">Konuşun veya yazın, veritabanına anlık kaydedin.</p>
    <div class="quick">
      <button onclick="quick('Hasta rutin kontrolden geçti, genel durum iyi.')">Rutin kontrol</button>
      <button onclick="quick('Hastaya 500 ml serum fizyolojik takıldı.')">Serum</button>
      <button onclick="quick('Hafif ağrı şikayeti var, 500 mg parasetamol verildi.')">Ağrı kesici</button>
    </div>
    <textarea id="note" placeholder="Tıbbi notu söyleyin veya yazın" aria-label="Tıbbi not"></textarea>
    <input id="treat" placeholder="Uygulanan tedavi veya ilaç (isteğe bağlı)" aria-label="Tedavi" style="margin-bottom:10px">
    <div class="row">
      <button id="mic" class="mic" onclick="toggleMic()">Mikrofonu başlat</button>
      <button class="btn-p" onclick="addRecord()">Kayıtlara ekle</button>
    </div>
  </section>

  <section class="card">
    <div class="row"><h2>Bulut Kayıt Geçmişi</h2><span class="sub" style="font-size:12px">Firestore Aktif</span></div>
    <div id="logs"></div>
  </section>
</main>
<div id="toast" role="status"></div>

<script>
/* ---------- Veri ve Firestore Dinleyicileri ---------- */
var USERS=[{id:'d1',name:'Dr. Selin Kaya',role:'doctor',pin:'1234'},{id:'d2',name:'Dr. Murat Aksoy',role:'doctor',pin:'5678'},{id:'n1',name:'Hemşire Canan',role:'nurse',pin:'0000'}];
var DOCS=USERS.filter(function(u){return u.role==='doctor'});
var PAT=[{id:1,name:'Ahmet Yılmaz',age:68,room:'302-B',tag:'TLP-8842',st:'Stabil',bpm:78,spo2:97,temp:36.6},
{id:2,name:'Fatma Şahin',age:74,room:'104-A',tag:'TLP-5519',st:'Gözlem',bpm:92,spo2:94,temp:37.2},
{id:3,name:'Mehmet Demir',age:59,room:'210-C',tag:'TLP-3301',st:'Kritik',bpm:112,spo2:91,temp:38.4}];
var DAUTH={1:{c:true,d:['d1']},2:{c:false,d:[]},3:{c:true,d:['d1','d2']}};

function ld(k,f){try{return JSON.parse(localStorage.getItem(k))||f}catch(e){return f}}
function sv(k,v){try{localStorage.setItem(k,JSON.stringify(v))}catch(e){}}

var AUTH=ld('tulpar_auth',DAUTH), me=null, pid=1, live={bpm:78,spo2:97,temp:36.6}, lastAlert={};
var LOGS={}; // Firestore'dan anlık dolacak
var unsubscribeLogs = null;

var $=function(i){return document.getElementById(i)};
function esc(s){return String(s).replace(/[&<>"']/g,function(c){return{'&':'&amp;','<':'&lt;','>':'&gt;','"':'&quot;',"'":'&#39;'}[c]})}
function cur(){return PAT.filter(function(p){return p.id===pid})[0]}
function toast(m){var t=$('toast');t.textContent=m;t.style.display='block';clearTimeout(t._h);t._h=setTimeout(function(){t.style.display='none'},3200)}

/* ---------- Yetki ---------- */
function canView(){return !!(me&&AUTH[pid].c)}
function canWrite(){return canView()&&(me.role==='nurse'||AUTH[pid].d.indexOf(me.id)>-1)}
function canDel(){return canView()&&me.role==='doctor'&&AUTH[pid].d.indexOf(me.id)>-1}
function patientPin(){var p=cur(),v=prompt(p.name+' için hasta PIN\'i (bileklik ID son 4 hane):');
  if(v===null)return false;if(v.trim()!==p.tag.slice(-4)){toast('Hasta PIN\'i yanlış. İşlem iptal edildi.');return false}return true}
function toggleConsent(){if(!patientPin())return;var a=AUTH[pid];a.c=!a.c;if(!a.c)a.d=[];sv('tulpar_auth',AUTH);
  toast(a.c?'Hasta onayı verildi.':'Onay geri çekildi, tüm doktor yetkileri kaldırıldı.');render()}
function toggleDoc(id){var a=AUTH[pid];if(!a.c){toast('Önce hasta onayı verilmeli.');return}if(!patientPin())return;
  var i=a.d.indexOf(id);i>-1?a.d.splice(i,1):a.d.push(id);sv('tulpar_auth',AUTH);render()}

/* ---------- Giriş ---------- */
$('lu').innerHTML=USERS.map(function(u){return '<option value="'+u.id+'">'+esc(u.name)+'</option>'}).join('');
function login(){var u=USERS.filter(function(x){return x.id===$('lu').value})[0];
  if(u&&$('lp').value===u.pin){me=u;$('lp').value='';try{sessionStorage.setItem('tu',u.id)}catch(e){}enter()}else toast('PIN hatalı.')}
function enter(){$('login').classList.add('hide');$('who').textContent=me.name+(me.role==='doctor'?' · Doktor':' · Hemşire');render()}
function logout(){me=null;try{sessionStorage.removeItem('tu')}catch(e){}$('login').classList.remove('hide')}
$('lp').addEventListener('keydown',function(e){if(e.key==='Enter')login()});

/* ---------- Firestore Canlı Kayıt Dinleme ---------- */
function initFirestoreSync() {
  if (!window.db) return;
  var { collection, onSnapshot, query, orderBy } = window.firebaseModules;
  
  // Her hasta değiştiğinde veya ilk açılışta o hastanın kayıtlarını buluttan dinle
  if (unsubscribeLogs) unsubscribeLogs();
  
  var q = query(collection(window.db, "patients", String(pid), "reports"), orderBy("createdAt", "desc"));
  unsubscribeLogs = onSnapshot(q, function(snapshot) {
    var items = [];
    snapshot.forEach(function(docSnap) {
      var data = docSnap.data();
      items.push({
        id: docSnap.id,
        t: data.t || 'Tarih yok',
        b: data.b || 0,
        o: data.o || 0,
        x: data.x || 0,
        n: data.n || '',
        r: data.r || '',
        by: data.by || 'Bilinmiyor'
      });
    });
    LOGS[pid] = items;
    logs();
  }, function(error) {
    console.error("Firestore okuma hatası:", error);
  });
}

/* ---------- Arayüz ---------- */
function render(){
  $('plist').innerHTML=PAT.map(function(p){return '<button class="chip'+(p.id===pid?' on':'')+'" onclick="pick('+p.id+')">'+esc(p.name)+(AUTH[p.id].c?'':' 🔒')+'<small>Oda '+p.room+' · '+p.tag+'</small></button>'}).join('');
  var p=cur();$('pname').textContent=p.name;$('pmeta').textContent='Yaş '+p.age+' · Oda '+p.room+' · '+p.tag;
  var s=$('pstat');s.textContent=p.st==='Gözlem'?'Gözlem altında':p.st;s.className='tag s-'+p.st;
  var a=AUTH[pid],b=$('cbtn');b.className=a.c?'btn-ok':'btn-no';b.textContent=a.c?'Onay var · geri çek':'Onay yok · onay ver';
  $('docs').innerHTML=DOCS.map(function(d){var on=a.d.indexOf(d.id)>-1;
    return '<button class="doc'+(on?' on':'')+'" style="'+(a.c?'':'opacity:.45')+'" onclick="toggleDoc(\''+d.id+'\')"><span>'+esc(d.name)+'</span><span>'+(on?'Yetkili':'Yetkisiz')+'</span></button>'}).join('');
  showVitals();
  initFirestoreSync();
}
function pick(id){pid=id;var p=cur();live={bpm:p.bpm,spo2:p.spo2,temp:p.temp};render()}
function showVitals(){var h=!canView(),l=live;
  $('vb').textContent=h?'--':Math.round(l.bpm);$('vo').textContent=h?'--':'%'+Math.round(l.spo2);$('vt').textContent=h?'--':l.temp.toFixed(1)+'°';
  $('nb').textContent=h?'Onay gerekli':l.bpm>100?'Yüksek':l.bpm<60?'Düşük':'Normal 60-100';
  $('no').textContent=h?'Onay gerekli':l.spo2<92?'Kritik düşük':l.spo2<95?'Düşük':'İdeal %95+';
  $('nt').textContent=h?'Onay gerekli':l.temp>=38?'Ateş':l.temp>=37.5?'Hafif yüksek':'Normal'}
function scan(){var b=$('scanbtn');b.textContent='Okunuyor...';setTimeout(function(){pick(pid%PAT.length+1);b.textContent='Bileklik okut';toast('Bileklik okundu: '+cur().name)},700)}

/* ---------- Canlı simülasyon ve EKG ---------- */
var buf=[],phase=0,cv=$('cv'),cx=cv.getContext('2d'),N=350;
function g(p,c,w,a){return a*Math.exp(-Math.pow(p-c,2)/(2*w*w))}
function ecg(p){return g(p,.18,.025,.12)+g(p,.3,.008,-.12)+g(p,.33,.01,1)+g(p,.36,.01,-.25)+g(p,.58,.05,.25)}
setInterval(function(){var y=0;if(canView()){phase+=.03*live.bpm/60;if(phase>=1)phase-=1;y=ecg(phase)+(Math.random()-.5)*.02}
  buf.push(y);if(buf.length>N)buf.shift();draw()},30);
function draw(){var w=cv.width,h=cv.height;cx.clearRect(0,0,w,h);
  cx.strokeStyle='#ffffff14';cx.lineWidth=1;cx.beginPath();for(var i=0;i<w;i+=35){cx.moveTo(i,0);cx.lineTo(i,h)}for(var j=0;j<h;j+=30){cx.moveTo(0,j);cx.lineTo(w,j)}cx.stroke();
  cx.strokeStyle='#f2a65a';cx.lineWidth=2.4;cx.lineJoin='round';cx.beginPath();
  buf.forEach(function(v,i){var X=i/N*w,Y=h*.72-v*h*.55;i?cx.lineTo(X,Y):cx.moveTo(X,Y)});cx.stroke()}
setInterval(function(){var p=cur(),r=function(n){return(Math.random()*2-1)*n};
  live.bpm=Math.max(45,Math.min(140,live.bpm+r(2)+(p.bpm-live.bpm)*.1));
  live.spo2=Math.max(85,Math.min(100,live.spo2+r(.8)+(p.spo2-live.spo2)*.2));
  live.temp=Math.max(35,Math.min(41,live.temp+r(.05)+(p.temp-live.temp)*.1));showVitals();
  if(canView()&&(live.spo2<90||live.bpm>125)&&!lastAlert[p.id]){lastAlert[p.id]=1;toast('Uyarı: '+p.name+' için kritik değer');
    if(navigator.vibrate)navigator.vibrate([200,100,200]);setTimeout(function(){lastAlert[p.id]=0},30000)}},2000);

/* ---------- Ses ---------- */
var SR=window.SpeechRecognition||window.webkitSpeechRecognition,rec=null,on=false;
if(SR){rec=new SR();rec.lang='tr-TR';rec.interimResults=false;
  rec.onresult=function(e){var t=e.results[0][0].transcript,n=$('note');n.value=n.value?n.value+' '+t:t;micOff()};
  rec.onerror=function(){micOff();toast('Ses tanıma hatası veya mikrofon izni yok.')};rec.onend=micOff}
function toggleMic(){if(!rec){toast('Bu tarayıcı ses tanımayı desteklemiyor. Notu yazabilirsiniz.');return}
  if(on){rec.stop();micOff();return}try{rec.start();on=true;$('mic').classList.add('rec-on');$('mic').textContent='Dinleniyor... durdur'}catch(e){micOff()}}
function micOff(){on=false;$('mic').classList.remove('rec-on');$('mic').textContent='Mikrofonu başlat'}
function quick(t){var n=$('note');n.value=n.value?n.value+' '+t:t}

/* ---------- Kayıtlar (Firestore) ---------- */
async function addRecord(){
  if(!canWrite()){toast(canView()?'Bu hastaya kayıt ekleme yetkiniz yok.':'Hasta onayı olmadan kayıt eklenemez.');return}
  var n=$('note').value.trim();if(!n){toast('Önce bir not söyleyin veya yazın.');return}
  var d=new Date(),z=function(x){return String(x).padStart(2,'0')};
  var tarihStr = d.getFullYear()+'-'+z(d.getMonth()+1)+'-'+z(d.getDate())+' '+z(d.getHours())+':'+z(d.getMinutes());
  
  try {
    var { collection, addDoc, serverTimestamp } = window.firebaseModules;
    await addDoc(collection(window.db, "patients", String(pid), "reports"), {
      t: tarihStr,
      b: Math.round(live.bpm),
      o: Math.round(live.spo2),
      x: +live.temp.toFixed(1),
      n: n,
      r: $('treat').value.trim()||'Rutin takip',
      by: me.name,
      createdAt: serverTimestamp()
    });
    $('note').value='';$('treat').value='';
    toast('Rapor buluta başarıyla kaydedildi.');
  } catch(e) {
    console.error(e);
    toast('Kayıt eklenirken hata oluştu.');
  }
}

function logs(){var el=$('logs');
  if(!canView()){el.innerHTML='<p class="lock">🔒 Kayıtları görmek için hastanın onayı gerekir.</p>';return}
  var L=LOGS[pid]||[];if(!L.length){el.innerHTML='<p class="lock">Bu hasta için henüz bulutta kayıt yok.</p>';return}
  var del=canDel();
  el.innerHTML=L.map(function(l){return '<div class="rec"><div class="row"><small>'+esc(l.t)+' · '+esc(l.by)+'</small>'+
    (del?'<button style="padding:2px 8px;font-size:12px" onclick="delLog(\''+l.id+'\')">Sil</button>':'')+'</div>'+
    '<p>'+esc(l.n)+'</p><p class="v"><span style="color:var(--hr)">'+l.b+' atım/dk</span> · <span style="color:var(--ox)">%'+l.o+'</span> · <span style="color:var(--tp)">'+l.x+'°C</span> · '+esc(l.r)+'</p></div>'}).join('')}

async function delLog(id){
  if(!canDel()){toast('Silme yetkiniz yok.');return}
  if(confirm('Bu kayıt buluttan silinsin mi?')){
    try {
      var { doc, deleteDoc } = window.firebaseModules;
      await deleteDoc(doc(window.db, "patients", String(pid), "reports", id));
      toast('Kayıt buluttan silindi.');
    } catch(e) {
      toast('Silme sırasında hata oluştu.');
    }
  }
}

/* ---------- PWA kurulum ve service worker ---------- */
var dp=null;
window.addEventListener('beforeinstallprompt',function(e){e.preventDefault();dp=e;$('install').classList.remove('hide')});
function installApp(){if(dp){dp.prompt();dp=null;$('install').classList.add('hide')}}
window.addEventListener('load',function(){
  if('serviceWorker' in navigator&&location.protocol.indexOf('http')===0)navigator.serviceWorker.register('service-worker.js').catch(function(){});
});

/* ---------- Başlat ---------- */
window.addEventListener('firebase-ready', function() {
  pick(1);
});

try{var su=USERS.filter(function(x){return x.id===sessionStorage.getItem('tu')})[0];if(su){me=su;enter()}}catch(e){}
</script>
</body>
</html>
