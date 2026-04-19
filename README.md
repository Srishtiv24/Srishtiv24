<div align="center">

# SRISHTI VERMA 

**MERN Developer | Pre Final Year Computer Science Engineering Student**

*"Consistency and curiosity are key to becoming a great engineer."*

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/srishtiiv24/)
[![Portfolio](https://img.shields.io/badge/Portfolio-000000?style=for-the-badge&logo=vercel&logoColor=white)](https://your-portfolio.com)
[![Email](https://img.shields.io/badge/Email-EA4335?style=for-the-badge&logo=gmail&logoColor=white)](mailto:vermasrishti74@gmail.com)
[![LeetCode](https://img.shields.io/badge/LeetCode-FFA116?style=for-the-badge&logo=leetcode&logoColor=black)](https://leetcode.com/u/e1ZRgaBXNa/)

</div>

<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8"/>
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>
<title>Srishti — Terminal</title>
<style>
* { box-sizing: border-box; margin: 0; padding: 0; }
body {
  min-height: 100vh;
  background: #010409;
  display: flex;
  align-items: center;
  justify-content: center;
  font-family: 'Courier New', monospace;
  padding: 2rem;
}
.terminal {
  width: 100%;
  max-width: 700px;
  background: #0d1117;
  border-radius: 12px;
  border: 1px solid #30363d;
  overflow: hidden;
  box-shadow: 0 0 60px rgba(39,201,63,0.07), 0 24px 64px rgba(0,0,0,0.6);
}
.titlebar {
  background: #161b22;
  padding: 12px 16px;
  display: flex;
  align-items: center;
  gap: 8px;
  border-bottom: 1px solid #21262d;
}
.dot { width: 13px; height: 13px; border-radius: 50%; }
.title-text {
  flex: 1; text-align: center; font-size: 12px;
  color: #484f58; font-family: monospace;
  margin-right: 42px; letter-spacing: 0.04em;
}
.body {
  padding: 20px 22px 28px;
  font-size: 13.5px;
  line-height: 1.9;
  min-height: 320px;
}
.line { display: flex; flex-wrap: wrap; align-items: baseline; min-height: 26px; }
.prompt-user { color: #39d353; font-weight: bold; }
.prompt-at   { color: #484f58; }
.prompt-host { color: #58a6ff; font-weight: bold; }
.prompt-sym  { color: #484f58; margin-right: 4px; }
.cmd         { color: #e6edf3; }
.out         { color: #8b949e; padding-left: 4px; }
.green       { color: #39d353; }
.blue        { color: #58a6ff; }
.pink        { color: #f778ba; }
.amber       { color: #e3b341; }
.white       { color: #e6edf3; }
.dim         { color: #484f58; }
.cursor {
  display: inline-block; width: 9px; height: 15px;
  background: #39d353; margin-left: 1px;
  vertical-align: middle;
  animation: blink 0.8s step-end infinite;
}
@keyframes blink { 50% { opacity: 0; } }
.scanline {
  position: fixed; top: 0; left: 0; right: 0; bottom: 0;
  background: repeating-linear-gradient(0deg, transparent, transparent 2px, rgba(0,0,0,0.025) 2px, rgba(0,0,0,0.025) 4px);
  pointer-events: none; z-index: 10;
}
</style>
</head>
<body>
<div class="scanline"></div>
<div class="terminal">
  <div class="titlebar">
    <div class="dot" style="background:#ff5f56"></div>
    <div class="dot" style="background:#ffbd2e"></div>
    <div class="dot" style="background:#27c93f"></div>
    <span class="title-text">srishti@github: ~</span>
  </div>
  <div class="body" id="body"></div>
</div>

<script>
const SCRIPT = [

  { type: 'cmd',  text: 'whoami' },
  { type: 'out',  parts: [{ t: 'Srishti', c: 'green' }, { t: '  —  3rd Year B.Tech CSE Student', c: 'white' }] },

  { type: 'gap' },

  { type: 'cmd',  text: 'echo $PASSION' },
  { type: 'out',  parts: [{ t: 'Full-Stack Web Development  ', c: 'amber' }, { t: '(MERN Stack)', c: 'dim' }] },

  { type: 'gap' },

  { type: 'cmd',  text: 'cat current_focus.txt' },
  { type: 'out',  parts: [{ t: '→ ', c: 'blue' }, { t: 'Building intuitive, user-focused websites', c: 'white' }] },
  { type: 'out',  parts: [{ t: '→ ', c: 'blue' }, { t: 'Practising DSA daily on ', c: 'out' }, { t: 'LeetCode', c: 'pink' }] },

  { type: 'gap' },

  { type: 'cmd',  text: 'cat skills.json | grep stack' },
  { type: 'out',  parts: [{ t: '"stack"', c: 'blue' }, { t: ' : ', c: 'dim' }, { t: '"MongoDB · Express · React · Node.js"', c: 'green' }] },
  { type: 'out',  parts: [{ t: '"extras"', c: 'blue' }, { t: ': ', c: 'dim' }, { t: '"Socket.io · WebRTC · JWT · OAuth · Multer"', c: 'green' }] },
  { type: 'out',  parts: [{ t: '"deploy"', c: 'blue' }, { t: ': ', c: 'dim' }, { t: '"Vercel · Netlify · Render"', c: 'amber' }] },

  { type: 'gap' },

  { type: 'cmd',  text: 'cat motto.txt' },
  { type: 'out',  parts: [{ t: '" Consistency + Curiosity = Great Engineer "', c: 'amber' }] },

  { type: 'gap' },

  { type: 'cmd',  text: 'ls interests/' },
  { type: 'out',  parts: [
    { t: 'creativity/', c: 'pink' }, { t: '   ', c: 'dim' },
    { t: 'fitness/', c: 'pink' },    { t: '   ', c: 'dim' },
    { t: 'building_things/', c: 'green' }
  ]},

  { type: 'gap' },

  { type: 'cmd',  text: 'echo $GOAL' },
  { type: 'out',  parts: [{ t: 'Always learning · staying challenged · contributing meaningfully 🚀', c: 'white' }] },

  { type: 'gap' },
  { type: 'cmd',  text: '' },
];

const body = document.getElementById('body');
let li = 0, ci = 0, phase = 'prompt';
let cmdSpan = null;

function mkPrompt() {
  const d = document.createElement('div');
  d.className = 'line';
  d.innerHTML =
    `<span class="prompt-user">srishti</span>` +
    `<span class="prompt-at">@</span>` +
    `<span class="prompt-host">github</span>` +
    `<span class="prompt-sym"> ~ $</span>`;
  cmdSpan = document.createElement('span');
  cmdSpan.className = 'cmd';
  cmdSpan.style.marginLeft = '6px';
  d.appendChild(cmdSpan);
  body.appendChild(d);
}

function putCursor(el) {
  dropCursor();
  const c = document.createElement('span');
  c.className = 'cursor'; c.id = 'cur';
  el.appendChild(c);
}

function dropCursor() {
  const c = document.getElementById('cur');
  if (c) c.remove();
}

function mkOutput(parts) {
  const d = document.createElement('div');
  d.className = 'line';
  d.style.paddingLeft = '4px';
  parts.forEach(p => {
    const s = document.createElement('span');
    s.className = p.c; s.textContent = p.t;
    d.appendChild(s);
  });
  body.appendChild(d);
}

function mkGap() {
  const d = document.createElement('div');
  d.style.height = '5px';
  body.appendChild(d);
}

function tick() {
  if (li >= SCRIPT.length) {
    dropCursor();
    putCursor(body.lastElementChild);
    return;
  }
  const node = SCRIPT[li];

  if (node.type === 'gap') {
    mkGap(); li++;
    setTimeout(tick, 60);
    return;
  }

  if (node.type === 'out') {
    mkOutput(node.parts); li++;
    setTimeout(tick, 50);
    return;
  }

  if (node.type === 'cmd') {
    if (phase === 'prompt') {
      mkPrompt();
      putCursor(cmdSpan);
      phase = 'typing'; ci = 0;
      setTimeout(tick, 180);
      return;
    }
    if (phase === 'typing') {
      if (ci < node.text.length) {
        dropCursor();
        cmdSpan.textContent += node.text[ci++];
        putCursor(cmdSpan);
        setTimeout(tick, 58);
      } else {
        dropCursor();
        li++; phase = 'prompt';
        setTimeout(tick, 350);
      }
    }
  }
}

setTimeout(tick, 900);
</script>
</body>
</html>


## Tech Stack

**Frontend**

![React](https://img.shields.io/badge/React-20232A?style=flat-square&logo=react&logoColor=61DAFB)
![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-06B6D4?style=flat-square&logo=tailwind-css&logoColor=white)
![Bootstrap](https://img.shields.io/badge/Bootstrap-7952B3?style=flat-square&logo=bootstrap&logoColor=purple)
![Material UI](https://img.shields.io/badge/Material_UI-007FFF?style=flat-square&logo=mui&logoColor=red)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat-square&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=flat-square&logo=css3&logoColor=yellow)

**Backend & Database**

![Node.js](https://img.shields.io/badge/Node.js-339933?style=flat-square&logo=nodedotjs&logoColor=white)
![Express.js](https://img.shields.io/badge/Express.js-000000?style=flat-square&logo=express&logoColor=white)
![Mongoose](https://img.shields.io/badge/Mongoose-880000?style=flat-square&logo=mongoose&logoColor=white)
![Multer](https://img.shields.io/badge/Multer-FF6C37?style=flat-square&logo=npm&logoColor=white)
![Nodemailer](https://img.shields.io/badge/Nodemailer-47A248?style=flat-square&logo=npm&logoColor=pink)
![EJS](https://img.shields.io/badge/EJS-B4CA65?style=flat-square&logo=ejs&logoColor=green)

**Database** 

![MongoDB](https://img.shields.io/badge/MongoDB-47A248?style=flat-square&logo=mongodb&logoColor=white)
![SQL](https://img.shields.io/badge/SQL-4479A1?style=flat-square&logo=mysql&logoColor=white)

**Real-Time & Communication**

![Socket.io](https://img.shields.io/badge/Socket.io-010101?style=flat-square&logo=socket.io&logoColor=white)
![WebRTC](https://img.shields.io/badge/WebRTC-333333?style=flat-square&logo=webrtc&logoColor=white)

**Auth & APIs**

![JWT](https://img.shields.io/badge/JWT-000000?style=flat-square&logo=jsonwebtokens&logoColor=white)
![Auth0](https://img.shields.io/badge/OAuth_2.0-EB5424?style=flat-square&logo=auth0&logoColor=white)
![REST API](https://img.shields.io/badge/REST_API-FF6C37?style=flat-square&logo=postman&logoColor=pink)
![Passport](https://img.shields.io/badge/Passport-000000?style=flat-square&logo=passport&logoColor=yellow)

**Deployment & Hosting**

![Vercel](https://img.shields.io/badge/Vercel-000000?style=flat-square&logo=vercel&logoColor=white)
![Netlify](https://img.shields.io/badge/Netlify-00C7B7?style=flat-square&logo=netlify&logoColor=white)
![Render](https://img.shields.io/badge/Render-46E3B7?style=flat-square&logo=render&logoColor=black)

---
## Languages

![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black)
![Java](https://img.shields.io/badge/Java-ED8B00?style=flat-square&logo=openjdk&logoColor=white)
![C](https://img.shields.io/badge/C-A8B9CC?style=flat-square&logo=c&logoColor=black)
![Python](https://img.shields.io/badge/python-A8B9CC?style=flat-square&logo=python&logoColor=blue)

---

## Tools & Version Control

![Git](https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white)
![GitHub](https://img.shields.io/badge/GitHub-181717?style=flat-square&logo=github&logoColor=white)
![VS Code](https://img.shields.io/badge/VS_Code-007ACC?style=flat-square&logo=visual-studio-code&logoColor=white)

---

## GitHub Stats

<div align="center">

![GitHub Stats](https://github-readme-stats.vercel.app/api?username=Srishtiv24&show_icons=true&theme=tokyonight&hide_border=true&count_private=true)

![Top Languages](https://github-readme-stats.vercel.app/api/top-langs/?username=Srishtiv24&layout=compact&theme=tokyonight&hide_border=true)

![GitHub Streak](https://github-readme-streak-stats.herokuapp.com/?user=Srishtiv24&theme=tokyonight&hide_border=true)

</div>

---

##  DSA Progress

<div align="center">

![LeetCode Stats](https://leetcard.jacoblin.cool/e1ZRgaBXNa?theme=dark&font=Nunito&ext=contest)

</div>

---

<div align="center">

**Thanks for visiting! Feel free to explore my repos and drop a ⭐ if something inspires you 🌟**

</div>
