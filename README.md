# Thobeka-Sibiya-Cv
!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Nothile Sibiya — IT Support & Customer Service</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=IBM+Plex+Mono:wght@400;500;600;700&family=IBM+Plex+Sans:wght@400;500;600;700&display=swap" rel="stylesheet">
<style>

  :root{
    --ink:#12161B;
    --ink-soft:#1B2129;
    --paper:#EFEDE5;
    --paper-2:#E4E1D6;
    --signal:#2E9E6D;
    --signal-dim:#1F6E4C;
    --amber:#D6883A;
    --line-dark:#2A323C;
    --line-light:#C9C4B5;
    --muted-dark:#8B93A0;
    --muted-light:#726B5A;
    --mono:'IBM Plex Mono', ui-monospace, monospace;
    --sans:'IBM Plex Sans', system-ui, sans-serif;
  }

  *{ box-sizing:border-box; margin:0; padding:0; }

  html{ scroll-behavior:smooth; }

  body{
    background:var(--paper);
    color:var(--ink);
    font-family:var(--sans);
    line-height:1.5;
    -webkit-font-smoothing:antialiased;
  }

  a{ color:inherit; }

  .wrap{
    max-width:920px;
    margin:0 auto;
    padding:0 28px;
  }
/* ---------- HERO / STATUS PANEL ---------- */

  .hero{
    background:var(--ink);
    color:var(--paper);
    border-bottom:1px solid var(--line-dark);
  }

  .statusbar{
    display:flex;
    align-items:center;
    justify-content:space-between;
    padding:16px 28px;
    font-family:var(--mono);
    font-size:12px;
    letter-spacing:.06em;
    color:var(--muted-dark);
    border-bottom:1px solid var(--line-dark);
    flex-wrap:wrap;
    gap:8px;
  }

  .statusbar .path::before{
    content:"support_desk://";
    color:var(--signal);
  }

  .statusbar .path{
    color:#D8DCE2;
  }

  .online{
    display:inline-flex;
    align-items:center;
    gap:8px;
    color:var(--signal);
  }

  .dot{
    width:7px; height:7px;
    border-radius:50%;
    background:var(--signal);
    box-shadow:0 0 0 0 rgba(46,158,109,.6);
    animation:pulse 2.2s infinite;
  }

  @keyframes pulse{
    0%{ box-shadow:0 0 0 0 rgba(46,158,109,.55); }
    70%{ box-shadow:0 0 0 8px rgba(46,158,109,0); }
    100%{ box-shadow:0 0 0 0 rgba(46,158,109,0); }
  }

  .hero-main{
    padding:72px 0 56px;
  }

  .eyebrow{
    font-family:var(--mono);
    font-size:12px;
    letter-spacing:.14em;
    text-transform:uppercase;
    color:var(--amber);
    margin-bottom:18px;
    display:flex;
    align-items:center;
    gap:10px;
  }

  .eyebrow::after{
    content:"";
    flex:1;
    height:1px;
    background:var(--line-dark);
  }
  .hero h1{
    font-family:var(--mono);
    font-weight:600;
    font-size:clamp(34px, 6vw, 58px);
    line-height:1.05;
    letter-spacing:-.01em;
    color:#F5F3EC;
  }

  .cursor{
    display:inline-block;
    width:.5em;
    background:var(--signal);
    margin-left:6px;
    animation:blink 1s steps(1) infinite;
  }

  @keyframes blink{ 50%{ opacity:0; } }

  @media (prefers-reduced-motion: reduce){
    .cursor{ animation:none; }
    .dot{ animation:none; }
    *{ scroll-behavior:auto !important; }
  }

  .hero .role{
    margin-top:14px;
    font-size:clamp(16px, 2.4vw, 20px);
    color:var(--muted-dark);
    max-width:46ch;
  }

  .hero .role strong{
    color:#F5F3EC;
    font-weight:600;
  }

  .stat-row{
    margin-top:44px;
    display:grid;
    grid-template-columns:repeat(3,1fr);
    border-top:1px solid var(--line-dark);
  }

  .stat{
    padding:18px 0 0;
    border-right:1px solid var(--line-dark);
  }
  .stat:last-child{ border-right:none; }

  .stat .num{
    font-family:var(--mono);
    font-size:26px;
    font-weight:600;
    color:var(--signal);
  }
  .stat .lab{
    font-family:var(--mono);
    font-size:11px;
    letter-spacing:.08em;
    text-transform:uppercase;
    color:var(--muted-dark);
    margin-top:4px;
  }
  /* ---------- SECTIONS ---------- */

  section{
    padding:64px 0;
    border-bottom:1px solid var(--line-light);
  }

  .sec-head{
    display:flex;
    align-items:baseline;
    gap:14px;
    margin-bottom:32px;
  }

  .sec-num{
    font-family:var(--mono);
    font-size:12px;
    color:var(--muted-light);
    letter-spacing:.08em;
  }

  .sec-title{
    font-family:var(--mono);
    font-weight:600;
    font-size:22px;
    letter-spacing:-.01em;
  }

  .sec-title .accent{ color:var(--signal-dim); }

  .reveal{
    opacity:0;
    transform:translateY(14px);
    transition:opacity .6s ease, transform .6s ease;
  }
  .reveal.in{
    opacity:1;
    transform:translateY(0);
  }
  @media (prefers-reduced-motion: reduce){
    .reveal{ opacity:1; transform:none; transition:none; }
  }

  @media print{
    .reveal{ opacity:1 !important; transform:none !important; transition:none !important; }
    .hero{ break-inside:avoid; }
    .ticket, .log-entry{ break-inside:avoid; }
    section{ break-inside:avoid-page; }
    body{ background:#fff; }
  }

  /* summary */
  .summary p{
    font-size:17px;
    max-width:64ch;
    color:#2A2E24;
  }

  /* competencies */
  .chips{
    display:flex;
    flex-wrap:wrap;
    gap:10px;
  }
  .chip{
    font-family:var(--mono);
    font-size:12.5px;
    padding:8px 12px;
    border:1px solid var(--line-light);
    border-radius:3px;
    background:#F7F5EF;
    color:#3A3A30;
    letter-spacing:.01em;
  }
  .chip::before{
    content:"▪ ";
    color:var(--signal-dim);
  }

  /* experience: ticket cards */
  .ticket{
    border:1px solid var(--line-light);
    background:#F7F5EF;
    border-radius:4px;
    margin-bottom:22px;
    overflow:hidden;
  }

  .ticket-head{
    display:flex;
    align-items:center;
    justify-content:space-between;
    padding:14px 18px;
    background:var(--paper-2);
    border-bottom:1px solid var(--line-light);
    font-family:var(--mono);
    font-size:12px;
    letter-spacing:.04em;
    flex-wrap:wrap;
    gap:8px;
  }
    .ticket-id{ color:var(--muted-light); }

  .badge{
    padding:3px 9px;
    border-radius:20px;
    font-size:11px;
    letter-spacing:.06em;
    text-transform:uppercase;
    font-weight:600;
  }
  .badge.closed{
    background:rgba(46,158,109,.14);
    color:var(--signal-dim);
    border:1px solid rgba(46,158,109,.35);
  }

  .ticket-body{ padding:20px 18px 22px; }

  .ticket-title{
    font-family:var(--mono);
    font-weight:600;
    font-size:18px;
  }

  .ticket-org{
    color:var(--muted-light);
    font-size:14px;
    margin-top:2px;
  }

  .ticket-org strong{ color:#3A3A30; }

  .ticket ul{
    margin-top:14px;
    padding-left:18px;
  }
  .ticket li{
    margin-bottom:7px;
    font-size:14.5px;
    color:#3A3A30;
  }
  .ticket li::marker{ color:var(--signal-dim); }

  /* education: log entries */
  .log{
    border-left:2px solid var(--line-light);
    padding-left:22px;
  }
  .log-entry{
    position:relative;
    margin-bottom:30px;
  }
  .log-entry:last-child{ margin-bottom:0; }
  .log-entry::before{
    content:"";
    position:absolute;
    left:-27px;
    top:5px;
    width:9px; height:9px;
    border-radius:50%;
    background:var(--paper);
    border:2px solid var(--signal-dim);
  }
  .log-time{
    font-family:var(--mono);
    font-size:12px;
    color:var(--muted-light);
    letter-spacing:.05em;
  }
  .log-title{
    font-weight:600;
    font-size:16.5px;
    margin-top:4px;
  }
  .log-org{
    color:var(--muted-light);
    font-size:14px;
    margin-top:2px;
  }

  /* technical / languages grid */
  .grid2{
    display:grid;
    grid-template-columns:1fr 1fr;
    gap:36px;
  }
  @media (max-width:640px){
    .grid2{ grid-template-columns:1fr; }
    .stat-row{ grid-template-columns:1fr; }
    .stat{ border-right:none; border-bottom:1px solid var(--line-dark); padding-bottom:14px; }
  }

  .subhead{
    font-family:var(--mono);
    font-size:12px;
    letter-spacing:.08em;
    text-transform:uppercase;
    color:var(--muted-light);
    margin-bottom:14px;
  }

  .kv{
    display:flex;
    justify-content:space-between;
    padding:9px 0;
    border-bottom:1px dashed var(--line-light);
    font-size:14.5px;
  }
  .kv:last-child{ border-bottom:none; }
  .kv .k{ color:#3A3A30; }
  .kv .v{
    font-family:var(--mono);
    color:var(--signal-dim);
    font-size:13px;
    font-weight:600;
  }

  /* footer / contact */
  footer{
    background:var(--ink);
    color:var(--paper);
    padding:56px 0 40px;
  }

  footer .sec-title{ color:#F5F3EC; }

  .contact-grid{
    display:flex;
    flex-wrap:wrap;
    gap:28px;
    margin-top:24px;
  }

  .contact-item{
    font-family:var(--mono);
    font-size:14px;
  }

  .contact-item .lab{
    display:block;
    font-size:11px;
    letter-spacing:.08em;
    text-transform:uppercase;
    color:var(--muted-dark);
    margin-bottom:6px;
  }

  .contact-item a{
    color:var(--signal);
    text-decoration:none;
    border-bottom:1px solid transparent;
  }
  .contact-item a:hover{ border-bottom-color:var(--signal); }

  .foot-line{
    margin-top:48px;
    padding-top:20px;
    border-top:1px solid var(--line-dark);
    font-family:var(--mono);
    font-size:11.5px;
    color:var(--muted-dark);
    display:flex;
    justify-content:space-between;
    flex-wrap:wrap;
    gap:8px;
  }

</style>
</head>
<body>

<header class="hero">
  <div class="statusbar">
    <span class="path">SIBIYA, T.N.</span>
    <span class="online"><span class="dot"></span>STATUS: ONLINE — OPEN TO WORK</span>
  </div>
  <div class="wrap hero-main">
    <div class="eyebrow">Support Desk Profile</div>
    <h1>Nothile<br>Sibiya<span class="cursor">&nbsp;</span></h1>
    <p class="role">IT Support &amp; Customer Service professional — currently completing a <strong>BIT in Business Systems</strong>, with hands-on experience resolving technical issues and managing client relationships.</p>

    <div class="stat-row">
      <div class="stat">
        <div class="num">3+ yrs</div>
        <div class="lab">Client-facing experience</div>
      </div>
      <div class="stat">
        <div class="num">NQF 5</div>
        <div class="lab">IT Support Services cert.</div>
      </div>
      <div class="stat">
        <div class="num">2</div>
        <div class="lab">Languages — EN / isiZulu</div>
      </div>
    </div>
  </div>
</header>

<main class="wrap">

  <section id="summary" class="reveal">
    <div class="sec-head">
      <span class="sec-num">01</span>
      <h2 class="sec-title">Profile <span class="accent">// summary</span></h2>
    </div>
    <div class="summary">
      <p>A dedicated and customer-focused individual currently pursuing a Bachelor of Information Technology in Business Systems, with hands-on experience in customer service. Skilled across operating systems, networking basics, and hardware &amp; software support — with a track record in customer service and hospitality that's built strong communication, problem-solving, and troubleshooting abilities. Looking to bring technical knowledge and client-first instincts to a team that values both.</p>
    </div>
      </section>

  <section id="skills" class="reveal">
    <div class="sec-head">
      <span class="sec-num">02</span>
      <h2 class="sec-title">Core <span class="accent">// competencies</span></h2>
    </div>
    <div class="chips">
      <span class="chip">Customer Service Excellence</span>
      <span class="chip">Hardware &amp; Software Support</span>
      <span class="chip">Troubleshooting &amp; Problem Resolution</span>
      <span class="chip">Networking Basics</span>
      <span class="chip">Operating Systems (Windows, Linux)</span>
      <span class="chip">Technical Support &amp; Consultation</span>
      <span class="chip">Communication &amp; Interpersonal Skills</span>
      <span class="chip">Time Management &amp; Multitasking</span>
      <span class="chip">Client Relationship Management</span>
      <span class="chip">Adaptability &amp; Learning Agility</span>
      <span class="chip">Technical Documentation</span>
      <span class="chip">SLA Compliance</span>
    </div>
  </section>

  <section id="experience" class="reveal">
    <div class="sec-head">
      <span class="sec-num">03</span>
      <h2 class="sec-title">Ticket <span class="accent">// resolution history</span></h2>
    </div>

    <div class="ticket">
      <div class="ticket-head">
        <span class="ticket-id">TICKET #2022-12 · PRIORITY: HIGH</span>
        <span class="badge closed">Resolved</span>
      </div>
      <div class="ticket-body">
        <div class="ticket-title">Customer Service Agent</div>
        <div class="ticket-org"><strong>Clientele Call Centre</strong> — Dec 2022 – Sep 2024</div>
        <ul>
          <li>Provided outstanding customer service, assisting clients with inquiries, complaints, and product support via phone, email, and chat.</li>
          <li>Troubleshot technical issues related to products and services, offering timely resolutions to ensure customer satisfaction.</li>
          <li>Managed client databases, keeping CRM records accurate and up to date.</li>
          <li>Maintained detailed records of client interactions and service requests for quality control.</li>
          <li>Consistently met or exceeded service delivery standards and sales targets, improving client retention.</li>
        </ul>
      </div>
    </div>

    <div class="ticket">
      <div class="ticket-head">
        <span class="ticket-id">TICKET #2021-06 · PRIORITY: MEDIUM</span>
        <span class="badge closed">Resolved</span>
      </div>
      <div class="ticket-body">
        <div class="ticket-title">Waitress</div>
        <div class="ticket-org"><strong>Wimpy</strong> — Jun 2021 – Mar 2022</div>
        <ul>
          <li>Delivered high-quality customer service, ensuring a welcoming and pleasant dining experience.</li>
          <li>Took customer orders, recommended menu items, and ensured timely service of food and beverages.</li>
          <li>Addressed customer concerns and resolved complaints professionally and courteously.</li>
          <li>Maintained cleanliness and organisation of the dining area to hygiene standards.</li>
          <li>Handled cash and card transactions, ensuring accurate billing and timely processing.</li>
        </ul>
      </div>
    </div>
  </section>

  <section id="education" class="reveal">
    <div class="sec-head">
      <span class="sec-num">04</span>
      <h2 class="sec-title">System <span class="accent">// education log</span></h2>
    </div>
    <div class="log">
      <div class="log-entry">
        <div class="log-time">2024</div>
        <div class="log-title">Higher Certificate in Information Technology in Support Services (NQF Lvl 5)</div>
        <div class="log-org">IIE Rosebank College</div>
      </div>
      <div class="log-entry">
        <div class="log-time">2021</div>
        <div class="log-title">National Senior Certificate (Matric)</div>
        <div class="log-org">Ethangeni Combined School</div>
      </div>
      <div class="log-entry">
        <div class="log-time">In progress</div>
        <div class="log-title">Bachelor of Information Technology in Business Systems</div>
        <div class="log-org">Current studies</div>
      </div>
    </div>
  </section>

  <section id="technical" class="reveal">
    <div class="sec-head">
      <span class="sec-num">05</span>
      <h2 class="sec-title">Technical <span class="accent">// &amp; languages</span></h2>
    </div>
    <div class="grid2">
      <div>
        <div class="subhead">Technical Skills</div>
        <div class="kv"><span class="k">Operating Systems</span><span class="v">WIN / LINUX</span></div>
        <div class="kv"><span class="k">Networking</span><span class="v">BASICS</span></div>
        <div class="kv"><span class="k">Hardware &amp; Software Support</span><span class="v">ACTIVE</span></div>
        <div class="kv"><span class="k">Troubleshooting</span><span class="v">ACTIVE</span></div>
        <div class="kv"><span class="k">Microsoft Office</span><span class="v">EXCEL / WORD / PPT</span></div>
        <div class="kv"><span class="k">CRM Systems</span><span class="v">ACTIVE</span></div>
      </div>
      <div>
        <div class="subhead">Languages</div>
        <div class="kv"><span class="k">English</span><span class="v">FLUENT</span></div>
        <div class="kv"><span class="k">isiZulu</span><span class="v">FLUENT</span></div>
      </div>
    </div>
  </section>

</main>

<footer>
  <div class="wrap">
    <div class="sec-head">
      <span class="sec-num">06</span>
      <h2 class="sec-title">Open <span class="accent">// a ticket</span></h2>
    </div>
    <p style="max-width:50ch; color:var(--muted-dark); font-size:15px;">Available for opportunities in IT support and customer service. Reach out below — references available on request.</p>

    <div class="contact-grid">
      <div class="contact-item">
        <span class="lab">Email</span>
        <a href="mailto:sibiyathobeza@gmail.com">sibiyathobeza@gmail.com</a>
      </div>
      <div class="contact-item">
        <span class="lab">Phone</span>
        <a href="tel:0676198059">067 619 8059</a>
      </div>
      <div class="contact-item">
        <span class="lab">Location</span>
        <span>Durban, South Africa</span>
      </div>
    </div>
  <div class="wrap">
    <div class="sec-head">
      <span class="sec-num">06</span>
      <h2 class="sec-title">Open <span class="accent">// a ticket</span></h2>
    </div>
    <p style="max-width:50ch; color:var(--muted-dark); font-size:15px;">Available for opportunities in IT support and customer service. Reach out below — references available on request.</p>

    <div class="contact-grid">
      <div class="contact-item">
        <span class="lab">Email</span>
        <a href="mailto:sibiyathobeza@gmail.com">sibiyathobeza@gmail.com</a>
      </div>
      <div class="contact-item">
        <span class="lab">Phone</span>
        <a href="tel:0676198059">067 619 8059</a>
      </div>
      <div class="contact-item">
        <span class="lab">Location</span>
        <span>Durban, South Africa</span>
      </div>
    </div>

    <div class="foot-line">
      <span>© 2026 T.N. Sibiya</span>
      <span>session closed — thank you for visiting</span>
    </div>
  </div>
</footer>

<script>
  const items = document.querySelectorAll('.reveal');
  const io = new IntersectionObserver((entries)=>{
    entries.forEach(e=>{
      if(e.isIntersecting){
        e.target.classList.add('in');
        io.unobserve(e.target);
      }
    });
  }, { threshold: 0.12 });
  items.forEach(i=>io.observe(i));
</script>

</body>
</html>
    <div class="foot-line">
      <span>© 2026 T.N. Sibiya</span>
      <span>session closed — thank you for visiting</span>
    </div>
  </div>
</footer>
