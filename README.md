pro and professional coder GitHub Profile README Generator

तैयार है — मैंने Pro & Professional GitHub Profile README Generator बनाया है।

इसमें शामिल हैं:

Live GitHub README Preview
Professional profile, bio और headline
Tech Stack sections
LinkedIn, X, YouTube, Website, Email links
Featured Projects dynamically add/remove
GitHub Stats
Streak Stats
Top Languages
Contribution Graph
Typing SVG banner
Services / Expertise section
One-click Copy Markdown
Download README.md
Browser में automatic local save
Demo profile loader
Responsive professional UI
डाउनलोड करें

🚀 Pro GitHub README Generator — ZIP

🌐 Direct index.html

इसे सीधे index.html खोलकर इस्तेमाल किया जा सकता है। GitHub Pages पर डालकर इसे अपना online README generator website भी बनाया जा सकता है। 

<!doctype html>
<html lang="en">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width,initial-scale=1">
<title>Pro GitHub Profile README Generator</title>
<meta name="description" content="Professional GitHub Profile README Generator with live preview and Markdown export.">
<style>
:root{
  --bg:#070b12;--panel:#0d1420;--panel2:#101a29;--text:#e8eef7;--muted:#8fa1b8;
  --line:#1d2a3a;--accent:#58a6ff;--accent2:#7ee787;--danger:#ff7b72;
  --shadow:0 20px 60px rgba(0,0,0,.35);--radius:18px;
}
*{box-sizing:border-box}
html{scroll-behavior:smooth}
body{
  margin:0;background:
  radial-gradient(circle at 10% 0%,rgba(88,166,255,.10),transparent 28%),
  radial-gradient(circle at 90% 10%,rgba(126,231,135,.08),transparent 25%),
  var(--bg);color:var(--text);
  font-family:Inter,ui-sans-serif,system-ui,-apple-system,Segoe UI,Roboto,Arial,sans-serif;
}
button,input,textarea,select{font:inherit}
button{cursor:pointer}
.app{min-height:100vh}
header{
  position:sticky;top:0;z-index:30;
  backdrop-filter:blur(16px);
  background:rgba(7,11,18,.82);border-bottom:1px solid var(--line)
}
.header-inner{max-width:1500px;margin:auto;padding:16px 22px;display:flex;align-items:center;justify-content:space-between;gap:18px}
.brand{display:flex;align-items:center;gap:12px}
.logo{
  width:42px;height:42px;border-radius:12px;display:grid;place-items:center;
  background:linear-gradient(135deg,#58a6ff,#7ee787);color:#071019;font-weight:900
}
.brand h1{font-size:17px;margin:0}
.brand p{font-size:12px;color:var(--muted);margin:2px 0 0}
.actions{display:flex;gap:8px;flex-wrap:wrap}
.btn{
  border:1px solid var(--line);background:var(--panel);color:var(--text);
  padding:9px 13px;border-radius:10px;transition:.18s;
}
.btn:hover{transform:translateY(-1px);border-color:#35506d}
.btn.primary{background:var(--accent);color:#06111e;border-color:transparent;font-weight:800}
.btn.green{background:var(--accent2);color:#07120a;border-color:transparent;font-weight:800}
.btn.danger{color:#ffd5d2}
.layout{max-width:1500px;margin:0 auto;padding:22px;display:grid;grid-template-columns:430px 1fr;gap:18px}
.card{
  background:linear-gradient(180deg,rgba(16,26,41,.96),rgba(10,17,28,.96));
  border:1px solid var(--line);border-radius:var(--radius);box-shadow:var(--shadow)
}
.panel{padding:18px}
.left{height:calc(100vh - 108px);overflow:auto;position:sticky;top:88px}
.right{min-width:0}
.section{padding:18px;border-bottom:1px solid var(--line)}
.section:last-child{border-bottom:0}
.section-title{display:flex;align-items:center;justify-content:space-between;margin-bottom:13px}
.section-title h2{font-size:14px;margin:0;letter-spacing:.2px}
.section-title span{font-size:11px;color:var(--muted)}
.grid{display:grid;gap:10px}
.grid.two{grid-template-columns:1fr 1fr}
.grid.three{grid-template-columns:repeat(3,1fr)}
label{font-size:11px;color:var(--muted);display:block;margin-bottom:5px}
input,textarea,select{
  width:100%;background:#09111c;color:var(--text);border:1px solid #213148;border-radius:10px;
  padding:10px 11px;outline:0
}
input:focus,textarea:focus,select:focus{border-color:#4c84c7;box-shadow:0 0 0 3px rgba(88,166,255,.08)}
textarea{min-height:80px;resize:vertical;line-height:1.45}
.checks{display:flex;flex-wrap:wrap;gap:8px}
.check{
  display:flex;align-items:center;gap:7px;background:#0a111c;border:1px solid #203047;
  padding:8px 10px;border-radius:10px;font-size:12px;color:#c7d2e1
}
.check input{width:auto}
.row{display:flex;gap:8px;align-items:end}
.row > *{flex:1}
.item{
  border:1px solid #1d2b3d;border-radius:12px;padding:12px;background:rgba(7,13,22,.55);
  margin-bottom:9px
}
.item-head{display:flex;align-items:center;justify-content:space-between;gap:8px;margin-bottom:9px}
.item-head strong{font-size:12px}
.small{font-size:11px;color:var(--muted)}
.icon-btn{background:transparent;border:0;color:#9fb0c5;padding:5px 8px;border-radius:8px}
.icon-btn:hover{background:#111d2d;color:white}
.preview-wrap{padding:18px}
.tabs{display:flex;gap:8px;margin-bottom:12px}
.tab{background:#0a111c;color:#b7c6d8;border:1px solid var(--line);padding:9px 12px;border-radius:10px}
.tab.active{background:#18263a;color:#fff;border-color:#385577}
.preview,.raw{
  background:#fff;color:#24292f;border-radius:14px;overflow:auto;min-height:720px;
  box-shadow:0 15px 50px rgba(0,0,0,.25)
}
.preview{padding:28px;line-height:1.6}
.raw{display:none;background:#08111c;color:#d8e2ee;border:1px solid var(--line)}
.raw textarea{height:100%;min-height:720px;border:0;border-radius:14px;background:#08111c;color:#d8e2ee;font-family:ui-monospace,SFMono-Regular,Consolas,monospace}
.md h1{font-size:2em;border-bottom:1px solid #d8dee4;padding-bottom:.3em}
.md h2{font-size:1.5em;border-bottom:1px solid #d8dee4;padding-bottom:.25em}
.md h3{font-size:1.25em}
.md img{max-width:100%}
.md a{color:#0969da}
.md code{background:#eff1f3;padding:.15em .3em;border-radius:6px}
.md table{border-collapse:collapse;width:100%;margin:12px 0}
.md th,.md td{border:1px solid #d0d7de;padding:6px 9px}
.status{font-size:11px;color:var(--muted);margin-top:8px;text-align:right}
footer{max-width:1500px;margin:auto;padding:0 22px 28px;color:#66788f;font-size:11px;text-align:center}
.hidden{display:none!important}
@media(max-width:1100px){
 .layout{grid-template-columns:1fr}
 .left{height:auto;position:static}
}
@media(max-width:700px){
 .grid.two,.grid.three{grid-template-columns:1fr}
 .header-inner{align-items:flex-start;flex-direction:column}
}
</style>
</head>
<body>
<div class="app">
<header>
  <div class="header-inner">
    <div class="brand">
      <div class="logo">&lt;/&gt;</div>
      <div><h1>Pro GitHub Profile README Generator</h1><p>Build a polished developer profile in minutes.</p></div>
    </div>
    <div class="actions">
      <button class="btn" id="demoBtn">Load Demo</button>
      <button class="btn" id="clearBtn">Clear</button>
      <button class="btn primary" id="copyBtn">Copy Markdown</button>
      <button class="btn green" id="downloadBtn">Download README.md</button>
    </div>
  </div>
</header>

<div class="layout">
  <aside class="card left" id="form">

    <div class="section">
      <div class="section-title"><h2>1. Identity</h2><span>Core profile</span></div>
      <div class="grid two">
        <div><label>Display name</label><input id="name" value="Your Name"></div>
        <div><label>GitHub username</label><input id="username" value="yourusername"></div>
      </div>
      <div class="grid two" style="margin-top:10px">
        <div><label>Headline</label><input id="headline" value="Full-Stack Developer • AI Builder • Open Source"></div>
        <div><label>Location</label><input id="location" value="India"></div>
      </div>
      <div style="margin-top:10px"><label>About</label><textarea id="about">I build modern web products, automation tools, and AI-powered experiences. I enjoy turning ideas into useful, scalable software.</textarea></div>
      <div style="margin-top:10px"><label>Profile image URL (optional)</label><input id="avatar" placeholder="https://..."></div>
    </div>

    <div class="section">
      <div class="section-title"><h2>2. Social & Contact</h2><span>Links</span></div>
      <div class="grid two">
        <div><label>Website</label><input id="website" placeholder="https://yourdomain.com"></div>
        <div><label>LinkedIn</label><input id="linkedin" placeholder="https://linkedin.com/in/username"></div>
        <div><label>X / Twitter</label><input id="twitter" placeholder="https://x.com/username"></div>
        <div><label>Email</label><input id="email" placeholder="you@example.com"></div>
        <div><label>YouTube</label><input id="youtube" placeholder="https://youtube.com/@username"></div>
        <div><label>Dev.to / Blog</label><input id="blog" placeholder="https://dev.to/username"></div>
      </div>
    </div>

    <div class="section">
      <div class="section-title"><h2>3. Tech Stack</h2><span>Comma separated</span></div>
      <div><label>Languages</label><input id="languages" value="JavaScript, TypeScript, Python, SQL"></div>
      <div style="margin-top:10px"><label>Frameworks / Libraries</label><input id="frameworks" value="React, Next.js, Node.js, Tailwind CSS"></div>
      <div style="margin-top:10px"><label>Tools / Cloud / DB</label><input id="tools" value="Git, GitHub, Docker, Firebase, MongoDB, PostgreSQL"></div>
    </div>

    <div class="section">
      <div class="section-title"><h2>4. Featured Projects</h2><button class="btn" id="addProject">+ Add</button></div>
      <div id="projects"></div>
    </div>

    <div class="section">
      <div class="section-title"><h2>5. Sections</h2><span>Toggle what appears</span></div>
      <div class="checks">
        <label class="check"><input type="checkbox" id="showTyping" checked> Typing banner</label>
        <label class="check"><input type="checkbox" id="showStats" checked> GitHub stats</label>
        <label class="check"><input type="checkbox" id="showStreak" checked> Streak stats</label>
        <label class="check"><input type="checkbox" id="showLangs" checked> Top languages</label>
        <label class="check"><input type="checkbox" id="showGraph" checked> Contribution graph</label>
        <label class="check"><input type="checkbox" id="showContact" checked> Contact</label>
        <label class="check"><input type="checkbox" id="showQuote" checked> Developer quote</label>
        <label class="check"><input type="checkbox" id="showServices"> Services</label>
      </div>
      <div style="margin-top:12px"><label>Services / Expertise (optional)</label><input id="services" value="AI Automation, Web Apps, Dashboards, API Integration"></div>
    </div>

    <div class="section">
      <div class="section-title"><h2>6. Contribution / Footer</h2><span>Branding</span></div>
      <div class="grid two">
        <div><label>Typing text</label><input id="typing" value="Full-Stack Developer;AI Builder;Open Source Enthusiast"></div>
        <div><label>Developer quote</label><input id="quote" value="Code. Create. Iterate. Ship."></div>
      </div>
      <div style="margin-top:10px"><label>Footer message</label><input id="footer" value="Thanks for visiting my profile! Let’s build something great."></div>
    </div>
  </aside>

  <main class="card right">
    <div class="preview-wrap">
      <div class="tabs">
        <button class="tab active" data-tab="preview">Live Preview</button>
        <button class="tab" data-tab="raw">Raw Markdown</button>
      </div>
      <div class="preview" id="preview"></div>
      <div class="raw" id="raw"><textarea id="markdown" spellcheck="false"></textarea></div>
      <div class="status" id="status">Auto-updating…</div>
    </div>
  </main>
</div>

<footer>Runs fully in your browser • No backend • No data sent anywhere • Edit and export your README locally.</footer>

<script>
const $ = id => document.getElementById(id);
const esc = s => String(s ?? '').replace(/&/g,'&amp;').replace(/</g,'&lt;').replace(/>/g,'&gt;');
const mdEsc = s => String(s ?? '').replace(/([\\\\`*_[\\]{}()#+.!|>])/g,'\\\\$1');
const split = s => String(s || '').split(',').map(x=>x.trim()).filter(Boolean);

const state = {
  projects: [
    {name:'AI Dashboard', desc:'A modern dashboard for AI tools, automation and analytics.', url:'https://github.com/yourusername/ai-dashboard', tech:'React, TypeScript, Tailwind'},
    {name:'Automation Toolkit', desc:'Practical utilities that automate repetitive workflows.', url:'https://github.com/yourusername/automation-toolkit', tech:'Python, APIs, GitHub Actions'}
  ]
};

function inputValue(id){ return $(id).value.trim(); }
function checked(id){ return $(id).checked; }

function renderProjectForm(){
  $('projects').innerHTML = state.projects.map((p,i)=>`
    <div class="item">
      <div class="item-head"><strong>Project ${i+1}</strong><button class="icon-btn" onclick="removeProject(${i})">✕ Remove</button></div>
      <div class="grid two">
        <div><label>Name</label><input data-p="${i}" data-k="name" value="${esc(p.name)}"></div>
        <div><label>URL</label><input data-p="${i}" data-k="url" value="${esc(p.url)}"></div>
      </div>
      <div style="margin-top:9px"><label>Description</label><input data-p="${i}" data-k="desc" value="${esc(p.desc)}"></div>
      <div style="margin-top:9px"><label>Tech</label><input data-p="${i}" data-k="tech" value="${esc(p.tech)}"></div>
    </div>`).join('');
  document.querySelectorAll('[data-p]').forEach(el=>{
    el.addEventListener('input',()=>{ state.projects[+el.dataset.p][el.dataset.k]=el.value; update(); });
  });
}
function removeProject(i){ state.projects.splice(i,1); renderProjectForm(); update(); }
window.removeProject = removeProject;

$('addProject').onclick = ()=>{state.projects.push({name:'New Project',desc:'Project description.',url:'https://github.com/yourusername/new-project',tech:'Tech stack'});renderProjectForm();update();};

function badge(label,link,img){
  return `[![${label}](${img})](${link})`;
}

function makeMarkdown(){
  const name=inputValue('name')||'Your Name';
  const username=inputValue('username')||'yourusername';
  const headline=inputValue('headline');
  const location=inputValue('location');
  const about=inputValue('about');
  let md = '';

  if(checked('showTyping')){
    const text=inputValue('typing') || headline || 'Developer';
    const encoded=encodeURIComponent(text.replace(/;/g,' • ')).replace(/%20/g,'_');
    md += `<p align="center">\\n  <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&size=24&pause=900&center=true&vCenter=true&width=760&lines=${encoded}" alt="Typing SVG" />\\n</p>\\n\\n`;
  }

  md += `# Hi, I'm ${name} 👋\\n\\n`;
  if(headline) md += `### ${headline}\\n\\n`;
  if(location) md += `📍 ${location}\\n\\n`;
  if(about) md += `${about}\\n\\n`;

  const links=[];
  if(inputValue('website')) links.push(`[🌐 Website](${inputValue('website')})`);
  if(inputValue('linkedin')) links.push(`[LinkedIn](${inputValue('linkedin')})`);
  if(inputValue('twitter')) links.push(`[X](${inputValue('twitter')})`);
  if(inputValue('youtube')) links.push(`[YouTube](${inputValue('youtube')})`);
  if(inputValue('blog')) links.push(`[Blog](${inputValue('blog')})`);
  if(links.length) md += `### Connect with me\\n\\n${links.join(' • ')}\\n\\n`;

  md += `## 🧰 Tech Stack\\n\\n`;
  const stacks=[
    ['Languages',split(inputValue('languages'))],
    ['Frameworks / Libraries',split(inputValue('frameworks'))],
    ['Tools / Cloud / Databases',split(inputValue('tools'))]
  ];
  stacks.forEach(([title,arr])=>{
    if(arr.length) md += `**${title}:**  ${arr.map(x=>'\`${x}\`').join(' · ')}\\n\\n`;
  });

  if(checked('showServices')){
    const sv=split(inputValue('services'));
    if(sv.length) md += `## 🚀 What I Do\\n\\n${sv.map(x=>`- ${x}`).join('\\n')}\\n\\n`;
  }

  if(state.projects.length){
    md += `## 🏆 Featured Projects\\n\\n`;
    state.projects.forEach(p=>{
      if(p.url) md += `### [${p.name}](${p.url})\\n`;
      else md += `### ${p.name}\\n`;
      if(p.desc) md += `${p.desc}\\n\\n`;
      if(p.tech) md += `**Tech:** ${p.tech}\\n\\n`;
    });
  }

  if(checked('showStats')){
    md += `## 📊 GitHub Stats\\n\\n<p align="center">\\n`;
    md += `  <img src="https://github-readme-stats.vercel.app/api?username=${encodeURIComponent(username)}&show_icons=true&hide_border=true&rank_icon=github" alt="GitHub Stats" />\\n`;
    md += `</p>\\n\\n`;
  }
  if(checked('showStreak')){
    md += `<p align="center"><img src="https://streak-stats.demolab.com?user=${encodeURIComponent(username)}&hide_border=true" alt="GitHub Streak" /></p>\\n\\n`;
  }
  if(checked('showLangs')){
    md += `<p align="center"><img src="https://github-readme-stats.vercel.app/api/top-langs/?username=${encodeURIComponent(username)}&layout=compact&hide_border=true&langs_count=8" alt="Top Languages" /></p>\\n\\n`;
  }
  if(checked('showGraph')){
    md += `## 📈 Contribution Graph\\n\\n[![${name}'s github activity graph](https://github-readme-activity-graph.vercel.app/graph?username=${encodeURIComponent(username)}&hide_border=true)](https://github.com/${username})\\n\\n`;
  }

  if(checked('showQuote') && inputValue('quote')){
    md += `> "${inputValue('quote')}"\\n\\n`;
  }

  if(checked('showContact') && inputValue('email')){
    md += `## 📫 Contact\\n\\nFeel free to reach out: **${inputValue('email')}**\\n\\n`;
  }

  md += `---\\n\\n<p align="center">${inputValue('footer') || 'Thanks for visiting my profile!'}\\n`;
  if(username) md += `\\n\\n<img src="https://komarev.com/ghpvc/?username=${encodeURIComponent(username)}&style=flat-square&color=blue" alt="Profile views" />`;
  md += `</p>\\n`;

  return md;
}

function mdToHtml(md){
  // Small self-contained Markdown renderer for the preview.
  let s=esc(md);
  s=s.replace(/^### (.*)$/gm,'<h3>$1</h3>')
     .replace(/^## (.*)$/gm,'<h2>$1</h2>')
     .replace(/^# (.*)$/gm,'<h1>$1</h1>');
  s=s.replace(/^\> (.*)$/gm,'<blockquote>$1</blockquote>');
  s=s.replace(/^- (.*)$/gm,'<li>$1</li>');
  s=s.replace(/(<li>.*<\\/li>)/gs,'<ul>$1</ul>');
  s=s.replace(/!\\[([^\\]]*)\\]\\(([^)]+)\\)/g,'<img alt="$1" src="$2">');
  s=s.replace(/\\[([^\\]]+)\\]\\(([^)]+)\\)/g,'<a href="$2" target="_blank" rel="noreferrer">$1</a>');
  s=s.replace(/`([^`]+)`/g,'<code>$1</code>');
  s=s.replace(/\\*\\*([^*]+)\\*\\*/g,'<strong>$1</strong>');
  s=s.replace(/---/g,'<hr>');
  s=s.replace(/\\n\\n/g,'</p><p>').replace(/\\n/g,'<br>');
  return `<div class="md"><p>${s}</p></div>`;
}

function update(){
  const md=makeMarkdown();
  $('markdown').value=md;
  $('preview').innerHTML=mdToHtml(md);
  $('status').textContent=`${md.length.toLocaleString()} characters • ${md.split('\\n').length} lines`;
  localStorage.setItem('github-readme-generator', JSON.stringify({
    fields:[...document.querySelectorAll('#form input,#form textarea')].reduce((o,e)=>{if(e.id)o[e.id]=e.type==='checkbox'?e.checked:e.value;return o},{}),
    projects:state.projects
  }));
}

document.querySelectorAll('#form input,#form textarea,#form select').forEach(el=>el.addEventListener('input',update));
document.querySelectorAll('.tab').forEach(btn=>btn.onclick=()=>{
  document.querySelectorAll('.tab').forEach(x=>x.classList.remove('active'));
  btn.classList.add('active');
  const isPreview=btn.dataset.tab==='preview';
  $('preview').style.display=isPreview?'block':'none';
  $('raw').style.display=isPreview?'none':'block';
});

$('copyBtn').onclick=async()=>{
  const md=$('markdown').value;
  await navigator.clipboard.writeText(md);
  const old=$('copyBtn').textContent;$('copyBtn').textContent='Copied ✓';
  setTimeout(()=>$('copyBtn').textContent=old,1400);
};
$('downloadBtn').onclick=()=>{
  const blob=new Blob([$('markdown').value],{type:'text/markdown;charset=utf-8'});
  const a=document.createElement('a');a.href=URL.createObjectURL(blob);a.download='README.md';a.click();
  URL.revokeObjectURL(a.href);
};
$('clearBtn').onclick=()=>{
  if(!confirm('Clear all profile fields and projects?')) return;
  document.querySelectorAll('#form input,#form textarea').forEach(el=>{
    if(el.type==='checkbox') el.checked=false;
    else el.value='';
  });
  state.projects=[];renderProjectForm();update();
};
$('demoBtn').onclick=()=>{
  const demo={
    name:'Manish Kaushik',username:'manishkaushik',headline:'Developer • AI Builder • Automation & Web Apps',
    location:'India',about:'I build modern web applications, dashboards, automation tools and AI-powered experiences. I like turning practical ideas into clean, useful software.',
    avatar:'',website:'https://example.com',linkedin:'https://linkedin.com/in/yourusername',twitter:'https://x.com/yourusername',
    email:'hello@example.com',youtube:'https://youtube.com/@yourusername',blog:'https://dev.to/yourusername',
    languages:'JavaScript, TypeScript, Python, SQL',frameworks:'React, Next.js, Node.js, Tailwind CSS',
    tools:'Git, GitHub, Docker, Firebase, MongoDB, PostgreSQL',services:'AI Automation, Web Apps, Dashboards, API Integration',
    typing:'Full-Stack Developer;AI Builder;Automation Enthusiast;Open Source',
    quote:'Build useful things. Keep learning. Ship often.',footer:'Thanks for visiting my profile! Let’s build something useful.'
  };
  Object.entries(demo).forEach(([k,v])=>{if($(k))$(k).value=v});
  ['showTyping','showStats','showStreak','showLangs','showGraph','showContact','showQuote','showServices'].forEach(k=>$(k).checked=true);
  state.projects=[
    {name:'Personal AI Dashboard',desc:'A customizable dashboard for AI settings, prompts and productivity workflows.',url:'https://github.com/yourusername/personal-ai-dashboard',tech:'HTML, CSS, JavaScript'},
    {name:'Automation Toolkit',desc:'A collection of practical utilities for automating repetitive tasks and data workflows.',url:'https://github.com/yourusername/automation-toolkit',tech:'Python, APIs, GitHub Actions'}
  ];
  renderProjectForm();update();
};

(function load(){
  renderProjectForm();
  try{
    const saved=JSON.parse(localStorage.getItem('github-readme-generator')||'');
    if(saved?.fields){
      Object.entries(saved.fields).forEach(([k,v])=>{if($(k)){if($(k).type==='checkbox')$(k).checked=!!v;else $(k).value=v}});
      state.projects=Array.isArray(saved.projects)?saved.projects:state.projects;
      renderProjectForm();
    }
  }catch(e){}
  update();
})();
</script>
</body>
</html>
index.html
HTML
