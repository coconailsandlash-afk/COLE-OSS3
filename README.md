```html
<!-- START REPLACEMENT -->
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width,initial-scale=1,maximum-scale=1,user-scalable=no">
<meta name="apple-mobile-web-app-capable" content="yes">
<meta name="theme-color" content="#0a0a0b">
<title>COLE</title>
<link href="https://fonts.googleapis.com/css2?family=Bebas+Neue&family=DM+Sans:wght@300;400;500;600;700&family=DM+Mono:wght@300;400;500&display=swap" rel="stylesheet">
<style>
*,*::before,*::after{box-sizing:border-box;margin:0;padding:0}
:root{
--bg:#0a0a0b;--card:#111114;--card2:#17171c;--card3:#1e1e26;
--accent:#d4a843;--accent-l:#e8c97a;--accent-dim:rgba(212,168,67,.1);
--text:#f0ead8;--text2:#a89f8e;--muted:#58534a;--muted2:#222018;
--green:#4ecb7f;--green-dim:rgba(78,203,127,.1);
--red:#e05252;--red-dim:rgba(224,82,82,.1);
--blue:#5b9bd5;--blue-dim:rgba(91,155,213,.1);
--purple:#a78bfa;--border:#1c1c22;--border2:#28282f;
}
body.theme-light{--bg:#f5f0ea;--card:#fff;--card2:#f0ebe3;--card3:#e8e0d8;--accent:#b8860b;--accent-l:#daa520;--accent-dim:rgba(184,134,11,.1);--text:#1a1a1a;--text2:#555;--muted:#888;--muted2:#ddd;--green:#2e7d32;--green-dim:rgba(46,125,50,.1);--red:#c62828;--red-dim:rgba(198,40,40,.1);--blue:#1565c0;--blue-dim:rgba(21,101,192,.1);--purple:#6a1b9a;--border:#e0d8d0;--border2:#ccc6be}
body.theme-dark{--bg:#000;--card:#0d0d0d;--card2:#151515;--card3:#1c1c1c;--accent:#e0e0e0;--accent-l:#fff;--accent-dim:rgba(224,224,224,.08);--text:#fff;--text2:#aaa;--muted:#555;--muted2:#1a1a1a;--green:#55ee88;--green-dim:rgba(85,238,136,.1);--red:#ff5555;--red-dim:rgba(255,85,85,.1);--blue:#66aaff;--blue-dim:rgba(102,170,255,.1);--purple:#cc88ff;--border:#222;--border2:#2e2e2e}
body.theme-chatgpt{--bg:#0d0e12;--card:#161b27;--card2:#1e2535;--card3:#252f42;--accent:#7c6aff;--accent-l:#9d8fff;--accent-dim:rgba(124,106,255,.12);--text:#e8e8f0;--text2:#9090a8;--muted:#505068;--muted2:#1a1e2e;--green:#4ade80;--green-dim:rgba(74,222,128,.1);--red:#f87171;--red-dim:rgba(248,113,113,.1);--blue:#60a5fa;--blue-dim:rgba(96,165,250,.1);--purple:#a78bfa;--border:#252d3d;--border2:#2d3650}
html,body,#root{height:100%;overflow:hidden;font-family:'DM Sans',sans-serif;background:var(--bg);color:var(--text);-webkit-font-smoothing:antialiased}
::-webkit-scrollbar{width:2px;height:2px}::-webkit-scrollbar-thumb{background:var(--border2);border-radius:2px}
input,textarea,select{background:var(--card2);border:1.5px solid var(--border2);border-radius:9px;color:var(--text);font-family:'DM Sans',sans-serif;font-size:13px;padding:9px 12px;outline:none;width:100%;transition:border-color .18s;-webkit-appearance:none}
input:focus,textarea:focus,select:focus{border-color:var(--accent)}
::placeholder{color:var(--muted)}
select option{background:var(--card2);color:var(--text)}
button{cursor:pointer;font-family:'DM Sans',sans-serif}
textarea{resize:vertical}
.fd{font-family:'Bebas Neue',sans-serif}
.fm{font-family:'DM Mono',monospace}
.sc{overflow-y:auto;-webkit-overflow-scrolling:touch}
.card{background:var(--card);border:1px solid var(--border);border-radius:14px;padding:14px 16px}
.card-sm{background:var(--card);border:1px solid var(--border);border-radius:11px;padding:10px 12px}
.sl{font-family:'DM Mono',monospace;font-size:9px;font-weight:600;letter-spacing:2px;text-transform:uppercase;color:var(--muted)}
.btn-p{width:100%;background:var(--accent);border:none;border-radius:10px;color:#000;font-weight:700;font-size:13px;padding:12px;letter-spacing:.4px;transition:opacity .18s}
.btn-p:hover{opacity:.88}.btn-p:active{opacity:.72}.btn-p:disabled{opacity:.4;cursor:not-allowed}
.btn-g{background:none;border:1.5px solid var(--border2);border-radius:9px;color:var(--text2);font-size:12px;padding:7px 13px;transition:border-color .18s,color .18s}
.btn-g:hover{border-color:var(--accent);color:var(--accent)}
.chip{padding:5px 12px;border-radius:20px;border:1.5px solid var(--border2);background:var(--card2);color:var(--muted);font-size:10px;white-space:nowrap;cursor:pointer;font-family:'DM Mono',monospace;font-weight:600;text-transform:uppercase;letter-spacing:.5px;transition:all .15s;flex-shrink:0}
.chip.on{background:var(--accent);color:#000;border-color:var(--accent)}
.prog-t{background:var(--border2);height:5px;border-radius:5px;overflow:hidden}
.prog-f{height:100%;border-radius:5px;transition:width .6s cubic-bezier(.4,0,.2,1)}
.modal-ov{position:fixed;inset:0;background:rgba(0,0,0,.8);z-index:900;display:flex;align-items:flex-end;animation:fadeIn .2s ease}
.modal-sh{background:var(--card);border-radius:20px 20px 0 0;padding:20px 18px 44px;width:100%;max-height:92vh;overflow-y:auto;animation:sheetUp .26s cubic-bezier(.4,0,.2,1)}
@keyframes sheetUp{from{transform:translateY(100%)}to{transform:translateY(0)}}
@keyframes fadeIn{from{opacity:0}to{opacity:1}}
@keyframes fadeUp{from{opacity:0;transform:translateY(10px)}to{opacity:1;transform:translateY(0)}}
@keyframes notifIn{from{transform:translateX(110%);opacity:0}to{transform:translateX(0);opacity:1}}
.notif-e{animation:notifIn .28s ease}
.afu{animation:fadeUp .28s ease}
.tog-t{width:40px;height:22px;background:var(--muted2);border-radius:11px;position:relative;cursor:pointer;transition:background .2s;flex-shrink:0}
.tog-t.on{background:var(--accent)}
.tog-th{position:absolute;width:16px;height:16px;background:#fff;border-radius:50%;top:3px;left:3px;transition:left .2s}
.tog-t.on .tog-th{left:21px}
#splash{position:fixed;inset:0;background:#0a0a0b;z-index:9999;display:flex;align-items:center;justify-content:center;transition:opacity .6s ease}
#splash.hide{opacity:0;pointer-events:none}
.splash-c{font-family:'Bebas Neue',sans-serif;font-size:120px;color:#d4a843;letter-spacing:8px;line-height:1;animation:splashPop 1.4s cubic-bezier(.4,0,.2,1) forwards}
@keyframes splashPop{0%{opacity:0;transform:scale(.4)}55%{opacity:1;transform:scale(1.1)}75%{transform:scale(.95)}100%{opacity:1;transform:scale(1)}}
</style>
</head>
<body>
<div id="splash"><div class="splash-c">C</div></div>
<div id="root"></div>
<script src="https://unpkg.com/react@18/umd/react.production.min.js"></script>
<script src="https://unpkg.com/react-dom@18/umd/react-dom.production.min.js"></script>
<script src="https://unpkg.com/@babel/standalone/babel.min.js"></script>
<script src="https://unpkg.com/recharts@2.8.0/umd/Recharts.js"></script>
<script type="text/babel">
setTimeout(()=>{const s=document.getElementById('splash');if(s){s.classList.add('hide');setTimeout(()=>{try{s.remove()}catch{}},700)}},1800);

const {useState,useEffect,useCallback,useMemo,useRef,createContext,useContext}=React;
const RC=typeof Recharts!=='undefined'?Recharts:{};
const {BarChart,Bar,XAxis,YAxis,Tooltip,ResponsiveContainer,PieChart,Pie,Cell,Legend,AreaChart,Area,CartesianGrid}=RC;

const STORE_KEY='cole_os_v4';
const MONTHS_S=['Jan','Feb','Mar','Apr','May','Jun','Jul','Aug','Sep','Oct','Nov','Dec'];
const DAYS=['Monday','Tuesday','Wednesday','Thursday','Friday','Saturday','Sunday'];
const QUOTES=[
  {text:'The grind never lies. Everything you want is on the other side of consistent work.',attr:'— Cole OS'},
  {text:'Discipline today, freedom tomorrow.',attr:'— Daily Reminder'},
  {text:'Done is better than perfect. Start. Refine. Repeat.',attr:'— Cole OS'},
  {text:'Hustle in silence. Let success make the noise.',attr:'— Unknown'},
  {text:"You don't rise to the level of your goals — you fall to the level of your systems.",attr:'— James Clear'},
  {text:'Small consistent steps beat big inconsistent leaps.',attr:'— Cole OS'},
  {text:'It always seems impossible until it is done.',attr:'— Mandela'},
];
const MOVEMENT_TYPES=[
  {value:'none',    label:'No Movement',      color:'#58534a',bg:'rgba(88,83,74,.12)',    icon:'—'},
  {value:'bui',     label:'BUI Collection',   color:'#4ecb7f',bg:'rgba(78,203,127,.12)', icon:'💰'},
  {value:'nail',    label:'Nail Appointment', color:'#d4a843',bg:'rgba(212,168,67,.12)',  icon:'💅'},
  {value:'clothing',label:'Clothing Delivery',color:'#5b9bd5',bg:'rgba(91,155,213,.12)', icon:'👗'},
  {value:'sales',   label:'Sales',            color:'#a78bfa',bg:'rgba(167,139,250,.12)',icon:'🛍'},
  {value:'delivery',label:'Delivery',         color:'#f59e0b',bg:'rgba(245,158,11,.12)', icon:'📦'},
  {value:'debt',    label:'Debt Recovery',    color:'#e05252',bg:'rgba(224,82,82,.12)',   icon:'↩'},
  {value:'other',   label:'Other Movement',   color:'#6b7280',bg:'rgba(107,114,128,.12)',icon:'⚡'},
];
const getMvType=v=>MOVEMENT_TYPES.find(m=>m.value===v)||MOVEMENT_TYPES[0];

const uid=()=>`${Date.now()}-${Math.floor(Math.random()*99999)}`;
const parseAmt=s=>{if(!s&&s!==0)return 0;const n=parseFloat(String(s).replace(/[₦,\s]/g,''));return isNaN(n)?0:n};
const fmt=n=>{if(n===null||n===undefined||isNaN(n))return'₦0';const abs=Math.abs(n),sign=n<0?'-':'';if(abs>=1000000)return`${sign}₦${(abs/1000000).toFixed(2)}M`;if(abs>=1000)return`${sign}₦${abs.toLocaleString()}`;return`${sign}₦${abs}`};
const todayStr=()=>new Date().toISOString().split('T')[0];
const fmtDate=s=>{if(!s)return'';const d=new Date(s);if(isNaN(d))return s;return`${d.getDate()} ${MONTHS_S[d.getMonth()]} ${d.getFullYear()}`};
const fmtDateShort=s=>{if(!s)return'';const d=new Date(s);if(isNaN(d))return s;return`${String(d.getDate()).padStart(2,'0')}/${String(d.getMonth()+1).padStart(2,'0')}/${String(d.getFullYear()).slice(2)}`};
const getDaysUntil=s=>{if(!s)return null;const t=new Date(s);t.setHours(0,0,0,0);const today=new Date();today.setHours(0,0,0,0);return Math.round((t-today)/86400000)};
const getFullDateLabel=()=>{const d=new Date();const days=['Sunday','Monday','Tuesday','Wednesday','Thursday','Friday','Saturday'];const months=['January','February','March','April','May','June','July','August','September','October','November','December'];return`${days[d.getDay()]}, ${d.getDate()} ${months[d.getMonth()]} ${d.getFullYear()}`};
const getGreeting=name=>{const h=new Date().getHours();if(h>=5&&h<12)return`Good morning, ${name} 👑`;if(h>=12&&h<17)return`Good afternoon, ${name} ✨`;return`Good evening, ${name} 🌙`};

function applyTheme(t){
  document.body.classList.remove('theme-light','theme-dark','theme-chatgpt');
  if(t==='light')document.body.classList.add('theme-light');
  else if(t==='dark')document.body.classList.add('theme-dark');
  else if(t==='chatgpt')document.body.classList.add('theme-chatgpt');
}
function applyFontSize(f){
  const sizes={sm:'12px',md:'15px',lg:'18px',xl:'22px'};
  document.documentElement.style.fontSize=sizes[f]||'15px';
}

const calc={
  netMovement:tasks=>tasks.filter(t=>t.done&&t.movementType&&t.movementType!=='none').reduce((s,t)=>s+parseAmt(t.income)-parseAmt(t.expenses),0),
  grossMovement:tasks=>tasks.filter(t=>t.done&&t.movementType&&t.movementType!=='none').reduce((s,t)=>s+parseAmt(t.income),0),
  taskExpenses:tasks=>tasks.filter(t=>t.done&&t.movementType&&t.movementType!=='none').reduce((s,t)=>s+parseAmt(t.expenses),0),
  creditPaid:credits=>credits.filter(c=>c.paid).reduce((s,c)=>s+parseAmt(c.amount),0),
  creditOwed:credits=>credits.filter(c=>!c.paid).reduce((s,c)=>s+parseAmt(c.amount),0),
  txIncome:txs=>txs.filter(t=>t.type==='income').reduce((s,t)=>s+t.amount,0),
  txExpense:txs=>txs.filter(t=>t.type==='expense').reduce((s,t)=>s+t.amount,0),
  currentTotal:(sb,tasks,credits)=>parseAmt(sb)+calc.netMovement(tasks)-calc.creditPaid(credits),
  fullBalance:(sb,tasks,txs,credits)=>parseAmt(sb)+calc.netMovement(tasks)+calc.txIncome(txs)-calc.txExpense(txs)-calc.creditPaid(credits),
  progress:(target,sb,tasks,credits)=>{const t=parseAmt(target);if(!t)return 0;return Math.min(100,Math.round((calc.currentTotal(sb,tasks,credits)/t)*100))},
  remaining:(target,sb,tasks,credits)=>Math.max(0,parseAmt(target)-calc.currentTotal(sb,tasks,credits)),
  breakdown:tasks=>{
    const types=['bui','nail','clothing','sales','delivery','debt','other'];const r={};
    types.forEach(type=>{const done=tasks.filter(t=>t.done&&t.movementType===type);r[type]={gross:done.reduce((s,t)=>s+parseAmt(t.income),0),expenses:done.reduce((s,t)=>s+parseAmt(t.expenses),0),net:done.reduce((s,t)=>s+parseAmt(t.income)-parseAmt(t.expenses),0),count:done.length}});return r},
  monthlyStats:(tasks,txs,months=6)=>{
    const now=new Date();
    return Array.from({length:months},(_,i)=>{
      const d=new Date(now.getFullYear(),now.getMonth()-(months-1-i),1);const m=d.getMonth(),y=d.getFullYear();
      const mt=txs.filter(t=>{const td=new Date(t.date);return td.getMonth()===m&&td.getFullYear()===y});
      const mm=tasks.filter(t=>{if(!t.done||!t.movementType||t.movementType==='none')return false;const td=new Date(t.completedAt||t.createdAt);return td.getMonth()===m&&td.getFullYear()===y});
      const inc=mt.filter(t=>t.type==='income').reduce((s,t)=>s+t.amount,0)+mm.reduce((s,t)=>s+parseAmt(t.income),0);
      const exp=mt.filter(t=>t.type==='expense').reduce((s,t)=>s+t.amount,0)+mm.reduce((s,t)=>s+parseAmt(t.expenses),0);
      return{month:MONTHS_S[m],income:inc,expense:exp,net:inc-exp};
    });
  },
  unifiedHistory:(tasks,txs,credits)=>{
    const ev=[];
    tasks.filter(t=>t.done&&t.movementType&&t.movementType!=='none').forEach(t=>{const inc=parseAmt(t.income),exp=parseAmt(t.expenses);ev.push({id:t.id,type:'movement',subtype:t.movementType,label:t.text,income:inc,expenses:exp,net:inc-exp,date:t.completedAt||t.createdAt,source:'task'})});
    txs.forEach(tx=>{ev.push({id:tx.id,type:tx.type==='income'?'income':'expense',subtype:tx.category||'other',label:tx.desc,income:tx.type==='income'?tx.amount:0,expenses:tx.type==='expense'?tx.amount:0,net:tx.type==='income'?tx.amount:-tx.amount,date:tx.date,source:'tx'})});
    credits.filter(c=>c.paid).forEach(c=>{ev.push({id:c.id,type:'credit-paid',subtype:c.category,label:`Credit paid: ${c.name}`,income:0,expenses:c.amount,net:-c.amount,date:c.paidAt||c.createdAt,source:'credit'})});
    return ev.sort((a,b)=>new Date(b.date)-new Date(a.date));
  },
};

const makeDefaultData=()=>{
  const now=new Date().toISOString();
  const tasks=[
    {id:uid(),text:'Follow up Faith payment — ₦100,000',tag:'client',urgent:true,day:'Monday',time:'09:00',done:false,completedAt:null,createdAt:now,movementType:'bui',income:'100000',expenses:'',businessId:'nail',note:'BUI Collection'},
    {id:uid(),text:'Schedule lash appointment',tag:'personal',urgent:false,day:'Monday',time:'',done:false,completedAt:null,createdAt:now,movementType:'none',income:'',expenses:'',businessId:'nail',note:''},
    {id:uid(),text:'Send rental clips to editor',tag:'content',urgent:false,day:'Monday',time:'',done:false,completedAt:null,createdAt:now,movementType:'none',income:'',expenses:'',businessId:'rental',note:''},
    {id:uid(),text:'AI clothing edits/uploads',tag:'content',urgent:false,day:'Monday',time:'',done:false,completedAt:null,createdAt:now,movementType:'none',income:'',expenses:'',businessId:'clothing',note:''},
    {id:uid(),text:'Record content for Logos',tag:'content',urgent:false,day:'Monday',time:'',done:false,completedAt:null,createdAt:now,movementType:'none',income:'',expenses:'',businessId:'',note:"Topic: what's the craziest spontaneous thing you've done?"},
    {id:uid(),text:'Light engagement — Favour',tag:'personal',urgent:false,day:'Monday',time:'',done:false,completedAt:null,createdAt:now,movementType:'none',income:'',expenses:'',businessId:'',note:''},
    {id:uid(),text:'Mainland pedicure booking follow-up',tag:'client',urgent:false,day:'Tuesday',time:'',done:false,completedAt:null,createdAt:now,movementType:'nail',income:'',expenses:'',businessId:'nail',note:''},
    {id:uid(),text:'Clothing AI edits/uploads',tag:'content',urgent:false,day:'Tuesday',time:'',done:false,completedAt:null,createdAt:now,movementType:'none',income:'',expenses:'',businessId:'clothing',note:''},
    {id:uid(),text:'Rental advert review',tag:'business',urgent:false,day:'Tuesday',time:'',done:false,completedAt:null,createdAt:now,movementType:'none',income:'',expenses:'',businessId:'rental',note:''},
    {id:uid(),text:'Record content for Ariyo',tag:'content',urgent:false,day:'Tuesday',time:'',done:false,completedAt:null,createdAt:now,movementType:'none',income:'',expenses:'',businessId:'',note:'Topic: what type of attention keeps you hooked?'},
    {id:uid(),text:'Light engagement — Jemil',tag:'personal',urgent:false,day:'Tuesday',time:'',done:false,completedAt:null,createdAt:now,movementType:'none',income:'',expenses:'',businessId:'',note:''},
    {id:uid(),text:'Cleaner appointment',tag:'expense',urgent:false,day:'Wednesday',time:'',done:false,completedAt:null,createdAt:now,movementType:'other',income:'',expenses:'25000',businessId:'',note:'₦25,000 — credit entry added'},
    {id:uid(),text:'Prepare island movement',tag:'personal',urgent:false,day:'Wednesday',time:'',done:false,completedAt:null,createdAt:now,movementType:'none',income:'',expenses:'',businessId:'',note:''},
    {id:uid(),text:'Prepare nail sets',tag:'business',urgent:false,day:'Wednesday',time:'',done:false,completedAt:null,createdAt:now,movementType:'none',income:'',expenses:'',businessId:'nail',note:''},
    {id:uid(),text:'Record content for Seyi',tag:'content',urgent:false,day:'Wednesday',time:'',done:false,completedAt:null,createdAt:now,movementType:'none',income:'',expenses:'',businessId:'',note:''},
    {id:uid(),text:'Record content for Doctor',tag:'content',urgent:false,day:'Wednesday',time:'',done:false,completedAt:null,createdAt:now,movementType:'none',income:'',expenses:'',businessId:'',note:''},
    {id:uid(),text:'Move to island',tag:'personal',urgent:false,day:'Thursday',time:'',done:false,completedAt:null,createdAt:now,movementType:'none',income:'',expenses:'',businessId:'',note:''},
    {id:uid(),text:'Island nail appointment',tag:'client',urgent:false,day:'Thursday',time:'',done:false,completedAt:null,createdAt:now,movementType:'nail',income:'',expenses:'',businessId:'nail',note:''},
    {id:uid(),text:'Nail content recording',tag:'content',urgent:false,day:'Thursday',time:'',done:false,completedAt:null,createdAt:now,movementType:'none',income:'',expenses:'',businessId:'nail',note:''},
    {id:uid(),text:'Upload clothing visuals',tag:'content',urgent:false,day:'Thursday',time:'',done:false,completedAt:null,createdAt:now,movementType:'none',income:'',expenses:'',businessId:'clothing',note:''},
    {id:uid(),text:'Meet Logos — ₦50,000',tag:'client',urgent:true,day:'Thursday',time:'',done:false,completedAt:null,createdAt:now,movementType:'bui',income:'50000',expenses:'',businessId:'nail',note:'BUI Collection'},
    {id:uid(),text:'Light engagement — Pizzle',tag:'personal',urgent:false,day:'Thursday',time:'',done:false,completedAt:null,createdAt:now,movementType:'none',income:'',expenses:'',businessId:'',note:'Topic: wild experience discussion'},
    {id:uid(),text:'Faith nails appointment',tag:'personal',urgent:false,day:'Friday',time:'',done:false,completedAt:null,createdAt:now,movementType:'none',income:'',expenses:'',businessId:'nail',note:'NOT a paid gig — accommodation-based island movement'},
    {id:uid(),text:'Client content recording',tag:'content',urgent:false,day:'Friday',time:'',done:false,completedAt:null,createdAt:now,movementType:'none',income:'',expenses:'',businessId:'',note:''},
    {id:uid(),text:'Meet Seyi — ₦100,000',tag:'client',urgent:true,day:'Friday',time:'',done:false,completedAt:null,createdAt:now,movementType:'bui',income:'100000',expenses:'',businessId:'nail',note:'BUI Collection'},
    {id:uid(),text:'Light engagement — Greatness',tag:'personal',urgent:false,day:'Friday',time:'',done:false,completedAt:null,createdAt:now,movementType:'none',income:'',expenses:'',businessId:'',note:'Topic: weekend escape planning'},
    {id:uid(),text:'Return mainland',tag:'personal',urgent:false,day:'Saturday',time:'',done:false,completedAt:null,createdAt:now,movementType:'none',income:'',expenses:'',businessId:'',note:''},
    {id:uid(),text:'Weekly upload check',tag:'business',urgent:false,day:'Saturday',time:'',done:false,completedAt:null,createdAt:now,movementType:'none',income:'',expenses:'',businessId:'',note:''},
    {id:uid(),text:'Record content for Kry',tag:'content',urgent:false,day:'Saturday',time:'',done:false,completedAt:null,createdAt:now,movementType:'none',income:'',expenses:'',businessId:'',note:'Topic: exclusive attention energy'},
    {id:uid(),text:'Light engagement — Ariyo',tag:'personal',urgent:false,day:'Saturday',time:'',done:false,completedAt:null,createdAt:now,movementType:'none',income:'',expenses:'',businessId:'',note:''},
  ];
  const credits=[
    {id:uid(),name:'Dami',    amount:40000,category:'repayment',priority:false,paid:false,paidAt:null,dueDate:'',note:'',createdAt:now},
    {id:uid(),name:'Krys',    amount:20000,category:'repayment',priority:false,paid:false,paidAt:null,dueDate:'',note:'',createdAt:now},
    {id:uid(),name:'Rasak',   amount:30000,category:'repayment',priority:true, paid:false,paidAt:null,dueDate:'',note:'',createdAt:now},
    {id:uid(),name:'Sultan',  amount:5000, category:'repayment',priority:false,paid:false,paidAt:null,dueDate:'',note:'',createdAt:now},
    {id:uid(),name:'Funke',   amount:10000,category:'personal', priority:false,paid:false,paidAt:null,dueDate:'',note:'',createdAt:now},
    {id:uid(),name:'Airbrush',amount:25000,category:'repayment',priority:false,paid:false,paidAt:null,dueDate:'',note:'',createdAt:now},
    {id:uid(),name:'Mom',     amount:12000,category:'personal', priority:true, paid:false,paidAt:null,dueDate:'',note:'',createdAt:now},
    {id:uid(),name:'Cleaner', amount:25000,category:'repayment',priority:false,paid:false,paidAt:null,dueDate:'',note:'Wednesday appointment',createdAt:now},
  ];
  const businesses=[
    {id:'nail',    name:'Coco Nails',    type:'nails',   color:'#d4a843',note:'Nail brand — coconailshq',   createdAt:now},
    {id:'clothing',name:'Clothing Brand',type:'clothing',color:'#5b9bd5',note:'C.Closet — bespoke clothing',createdAt:now},
    {id:'rental',  name:'Rental Space',  type:'services',color:'#4ecb7f',note:'Studio workstation rentals',  createdAt:now},
  ];
  const transactions=[
    {id:uid(),type:'income', desc:'Faith payment',      amount:100000,category:'other',   businessId:'nail',   date:todayStr(),note:'Monday',createdAt:now},
    {id:uid(),type:'expense',desc:'Transport/logistics', amount:0,     category:'other',   businessId:'',       date:todayStr(),note:'Monday — update amount',createdAt:now},
    {id:uid(),type:'income', desc:'Pedicure payment',    amount:0,     category:'services',businessId:'nail',   date:todayStr(),note:'Tuesday — update amount',createdAt:now},
    {id:uid(),type:'expense',desc:'Feeding prep',        amount:0,     category:'other',   businessId:'',       date:todayStr(),note:'Tuesday — update amount',createdAt:now},
    {id:uid(),type:'expense',desc:'Cleaner payment',     amount:25000, category:'salary',  businessId:'',       date:todayStr(),note:'Wednesday',createdAt:now},
    {id:uid(),type:'expense',desc:'Island logistics',    amount:0,     category:'other',   businessId:'',       date:todayStr(),note:'Wednesday — update amount',createdAt:now},
    {id:uid(),type:'income', desc:'Nail appointment',    amount:0,     category:'services',businessId:'nail',   date:todayStr(),note:'Thursday — update amount',createdAt:now},
    {id:uid(),type:'income', desc:'Logos BUI',           amount:50000, category:'other',   businessId:'nail',   date:todayStr(),note:'Thursday',createdAt:now},
    {id:uid(),type:'expense',desc:'Island transport',    amount:0,     category:'other',   businessId:'',       date:todayStr(),note:'Thursday — update amount',createdAt:now},
    {id:uid(),type:'income', desc:'Seyi BUI',            amount:100000,category:'other',   businessId:'nail',   date:todayStr(),note:'Friday',createdAt:now},
    {id:uid(),type:'expense',desc:'Rental advert',       amount:0,     category:'marketing',businessId:'rental',date:todayStr(),note:'Friday — update amount',createdAt:now},
    {id:uid(),type:'expense',desc:'Return transport',    amount:0,     category:'other',   businessId:'',       date:todayStr(),note:'Saturday — update amount',createdAt:now},
  ];
  return{tasks,credits,businesses,transactions};
};

const StoreCtx=createContext(null);
const NotifCtx=createContext(null);
const NavCtx=createContext(null);

function loadState(){try{const r=localStorage.getItem(STORE_KEY);if(r)return JSON.parse(r)}catch{}return null}
function saveState(s){try{localStorage.setItem(STORE_KEY,JSON.stringify(s))}catch{}}

function StoreProvider({children}){
  const saved=loadState();
  const isFirst=!saved;
  const def=isFirst?makeDefaultData():{tasks:[],credits:[],businesses:[],transactions:[]};
  const [tasks,setTasks]=useState(saved?.tasks||def.tasks);
  const [transactions,setTransactions]=useState(saved?.transactions||def.transactions);
  const [credits,setCredits]=useState(saved?.credits||def.credits);
  const [deadlines,setDeadlines]=useState(saved?.deadlines||[]);
  const [businesses,setBusinesses]=useState(saved?.businesses||def.businesses);
  const [target,setTargetState]=useState(saved?.target||{total:0,startingBalance:0,label:''});
  const [settings,setSettings]=useState(saved?.settings||{userName:'Gbemi',notifications:true,fontSize:'md',theme:'default'});
  const [savedAt,setSavedAt]=useState(saved?._savedAt||null);

  useEffect(()=>{
    const s={tasks,transactions,credits,deadlines,businesses,target,settings,_savedAt:new Date().toISOString()};
    saveState(s);setSavedAt(s._savedAt);
  },[tasks,transactions,credits,deadlines,businesses,target,settings]);

  useEffect(()=>{applyFontSize(settings.fontSize||'md')},[settings.fontSize]);
  useEffect(()=>{applyTheme(settings.theme||'default')},[settings.theme]);

  const store={
    tasks,transactions,credits,deadlines,businesses,target,settings,savedAt,
    addTask:d=>setTasks(p=>[...p,{id:uid(),text:d.text||'',tag:d.tag||'personal',urgent:d.urgent||d.tag==='urgent'||false,day:d.day||'',time:d.time||'',note:d.note||'',done:false,completedAt:null,createdAt:new Date().toISOString(),movementType:d.movementType||'none',income:d.income||'',expenses:d.expenses||'',businessId:d.businessId||''}]),
    updateTask:(id,u)=>setTasks(p=>p.map(t=>t.id===id?{...t,...u}:t)),
    toggleTask:id=>{let r=null;setTasks(p=>p.map(t=>{if(t.id!==id)return t;const done=!t.done;r={...t,done};return{...t,done,completedAt:done?new Date().toISOString():null}}));return r},
    deleteTask:id=>setTasks(p=>p.filter(t=>t.id!==id)),
    addTransaction:d=>setTransactions(p=>[...p,{id:uid(),type:d.type,desc:d.desc,amount:parseAmt(d.amount),category:d.category||'other',businessId:d.businessId||'',date:d.date||todayStr(),note:d.note||'',createdAt:new Date().toISOString()}]),
    deleteTransaction:id=>setTransactions(p=>p.filter(t=>t.id!==id)),
    updateTransaction:(id,u)=>setTransactions(p=>p.map(t=>t.id===id?{...t,...u,amount:u.amount!==undefined?parseAmt(String(u.amount)):t.amount}:t)),
    addCredit:d=>{const c={id:uid(),name:d.name||'',amount:parseAmt(String(d.amount||0)),category:d.category||'repayment',priority:d.priority||false,paid:false,paidAt:null,dueDate:d.dueDate||'',note:d.note||'',createdAt:new Date().toISOString()};setCredits(p=>[...p,c]);return c.id},
    updateCredit:(id,u)=>setCredits(p=>p.map(c=>c.id===id?{...c,...u,amount:u.amount!==undefined?parseAmt(String(u.amount)):c.amount}:c)),
    toggleCredit:id=>{let r=null;setCredits(p=>p.map(c=>{if(c.id!==id)return c;const paid=!c.paid;r={...c,paid};return{...c,paid,paidAt:paid?new Date().toISOString():null}}));return r},
    deleteCredit:id=>setCredits(p=>p.filter(c=>c.id!==id)),
    setTarget:(total,sb,label)=>setTargetState({total:parseAmt(String(total)),startingBalance:parseAmt(String(sb)),label:label||''}),
    addDeadline:d=>setDeadlines(p=>[...p,{id:uid(),title:d.title,date:d.date,amount:d.amount?parseAmt(String(d.amount)):0,category:d.category||'general',done:false,urgent:d.urgent||false,note:d.note||'',createdAt:new Date().toISOString()}]),
    toggleDeadline:id=>setDeadlines(p=>p.map(d=>d.id===id?{...d,done:!d.done}:d)),
    deleteDeadline:id=>setDeadlines(p=>p.filter(d=>d.id!==id)),
    addBusiness:d=>setBusinesses(p=>[...p,{id:uid(),name:d.name,type:d.type||'general',color:d.color||'#d4a843',note:d.note||'',createdAt:new Date().toISOString()}]),
    updateBusiness:(id,u)=>setBusinesses(p=>p.map(b=>b.id===id?{...b,...u}:b)),
    deleteBusiness:id=>setBusinesses(p=>p.filter(b=>b.id!==id)),
    updateSettings:u=>setSettings(p=>({...p,...u})),
    resetAll:()=>{
      try{localStorage.removeItem(STORE_KEY);Object.keys(localStorage).filter(k=>k.startsWith('cole')).forEach(k=>localStorage.removeItem(k))}catch{}
      setTasks([]);setTransactions([]);setCredits([]);setDeadlines([]);
      setBusinesses([]);setTargetState({total:0,startingBalance:0,label:''});
      setSettings({userName:'Cole',notifications:true,fontSize:'md',theme:'default'});
    },
    getNetMovement:()=>calc.netMovement(tasks),
    getGrossMovement:()=>calc.grossMovement(tasks),
    getTaskExpenses:()=>calc.taskExpenses(tasks),
    getFullBalance:()=>calc.fullBalance(target.startingBalance,tasks,transactions,credits),
    getCurrentTotal:()=>calc.currentTotal(target.startingBalance,tasks,credits),
    getProgress:()=>calc.progress(target.total,target.startingBalance,tasks,credits),
    getRemaining:()=>calc.remaining(target.total,target.startingBalance,tasks,credits),
    getCreditPaid:()=>calc.creditPaid(credits),
    getCreditOwed:()=>calc.creditOwed(credits),
    getBreakdown:()=>calc.breakdown(tasks),
    getMonthlyStats:(m)=>calc.monthlyStats(tasks,transactions,m||6),
    getUnifiedHistory:()=>calc.unifiedHistory(tasks,transactions,credits),
    getBizStats:id=>{
      const mI=tasks.filter(t=>t.done&&t.businessId===id&&t.movementType!=='none').reduce((s,t)=>s+parseAmt(t.income),0);
      const mE=tasks.filter(t=>t.done&&t.businessId===id&&t.movementType!=='none').reduce((s,t)=>s+parseAmt(t.expenses),0);
      const tI=transactions.filter(t=>t.type==='income'&&t.businessId===id).reduce((s,t)=>s+t.amount,0);
      const tE=transactions.filter(t=>t.type==='expense'&&t.businessId===id).reduce((s,t)=>s+t.amount,0);
      return{income:mI+tI,expense:mE+tE,net:mI+tI-mE-tE,movCount:tasks.filter(t=>t.done&&t.businessId===id&&t.movementType!=='none').length};
    },
  };
  return React.createElement(StoreCtx.Provider,{value:store},children);
}
const useStore=()=>useContext(StoreCtx);

function NotifProvider({children}){
  const [notifs,setNotifs]=useState([]);
  const push=useCallback((msg,type='info',dur=4000)=>{const id=Date.now()+Math.random();setNotifs(n=>[...n,{id,msg,type}]);setTimeout(()=>setNotifs(n=>n.filter(x=>x.id!==id)),dur)},[]);
  const dismiss=useCallback(id=>setNotifs(n=>n.filter(x=>x.id!==id)),[]);
  return React.createElement(NotifCtx.Provider,{value:{notifs,push,dismiss}},children);
}
const useNotif=()=>useContext(NotifCtx);

function NavProvider({children}){
  const [page,setPage]=useState('home');
  const [sidebarOpen,setSidebarOpen]=useState(false);
  const navigate=useCallback(p=>{setPage(p);setSidebarOpen(false)},[]);
  return React.createElement(NavCtx.Provider,{value:{page,navigate,sidebarOpen,setSidebarOpen}},children);
}
const useNav=()=>useContext(NavCtx);

const NC={info:'#d4a843',success:'#4ecb7f',error:'#e05252',warning:'#f59e0b',income:'#4ecb7f',expense:'#e05252',movement:'#d4a843'};
function NotifStack(){
  const {notifs,dismiss}=useNotif();
  if(!notifs.length)return null;
  return React.createElement('div',{style:{position:'fixed',top:0,left:0,right:0,zIndex:9000,pointerEvents:'none',display:'flex',flexDirection:'column'}},
    notifs.map(n=>React.createElement('div',{key:n.id,className:'notif-e',style:{background:'var(--card)',borderBottom:`2px solid ${NC[n.type]||NC.info}`,padding:'10px 14px',display:'flex',alignItems:'center',gap:10,pointerEvents:'all',boxShadow:'0 4px 24px rgba(0,0,0,.45)'}},
      React.createElement('div',{style:{width:6,height:6,borderRadius:'50%',background:NC[n.type]||NC.info,flexShrink:0}}),
      React.createElement('div',{style:{flex:1,fontSize:12,fontWeight:600,color:'var(--text)',lineHeight:1.4}},n.msg),
      React.createElement('button',{onClick:()=>dismiss(n.id),style:{background:'none',border:'none',color:'var(--muted)',pointerEvents:'all',fontSize:16,lineHeight:1}},'×')
    ))
  );
}

function Card({children,style,onClick,className=''}){return React.createElement('div',{className:`card ${onClick?'card-hover':''} ${className}`,style:{cursor:onClick?'pointer':'default',...style},onClick},children)}
function MiniStat({label,value,color,sub}){return React.createElement('div',{style:{background:'var(--card2)',border:'1px solid var(--border)',borderRadius:10,padding:'9px 11px'}},React.createElement('div',{className:'sl',style:{marginBottom:3,color}},label),React.createElement('div',{className:'fm',style:{fontSize:14,fontWeight:700,color:color||'var(--text)'}},value),sub&&React.createElement('div',{className:'fm',style:{fontSize:8,color:'var(--muted)',marginTop:2}},sub))}
function StatCard({label,value,sub,color,onClick}){return React.createElement('div',{className:'card-sm',onClick,style:{background:'var(--card)',border:'1px solid var(--border)',cursor:onClick?'pointer':'default',position:'relative',overflow:'hidden'}},React.createElement('div',{style:{position:'absolute',top:0,left:0,width:2,height:'100%',background:'var(--accent)',opacity:.45}}),React.createElement('div',{className:'sl',style:{marginBottom:5}},label),React.createElement('div',{className:'fm',style:{fontSize:19,fontWeight:700,color:color||'var(--text)',lineHeight:1.1}},value),sub&&React.createElement('div',{className:'fm',style:{fontSize:9,color:'var(--muted)',marginTop:3}},sub))}
function ProgBar({value,max,color}){const p=max>0?Math.min(100,Math.round((value/max)*100)):0;return React.createElement('div',{className:'prog-t'},React.createElement('div',{className:'prog-f',style:{width:`${p}%`,background:color||'var(--accent)'}}))}
function Toggle({on,onChange}){return React.createElement('div',{className:`tog-t ${on?'on':''}`,onClick:onChange},React.createElement('div',{className:'tog-th'}))}
function Field({label,children}){return React.createElement('div',{style:{marginBottom:12}},label&&React.createElement('div',{className:'sl',style:{marginBottom:5}},label),children)}
function R2({children,gap=8}){return React.createElement('div',{style:{display:'flex',gap,alignItems:'flex-start'}},children)}
function EmptyState({icon,title,sub,action,onAction}){return React.createElement('div',{className:'afu',style:{textAlign:'center',padding:'40px 20px'}},icon&&React.createElement('div',{style:{fontSize:30,marginBottom:10}},icon),React.createElement('div',{style:{fontSize:13,fontWeight:600,color:'var(--text2)',marginBottom:6}},title),sub&&React.createElement('div',{style:{fontSize:11,color:'var(--muted)',lineHeight:1.5,marginBottom:16,maxWidth:240,margin:'0 auto 16px'}},sub),action&&onAction&&React.createElement('button',{className:'btn-g',onClick:onAction,style:{fontSize:11}},action))}
function ModalSheet({title,onClose,children}){return React.createElement('div',{className:'modal-ov',onClick:e=>{if(e.target===e.currentTarget)onClose()}},React.createElement('div',{className:'modal-sh'},React.createElement('div',{style:{display:'flex',alignItems:'center',justifyContent:'space-between',marginBottom:18}},React.createElement('div',{className:'fd',style:{fontSize:20,letterSpacing:3,color:'var(--text)'}},title),React.createElement('button',{onClick:onClose,className:'btn-g',style:{fontSize:11,padding:'5px 10px'}},'✕ Close')),children))}

const NAV_SVG={
  home:React.createElement('svg',{width:15,height:15,viewBox:'0 0 24 24',fill:'none',stroke:'currentColor',strokeWidth:2,strokeLinecap:'round',strokeLinejoin:'round'},React.createElement('path',{d:'M3 9l9-7 9 7v11a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2z'}),React.createElement('polyline',{points:'9 22 9 12 15 12 15 22'})),
  tasks:React.createElement('svg',{width:15,height:15,viewBox:'0 0 24 24',fill:'none',stroke:'currentColor',strokeWidth:2,strokeLinecap:'round',strokeLinejoin:'round'},React.createElement('polyline',{points:'9 11 12 14 22 4'}),React.createElement('path',{d:'M21 12v7a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2V5a2 2 0 0 1 2-2h11'})),
  movements:React.createElement('svg',{width:15,height:15,viewBox:'0 0 24 24',fill:'none',stroke:'currentColor',strokeWidth:2,strokeLinecap:'round',strokeLinejoin:'round'},React.createElement('polyline',{points:'22 12 18 12 15 21 9 3 6 12 2 12'})),
  finance:React.createElement('svg',{width:15,height:15,viewBox:'0 0 24 24',fill:'none',stroke:'currentColor',strokeWidth:2,strokeLinecap:'round',strokeLinejoin:'round'},React.createElement('line',{x1:'12',y1:'1',x2:'12',y2:'23'}),React.createElement('path',{d:'M17 5H9.5a3.5 3.5 0 0 0 0 7h5a3.5 3.5 0 0 1 0 7H6'})),
  target:React.createElement('svg',{width:15,height:15,viewBox:'0 0 24 24',fill:'none',stroke:'currentColor',strokeWidth:2,strokeLinecap:'round',strokeLinejoin:'round'},React.createElement('circle',{cx:12,cy:12,r:10}),React.createElement('circle',{cx:12,cy:12,r:6}),React.createElement('circle',{cx:12,cy:12,r:2})),
  analytics:React.createElement('svg',{width:15,height:15,viewBox:'0 0 24 24',fill:'none',stroke:'currentColor',strokeWidth:2,strokeLinecap:'round',strokeLinejoin:'round'},React.createElement('line',{x1:'18',y1:'20',x2:'18',y2:'10'}),React.createElement('line',{x1:'12',y1:'20',x2:'12',y2:'4'}),React.createElement('line',{x1:'6',y1:'20',x2:'6',y2:'14'})),
  businesses:React.createElement('svg',{width:15,height:15,viewBox:'0 0 24 24',fill:'none',stroke:'currentColor',strokeWidth:2,strokeLinecap:'round',strokeLinejoin:'round'},React.createElement('rect',{x:2,y:7,width:20,height:14,rx:2,ry:2}),React.createElement('path',{d:'M16 7V5a2 2 0 0 0-2-2h-4a2 2 0 0 0-2 2v2'})),
  deadlines:React.createElement('svg',{width:15,height:15,viewBox:'0 0 24 24',fill:'none',stroke:'currentColor',strokeWidth:2,strokeLinecap:'round',strokeLinejoin:'round'},React.createElement('rect',{x:3,y:4,width:18,height:18,rx:2,ry:2}),React.createElement('line',{x1:16,y1:2,x2:16,y2:6}),React.createElement('line',{x1:8,y1:2,x2:8,y2:6}),React.createElement('line',{x1:3,y1:10,x2:21,y2:10})),
  settings:React.createElement('svg',{width:15,height:15,viewBox:'0 0 24 24',fill:'none',stroke:'currentColor',strokeWidth:2,strokeLinecap:'round',strokeLinejoin:'round'},React.createElement('circle',{cx:12,cy:12,r:3}),React.createElement('path',{d:'M19.4 15a1.65 1.65 0 0 0 .33 1.82l.06.06a2 2 0 0 1-2.83 2.83l-.06-.06a1.65 1.65 0 0 0-1.82-.33 1.65 1.65 0 0 0-1 1.51V21a2 2 0 0 1-4 0v-.09A1.65 1.65 0 0 0 9 19.4a1.65 1.65 0 0 0-1.82.33l-.06.06a2 2 0 0 1-2.83-2.83l.06-.06A1.65 1.65 0 0 0 4.68 15a1.65 1.65 0 0 0-1.51-1H3a2 2 0 0 1 0-4h.09A1.65 1.65 0 0 0 4.6 9a1.65 1.65 0 0 0-.33-1.82l-.06-.06a2 2 0 0 1 2.83-2.83l.06.06A1.65 1.65 0 0 0 9 4.68a1.65 1.65 0 0 0 1-1.51V3a2 2 0 0 1 4 0v.09a1.65 1.65 0 0 0 1 1.51 1.65 1.65 0 0 0 1.82-.33l.06-.06a2 2 0 0 1 2.83 2.83l-.06.06A1.65 1.65 0 0 0 19.4 9a1.65 1.65 0 0 0 1.51 1H21a2 2 0 0 1 0 4h-.09a1.65 1.65 0 0 0-1.51 1z'}))
};
const NAV_ITEMS=[{id:'home',label:'Home'},{id:'tasks',label:'Tasks'},{id:'movements',label:'Movements'},{id:'finance',label:'Finance'},{id:'target',label:'Target'},{id:'analytics',label:'Analytics'},{id:'businesses',label:'Businesses'},{id:'deadlines',label:'Deadlines'},{id:'settings',label:'Settings'}];

function Sidebar(){
  const {page,navigate,sidebarOpen,setSidebarOpen}=useNav();
  return React.createElement(React.Fragment,null,
    sidebarOpen&&React.createElement('div',{onClick:()=>setSidebarOpen(false),style:{position:'fixed',inset:0,background:'rgba(0,0,0,.72)',zIndex:400}}),
    React.createElement('div',{style:{position:'fixed',top:0,bottom:0,left:0,width:216,background:'var(--card)',borderRight:'1px solid var(--border)',zIndex:500,display:'flex',flexDirection:'column',transform:sidebarOpen?'translateX(0)':'translateX(-100%)',transition:'transform .26s cubic-bezier(.4,0,.2,1)',overflowY:'auto'}},
      React.createElement('div',{style:{padding:'52px 18px 16px',borderBottom:'1px solid var(--border)',display:'flex',justifyContent:'space-between',alignItems:'flex-start'}},
        React.createElement('div',null,React.createElement('div',{className:'fd',style:{fontSize:28,letterSpacing:7,color:'var(--accent)',lineHeight:1}},'COLE'),React.createElement('div',{className:'sl',style:{marginTop:4}},'Operating System')),
        React.createElement('button',{onClick:()=>setSidebarOpen(false),style:{background:'none',border:'none',color:'var(--muted)',fontSize:18,lineHeight:1}},'×')
      ),
      React.createElement('div',{style:{flex:1,paddingTop:6}},
        NAV_ITEMS.map(item=>{
          const active=page===item.id;
          return React.createElement('div',{key:item.id,onClick:()=>navigate(item.id),style:{display:'flex',alignItems:'center',gap:11,padding:'12px 18px',borderBottom:'1px solid var(--border)',cursor:'pointer',background:active?'var(--card2)':'transparent',transition:'background .15s',position:'relative'}},
            active&&React.createElement('div',{style:{position:'absolute',left:0,top:0,bottom:0,width:2,background:'var(--accent)',borderRadius:'0 2px 2px 0'}}),
            React.createElement('div',{style:{width:30,height:30,borderRadius:8,flexShrink:0,background:active?'var(--accent-dim)':'var(--card2)',display:'flex',alignItems:'center',justifyContent:'center',color:active?'var(--accent)':'var(--muted)'}},NAV_SVG[item.id]),
            React.createElement('span',{style:{fontSize:13,fontWeight:active?600:400,color:active?'var(--text)':'var(--text2)'}},item.label)
          );
        })
      ),
      React.createElement('div',{style:{padding:'12px 18px',borderTop:'1px solid var(--border)'}},React.createElement('div',{className:'sl'},'v2.0 · Cole OS'))
    )
  );
}

const PT={home:'COLE OS',tasks:'TASKS',movements:'MOVEMENTS',finance:'FINANCE',target:'TARGET',analytics:'ANALYTICS',businesses:'BUSINESSES',deadlines:'DEADLINES',settings:'SETTINGS'};
function TopBar(){
  const {page,setSidebarOpen}=useNav();
  const {settings,savedAt}=useStore();
  return React.createElement('div',{style:{display:'flex',alignItems:'center',gap:12,padding:'48px 16px 10px',borderBottom:'1px solid var(--border)',background:'var(--bg)',flexShrink:0}},
    React.createElement('button',{onClick:()=>setSidebarOpen(true),style:{width:36,height:36,background:'var(--card)',border:'1px solid var(--border)',borderRadius:10,display:'flex',alignItems:'center',justifyContent:'center',flexShrink:0,color:'var(--text)'}},
      React.createElement('svg',{width:16,height:16,viewBox:'0 0 24 24',fill:'none',stroke:'currentColor',strokeWidth:2,strokeLinecap:'round'},React.createElement('line',{x1:3,y1:6,x2:21,y2:6}),React.createElement('line',{x1:3,y1:12,x2:21,y2:12}),React.createElement('line',{x1:3,y1:18,x2:21,y2:18}))
    ),
    React.createElement('div',{style:{flex:1}},React.createElement('div',{className:'fd',style:{fontSize:17,letterSpacing:4,color:'var(--text)',lineHeight:1}},PT[page]||page.toUpperCase()),settings.userName&&React.createElement('div',{className:'sl',style:{marginTop:1}},settings.userName,"'s workspace")),
    React.createElement('div',{className:'fm',style:{background:'var(--card)',border:'1px solid var(--border)',borderRadius:8,padding:'5px 9px',fontSize:8,fontWeight:700,letterSpacing:1,color:savedAt?'var(--green)':'var(--muted)'}},savedAt?'● SAVED':'○ READY')
  );
}

const EMPTY_TASK={text:'',tag:'personal',urgent:false,day:'',time:'',note:'',movementType:'none',income:'',expenses:'',businessId:''};
function TaskModal({task,onClose}){
  const store=useStore();const{push}=useNotif();
  const isEdit=!!task;
  const [form,setForm]=useState(isEdit?{...EMPTY_TASK,...task,income:task.income||'',expenses:task.expenses||''}:{...EMPTY_TASK});
  const set=(k,v)=>setForm(f=>({...f,[k]:v}));
  const mv=getMvType(form.movementType);
  const hasMove=form.movementType!=='none';
  const net=parseAmt(form.income)-parseAmt(form.expenses);
  const submit=()=>{
    if(!form.text.trim())return push('Task text required','error');
    if(hasMove&&!form.income)return push('Enter income for this movement','error');
    if(isEdit){store.updateTask(task.id,form);push('Task updated','success')}else{store.addTask(form);push('Task added','success')}
    onClose();
  };
  return React.createElement(ModalSheet,{title:isEdit?'EDIT TASK':'ADD TASK',onClose},
    React.createElement(Field,{label:'Task'},React.createElement('input',{value:form.text,onChange:e=>set('text',e.target.value),placeholder:'What needs to be done?',autoFocus:true})),
    React.createElement(Field,{label:'Movement Type'},React.createElement('div',{style:{display:'flex',gap:6,flexWrap:'wrap'}},MOVEMENT_TYPES.map(m=>React.createElement('button',{key:m.value,onClick:()=>set('movementType',m.value),style:{padding:'5px 10px',borderRadius:9,border:'1.5px solid',borderColor:form.movementType===m.value?m.color:'var(--border2)',background:form.movementType===m.value?m.bg:'var(--card2)',color:form.movementType===m.value?m.color:'var(--muted)',fontSize:10,fontFamily:'DM Mono,monospace',fontWeight:700,cursor:'pointer',transition:'all .15s',margin:'2px 0'}},m.icon,' ',m.label)))),
    hasMove&&React.createElement('div',{style:{background:mv.bg,border:`1.5px solid ${mv.color}33`,borderRadius:10,padding:'12px 14px',marginBottom:12}},
      React.createElement('div',{className:'sl',style:{color:mv.color,marginBottom:10}},mv.icon,' ',mv.label.toUpperCase(),' — AMOUNTS'),
      React.createElement(R2,null,React.createElement('div',{style:{flex:1}},React.createElement(Field,{label:'Income (₦)'},React.createElement('input',{type:'number',value:form.income,onChange:e=>set('income',e.target.value),placeholder:'0'}))),React.createElement('div',{style:{flex:1}},React.createElement(Field,{label:'Expenses (₦)'},React.createElement('input',{type:'number',value:form.expenses,onChange:e=>set('expenses',e.target.value),placeholder:'0'})))),
      (form.income||form.expenses)&&React.createElement('div',{style:{marginTop:8,padding:'7px 10px',background:'rgba(0,0,0,.2)',borderRadius:7,display:'flex',justifyContent:'space-between',alignItems:'center'}},React.createElement('span',{className:'sl'},'Net Movement'),React.createElement('span',{className:'fm',style:{fontSize:14,fontWeight:700,color:net>=0?'var(--green)':'var(--red)'}},fmt(net))),
      React.createElement('div',{style:{fontSize:10,color:mv.color,marginTop:8,opacity:.7}},'Completing this task auto-syncs to target and finances.')
    ),
    React.createElement(Field,{label:'Business (optional)'},React.createElement('select',{value:form.businessId,onChange:e=>set('businessId',e.target.value)},React.createElement('option',{value:''},'None'),store.businesses.map(b=>React.createElement('option',{key:b.id,value:b.id},b.name)))),
    React.createElement(R2,null,React.createElement('div',{style:{flex:1}},React.createElement(Field,{label:'Tag'},React.createElement('select',{value:form.tag,onChange:e=>set('tag',e.target.value)},[{v:'personal',l:'Personal'},{v:'urgent',l:'Urgent'},{v:'client',l:'Client — Money In'},{v:'expense',l:'Expense — Money Out'},{v:'business',l:'Business'},{v:'content',l:'Content'},{v:'admin',l:'Admin'}].map(t=>React.createElement('option',{key:t.v,value:t.v},t.l))))),React.createElement('div',{style:{flex:1}},React.createElement(Field,{label:'Day'},React.createElement('select',{value:form.day,onChange:e=>set('day',e.target.value)},React.createElement('option',{value:''},'No day'),DAYS.map(d=>React.createElement('option',{key:d,value:d},d)))))),
    React.createElement(R2,null,React.createElement('div',{style:{flex:1}},React.createElement(Field,{label:'Time'},React.createElement('input',{type:'time',value:form.time,onChange:e=>set('time',e.target.value)}))),React.createElement('div',{style:{flex:1,display:'flex',alignItems:'center',gap:8,paddingTop:20}},React.createElement('input',{type:'checkbox',id:'urg-cb',checked:form.urgent,onChange:e=>set('urgent',e.target.checked),style:{width:'auto',margin:0,accentColor:'var(--red)'}}),React.createElement('label',{htmlFor:'urg-cb',style:{fontSize:13,color:'var(--text)',cursor:'pointer'}},'Urgent'))),
    React.createElement(Field,{label:'Note (optional)'},React.createElement('textarea',{value:form.note,onChange:e=>set('note',e.target.value),rows:2,placeholder:'Context...'})),
    React.createElement('button',{className:'btn-p',onClick:submit,style:{marginTop:4}},isEdit?'Save Changes':hasMove?`+ Add Task (${mv.icon} ${mv.label})`:'+ Add Task')
  );
}

function HomePage(){
  const store=useStore();const{navigate}=useNav();
  const [qIdx,setQIdx]=useState((new Date().getDate()+new Date().getMonth()*31)%QUOTES.length);
  const net=store.getNetMovement(),gross=store.getGrossMovement(),expenses=store.getTaskExpenses();
  const current=store.getCurrentTotal(),remaining=store.getRemaining(),progress=store.getProgress();
  const breakdown=store.getBreakdown(),hasTarget=store.target.total>0;
  const pendingTasks=store.tasks.filter(t=>!t.done);
  const urgentTasks=store.tasks.filter(t=>t.urgent&&!t.done);
  const completedMov=store.tasks.filter(t=>t.done&&t.movementType!=='none'&&t.movementType);
  const outstandingCredits=store.credits.filter(c=>!c.paid);
  const upcomingDl=store.deadlines.filter(d=>!d.done).sort((a,b)=>new Date(a.date)-new Date(b.date)).slice(0,3);
  const isEmpty=store.tasks.length===0&&store.transactions.length===0;
  const q=QUOTES[qIdx];
  return React.createElement('div',{className:'sc',style:{flex:1,paddingBottom:60}},
    React.createElement('div',{style:{padding:'6px 16px 14px'}},React.createElement('div',{className:'fd',style:{fontSize:24,letterSpacing:3,color:'var(--accent)',lineHeight:1.1}},getGreeting(store.settings.userName)),React.createElement('div',{className:'sl',style:{marginTop:4}},getFullDateLabel())),
    isEmpty&&React.createElement('div',{style:{margin:'0 16px 14px'}},React.createElement(Card,{style:{background:'linear-gradient(135deg,rgba(212,168,67,.07),rgba(212,168,67,.02))',borderColor:'rgba(212,168,67,.18)'}},React.createElement('div',{className:'sl',style:{color:'var(--accent)',marginBottom:8}},'WELCOME TO COLE OS'),React.createElement('div',{style:{fontSize:12,color:'var(--text2)',lineHeight:1.6,marginBottom:14}},'Start by setting your target, then add tasks with linked movements.'),React.createElement('div',{style:{display:'flex',gap:8,flexWrap:'wrap'}},[['Set Target','target'],['Add Task','tasks'],['Log Finance','finance']].map(([l,p])=>React.createElement('button',{key:p,className:'btn-g',onClick:()=>navigate(p),style:{fontSize:11}},l))))),
    hasTarget&&React.createElement('div',{style:{margin:'0 16px 12px'}},React.createElement('div',{onClick:()=>navigate('target'),style:{background:'linear-gradient(135deg,var(--accent),var(--accent-l))',borderRadius:16,padding:'18px 20px',cursor:'pointer',position:'relative',overflow:'hidden'}},React.createElement('div',{style:{position:'absolute',top:-25,right:-25,width:90,height:90,background:'rgba(255,255,255,.1)',borderRadius:'50%'}}),React.createElement('div',{className:'sl',style:{color:'rgba(0,0,0,.55)',marginBottom:4}},store.target.label||'TARGET PROGRESS'),React.createElement('div',{style:{display:'flex',justifyContent:'space-between',alignItems:'flex-end',marginBottom:12}},React.createElement('div',null,React.createElement('div',{className:'fm',style:{fontSize:30,fontWeight:700,color:'#000',lineHeight:1}},fmt(current)),React.createElement('div',{className:'fm',style:{fontSize:10,color:'rgba(0,0,0,.5)',marginTop:3}},'of ',fmt(store.target.total),' target')),React.createElement('div',{style:{textAlign:'right'}},React.createElement('div',{className:'fm',style:{fontSize:32,fontWeight:700,color:'#000',lineHeight:1}},progress,'%'),React.createElement('div',{className:'fm',style:{fontSize:9,color:'rgba(0,0,0,.5)'}},fmt(remaining),' remaining'))),React.createElement('div',{style:{background:'rgba(0,0,0,.15)',height:6,borderRadius:6,overflow:'hidden'}},React.createElement('div',{style:{height:'100%',width:`${progress}%`,background:'#000',borderRadius:6,opacity:.6,transition:'width .6s ease'}})))),
    completedMov.length>0&&React.createElement('div',{style:{display:'grid',gridTemplateColumns:'1fr 1fr 1fr',gap:8,margin:'0 16px 12px'}},React.createElement(MiniStat,{label:'Gross',value:fmt(gross),color:'var(--green)'}),React.createElement(MiniStat,{label:'Expenses',value:fmt(expenses),color:'var(--red)'}),React.createElement(MiniStat,{label:'Net',value:fmt(net),color:net>=0?'var(--green)':'var(--red)'})),
    React.createElement('div',{style:{display:'grid',gridTemplateColumns:'1fr 1fr',gap:8,margin:'0 16px 12px'}},React.createElement(StatCard,{label:'Active Tasks',value:pendingTasks.length,color:'var(--text)',sub:urgentTasks.length>0?`${urgentTasks.length} urgent`:'all clear',onClick:()=>navigate('tasks')}),React.createElement(StatCard,{label:'Movements Done',value:completedMov.length,color:'var(--green)',sub:`${fmt(net)} net`,onClick:()=>navigate('movements')})),
    completedMov.length>0&&React.createElement('div',{style:{margin:'0 16px 12px'}},React.createElement('div',{className:'sl',style:{marginBottom:8}},'MOVEMENT BREAKDOWN'),React.createElement(Card,null,Object.entries(breakdown).filter(([,v])=>v.count>0).map(([type,v])=>{const mv=getMvType(type);return React.createElement('div',{key:type,style:{display:'flex',alignItems:'center',gap:10,padding:'8px 0',borderBottom:'1px solid var(--border)'}},React.createElement('div',{style:{width:28,height:28,borderRadius:8,flexShrink:0,background:mv.bg,display:'flex',alignItems:'center',justifyContent:'center',fontSize:13}},mv.icon),React.createElement('div',{style:{flex:1}},React.createElement('div',{style:{fontSize:12,fontWeight:600,color:'var(--text)'}},mv.label),React.createElement('div',{className:'fm',style:{fontSize:9,color:'var(--muted)',marginTop:1}},v.count,' done · exp ',fmt(v.expenses))),React.createElement('div',{style:{textAlign:'right',flexShrink:0}},React.createElement('div',{className:'fm',style:{fontSize:13,fontWeight:700,color:v.net>=0?'var(--green)':'var(--red)'}},fmt(v.net)),React.createElement('div',{className:'fm',style:{fontSize:8,color:'var(--muted)'}},'net')))}))),
    urgentTasks.length>0&&React.createElement('div',{style:{margin:'0 16px 12px'}},React.createElement('div',{className:'sl',style:{marginBottom:8}},'URGENT'),React.createElement(Card,{style:{padding:'4px 14px'}},urgentTasks.slice(0,4).map((t,i)=>{const mv=getMvType(t.movementType);return React.createElement('div',{key:t.id,style:{display:'flex',alignItems:'center',gap:10,padding:'10px 0',borderBottom:i<Math.min(urgentTasks.length,4)-1?'1px solid var(--border)':'none'}},React.createElement('div',{style:{width:6,height:6,borderRadius:'50%',background:'var(--red)',flexShrink:0}}),React.createElement('div',{style:{flex:1,fontSize:13,fontWeight:600,color:'var(--text)',lineHeight:1.3}},t.text),t.movementType!=='none'&&t.movementType&&React.createElement('div',{style:{fontSize:8,padding:'2px 7px',borderRadius:7,background:mv.bg,color:mv.color,fontFamily:'DM Mono,monospace',fontWeight:700,flexShrink:0}},mv.icon,' ',fmt(parseAmt(t.income))))}),urgentTasks.length>4&&React.createElement('div',{onClick:()=>navigate('tasks'),style:{fontSize:11,color:'var(--accent)',cursor:'pointer',padding:'8px 0'}},'+',urgentTasks.length-4,' more →'))),
    outstandingCredits.length>0&&React.createElement('div',{style:{margin:'0 16px 12px'}},React.createElement('div',{className:'sl',style:{marginBottom:8}},'OUTSTANDING CREDITS'),React.createElement(Card,{style:{padding:'4px 14px'}},outstandingCredits.slice(0,4).map((c,i)=>React.createElement('div',{key:c.id,style:{display:'flex',alignItems:'center',gap:10,padding:'9px 0',borderBottom:i<Math.min(outstandingCredits.length,4)-1?'1px solid var(--border)':'none'}},c.priority&&React.createElement('span',{style:{fontSize:11,color:'var(--red)',flexShrink:0}},'⚠'),React.createElement('div',{style:{flex:1,fontSize:13,color:'var(--text)'}},c.name),React.createElement('div',{className:'fm',style:{fontSize:12,fontWeight:700,color:'var(--red)'}},fmt(c.amount)))))),
    upcomingDl.length>0&&React.createElement('div',{style:{margin:'0 16px 12px'}},React.createElement('div',{className:'sl',style:{marginBottom:8}},'UPCOMING DEADLINES'),React.createElement(Card,{style:{padding:'4px 14px'}},upcomingDl.map((d,i)=>{const dl=getDaysUntil(d.date);return React.createElement('div',{key:d.id,style:{display:'flex',alignItems:'center',gap:10,padding:'9px 0',borderBottom:i<upcomingDl.length-1?'1px solid var(--border)':'none'}},React.createElement('div',{style:{flex:1,fontSize:13,color:'var(--text)'}},d.title),d.amount>0&&React.createElement('div',{className:'fm',style:{fontSize:11,color:'var(--accent)'}},fmt(d.amount)),React.createElement('div',{className:'fm',style:{fontSize:9,fontWeight:700,color:dl!==null&&dl<0?'var(--red)':dl===0?'var(--accent)':dl!==null&&dl<=7?'var(--accent)':'var(--muted)'}},dl===null?'':dl<0?'OVERDUE':dl===0?'TODAY':`${dl}D`))}))),
    React.createElement('div',{style:{margin:'0 16px 16px'}},React.createElement(Card,{style:{background:'linear-gradient(135deg,var(--card),var(--card2))',position:'relative',overflow:'hidden'}},React.createElement('div',{style:{position:'absolute',top:-20,right:-20,width:80,height:80,background:'var(--accent)',opacity:.04,borderRadius:'50%'}}),React.createElement('button',{onClick:()=>setQIdx(i=>(i+1)%QUOTES.length),style:{position:'absolute',top:12,right:12,background:'none',border:'1px solid var(--border)',borderRadius:7,padding:'4px 8px',color:'var(--muted)',fontSize:10}},'↻'),React.createElement('div',{style:{fontSize:18,color:'var(--accent)',opacity:.6,marginBottom:8,fontFamily:'Georgia,serif'}},'❝'),React.createElement('div',{style:{fontSize:13,color:'var(--text)',lineHeight:1.6,fontStyle:'italic',paddingRight:30}},q.text),React.createElement('div',{className:'sl',style:{marginTop:8}},q.attr)))
  );
}

function TaskRow({task,onEdit}){
  const store=useStore();const{push}=useNotif();
  const mv=getMvType(task.movementType);
  const hasMove=task.movementType&&task.movementType!=='none';
  const net=parseAmt(task.income)-parseAmt(task.expenses);
  const bizName=store.businesses.find(b=>b.id===task.businessId)?.name;
  const tagColors={personal:'var(--blue)',urgent:'var(--red)',client:'var(--green)',expense:'var(--red)',business:'var(--green)',admin:'var(--muted)',content:'var(--accent)'};
  const handleToggle=()=>{
    const result=store.toggleTask(task.id);if(!result)return;
    if(result.done){if(hasMove)push(`✓ ${result.text.slice(0,35)} — ${mv.icon} ${mv.label}: ${fmt(net)} net synced`,'movement',5000);else push(`Done: ${result.text.slice(0,45)}`,'success')}
    else{if(hasMove)push(`Undone: ${result.text.slice(0,35)} — movement reversed`,'warning');else push(`Reopened: ${result.text.slice(0,35)}`,'info')}
  };
  return React.createElement('div',{style:{display:'flex',alignItems:'flex-start',gap:10,padding:'12px 0',borderBottom:'1px solid var(--border)',opacity:task.done?.55:1,transition:'opacity .2s'}},
    React.createElement('button',{onClick:handleToggle,style:{background:'none',border:'none',padding:'2px 0',flexShrink:0,marginTop:1,fontSize:20,lineHeight:1,color:task.done?(hasMove?mv.color:'var(--accent)'):(task.urgent?'var(--red)':'var(--muted)')}},task.done?'☑':'☐'),
    React.createElement('div',{style:{flex:1,minWidth:0}},
      React.createElement('div',{style:{fontSize:14,fontWeight:task.urgent&&!task.done?600:500,color:task.done?'var(--muted)':task.urgent?'var(--red)':'var(--text)',textDecoration:task.done?'line-through':'none',lineHeight:1.35}},task.text),
      React.createElement('div',{style:{display:'flex',alignItems:'center',gap:6,marginTop:4,flexWrap:'wrap'}},
        React.createElement('span',{style:{fontSize:8,padding:'2px 7px',borderRadius:7,background:`${tagColors[task.tag]||'var(--muted)'}18`,color:tagColors[task.tag]||'var(--muted)',fontFamily:'DM Mono,monospace',fontWeight:700,textTransform:'uppercase'}},task.tag),
        hasMove&&React.createElement('span',{style:{fontSize:8,padding:'2px 8px',borderRadius:7,background:mv.bg,color:mv.color,fontFamily:'DM Mono,monospace',fontWeight:700}},mv.icon,' ',mv.label),
        hasMove&&task.income&&React.createElement('span',{className:'fm',style:{fontSize:10,fontWeight:700,color:task.done?'var(--green)':mv.color}},'+',fmt(parseAmt(task.income)),task.expenses&&parseAmt(task.expenses)>0&&React.createElement('span',{style:{color:'var(--red)',marginLeft:3}},'−',fmt(parseAmt(task.expenses))),' ',React.createElement('span',{style:{color:net>=0?'var(--green)':'var(--red)'}},'=',fmt(net))),
        (task.day||task.time)&&React.createElement('span',{className:'fm',style:{fontSize:9,color:'var(--muted)'}},task.day,task.day&&task.time?' · ':'',task.time),
        bizName&&React.createElement('span',{className:'fm',style:{fontSize:9,color:'var(--accent)'}},bizName),
        task.done&&hasMove&&React.createElement('span',{style:{fontSize:8,padding:'2px 7px',borderRadius:7,background:'var(--green-dim)',color:'var(--green)',fontFamily:'DM Mono,monospace',fontWeight:700}},'SYNCED')
      ),
      task.note&&React.createElement('div',{style:{fontSize:11,color:'var(--muted)',marginTop:3,fontStyle:'italic'}},task.note)
    ),
    task.urgent&&!task.done&&React.createElement('div',{style:{width:7,height:7,borderRadius:'50%',background:'var(--red)',flexShrink:0,marginTop:4}}),
    React.createElement('div',{style:{display:'flex',gap:2,flexShrink:0}},React.createElement('button',{onClick:()=>onEdit(task),style:{background:'none',border:'none',color:'var(--muted)',padding:'4px 5px',fontSize:12}},'✏'),React.createElement('button',{onClick:()=>{if(confirm('Delete task?'))store.deleteTask(task.id)},style:{background:'none',border:'none',color:'var(--red)',opacity:.6,padding:'4px 5px',fontSize:14}},'×'))
  );
}

function TasksPage(){
  const store=useStore();
  const [showAdd,setShowAdd]=useState(false);const [editTask,setEditTask]=useState(null);
  const [filter,setFilter]=useState('all');const [dayFilter,setDayFilter]=useState('all');
  const total=store.tasks.length,done=store.tasks.filter(t=>t.done).length;
  const pctDone=total>0?Math.round((done/total)*100):0;
  const filtered=store.tasks.filter(t=>{
    const matchF=filter==='all'?true:filter==='pending'?!t.done:filter==='urgent'?t.urgent&&!t.done:filter==='movement'?t.movementType&&t.movementType!=='none':filter==='done'?t.done:t.tag===filter;
    const matchD=dayFilter==='all'?true:t.day===dayFilter;
    return matchF&&matchD;
  });
  const pending=filtered.filter(t=>!t.done),completed=filtered.filter(t=>t.done);
  return React.createElement('div',{className:'sc',style:{flex:1}},
    React.createElement('div',{style:{padding:'8px 16px 10px'}},React.createElement('div',{style:{display:'flex',justifyContent:'space-between',alignItems:'center',marginBottom:6}},React.createElement('div',{className:'sl'},done,'/',total,' completed'),React.createElement('div',{className:'fm',style:{fontSize:11,fontWeight:700,color:'var(--accent)'}},pctDone,'%')),React.createElement(ProgBar,{value:done,max:total||1,color:'var(--accent)'})),
    React.createElement('div',{style:{padding:'0 16px 10px'}},React.createElement('button',{className:'btn-p',onClick:()=>setShowAdd(true),style:{display:'flex',alignItems:'center',justifyContent:'center',gap:6}},'+  Add Task')),
    React.createElement('div',{style:{display:'flex',gap:6,padding:'0 16px',marginBottom:6,overflowX:'auto'}},[{v:'all',l:'All'},{v:'pending',l:'Pending'},{v:'urgent',l:'Urgent'},{v:'movement',l:'Movement'},{v:'done',l:'Done'},{v:'client',l:'Client'},{v:'expense',l:'Expense'},{v:'content',l:'Content'}].map(f=>React.createElement('button',{key:f.v,className:`chip ${filter===f.v?'on':''}`,onClick:()=>setFilter(f.v)},f.l))),
    React.createElement('div',{style:{display:'flex',gap:6,padding:'0 16px',marginBottom:12,overflowX:'auto'}},[{v:'all',l:'All Days'},...DAYS.map(d=>({v:d,l:d.slice(0,3)}))].map(f=>React.createElement('button',{key:f.v,className:`chip ${dayFilter===f.v?'on':''}`,onClick:()=>setDayFilter(f.v),style:{fontSize:9,padding:'4px 9px'}},f.l))),
    React.createElement('div',{style:{padding:'0 16px 40px'}},
      filtered.length===0?React.createElement(EmptyState,{icon:'✓',title:'No tasks',sub:'Add tasks with linked movements.',action:'Add Task',onAction:()=>setShowAdd(true)}):
      React.createElement(React.Fragment,null,
        pending.length>0&&React.createElement(React.Fragment,null,React.createElement('div',{className:'sl',style:{marginBottom:4}},'PENDING — ',pending.length),pending.map(t=>React.createElement(TaskRow,{key:t.id,task:t,onEdit:setEditTask}))),
        completed.length>0&&React.createElement(React.Fragment,null,React.createElement('div',{className:'sl',style:{margin:'14px 0 4px'}},'COMPLETED — ',completed.length),completed.map(t=>React.createElement(TaskRow,{key:t.id,task:t,onEdit:setEditTask})))
      )
    ),
    showAdd&&React.createElement(TaskModal,{onClose:()=>setShowAdd(false)}),
    editTask&&React.createElement(TaskModal,{task:editTask,onClose:()=>setEditTask(null)})
  );
}

function MovementsPage(){
  const store=useStore();
  const completedMov=store.tasks.filter(t=>t.done&&t.movementType&&t.movementType!=='none').sort((a,b)=>new Date(b.completedAt||b.createdAt)-new Date(a.completedAt||a.createdAt));
  const breakdown=store.getBreakdown(),gross=store.getGrossMovement(),expenses=store.getTaskExpenses(),net=store.getNetMovement();
  if(!completedMov.length)return React.createElement('div',{className:'sc',style:{flex:1,padding:'0 16px'}},React.createElement(EmptyState,{icon:'⚡',title:'No movements yet',sub:'Complete tasks with a linked movement type.'}));
  return React.createElement('div',{className:'sc',style:{flex:1}},
    React.createElement('div',{style:{display:'grid',gridTemplateColumns:'repeat(3,1fr)',gap:8,padding:'8px 16px 12px'}},React.createElement(StatCard,{label:'Gross',value:fmt(gross),color:'var(--green)',sub:'total income'}),React.createElement(StatCard,{label:'Expenses',value:fmt(expenses),color:'var(--red)',sub:'deducted'}),React.createElement(StatCard,{label:'Net',value:fmt(net),color:net>=0?'var(--green)':'var(--red)',sub:'toward target'})),
    React.createElement('div',{style:{margin:'0 16px 14px'}},React.createElement('div',{className:'sl',style:{marginBottom:8}},'BY MOVEMENT TYPE'),React.createElement(Card,null,MOVEMENT_TYPES.filter(m=>m.value!=='none').map(m=>{const b=breakdown[m.value];if(!b||b.count===0)return null;return React.createElement('div',{key:m.value,style:{display:'flex',alignItems:'center',gap:10,padding:'10px 0',borderBottom:'1px solid var(--border)'}},React.createElement('div',{style:{width:34,height:34,borderRadius:9,flexShrink:0,background:m.bg,display:'flex',alignItems:'center',justifyContent:'center',fontSize:15}},m.icon),React.createElement('div',{style:{flex:1}},React.createElement('div',{style:{fontSize:13,fontWeight:600,color:'var(--text)'}},m.label),React.createElement('div',{className:'fm',style:{fontSize:9,color:'var(--muted)',marginTop:2}},b.count,' completed · gross ',fmt(b.gross),' · exp ',fmt(b.expenses))),React.createElement('div',{style:{textAlign:'right',flexShrink:0}},React.createElement('div',{className:'fm',style:{fontSize:14,fontWeight:700,color:b.net>=0?'var(--green)':'var(--red)'}},fmt(b.net)),React.createElement('div',{className:'fm',style:{fontSize:8,color:'var(--muted)'}},'net')))}))),
    React.createElement('div',{style:{margin:'0 16px 40px'}},React.createElement('div',{className:'sl',style:{marginBottom:8}},'MOVEMENT LOG (',completedMov.length,')'),React.createElement(Card,{style:{padding:'4px 14px'}},completedMov.map((t,i)=>{const mv=getMvType(t.movementType),inc=parseAmt(t.income),exp=parseAmt(t.expenses),n=inc-exp;return React.createElement('div',{key:t.id,style:{display:'flex',alignItems:'flex-start',gap:10,padding:'11px 0',borderBottom:i<completedMov.length-1?'1px solid var(--border)':'none'}},React.createElement('div',{style:{width:32,height:32,borderRadius:9,flexShrink:0,background:mv.bg,display:'flex',alignItems:'center',justifyContent:'center',fontSize:14}},mv.icon),React.createElement('div',{style:{flex:1,minWidth:0}},React.createElement('div',{style:{fontSize:13,fontWeight:600,color:'var(--text)',lineHeight:1.25}},t.text),React.createElement('div',{style:{display:'flex',gap:8,marginTop:3,flexWrap:'wrap'}},React.createElement('span',{className:'fm',style:{fontSize:9,color:mv.color,fontWeight:700}},mv.label),t.completedAt&&React.createElement('span',{className:'fm',style:{fontSize:9,color:'var(--muted)'}},fmtDate(t.completedAt))),exp>0&&React.createElement('div',{className:'fm',style:{fontSize:9,color:'var(--muted)',marginTop:2}},'Income ',fmt(inc),' − Expenses ',fmt(exp))),React.createElement('div',{style:{textAlign:'right',flexShrink:0}},React.createElement('div',{className:'fm',style:{fontSize:14,fontWeight:700,color:n>=0?'var(--green)':'var(--red)'}},fmt(n)),React.createElement('div',{className:'fm',style:{fontSize:8,color:'var(--muted)'}},'net')))})))
  );
}

function CreditModal({credit,onClose}){
  const store=useStore();const{push}=useNotif();
  const isEdit=!!credit;
  const [name,setName]=useState(credit?.name??'');
  const [amount,setAmount]=useState(credit?.amount?String(credit.amount):'');
  const [category,setCategory]=useState(credit?.category??'repayment');
  const [priority,setPriority]=useState(credit?.priority??false);
  const [dueDate,setDueDate]=useState(credit?.dueDate??'');
  const [note,setNote]=useState(credit?.note??'');
  const submit=()=>{
    if(!name.trim())return push('Enter a name','error');
    if(!amount||parseAmt(amount)<=0)return push('Enter a valid amount','error');
    if(isEdit){store.updateCredit(credit.id,{name,amount,category,priority,dueDate,note});push(`Credit updated: ${name}`,'success')}
    else{store.addCredit({name,amount,category,priority,dueDate,note});push(`Credit added: ${name} — ${fmt(parseAmt(amount))}`,'success')}
    onClose();
  };
  return React.createElement(ModalSheet,{title:isEdit?'EDIT CREDIT':'ADD CREDIT',onClose},
    React.createElement(Field,{label:'Name'},React.createElement('input',{value:name,onChange:e=>setName(e.target.value),placeholder:'e.g. Dami, Rasak, Mom...',autoFocus:true})),
    React.createElement(Field,{label:'Amount (₦)'},React.createElement('input',{type:'number',value:amount,onChange:e=>setAmount(e.target.value),placeholder:'0'})),
    React.createElement(Field,{label:'Category'},React.createElement('div',{style:{display:'flex',gap:8}},[{v:'repayment',l:'Repayment'},{v:'personal',l:'Personal Credit'}].map(opt=>React.createElement('button',{key:opt.v,onClick:()=>setCategory(opt.v),style:{flex:1,padding:9,borderRadius:9,border:'1.5px solid',borderColor:category===opt.v?'var(--accent)':'var(--border2)',background:category===opt.v?'var(--accent-dim)':'var(--card2)',color:category===opt.v?'var(--accent)':'var(--muted)',fontWeight:700,fontSize:12,transition:'all .15s'}},opt.l)))),
    React.createElement(R2,null,React.createElement('div',{style:{flex:1}},React.createElement(Field,{label:'Due Date (optional)'},React.createElement('input',{type:'date',value:dueDate,onChange:e=>setDueDate(e.target.value)}))),React.createElement('div',{style:{flex:1,display:'flex',alignItems:'center',gap:8,paddingTop:20}},React.createElement('input',{type:'checkbox',id:'pri-cb',checked:priority,onChange:e=>setPriority(e.target.checked),style:{width:'auto',margin:0,accentColor:'var(--red)'}}),React.createElement('label',{htmlFor:'pri-cb',style:{fontSize:13,color:'var(--text)',cursor:'pointer'}},'⚠ Priority'))),
    React.createElement(Field,{label:'Note (optional)'},React.createElement('textarea',{value:note,onChange:e=>setNote(e.target.value),placeholder:'Context...',rows:2})),
    React.createElement('button',{className:'btn-p',onClick:submit},isEdit?'Save Changes':'+ Add Credit Entry')
  );
}

function CreditEntry({credit,onEdit,isLast}){
  const store=useStore();const{push}=useNotif();
  const dl=getDaysUntil(credit.dueDate);
  const isOverdue=!credit.paid&&dl!==null&&dl<0;
  const handleToggle=()=>{
    const result=store.toggleCredit(credit.id);if(!result)return;
    if(result.paid)push(`✓ ${result.name} — ${fmt(result.amount)} paid. Balance reduced.`,'expense',5000);
    else push(`${result.name} — ${fmt(result.amount)} unpaid. Balance restored.`,'info',3500);
  };
  const handleDelete=()=>{
    const msg=credit.paid?`Delete "${credit.name}"? This will restore ${fmt(credit.amount)} to your balance.`:`Delete "${credit.name}"?`;
    if(!confirm(msg))return;
    store.deleteCredit(credit.id);
    if(credit.paid)push(`Deleted & ${fmt(credit.amount)} restored to balance`,'success');
    else push('Credit entry deleted','info');
  };
  return React.createElement('div',{style:{display:'flex',alignItems:'flex-start',gap:10,padding:'12px 0',borderBottom:isLast?'none':'1px solid var(--border)',opacity:credit.paid?.55:1,transition:'opacity .2s'}},
    React.createElement('button',{onClick:handleToggle,style:{background:'none',border:'none',padding:'2px 0',flexShrink:0,marginTop:1,fontSize:20,lineHeight:1,color:credit.paid?'var(--green)':(credit.priority?'var(--red)':'var(--muted)')}},credit.paid?'●':'○'),
    React.createElement('div',{style:{flex:1,minWidth:0}},
      React.createElement('div',{style:{display:'flex',alignItems:'center',gap:6,marginBottom:3}},credit.priority&&!credit.paid&&React.createElement('span',{style:{fontSize:11,color:'var(--red)'}},'⚠'),React.createElement('div',{style:{fontSize:14,fontWeight:credit.priority&&!credit.paid?700:500,color:credit.paid?'var(--muted)':isOverdue?'var(--red)':credit.priority?'var(--red)':'var(--text)',textDecoration:credit.paid?'line-through':'none',lineHeight:1.3}},credit.name)),
      React.createElement('div',{style:{display:'flex',gap:6,flexWrap:'wrap',alignItems:'center'}},
        React.createElement('span',{style:{fontSize:8,padding:'2px 7px',borderRadius:7,background:credit.category==='repayment'?'var(--red-dim)':'var(--accent-dim)',color:credit.category==='repayment'?'var(--red)':'var(--accent)',fontFamily:'DM Mono,monospace',fontWeight:700,textTransform:'uppercase'}},credit.category),
        credit.priority&&!credit.paid&&React.createElement('span',{style:{fontSize:8,padding:'2px 7px',borderRadius:7,background:'var(--red-dim)',color:'var(--red)',fontFamily:'DM Mono,monospace',fontWeight:700}},'PRIORITY'),
        credit.dueDate&&!credit.paid&&React.createElement('span',{className:'fm',style:{fontSize:9,color:isOverdue?'var(--red)':dl!==null&&dl<=7?'var(--accent)':'var(--muted)'}},isOverdue?'OVERDUE':dl===0?'DUE TODAY':`Due ${fmtDate(credit.dueDate)}${dl!==null?` (${dl}d)`:''}`),
        credit.paid&&React.createElement('span',{style:{fontSize:8,padding:'2px 7px',borderRadius:7,background:'var(--green-dim)',color:'var(--green)',fontFamily:'DM Mono,monospace',fontWeight:700}},'PAID · ',fmtDateShort(credit.paidAt)),
        credit.note&&React.createElement('span',{style:{fontSize:10,color:'var(--muted)',fontStyle:'italic'}},credit.note)
      )
    ),
    React.createElement('div',{style:{textAlign:'right',flexShrink:0}},React.createElement('div',{className:'fm',style:{fontSize:14,fontWeight:700,color:credit.paid?'var(--muted)':'var(--red)'}},fmt(credit.amount)),React.createElement('div',{style:{display:'flex',justifyContent:'flex-end',gap:2,marginTop:3}},React.createElement('button',{onClick:()=>onEdit(credit),style:{background:'none',border:'none',color:'var(--muted)',padding:'2px 4px',fontSize:12}},'✏'),React.createElement('button',{onClick:handleDelete,style:{background:'none',border:'none',color:'var(--red)',opacity:.6,padding:'2px 4px',fontSize:14}},'×')))
  );
}

function TxModal({onClose}){
  const store=useStore();const{push}=useNotif();
  const [form,setForm]=useState({type:'income',desc:'',amount:'',category:'sales',businessId:'',date:todayStr(),note:''});
  const set=(k,v)=>setForm(f=>({...f,[k]:v}));
  const submit=()=>{
    if(!form.desc)return push('Enter a description','error');
    if(!form.amount)return push('Enter an amount','error');
    store.addTransaction(form);
    push(`${form.type==='income'?'Income':'Expense'} logged: ${fmt(parseAmt(form.amount))}`,form.type==='income'?'income':'expense');
    onClose();
  };
  return React.createElement(ModalSheet,{title:'LOG TRANSACTION',onClose},
    React.createElement(Field,{label:'Type'},React.createElement('div',{style:{display:'flex',gap:8}},['income','expense'].map(t=>React.createElement('button',{key:t,onClick:()=>set('type',t),style:{flex:1,padding:9,borderRadius:9,border:'1.5px solid',borderColor:form.type===t?(t==='income'?'var(--green)':'var(--red)'):'var(--border2)',background:form.type===t?(t==='income'?'var(--green-dim)':'var(--red-dim)'):'var(--card2)',color:form.type===t?(t==='income'?'var(--green)':'var(--red)'):'var(--muted)',fontWeight:700,fontSize:12,textTransform:'uppercase',letterSpacing:1}},t)))),
    React.createElement(Field,{label:'Description'},React.createElement('input',{value:form.desc,onChange:e=>set('desc',e.target.value),placeholder:'What is this for?',autoFocus:true})),
    React.createElement(R2,null,React.createElement('div',{style:{flex:1}},React.createElement(Field,{label:'Amount (₦)'},React.createElement('input',{type:'number',value:form.amount,onChange:e=>set('amount',e.target.value),placeholder:'0'}))),React.createElement('div',{style:{flex:1}},React.createElement(Field,{label:'Date'},React.createElement('input',{type:'date',value:form.date,onChange:e=>set('date',e.target.value)})))),
    React.createElement(Field,{label:'Category'},React.createElement('select',{value:form.category,onChange:e=>set('category',e.target.value)},[{v:'sales',l:'Sales/Orders'},{v:'services',l:'Services'},{v:'materials',l:'Materials/Stock'},{v:'rent',l:'Rent/Utilities'},{v:'marketing',l:'Marketing'},{v:'salary',l:'Salary/Wages'},{v:'other',l:'Other'}].map(c=>React.createElement('option',{key:c.v,value:c.v},c.l)))),
    store.businesses.length>0&&React.createElement(Field,{label:'Business'},React.createElement('select',{value:form.businessId,onChange:e=>set('businessId',e.target.value)},React.createElement('option',{value:''},'General'),store.businesses.map(b=>React.createElement('option',{key:b.id,value:b.id},b.name)))),
    React.createElement(Field,{label:'Note (optional)'},React.createElement('input',{value:form.note,onChange:e=>set('note',e.target.value),placeholder:'Optional'})),
    React.createElement('button',{className:'btn-p',onClick:submit},'+ Log Transaction')
  );
}

function FinancePage(){
  const store=useStore();const{push}=useNotif();
  const [activeTab,setActiveTab]=useState('overview');
  const [showAddTx,setShowAddTx]=useState(false);const [showAddCredit,setShowAddCredit]=useState(false);const [editCredit,setEditCredit]=useState(null);const [txFilter,setTxFilter]=useState('all');
  const balance=store.getFullBalance();
  const creditPaid=store.getCreditPaid(),creditOwed=store.getCreditOwed();
  const txIncome=calc.txIncome(store.transactions),txExpense=calc.txExpense(store.transactions);
  const totalCredit=store.credits.reduce((s,c)=>s+c.amount,0);
  const paidCount=store.credits.filter(c=>c.paid).length;
  const priorityCredits=store.credits.filter(c=>c.priority&&!c.paid);
  const repaymentOwed=store.credits.filter(c=>c.category==='repayment'&&!c.paid).reduce((s,c)=>s+c.amount,0);
  const personalOwed=store.credits.filter(c=>c.category==='personal'&&!c.paid).reduce((s,c)=>s+c.amount,0);
  const sortedTx=[...store.transactions].sort((a,b)=>new Date(b.date)-new Date(a.date));
  const filteredTx=txFilter==='all'?sortedTx:txFilter==='income'?sortedTx.filter(t=>t.type==='income'):sortedTx.filter(t=>t.type==='expense');
  const bizLabel=id=>store.businesses.find(b=>b.id===id)?.name||'General';
  const TABS=[{v:'overview',l:'Overview'},{v:'credit',l:`Credit (${store.credits.filter(c=>!c.paid).length})`},{v:'transactions',l:'Transactions'}];
  return React.createElement('div',{className:'sc',style:{flex:1}},
    React.createElement('div',{style:{margin:'8px 16px 12px'}},React.createElement('div',{style:{background:'linear-gradient(135deg,var(--accent),var(--accent-l))',borderRadius:16,padding:'18px 20px',position:'relative',overflow:'hidden'}},React.createElement('div',{style:{position:'absolute',top:-25,right:-25,width:90,height:90,background:'rgba(255,255,255,.1)',borderRadius:'50%'}}),React.createElement('div',{className:'sl',style:{color:'rgba(0,0,0,.55)',marginBottom:4}},'CURRENT BALANCE'),React.createElement('div',{className:'fm',style:{fontSize:36,fontWeight:700,color:'#000',position:'relative',zIndex:1,lineHeight:1}},fmt(balance)),React.createElement('div',{className:'fm',style:{fontSize:9,color:'rgba(0,0,0,.45)',marginTop:5,lineHeight:1.5}},'Starting ',fmt(store.target.startingBalance),' + movements − ',fmt(creditPaid),' credit paid'))),
    React.createElement('div',{style:{display:'flex',gap:6,padding:'0 16px',marginBottom:12,overflowX:'auto'}},TABS.map(t=>React.createElement('button',{key:t.v,className:`chip ${activeTab===t.v?'on':''}`,onClick:()=>setActiveTab(t.v)},t.l))),
    activeTab==='overview'&&React.createElement('div',{style:{padding:'0 16px'}},
      React.createElement('div',{style:{display:'grid',gridTemplateColumns:'1fr 1fr',gap:8,marginBottom:12}},React.createElement(MiniStat,{label:'TX Income',value:fmt(txIncome),color:'var(--green)',sub:`${store.transactions.filter(t=>t.type==='income').length} tx`}),React.createElement(MiniStat,{label:'TX Expense',value:fmt(txExpense),color:'var(--red)',sub:`${store.transactions.filter(t=>t.type==='expense').length} tx`}),React.createElement(MiniStat,{label:'Credit Paid',value:fmt(creditPaid),color:'var(--red)',sub:`${paidCount} paid`}),React.createElement(MiniStat,{label:'Credit Owed',value:fmt(creditOwed),color:'var(--accent)',sub:`${store.credits.filter(c=>!c.paid).length} remaining`})),
      store.credits.length>0&&React.createElement(Card,{style:{marginBottom:12}},React.createElement('div',{className:'sl',style:{marginBottom:10}},'CREDIT OUTSTANDING'),React.createElement('div',{style:{display:'flex',justifyContent:'space-between',alignItems:'flex-end',marginBottom:10}},React.createElement('div',{className:'fm',style:{fontSize:22,fontWeight:700,color:'var(--red)'}},fmt(creditOwed)),React.createElement('div',{className:'fm',style:{fontSize:11,color:'var(--muted)'}},'of ',fmt(totalCredit),' total')),React.createElement(ProgBar,{value:creditPaid,max:totalCredit||1,color:'var(--green)'}),React.createElement('div',{style:{display:'flex',gap:12,marginTop:10}},repaymentOwed>0&&React.createElement('div',{className:'fm',style:{fontSize:10,color:'var(--red)'}},'Repayments: ',fmt(repaymentOwed)),personalOwed>0&&React.createElement('div',{className:'fm',style:{fontSize:10,color:'var(--accent)'}},'Personal: ',fmt(personalOwed)))),
      priorityCredits.length>0&&React.createElement(Card,{style:{marginBottom:12,borderColor:'rgba(224,82,82,.25)',background:'rgba(224,82,82,.03)'}},React.createElement('div',{className:'sl',style:{color:'var(--red)',marginBottom:8}},'PRIORITY CREDITS'),priorityCredits.map((c,i)=>React.createElement('div',{key:c.id,style:{display:'flex',alignItems:'center',gap:8,padding:'8px 0',borderBottom:i<priorityCredits.length-1?'1px solid var(--border)':'none'}},React.createElement('span',{style:{color:'var(--red)',fontSize:13}},'⚠'),React.createElement('div',{style:{flex:1,fontSize:13,fontWeight:600,color:'var(--text)'}},c.name),c.dueDate&&React.createElement('div',{className:'fm',style:{fontSize:9,color:getDaysUntil(c.dueDate)<0?'var(--red)':'var(--muted)'}},fmtDate(c.dueDate)),React.createElement('div',{className:'fm',style:{fontSize:13,fontWeight:700,color:'var(--red)'}},fmt(c.amount))))),
      React.createElement('div',{style:{display:'flex',gap:8}},React.createElement('button',{className:'btn-p',onClick:()=>setShowAddTx(true),style:{flex:1}},'+  Log Transaction'),React.createElement('button',{className:'btn-g',onClick:()=>{setActiveTab('credit');setShowAddCredit(true)},style:{flex:1}},'+  Credit'))
    ),
    activeTab==='credit'&&React.createElement('div',{style:{padding:'0 16px'}},
      React.createElement('div',{style:{display:'grid',gridTemplateColumns:'repeat(3,1fr)',gap:8,marginBottom:12}},React.createElement(MiniStat,{label:'Outstanding',value:fmt(creditOwed),color:'var(--red)',sub:`${store.credits.filter(c=>!c.paid).length} entries`}),React.createElement(MiniStat,{label:'Paid',value:fmt(creditPaid),color:'var(--green)',sub:`${paidCount} cleared`}),React.createElement(MiniStat,{label:'Total',value:fmt(totalCredit),color:'var(--accent)',sub:`${store.credits.length} total`})),
      React.createElement('button',{className:'btn-p',onClick:()=>setShowAddCredit(true),style:{display:'flex',alignItems:'center',justifyContent:'center',gap:6,marginBottom:12}},'+  Add Credit Entry'),
      store.credits.length===0?React.createElement(EmptyState,{icon:'💳',title:'No credit entries',sub:'Add money you owe — when marked paid, it automatically reduces your balance.',action:'Add Credit',onAction:()=>setShowAddCredit(true)}):
      React.createElement(React.Fragment,null,
        store.credits.filter(c=>!c.paid).length>0&&React.createElement(React.Fragment,null,React.createElement('div',{className:'sl',style:{marginBottom:6}},'OUTSTANDING — ',fmt(creditOwed)),React.createElement(Card,{style:{padding:'4px 14px',marginBottom:12}},[...store.credits.filter(c=>!c.paid&&c.priority),...store.credits.filter(c=>!c.paid&&!c.priority)].map((c,i,arr)=>React.createElement(CreditEntry,{key:c.id,credit:c,onEdit:setEditCredit,isLast:i===arr.length-1})))),
        store.credits.filter(c=>c.paid).length>0&&React.createElement(React.Fragment,null,React.createElement('div',{className:'sl',style:{marginBottom:6}},'PAID / CLEARED — ',fmt(creditPaid)),React.createElement(Card,{style:{padding:'4px 14px'}},store.credits.filter(c=>c.paid).map((c,i,arr)=>React.createElement(CreditEntry,{key:c.id,credit:c,onEdit:setEditCredit,isLast:i===arr.length-1}))))
      )
    ),
    activeTab==='transactions'&&React.createElement('div',{style:{padding:'0 16px'}},
      React.createElement('button',{className:'btn-p',onClick:()=>setShowAddTx(true),style:{display:'flex',alignItems:'center',justifyContent:'center',gap:6,marginBottom:10}},'+  Log Transaction'),
      React.createElement('div',{style:{display:'flex',gap:6,marginBottom:10}},[{v:'all',l:'All'},{v:'income',l:'Income'},{v:'expense',l:'Expense'}].map(f=>React.createElement('button',{key:f.v,className:`chip ${txFilter===f.v?'on':''}`,onClick:()=>setTxFilter(f.v)},f.l))),
      filteredTx.length===0?React.createElement(EmptyState,{icon:'💳',title:'No transactions',sub:'Log manual income and expenses here.',action:'Log Transaction',onAction:()=>setShowAddTx(true)}):
      React.createElement(Card,{style:{padding:'4px 14px'}},filteredTx.map((t,i)=>React.createElement('div',{key:t.id,style:{display:'flex',alignItems:'flex-start',gap:10,padding:'11px 0',borderBottom:i<filteredTx.length-1?'1px solid var(--border)':'none'}},React.createElement('div',{style:{width:30,height:30,borderRadius:8,flexShrink:0,display:'flex',alignItems:'center',justifyContent:'center',fontSize:9,fontWeight:700,fontFamily:'DM Mono,monospace',background:t.type==='income'?'var(--green-dim)':'var(--red-dim)',color:t.type==='income'?'var(--green)':'var(--red)'}},t.type==='income'?'IN':'OUT'),React.createElement('div',{style:{flex:1,minWidth:0}},React.createElement('div',{style:{fontSize:13,fontWeight:600,color:'var(--text)',lineHeight:1.25}},t.desc),React.createElement('div',{className:'fm',style:{fontSize:9,color:'var(--muted)',marginTop:2}},(t.category||'').toUpperCase(),' · ',t.businessId?bizLabel(t.businessId):'GENERAL',' · ',fmtDateShort(t.date)),t.note&&React.createElement('div',{style:{fontSize:10,color:'var(--muted)',marginTop:2,fontStyle:'italic'}},t.note)),React.createElement('div',{style:{textAlign:'right',flexShrink:0}},React.createElement('div',{className:'fm',style:{fontSize:13,fontWeight:700,color:t.type==='income'?'var(--green)':'var(--red)'}},t.type==='income'?'+':'−',fmt(t.amount)),React.createElement('button',{onClick:()=>{if(confirm('Delete transaction?')){store.deleteTransaction(t.id);push('Transaction deleted','info')}},style:{background:'none',border:'none',color:'var(--red)',opacity:.5,padding:'2px 0',marginTop:2,fontSize:12}},'×')))))
    ),
    showAddTx&&React.createElement(TxModal,{onClose:()=>setShowAddTx(false)}),
    showAddCredit&&React.createElement(CreditModal,{onClose:()=>setShowAddCredit(false)}),
    editCredit&&React.createElement(CreditModal,{credit:editCredit,onClose:()=>setEditCredit(null)})
  );
}

function SetTargetModal({onClose}){
  const store=useStore();const{push}=useNotif();
  const [total,setTotal]=useState(store.target.total>0?String(store.target.total):'');
  const [startBal,setStartBal]=useState(store.target.startingBalance>0?String(store.target.startingBalance):'');
  const [label,setLabel]=useState(store.target.label||'');
  const submit=()=>{const t=parseAmt(total);if(!t)return push('Enter a target amount','error');store.setTarget(t,parseAmt(startBal),label);push('Target set: '+fmt(t),'success');onClose()};
  return React.createElement(ModalSheet,{title:'SET TARGET',onClose},
    React.createElement('div',{style:{background:'var(--accent-dim)',border:'1px solid rgba(212,168,67,.2)',borderRadius:9,padding:'11px 13px',marginBottom:16,fontSize:11,color:'var(--accent)',lineHeight:1.6}},'Set your total target once. Completed movement tasks automatically update your progress.'),
    React.createElement(Field,{label:'Total Target Amount (₦)'},React.createElement('input',{type:'number',value:total,onChange:e=>setTotal(e.target.value),placeholder:'e.g. 2000000',autoFocus:true})),
    React.createElement(Field,{label:'Current Available Balance (₦)'},React.createElement('input',{type:'number',value:startBal,onChange:e=>setStartBal(e.target.value),placeholder:'What you have right now'})),
    React.createElement(Field,{label:'Label (optional)'},React.createElement('input',{value:label,onChange:e=>setLabel(e.target.value),placeholder:'e.g. Rent June, Monthly Target'})),
    React.createElement('button',{className:'btn-p',onClick:submit},'Set Target')
  );
}

function TargetPage(){
  const store=useStore();const[showSet,setShowSet]=useState(false);
  const progress=store.getProgress(),current=store.getCurrentTotal(),remaining=store.getRemaining();
  const net=store.getNetMovement(),gross=store.getGrossMovement(),expenses=store.getTaskExpenses();
  const breakdown=store.getBreakdown(),creditPaid=store.getCreditPaid(),hasTarget=store.target.total>0;
  const completedMov=store.tasks.filter(t=>t.done&&t.movementType&&t.movementType!=='none');
  const pendingMov=store.tasks.filter(t=>!t.done&&t.movementType&&t.movementType!=='none');
  const projectedInflow=pendingMov.reduce((s,t)=>s+parseAmt(t.income)-parseAmt(t.expenses),0);
  const projectedTotal=current+projectedInflow;
  const projectedPct=store.target.total>0?Math.min(100,Math.round((projectedTotal/store.target.total)*100)):0;
  return React.createElement('div',{className:'sc',style:{flex:1}},
    React.createElement('div',{style:{padding:'8px 16px 40px'}},
      React.createElement('div',{style:{display:'flex',justifyContent:'flex-end',marginBottom:12}},React.createElement('button',{className:'btn-g',onClick:()=>setShowSet(true),style:{display:'flex',alignItems:'center',gap:5,fontSize:11}},'✏  ',hasTarget?'Edit Target':'Set Target')),
      !hasTarget?React.createElement(Card,null,React.createElement(EmptyState,{icon:'◎',title:'No target set',sub:'Set your total target and starting balance. The app automatically tracks progress from every completed movement task.',action:'Set Target',onAction:()=>setShowSet(true)})):
      React.createElement(React.Fragment,null,
        React.createElement(Card,{style:{marginBottom:12,background:'linear-gradient(135deg,var(--card),var(--card2))'}},
          React.createElement('div',{style:{display:'flex',justifyContent:'space-between',alignItems:'flex-start',marginBottom:16}},React.createElement('div',null,React.createElement('div',{className:'sl',style:{marginBottom:5}},store.target.label||'TARGET PROGRESS'),React.createElement('div',{className:'fm',style:{fontSize:30,fontWeight:700,color:'var(--text)',lineHeight:1}},fmt(current)),React.createElement('div',{className:'fm',style:{fontSize:10,color:'var(--muted)',marginTop:4}},'of ',fmt(store.target.total),' target')),React.createElement('div',{style:{textAlign:'right'}},React.createElement('div',{className:'fm',style:{fontSize:38,fontWeight:700,lineHeight:1,color:progress>=100?'var(--green)':'var(--accent)'}},progress,'%'),React.createElement('div',{className:'fm',style:{fontSize:9,color:'var(--muted)',marginTop:2}},progress>=100?'🎉 TARGET HIT!':'progress'))),
          React.createElement(ProgBar,{value:current,max:store.target.total,color:progress>=100?'var(--green)':'var(--accent)'}),
          React.createElement('div',{style:{display:'grid',gridTemplateColumns:'repeat(3,1fr)',gap:8,marginTop:14}},[{l:'Starting',v:fmt(store.target.startingBalance),c:'var(--green)'},{l:'Net Moved',v:fmt(net),c:'var(--accent)'},{l:'Remaining',v:fmt(remaining),c:'var(--red)'}].map(s=>React.createElement('div',{key:s.l,style:{background:'var(--card2)',borderRadius:9,padding:'9px 10px',border:'1px solid var(--border)',textAlign:'center'}},React.createElement('div',{className:'sl',style:{color:s.c,marginBottom:3}},s.l),React.createElement('div',{className:'fm',style:{fontSize:12,fontWeight:700,color:s.c}},s.v))))
        ),
        React.createElement(Card,{style:{marginBottom:12}},React.createElement('div',{className:'sl',style:{marginBottom:10}},'MOVEMENT SUMMARY'),React.createElement('div',{style:{display:'grid',gridTemplateColumns:'1fr 1fr',gap:8}},React.createElement(MiniStat,{label:'Gross Income',value:fmt(gross),color:'var(--green)',sub:completedMov.length+' movements'}),React.createElement(MiniStat,{label:'Task Expenses',value:fmt(expenses),color:'var(--red)',sub:'deducted from gross'}),React.createElement(MiniStat,{label:'Net Movement',value:fmt(net),color:net>=0?'var(--green)':'var(--red)',sub:'added to target'}),React.createElement(MiniStat,{label:'Credit Deducted',value:fmt(creditPaid),color:'var(--red)',sub:'paid credits'}))),
        projectedInflow>0&&React.createElement(Card,{style:{marginBottom:12,background:'var(--blue-dim)',borderColor:'rgba(91,155,213,.2)'}},React.createElement('div',{className:'sl',style:{color:'var(--blue)',marginBottom:8}},'PROJECTED — ',pendingMov.length,' PENDING TASKS'),React.createElement('div',{style:{display:'flex',justifyContent:'space-between',alignItems:'center',marginBottom:10}},React.createElement('div',{className:'fm',style:{fontSize:20,fontWeight:700,color:'var(--blue)'}},fmt(projectedTotal)),React.createElement('div',{className:'fm',style:{fontSize:16,fontWeight:700,color:'var(--blue)'}},projectedPct,'%')),React.createElement(ProgBar,{value:projectedTotal,max:store.target.total,color:'var(--blue)'}),React.createElement('div',{className:'fm',style:{fontSize:10,color:'var(--blue)',marginTop:8,opacity:.75,lineHeight:1.5}},'If all ',pendingMov.length,' pending tasks complete → ',fmt(projectedTotal),' (',projectedPct,'%)')),
        completedMov.length>0&&React.createElement(Card,{style:{marginBottom:12}},React.createElement('div',{className:'sl',style:{marginBottom:10}},'HOW MOVEMENT CAME IN'),MOVEMENT_TYPES.filter(m=>m.value!=='none').map(m=>{const b=breakdown[m.value];if(!b||b.count===0)return null;const p=current>0?Math.round((b.net/current)*100):0;return React.createElement('div',{key:m.value,style:{display:'flex',alignItems:'center',gap:10,padding:'9px 0',borderBottom:'1px solid var(--border)'}},React.createElement('div',{style:{width:30,height:30,borderRadius:8,flexShrink:0,background:m.bg,display:'flex',alignItems:'center',justifyContent:'center',fontSize:14}},m.icon),React.createElement('div',{style:{flex:1}},React.createElement('div',{style:{fontSize:12,fontWeight:600,color:'var(--text)'}},m.label),React.createElement('div',{className:'fm',style:{fontSize:9,color:'var(--muted)',marginTop:1}},b.count,' done · ',p,'% · exp ',fmt(b.expenses))),React.createElement('div',{style:{textAlign:'right',flexShrink:0}},React.createElement('div',{className:'fm',style:{fontSize:13,fontWeight:700,color:b.net>=0?m.color:'var(--red)'}},fmt(b.net)),React.createElement('div',{className:'fm',style:{fontSize:8,color:'var(--muted)'}},'net')))})),
        completedMov.length>0&&React.createElement(Card,null,React.createElement('div',{className:'sl',style:{marginBottom:10}},'COMPLETED MOVEMENT LOG'),[...completedMov].sort((a,b)=>new Date(b.completedAt||b.createdAt)-new Date(a.completedAt||a.createdAt)).map((t,i,arr)=>{const mv=getMvType(t.movementType),n=parseAmt(t.income)-parseAmt(t.expenses);return React.createElement('div',{key:t.id,style:{display:'flex',alignItems:'center',gap:10,padding:'9px 0',borderBottom:i<arr.length-1?'1px solid var(--border)':'none'}},React.createElement('span',{style:{fontSize:15,flexShrink:0}},mv.icon),React.createElement('div',{style:{flex:1,minWidth:0}},React.createElement('div',{style:{fontSize:12,fontWeight:500,color:'var(--text2)',lineHeight:1.3}},t.text),t.completedAt&&React.createElement('div',{className:'fm',style:{fontSize:8,color:'var(--muted)',marginTop:1}},fmtDate(t.completedAt))),React.createElement('div',{className:'fm',style:{fontSize:12,fontWeight:700,color:n>=0?'var(--green)':'var(--red)',flexShrink:0}},fmt(n)));})
        )
      )
    ),
    showSet&&React.createElement(SetTargetModal,{onClose:()=>setShowSet(false)})
  );
}

function AnalyticsPage(){
  const store=useStore();const[period,setPeriod]=useState('month');
  const now=new Date();
  const filteredTx=store.transactions.filter(t=>{const d=new Date(t.date);if(period==='week'){const m=new Date(now);m.setDate(now.getDate()-now.getDay()+1);m.setHours(0,0,0,0);return d>=m}if(period==='month')return d.getMonth()===now.getMonth()&&d.getFullYear()===now.getFullYear();if(period==='3m'){const s=new Date(now.getFullYear(),now.getMonth()-2,1);return d>=s}return true});
  const txIncome=filteredTx.filter(t=>t.type==='income').reduce((s,t)=>s+t.amount,0);
  const txExpense=filteredTx.filter(t=>t.type==='expense').reduce((s,t)=>s+t.amount,0);
  const completedMov=store.tasks.filter(t=>t.done&&t.movementType&&t.movementType!=='none');
  const netMovement=store.getNetMovement(),taskExpenses=store.getTaskExpenses();
  const breakdown=store.getBreakdown();
  const creditPaid=store.getCreditPaid(),creditOwed=store.getCreditOwed();
  const unifiedHistory=store.getUnifiedHistory();
  const barData=store.getMonthlyStats(6);
  const movPieData=MOVEMENT_TYPES.filter(m=>m.value!=='none').map(m=>{const b=breakdown[m.value];return b?.net>0?{name:m.label,value:b.net,fill:m.color}:null}).filter(Boolean);
  const expCats={};filteredTx.filter(t=>t.type==='expense').forEach(t=>{expCats[t.category||'other']=(expCats[t.category||'other']||0)+t.amount});
  const expPieData=Object.entries(expCats).map(([name,value],i)=>({name:name.charAt(0).toUpperCase()+name.slice(1),value,fill:['#d4a843','#4ecb7f','#5b9bd5','#e05252','#a78bfa','#f59e0b','#10b981'][i%7]}));
  const hasBars=barData.some(d=>d.income>0||d.expense>0);
  const hasData=store.tasks.length>0||store.transactions.length>0;
  const tProgress=store.getProgress(),tCurrent=store.getCurrentTotal();
  const pendMovCount=store.tasks.filter(t=>!t.done&&t.movementType&&t.movementType!=='none').length;
  const pendMovValue=store.tasks.filter(t=>!t.done&&t.movementType&&t.movementType!=='none').reduce((s,t)=>s+parseAmt(t.income)-parseAmt(t.expenses),0);
  if(!hasData)return React.createElement('div',{className:'sc',style:{flex:1,padding:'0 16px'}},React.createElement(EmptyState,{icon:'▲',title:'No data yet',sub:'Add tasks with movements and log transactions to see analytics.'}));
  const TT=({active,payload,label})=>{if(!active||!payload?.length)return null;return React.createElement('div',{style:{background:'var(--card2)',border:'1px solid var(--border2)',borderRadius:8,padding:'8px 12px',fontSize:11,fontFamily:'DM Mono,monospace'}},label&&React.createElement('div',{style:{color:'var(--accent)',fontWeight:700,marginBottom:4}},label),payload.map((p,i)=>React.createElement('div',{key:i,style:{color:p.color,display:'flex',gap:8}},React.createElement('span',null,p.name,':'),React.createElement('span',null,fmt(p.value)))))};
  const hasCharts=typeof BarChart!=='undefined';
  return React.createElement('div',{className:'sc',style:{flex:1}},
    React.createElement('div',{style:{display:'flex',gap:6,padding:'8px 16px 12px',overflowX:'auto'}},[{v:'week',l:'Week'},{v:'month',l:'Month'},{v:'3m',l:'3 Months'},{v:'all',l:'All'}].map(p=>React.createElement('button',{key:p.v,className:`chip ${period===p.v?'on':''}`,onClick:()=>setPeriod(p.v)},p.l))),
    React.createElement('div',{style:{display:'grid',gridTemplateColumns:'1fr 1fr',gap:8,padding:'0 16px 12px'}},React.createElement(StatCard,{label:'Net Movement',value:fmt(netMovement),color:netMovement>=0?'var(--green)':'var(--red)',sub:`${completedMov.length} movements`}),React.createElement(StatCard,{label:'TX Income',value:fmt(txIncome),color:'var(--green)',sub:`${filteredTx.filter(t=>t.type==='income').length} tx`}),React.createElement(StatCard,{label:'All Expenses',value:fmt(txExpense+taskExpenses),color:'var(--red)',sub:'tx + task expenses'}),React.createElement(StatCard,{label:'Credit Paid',value:fmt(creditPaid),color:'var(--red)',sub:`${fmt(creditOwed)} outstanding`})),
    tProgress>0&&React.createElement('div',{style:{margin:'0 16px 12px'}},React.createElement(Card,{style:{background:'linear-gradient(135deg,rgba(212,168,67,.05),rgba(212,168,67,.01))',borderColor:'rgba(212,168,67,.18)'}},React.createElement('div',{className:'sl',style:{color:'var(--accent)',marginBottom:10}},'TARGET ANALYTICS'),React.createElement('div',{style:{display:'grid',gridTemplateColumns:'1fr 1fr',gap:8}},[{l:'Confirmed',v:fmt(tCurrent),c:'var(--green)'},{l:'Progress',v:`${tProgress}%`,c:'var(--accent)'},{l:'Projected',v:fmt(pendMovValue),c:'var(--blue)'},{l:'Credit Left',v:fmt(creditOwed),c:'var(--red)'}].map(s=>React.createElement('div',{key:s.l,style:{background:'var(--card2)',borderRadius:9,padding:'9px 11px',border:'1px solid var(--border)'}},React.createElement('div',{className:'sl',style:{color:s.c,marginBottom:3}},s.l),React.createElement('div',{className:'fm',style:{fontSize:14,fontWeight:700,color:s.c}},s.v)))),pendMovCount>0&&React.createElement('div',{className:'fm',style:{fontSize:10,color:'var(--blue)',marginTop:10,lineHeight:1.5}},pendMovCount,' pending movement tasks will add ',fmt(pendMovValue),' if completed.'))),
    hasBars&&hasCharts&&React.createElement('div',{style:{margin:'0 16px 12px'}},React.createElement(Card,null,React.createElement('div',{className:'sl',style:{marginBottom:12}},'6-MONTH INCOME VS EXPENSES'),React.createElement(ResponsiveContainer,{width:'100%',height:170},React.createElement(BarChart,{data:barData,margin:{top:5,right:5,bottom:0,left:0}},React.createElement(XAxis,{dataKey:'month',tick:{fill:'var(--muted)',fontSize:10},axisLine:false,tickLine:false}),React.createElement(YAxis,{tick:{fill:'var(--muted)',fontSize:9},axisLine:false,tickLine:false,tickFormatter:v=>v>=1000?`₦${(v/1000).toFixed(0)}k`:`₦${v}`,width:42}),React.createElement(Tooltip,{content:TT,cursor:{fill:'rgba(255,255,255,.03)'}}),React.createElement(Bar,{dataKey:'income',name:'Income',fill:'#4ecb7f',radius:[3,3,0,0],maxBarSize:16}),React.createElement(Bar,{dataKey:'expense',name:'Expense',fill:'#e05252',radius:[3,3,0,0],maxBarSize:16}))))),
    hasBars&&hasCharts&&React.createElement('div',{style:{margin:'0 16px 12px'}},React.createElement(Card,null,React.createElement('div',{className:'sl',style:{marginBottom:12}},'NET PROFIT TREND'),React.createElement(ResponsiveContainer,{width:'100%',height:130},React.createElement(AreaChart,{data:barData,margin:{top:5,right:5,bottom:0,left:0}},React.createElement('defs',null,React.createElement('linearGradient',{id:'ng',x1:'0',y1:'0',x2:'0',y2:'1'},React.createElement('stop',{offset:'5%',stopColor:'#d4a843',stopOpacity:0.15}),React.createElement('stop',{offset:'95%',stopColor:'#d4a843',stopOpacity:0}))),React.createElement(CartesianGrid,{strokeDasharray:'3 3',stroke:'rgba(255,255,255,.04)'}),React.createElement(XAxis,{dataKey:'month',tick:{fill:'var(--muted)',fontSize:10},axisLine:false,tickLine:false}),React.createElement(YAxis,{tick:{fill:'var(--muted)',fontSize:9},axisLine:false,tickLine:false,tickFormatter:v=>`₦${(v/1000).toFixed(0)}k`,width:40}),React.createElement(Tooltip,{content:TT}),React.createElement(Area,{type:'monotone',dataKey:'net',name:'Net',stroke:'#d4a843',fill:'url(#ng)',strokeWidth:2,dot:{fill:'#d4a843',r:3}}))))),
    movPieData.length>0&&hasCharts&&React.createElement('div',{style:{margin:'0 16px 12px'}},React.createElement(Card,null,React.createElement('div',{className:'sl',style:{marginBottom:12}},'MOVEMENT BREAKDOWN (NET)'),React.createElement(ResponsiveContainer,{width:'100%',height:190},React.createElement(PieChart,null,React.createElement(Pie,{data:movPieData,cx:'50%',cy:'50%',innerRadius:48,outerRadius:75,paddingAngle:3,dataKey:'value'},movPieData.map((e,i)=>React.createElement(Cell,{key:i,fill:e.fill}))),React.createElement(Legend,{formatter:v=>React.createElement('span',{style:{fontSize:10,color:'var(--text2)',fontFamily:'DM Mono,monospace'}},v)}),React.createElement(Tooltip,{formatter:v=>fmt(v),contentStyle:{background:'var(--card2)',border:'1px solid var(--border)',borderRadius:8,fontSize:11}}))))),
    expPieData.length>0&&hasCharts&&React.createElement('div',{style:{margin:'0 16px 12px'}},React.createElement(Card,null,React.createElement('div',{className:'sl',style:{marginBottom:12}},'EXPENSE CATEGORIES'),React.createElement(ResponsiveContainer,{width:'100%',height:190},React.createElement(PieChart,null,React.createElement(Pie,{data:expPieData,cx:'50%',cy:'50%',outerRadius:72,paddingAngle:3,dataKey:'value'},expPieData.map((e,i)=>React.createElement(Cell,{key:i,fill:e.fill}))),React.createElement(Legend,{formatter:v=>React.createElement('span',{style:{fontSize:10,color:'var(--text2)',fontFamily:'DM Mono,monospace'}},v)}),React.createElement(Tooltip,{formatter:v=>fmt(v),contentStyle:{background:'var(--card2)',border:'1px solid var(--border)',borderRadius:8,fontSize:11}}))))),
    store.tasks.length>0&&React.createElement('div',{style:{margin:'0 16px 12px'}},React.createElement(Card,null,React.createElement('div',{className:'sl',style:{marginBottom:10}},'TASK ANALYTICS'),React.createElement('div',{style:{display:'grid',gridTemplateColumns:'repeat(3,1fr)',gap:8,marginBottom:8}},[{l:'Total',v:store.tasks.length,c:'var(--text)'},{l:'Done',v:store.tasks.filter(t=>t.done).length,c:'var(--green)'},{l:'Pending',v:store.tasks.filter(t=>!t.done).length,c:'var(--accent)'},{l:'Urgent',v:store.tasks.filter(t=>t.urgent&&!t.done).length,c:'var(--red)'},{l:'w/Move',v:store.tasks.filter(t=>t.movementType&&t.movementType!=='none').length,c:'var(--blue)'},{l:'MoveDone',v:store.tasks.filter(t=>t.done&&t.movementType&&t.movementType!=='none').length,c:'var(--green)'}].map(s=>React.createElement('div',{key:s.l,style:{background:'var(--card2)',borderRadius:9,padding:'9px 8px',border:'1px solid var(--border)',textAlign:'center'}},React.createElement('div',{className:'fm',style:{fontSize:18,fontWeight:700,color:s.c}},s.v),React.createElement('div',{className:'sl',style:{marginTop:2}},s.l)))),React.createElement('div',{style:{display:'flex',alignItems:'center',gap:8}},React.createElement('div',{style:{flex:1,background:'var(--border2)',height:6,borderRadius:6,overflow:'hidden'}},React.createElement('div',{style:{height:'100%',width:`${store.tasks.length>0?Math.round((store.tasks.filter(t=>t.done).length/store.tasks.length)*100):0}%`,background:'var(--green)',borderRadius:6,transition:'width .6s ease'}})),React.createElement('div',{className:'fm',style:{fontSize:11,fontWeight:700,color:'var(--green)',flexShrink:0}},store.tasks.length>0?Math.round((store.tasks.filter(t=>t.done).length/store.tasks.length)*100):0,'% done')))),
    store.credits.length>0&&React.createElement('div',{style:{margin:'0 16px 12px'}},React.createElement(Card,null,React.createElement('div',{className:'sl',style:{marginBottom:10}},'CREDIT ANALYSIS'),React.createElement('div',{style:{display:'grid',gridTemplateColumns:'1fr 1fr',gap:8,marginBottom:12}},React.createElement(MiniStat,{label:'Total Owed',value:fmt(creditOwed),color:'var(--red)',sub:`${store.credits.filter(c=>!c.paid).length} outstanding`}),React.createElement(MiniStat,{label:'Total Paid',value:fmt(creditPaid),color:'var(--green)',sub:`${store.credits.filter(c=>c.paid).length} cleared`}),React.createElement(MiniStat,{label:'Repayment',value:fmt(store.credits.filter(c=>c.category==='repayment'&&!c.paid).reduce((s,c)=>s+c.amount,0)),color:'var(--red)',sub:'outstanding'}),React.createElement(MiniStat,{label:'Personal',value:fmt(store.credits.filter(c=>c.category==='personal'&&!c.paid).reduce((s,c)=>s+c.amount,0)),color:'var(--accent)',sub:'outstanding'})),store.credits.filter(c=>c.priority&&!c.paid).length>0&&React.createElement('div',{style:{background:'var(--red-dim)',borderRadius:9,padding:'9px 12px',border:'1px solid rgba(224,82,82,.2)'}},React.createElement('div',{className:'sl',style:{color:'var(--red)',marginBottom:3}},'PRIORITY OUTSTANDING'),React.createElement('div',{className:'fm',style:{fontSize:16,fontWeight:700,color:'var(--red)'}},fmt(store.credits.filter(c=>c.priority&&!c.paid).reduce((s,c)=>s+c.amount,0)))))),
    unifiedHistory.length>0&&React.createElement('div',{style:{margin:'0 16px 12px'}},React.createElement(Card,null,React.createElement('div',{className:'sl',style:{marginBottom:10}},'UNIFIED HISTORY (',unifiedHistory.length,' events)'),React.createElement('div',{style:{maxHeight:280,overflowY:'auto'}},unifiedHistory.slice(0,20).map((ev,i)=>{const tc={movement:{color:'var(--green)',icon:'⚡'},income:{color:'var(--green)',icon:'↑'},expense:{color:'var(--red)',icon:'↓'},'credit-paid':{color:'var(--red)',icon:'💳'}}[ev.type]||{color:'var(--muted)',icon:'·'};return React.createElement('div',{key:ev.id+i,style:{display:'flex',alignItems:'flex-start',gap:10,padding:'9px 0',borderBottom:i<Math.min(unifiedHistory.length,20)-1?'1px solid var(--border)':'none'}},React.createElement('div',{style:{width:28,height:28,borderRadius:8,flexShrink:0,background:`${tc.color}18`,display:'flex',alignItems:'center',justifyContent:'center',fontSize:13}},tc.icon),React.createElement('div',{style:{flex:1,minWidth:0}},React.createElement('div',{style:{fontSize:12,fontWeight:600,color:'var(--text)',lineHeight:1.25}},ev.label),React.createElement('div',{className:'fm',style:{fontSize:8,color:'var(--muted)',marginTop:2}},ev.subtype?ev.subtype.toUpperCase():ev.type.toUpperCase(),' · ',ev.source.toUpperCase(),' · ',new Date(ev.date).toLocaleDateString())),React.createElement('div',{className:'fm',style:{fontSize:12,fontWeight:700,color:ev.net>=0?'var(--green)':'var(--red)',flexShrink:0}},ev.net>=0?'+':'',fmt(ev.net)));}),unifiedHistory.length>20&&React.createElement('div',{className:'fm',style:{fontSize:10,color:'var(--muted)',textAlign:'center',padding:'8px 0'}},'Showing 20 of ',unifiedHistory.length,' events')))),
    React.createElement('div',{style:{margin:'0 16px 40px'}},React.createElement(Card,{style:{background:'linear-gradient(135deg,rgba(212,168,67,.06),rgba(212,168,67,.02))',borderColor:'rgba(212,168,67,.15)'}},React.createElement('div',{className:'sl',style:{color:'var(--accent)',marginBottom:10}},'SMART INSIGHTS'),[netMovement>0&&{icon:'💰',text:`Net movement of ${fmt(netMovement)} from ${completedMov.length} completed tasks.`},netMovement<0&&{icon:'⚠️',text:`Net movement is negative (${fmt(netMovement)}). Review expenses.`},creditOwed>0&&{icon:'💳',text:`${fmt(creditOwed)} in outstanding credit reduces your balance when paid.`},taskExpenses>0&&{icon:'📉',text:`${fmt(taskExpenses)} in task-linked expenses deducted from gross.`},expPieData[0]&&{icon:'📊',text:`Top expense: ${expPieData[0].name} at ${fmt(expPieData[0].value)}.`},movPieData[0]&&{icon:'⚡',text:`Top movement: ${movPieData[0].name} — ${fmt(movPieData[0].value)} net.`}].filter(Boolean).slice(0,6).map((ins,i,arr)=>React.createElement('div',{key:i,style:{fontSize:12,color:'var(--text)',padding:'6px 0',borderBottom:i<arr.length-1?'1px solid var(--border)':'none',lineHeight:1.5}},React.createElement('span',{style:{marginRight:7}},ins.icon),ins.text))))
  );
}

function BusinessModal({biz,onClose}){
  const store=useStore();const{push}=useNotif();
  const isEdit=!!biz;
  const BIZ_COLORS=['#d4a843','#4ecb7f','#5b9bd5','#e05252','#a78bfa','#f59e0b','#10b981','#6366f1'];
  const [name,setName]=useState(biz?.name??'');
  const [type,setType]=useState(biz?.type??'general');
  const [color,setColor]=useState(biz?.color??BIZ_COLORS[0]);
  const [note,setNote]=useState(biz?.note??'');
  const submit=()=>{
    if(!name.trim())return push('Business name required','error');
    if(isEdit){store.updateBusiness(biz.id,{name,type,color,note});push('Business updated','success')}
    else{store.addBusiness({name,type,color,note});push(`Business added: ${name}`,'success')}
    onClose();
  };
  return React.createElement(ModalSheet,{title:isEdit?'EDIT BUSINESS':'ADD BUSINESS',onClose},
    React.createElement(Field,{label:'Business Name'},React.createElement('input',{value:name,onChange:e=>setName(e.target.value),placeholder:'e.g. Coco Nails, C.Closet...',autoFocus:true})),
    React.createElement(Field,{label:'Type'},React.createElement('select',{value:type,onChange:e=>setType(e.target.value)},[{v:'nails',l:'Nails'},{v:'clothing',l:'Clothing/Fashion'},{v:'salon',l:'Salon/Beauty'},{v:'services',l:'Services'},{v:'retail',l:'Retail'},{v:'food',l:'Food'},{v:'tech',l:'Tech/Digital'},{v:'general',l:'General'}].map(t=>React.createElement('option',{key:t.v,value:t.v},t.l)))),
    React.createElement(Field,{label:'Color'},React.createElement('div',{style:{display:'flex',gap:8,flexWrap:'wrap',padding:'4px 0'}},BIZ_COLORS.map(c=>React.createElement('div',{key:c,onClick:()=>setColor(c),style:{width:26,height:26,borderRadius:'50%',background:c,cursor:'pointer',border:color===c?'3px solid #fff':'3px solid transparent',boxSizing:'border-box',transition:'border .15s'}})))),
    React.createElement(Field,{label:'Note (optional)'},React.createElement('textarea',{value:note,onChange:e=>setNote(e.target.value),rows:2,placeholder:'Location, description...'})),
    React.createElement('button',{className:'btn-p',onClick:submit},isEdit?'Save Changes':'+ Add Business')
  );
}

function BusinessesPage(){
  const store=useStore();const{push}=useNotif();
  const [showAdd,setShowAdd]=useState(false);const [editBiz,setEditBiz]=useState(null);
  const totalIncome=store.businesses.reduce((s,biz)=>s+store.getBizStats(biz.id).income,0);
  const totalExpense=store.businesses.reduce((s,biz)=>s+store.getBizStats(biz.id).expense,0);
  return React.createElement('div',{className:'sc',style:{flex:1}},
    store.businesses.length>0&&React.createElement('div',{style:{display:'grid',gridTemplateColumns:'1fr 1fr',gap:8,padding:'8px 16px 12px'}},React.createElement(MiniStat,{label:'Total Income',value:fmt(totalIncome),color:'var(--green)',sub:`${store.businesses.length} businesses`}),React.createElement(MiniStat,{label:'Total Expense',value:fmt(totalExpense),color:'var(--red)',sub:'all businesses'})),
    React.createElement('div',{style:{padding:store.businesses.length>0?'0 16px 12px':'8px 16px 12px'}},React.createElement('button',{className:'btn-p',onClick:()=>setShowAdd(true),style:{display:'flex',alignItems:'center',justifyContent:'center',gap:6}},'+  Add Business')),
    React.createElement('div',{style:{padding:'0 16px 40px'}},
      store.businesses.length===0?React.createElement(EmptyState,{icon:'⬡',title:'No businesses yet',sub:'Add your businesses to track income and expenses per brand.',action:'Add Business',onAction:()=>setShowAdd(true)}):
      store.businesses.map(biz=>{
        const stats=store.getBizStats(biz.id);
        return React.createElement(Card,{key:biz.id,style:{marginBottom:12,borderLeft:`3px solid ${biz.color||'var(--accent)'}`}},
          React.createElement('div',{style:{display:'flex',justifyContent:'space-between',alignItems:'flex-start',marginBottom:12}},
            React.createElement('div',{style:{display:'flex',alignItems:'center',gap:10}},React.createElement('div',{style:{width:36,height:36,borderRadius:10,background:`${biz.color||'var(--accent)'}22`,display:'flex',alignItems:'center',justifyContent:'center',fontSize:16}},biz.type==='nails'?'💅':biz.type==='clothing'?'👗':biz.type==='salon'?'✂':'🏢'),React.createElement('div',null,React.createElement('div',{style:{fontSize:15,fontWeight:700,color:'var(--text)'}},biz.name),React.createElement('div',{className:'sl',style:{marginTop:2,color:biz.color}},biz.type.toUpperCase()))),
            React.createElement('div',{style:{display:'flex',gap:4}},React.createElement('button',{onClick:()=>setEditBiz(biz),style:{background:'none',border:'none',color:'var(--muted)',padding:'4px 5px',fontSize:12}},'✏'),React.createElement('button',{onClick:()=>{if(confirm(`Delete "${biz.name}"?`)){store.deleteBusiness(biz.id);push('Business deleted','info')}},style:{background:'none',border:'none',color:'var(--red)',opacity:.6,padding:'4px 5px',fontSize:14}},'×'))
          ),
          biz.note&&React.createElement('div',{style:{fontSize:11,color:'var(--muted)',fontStyle:'italic',marginBottom:12}},biz.note),
          React.createElement('div',{style:{display:'grid',gridTemplateColumns:'repeat(3,1fr)',gap:8}},React.createElement(MiniStat,{label:'Income',value:fmt(stats.income),color:'var(--green)',sub:'tx+movements'}),React.createElement(MiniStat,{label:'Expense',value:fmt(stats.expense),color:'var(--red)',sub:'tx+task exp'}),React.createElement(MiniStat,{label:'Net',value:fmt(stats.net),color:stats.net>=0?'var(--green)':'var(--red)',sub:stats.net>=0?'profit':'loss'})),
          stats.movCount>0&&React.createElement('div',{className:'fm',style:{fontSize:10,color:'var(--muted)',marginTop:10}},stats.movCount,' linked movement',stats.movCount!==1?'s':'',' completed')
        );
      })
    ),
    showAdd&&React.createElement(BusinessModal,{onClose:()=>setShowAdd(false)}),
    editBiz&&React.createElement(BusinessModal,{biz:editBiz,onClose:()=>setEditBiz(null)})
  );
}

function DeadlineModal({onClose}){
  const store=useStore();const{push}=useNotif();
  const [form,setForm]=useState({title:'',date:'',amount:'',category:'general',urgent:false,note:''});
  const set=(k,v)=>setForm(f=>({...f,[k]:v}));
  const submit=()=>{if(!form.title||!form.date)return push('Title and date required','error');store.addDeadline(form);push(`Deadline added: ${form.title}`,'success');onClose()};
  return React.createElement(ModalSheet,{title:'ADD DEADLINE',onClose},
    React.createElement(Field,{label:'Title'},React.createElement('input',{value:form.title,onChange:e=>set('title',e.target.value),placeholder:'e.g. Pay rent, Client delivery...',autoFocus:true})),
    React.createElement(R2,null,React.createElement('div',{style:{flex:1}},React.createElement(Field,{label:'Date'},React.createElement('input',{type:'date',value:form.date,onChange:e=>set('date',e.target.value)}))),React.createElement('div',{style:{flex:1}},React.createElement(Field,{label:'Amount (optional)'},React.createElement('input',{type:'number',value:form.amount,onChange:e=>set('amount',e.target.value),placeholder:'₦'})))),
    React.createElement(Field,{label:'Category'},React.createElement('select',{value:form.category,onChange:e=>set('category',e.target.value)},[{v:'payment',l:'Payment'},{v:'delivery',l:'Delivery'},{v:'submission',l:'Submission'},{v:'meeting',l:'Meeting'},{v:'general',l:'General'},{v:'personal',l:'Personal'},{v:'business',l:'Business'}].map(c=>React.createElement('option',{key:c.v,value:c.v},c.l)))),
    React.createElement('div',{style:{display:'flex',alignItems:'center',gap:10,marginBottom:14}},React.createElement('input',{type:'checkbox',id:'dl-urg',checked:form.urgent,onChange:e=>set('urgent',e.target.checked),style:{width:'auto',margin:0}}),React.createElement('label',{htmlFor:'dl-urg',style:{fontSize:13,color:'var(--text)',cursor:'pointer'}},'Mark as urgent')),
    React.createElement(Field,{label:'Note (optional)'},React.createElement('textarea',{value:form.note,onChange:e=>set('note',e.target.value),rows:2})),
    React.createElement('button',{className:'btn-p',onClick:submit},'+ Add Deadline')
  );
}

function DeadlinesPage(){
  const store=useStore();const{push}=useNotif();
  const [showAdd,setShowAdd]=useState(false);const [filter,setFilter]=useState('pending');
  const pending=store.deadlines.filter(d=>!d.done),done=store.deadlines.filter(d=>d.done);
  const overdue=pending.filter(d=>getDaysUntil(d.date)!==null&&getDaysUntil(d.date)<0);
  const todayDl=pending.filter(d=>getDaysUntil(d.date)===0);
  const sorted=[...store.deadlines].sort((a,b)=>{if(a.done!==b.done)return a.done?1:-1;return(getDaysUntil(a.date)??9999)-(getDaysUntil(b.date)??9999)});
  const filtered=filter==='pending'?sorted.filter(d=>!d.done):filter==='overdue'?sorted.filter(d=>!d.done&&getDaysUntil(d.date)!==null&&getDaysUntil(d.date)<0):filter==='urgent'?sorted.filter(d=>!d.done&&(d.urgent||(getDaysUntil(d.date)!==null&&getDaysUntil(d.date)<=3))):sorted.filter(d=>d.done);
  return React.createElement('div',{className:'sc',style:{flex:1}},
    pending.length>0&&React.createElement('div',{style:{display:'flex',gap:8,padding:'8px 16px 12px',overflowX:'auto'}},[{l:'Overdue',v:overdue.length,c:'var(--red)'},{l:'Today',v:todayDl.length,c:'var(--accent)'},{l:'Pending',v:pending.length,c:'var(--text)'},{l:'Done',v:done.length,c:'var(--green)'}].map(s=>React.createElement('div',{key:s.l,style:{flexShrink:0,background:'var(--card)',border:'1px solid var(--border)',borderRadius:10,padding:'8px 13px',minWidth:72,textAlign:'center'}},React.createElement('div',{className:'fm',style:{fontSize:18,fontWeight:700,color:s.c}},s.v),React.createElement('div',{className:'sl',style:{marginTop:2}},s.l)))),
    React.createElement('div',{style:{padding:pending.length>0?'0 16px 10px':'8px 16px 10px'}},React.createElement('button',{className:'btn-p',onClick:()=>setShowAdd(true),style:{display:'flex',alignItems:'center',justifyContent:'center',gap:6}},'+  Add Deadline')),
    React.createElement('div',{style:{display:'flex',gap:6,padding:'0 16px',marginBottom:12,overflowX:'auto'}},[{v:'pending',l:`Pending(${pending.length})`},{v:'overdue',l:`Overdue(${overdue.length})`},{v:'urgent',l:'Urgent'},{v:'done',l:`Done(${done.length})`}].map(f=>React.createElement('button',{key:f.v,className:`chip ${filter===f.v?'on':''}`,onClick:()=>setFilter(f.v)},f.l))),
    React.createElement('div',{style:{padding:'0 16px 40px'}},
      filtered.length===0?React.createElement(EmptyState,{icon:'◷',title:'No deadlines',sub:'Add payment deadlines and important upcoming dates.'}):
      React.createElement(Card,{style:{padding:'4px 14px'}},
        filtered.map((d,i)=>{
          const dl=getDaysUntil(d.date),isOverdue=!d.done&&dl!==null&&dl<0,isToday=dl===0,isUrgent=!d.done&&(d.urgent||(dl!==null&&dl<=3));
          const urgColor=d.done?'var(--green)':isOverdue?'var(--red)':isToday?'var(--accent)':dl!==null&&dl<=7?'var(--accent)':'var(--muted)';
          return React.createElement('div',{key:d.id,style:{display:'flex',alignItems:'flex-start',gap:10,padding:'12px 0',borderBottom:i<filtered.length-1?'1px solid var(--border)':'none',opacity:d.done?.55:1}},
            React.createElement('button',{onClick:()=>{store.toggleDeadline(d.id);push(d.done?'Reopened':'Completed','success')},style:{background:'none',border:'none',padding:'2px 0',flexShrink:0,marginTop:1,fontSize:19,lineHeight:1,color:d.done?'var(--green)':isOverdue?'var(--red)':'var(--muted)'}},d.done?'☑':'☐'),
            React.createElement('div',{style:{flex:1,minWidth:0}},
              React.createElement('div',{style:{display:'flex',alignItems:'center',gap:5,marginBottom:3}},isOverdue&&!d.done&&React.createElement('span',{style:{fontSize:11,color:'var(--red)'}},'⚠'),isToday&&!d.done&&React.createElement('span',{style:{fontSize:11,color:'var(--accent)'}},'⏰'),React.createElement('div',{style:{fontSize:14,fontWeight:isUrgent?700:500,color:d.done?'var(--muted)':isOverdue?'var(--red)':'var(--text)',textDecoration:d.done?'line-through':'none'}},d.title)),
              React.createElement('div',{style:{display:'flex',gap:6,flexWrap:'wrap',alignItems:'center'}},React.createElement('span',{style:{fontSize:8,padding:'2px 7px',borderRadius:7,background:'var(--card2)',color:'var(--muted)',fontFamily:'DM Mono,monospace',fontWeight:700,textTransform:'uppercase'}},d.category),React.createElement('span',{className:'fm',style:{fontSize:9,color:urgColor,fontWeight:dl!==null&&dl<=3?700:400}},d.done?`Done · ${fmtDate(d.date)}`:isOverdue?`OVERDUE — ${fmtDate(d.date)}`:isToday?'DUE TODAY':`${fmtDate(d.date)}${dl!==null?` · ${dl}d`:''}`)),
              d.note&&React.createElement('div',{style:{fontSize:11,color:'var(--muted)',marginTop:3,fontStyle:'italic'}},d.note)
            ),
            React.createElement('div',{style:{textAlign:'right',flexShrink:0}},d.amount>0&&React.createElement('div',{className:'fm',style:{fontSize:13,fontWeight:700,color:'var(--accent)'}},fmt(d.amount)),React.createElement('button',{onClick:()=>{if(confirm('Delete?')){store.deleteDeadline(d.id);push('Deleted','info')}},style:{background:'none',border:'none',color:'var(--red)',opacity:.5,padding:'2px 0',marginTop:2,fontSize:12}},'×'))
          );
        })
      )
    ),
    showAdd&&React.createElement(DeadlineModal,{onClose:()=>setShowAdd(false)})
  );
}

function SettingsPage(){
  const store=useStore();const{push}=useNotif();const{navigate}=useNav();
  const [confirmReset,setConfirmReset]=useState(false);const [resetText,setResetText]=useState('');
  const FONT_SIZES=[{v:'sm',l:'Small',size:'12px'},{v:'md',l:'Medium',size:'15px'},{v:'lg',l:'Large',size:'18px'},{v:'xl',l:'X-Large',size:'22px'}];
  const THEMES_LIST=[
    {v:'default',l:'Default',   desc:'Dark gold — classic',     swatch:'linear-gradient(135deg,#0a0a0b 50%,#d4a843 100%)'},
    {v:'light',  l:'Light',    desc:'Clean light mode',        swatch:'linear-gradient(135deg,#f5f0ea 50%,#b8860b 100%)'},
    {v:'dark',   l:'Dark',     desc:'Pure black minimal',      swatch:'linear-gradient(135deg,#000 50%,#e0e0e0 100%)'},
    {v:'chatgpt',l:'ChatGPT',  desc:'Blue-purple dark',        swatch:'linear-gradient(135deg,#0d0e12 50%,#7c6aff 100%)'},
  ];
  const totalEntries=store.tasks.length+store.transactions.length+store.credits.length+store.deadlines.length+store.businesses.length;
  const handleReset=()=>{
    if(resetText!=='RESET')return push('Type RESET to confirm','error');
    store.resetAll();push('All data cleared.','info',4000);
    setConfirmReset(false);setResetText('');navigate('home');
  };
  const handleExport=()=>{
    const data={tasks:store.tasks,transactions:store.transactions,credits:store.credits,deadlines:store.deadlines,businesses:store.businesses,target:store.target,settings:store.settings,exportedAt:new Date().toISOString()};
    const blob=new Blob([JSON.stringify(data,null,2)],{type:'application/json'});
    const url=URL.createObjectURL(blob);const a=document.createElement('a');
    a.href=url;a.download=`cole-os-backup-${todayStr()}.json`;a.click();URL.revokeObjectURL(url);
    push('Data exported as JSON','success');
  };
  const curTheme=store.settings.theme||'default';
  const curFs=store.settings.fontSize||'md';
  return React.createElement('div',{className:'sc',style:{flex:1}},
    React.createElement('div',{style:{padding:'8px 16px 40px'}},
      React.createElement('div',{style:{marginBottom:16}},
        React.createElement('div',{className:'sl',style:{marginBottom:8}},'PROFILE'),
        React.createElement(Card,null,React.createElement(Field,{label:'Your Name'},React.createElement('input',{value:store.settings.userName||'',onChange:e=>store.updateSettings({userName:e.target.value}),placeholder:'Cole, Gbemi...'})),React.createElement('div',{style:{fontSize:11,color:'var(--muted)',marginTop:-6}},'Shown in greeting and workspace header'))
      ),
      React.createElement('div',{style:{marginBottom:16}},
        React.createElement('div',{className:'sl',style:{marginBottom:8}},'APPEARANCE'),
        React.createElement(Card,null,
          React.createElement('div',{style:{display:'grid',gridTemplateColumns:'1fr 1fr',gap:10,marginBottom:0}},
            THEMES_LIST.map(t=>React.createElement('button',{
              key:t.v,
              onClick:()=>{store.updateSettings({theme:t.v});applyTheme(t.v);push(`Theme: ${t.l}`,'success',1500)},
              style:{border:'2px solid',borderColor:curTheme===t.v?'var(--accent)':'var(--border2)',background:curTheme===t.v?'var(--accent-dim)':'var(--card2)',borderRadius:12,padding:'10px 10px',cursor:'pointer',transition:'all .15s',textAlign:'left'}
            },
              React.createElement('div',{style:{width:'100%',height:30,borderRadius:7,background:t.swatch,marginBottom:8}}),
              React.createElement('div',{style:{fontSize:12,fontWeight:700,color:curTheme===t.v?'var(--accent)':'var(--text)',marginBottom:2}},t.l),
              React.createElement('div',{style:{fontSize:9,color:'var(--muted)',fontFamily:'DM Mono,monospace'}},t.desc)
            ))
          )
        )
      ),
      React.createElement('div',{style:{marginBottom:16}},
        React.createElement('div',{className:'sl',style:{marginBottom:8}},'TEXT SIZE'),
        React.createElement(Card,null,
          React.createElement('div',{style:{display:'grid',gridTemplateColumns:'repeat(4,1fr)',gap:8}},
            FONT_SIZES.map(f=>React.createElement('button',{
              key:f.v,
              onClick:()=>{store.updateSettings({fontSize:f.v});applyFontSize(f.v);push(`Text size: ${f.l}`,'success',1500)},
              style:{border:'2px solid',borderColor:curFs===f.v?'var(--accent)':'var(--border2)',background:curFs===f.v?'var(--accent-dim)':'var(--card2)',borderRadius:10,padding:'10px 4px',cursor:'pointer',transition:'all .15s',display:'flex',flexDirection:'column',alignItems:'center',gap:5}
            },
              React.createElement('span',{style:{fontFamily:'DM Sans,sans-serif',fontSize:f.size,fontWeight:700,color:curFs===f.v?'var(--accent)':'var(--text2)',lineHeight:1}},'Aa'),
              React.createElement('span',{style:{fontSize:9,fontFamily:'DM Mono,monospace',fontWeight:600,color:curFs===f.v?'var(--accent)':'var(--muted)',letterSpacing:1,textTransform:'uppercase'}},f.l)
            ))
          ),
          React.createElement('div',{style:{fontSize:11,color:'var(--muted)',marginTop:12}},'Current: ',React.createElement('strong',{style:{color:'var(--accent)'}},FONT_SIZES.find(f=>f.v===curFs)?.l,' (',FONT_SIZES.find(f=>f.v===curFs)?.size,')'))
        )
      ),
      React.createElement('div',{style:{marginBottom:16}},
        React.createElement('div',{className:'sl',style:{marginBottom:8}},'NOTIFICATIONS'),
        React.createElement(Card,null,React.createElement('div',{style:{display:'flex',alignItems:'center',justifyContent:'space-between'}},React.createElement('div',null,React.createElement('div',{style:{fontSize:14,fontWeight:500,color:'var(--text)'}},'In-app Alerts'),React.createElement('div',{style:{fontSize:10,color:'var(--muted)',marginTop:2}},'Movement confirmations, task syncs')),React.createElement(Toggle,{on:store.settings.notifications!==false,onChange:()=>store.updateSettings({notifications:!store.settings.notifications})})))
      ),
      React.createElement('div',{style:{marginBottom:16}},
        React.createElement('div',{className:'sl',style:{marginBottom:8}},'DATA OVERVIEW'),
        React.createElement(Card,null,React.createElement('div',{style:{display:'grid',gridTemplateColumns:'repeat(3,1fr)',gap:8}},[['Tasks',store.tasks.length],['Transactions',store.transactions.length],['Credits',store.credits.length],['Deadlines',store.deadlines.length],['Businesses',store.businesses.length],['Total',totalEntries]].map(([k,v])=>React.createElement('div',{key:k,style:{textAlign:'center',background:'var(--card2)',borderRadius:9,padding:'9px 4px',border:'1px solid var(--border)'}},React.createElement('div',{className:'fm',style:{fontSize:18,fontWeight:700,color:v>0?'var(--accent)':'var(--muted)'}},v),React.createElement('div',{className:'sl',style:{marginTop:2}},k)))),store.savedAt&&React.createElement('div',{className:'fm',style:{fontSize:10,color:'var(--muted)',marginTop:12,textAlign:'center'}},'Auto-saved · ',new Date(store.savedAt).toLocaleTimeString([],{hour:'2-digit',minute:'2-digit',second:'2-digit'})))
      ),
      React.createElement('div',{style:{marginBottom:16}},
        React.createElement('div',{className:'sl',style:{marginBottom:8}},'BACKUP'),
        React.createElement(Card,null,React.createElement('div',{style:{fontSize:12,color:'var(--text2)',marginBottom:12,lineHeight:1.5}},'Export all data as a JSON backup.',totalEntries>0?` You have ${totalEntries} entries.`:' No data yet.'),React.createElement('button',{className:'btn-p',onClick:handleExport,disabled:totalEntries===0,style:{display:'flex',alignItems:'center',justifyContent:'center',gap:6,opacity:totalEntries===0?.5:1}},'Export Data (JSON)'))
      ),
      React.createElement('div',{style:{marginBottom:16}},
        React.createElement('div',{className:'sl',style:{marginBottom:8}},'ABOUT'),
        React.createElement(Card,null,[['Version','2.0.0'],['Storage','localStorage'],['Stack','React + Recharts'],['Movement Sync','Active']].map(([k,v])=>React.createElement('div',{key:k,style:{display:'flex',justifyContent:'space-between',padding:'7px 0',borderBottom:'1px solid var(--border)'}},React.createElement('span',{style:{fontSize:13,color:'var(--text2)'}},k),React.createElement('span',{className:'fm',style:{fontSize:12,color:'var(--accent)'}},v))))
      ),
      React.createElement('div',null,
        React.createElement('div',{className:'sl',style:{marginBottom:8,color:'var(--red)'}},'DANGER ZONE'),
        React.createElement(Card,{style:{background:'rgba(224,82,82,.03)',borderColor:'rgba(224,82,82,.18)'}},
          React.createElement('div',{style:{display:'flex',gap:10,marginBottom:14}},React.createElement('span',{style:{fontSize:18,color:'var(--red)',flexShrink:0,marginTop:2}},'⚠'),React.createElement('div',null,React.createElement('div',{style:{fontSize:14,fontWeight:600,color:'var(--red)',marginBottom:4}},'Reset All Data'),React.createElement('div',{style:{fontSize:12,color:'var(--text2)',lineHeight:1.5}},'Permanently deletes ALL data. localStorage is fully cleared.'),totalEntries>0&&React.createElement('div',{className:'fm',style:{fontSize:11,color:'var(--red)',marginTop:6}},totalEntries,' entries will be deleted.'))),
          !confirmReset
            ?React.createElement('button',{onClick:()=>setConfirmReset(true),style:{width:'100%',background:'none',border:'1.5px solid var(--red)',color:'var(--red)',borderRadius:10,padding:12,fontSize:13,fontWeight:600,display:'flex',alignItems:'center',justifyContent:'center',gap:6}},'Reset All App Data')
            :React.createElement('div',null,
              React.createElement('div',{style:{fontSize:12,color:'var(--text2)',marginBottom:10}},'Type ',React.createElement('strong',{style:{color:'var(--red)',fontFamily:'DM Mono,monospace'}},'RESET'),' to confirm:'),
              React.createElement('input',{value:resetText,onChange:e=>setResetText(e.target.value),placeholder:'Type RESET',style:{marginBottom:10,borderColor:'var(--red)'},autoFocus:true}),
              React.createElement('div',{style:{display:'flex',gap:8}},
                React.createElement('button',{onClick:handleReset,disabled:resetText!=='RESET',style:{flex:1,background:resetText==='RESET'?'var(--red)':'var(--card2)',border:'none',borderRadius:10,color:resetText==='RESET'?'#fff':'var(--muted)',padding:12,fontSize:13,fontWeight:700,cursor:resetText==='RESET'?'pointer':'not-allowed',transition:'all .2s'}},'Confirm Reset'),
                React.createElement('button',{onClick:()=>{setConfirmReset(false);setResetText('')},className:'btn-g',style:{flex:1}},'Cancel')
              )
            )
        )
      )
    )
  );
}

const PAGES={home:HomePage,tasks:TasksPage,movements:MovementsPage,finance:FinancePage,target:TargetPage,analytics:AnalyticsPage,businesses:BusinessesPage,deadlines:DeadlinesPage,settings:SettingsPage};
function PageRouter(){const{page}=useNav();const C=PAGES[page]||HomePage;return React.createElement(C,null)}

function App(){
  return React.createElement(StoreProvider,null,
    React.createElement(NotifProvider,null,
      React.createElement(NavProvider,null,
        React.createElement('div',{style:{display:'flex',flexDirection:'column',height:'100%',background:'var(--bg)',overflow:'hidden',position:'relative'}},
          React.createElement(NotifStack,null),
          React.createElement(Sidebar,null),
          React.createElement('div',{style:{display:'flex',flexDirection:'column',height:'100%',overflow:'hidden'}},
            React.createElement(TopBar,null),
            React.createElement('div',{style:{flex:1,overflow:'hidden',display:'flex',flexDirection:'column'}},
              React.createElement(PageRouter,null)
            )
          )
        )
      )
    )
  );
}

ReactDOM.createRoot(document.getElementById('root')).render(React.createElement(App,null));
</script>
</body>
</html>
<!-- END REPLACEMENT -->
```
