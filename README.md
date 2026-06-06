
<style>
  @import url('https://fonts.googleapis.com/css2?family=DM+Mono:wght@400;500&family=Sora:wght@300;400;500;600&display=swap');
  .rm-wrap { font-family: 'Sora', sans-serif; max-width: 680px; margin: 0 auto; padding: 1.5rem 0; color: var(--color-text-primary); }
  .rm-header { border-bottom: 0.5px solid var(--color-border-tertiary); padding-bottom: 1.5rem; margin-bottom: 1.5rem; }
  .rm-greeting { font-size: 13px; font-weight: 400; color: var(--color-text-secondary); letter-spacing: 0.08em; text-transform: uppercase; margin: 0 0 6px; }
  .rm-name { font-size: 28px; font-weight: 600; margin: 0 0 4px; }
  .rm-tagline { font-size: 14px; color: var(--color-text-secondary); font-weight: 300; margin: 0 0 16px; }
  .rm-badges { display: flex; flex-wrap: wrap; gap: 8px; margin-bottom: 12px; }
  .badge { font-family: 'DM Mono', monospace; font-size: 11px; padding: 4px 10px; border-radius: 4px; background: var(--color-background-secondary); border: 0.5px solid var(--color-border-tertiary); color: var(--color-text-secondary); }
  .badge.open { background: #EAF3DE; color: #3B6D11; border-color: #97C459; }
  .section { margin-bottom: 1.75rem; }
  .section-label { font-family: 'DM Mono', monospace; font-size: 11px; letter-spacing: 0.1em; text-transform: uppercase; color: var(--color-text-secondary); margin: 0 0 10px; display: flex; align-items: center; gap: 8px; }
  .section-label::after { content: ''; flex: 1; height: 0.5px; background: var(--color-border-tertiary); }
  .about-text { font-size: 14px; line-height: 1.8; color: var(--color-text-primary); margin: 0; }
  .about-text em { font-style: normal; color: var(--color-text-secondary); }
  .stack-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(130px, 1fr)); gap: 8px; }
  .stack-item { background: var(--color-background-secondary); border: 0.5px solid var(--color-border-tertiary); border-radius: var(--border-radius-md); padding: 10px 12px; display: flex; align-items: center; gap: 8px; font-size: 13px; font-weight: 500; }
  .stack-dot { width: 8px; height: 8px; border-radius: 50%; flex-shrink: 0; }
  .dot-php { background: #7F77DD; }
  .dot-js { background: #EF9F27; }
  .dot-py { background: #1D9E75; }
  .dot-cpp { background: #378ADD; }
  .dot-html { background: #D85A30; }
  .dot-css { background: #D4537E; }
  .dot-sql { background: #888780; }
  .dot-git { background: #E24B4A; }
  .projects-grid { display: grid; gap: 10px; }
  .project-card { background: var(--color-background-primary); border: 0.5px solid var(--color-border-tertiary); border-radius: var(--border-radius-lg); padding: 14px 16px; cursor: pointer; transition: border-color 0.2s; }
  .project-card:hover { border-color: var(--color-border-secondary); }
  .project-top { display: flex; justify-content: space-between; align-items: flex-start; margin-bottom: 6px; }
  .project-name { font-size: 14px; font-weight: 500; margin: 0; }
  .project-link { font-family: 'DM Mono', monospace; font-size: 11px; color: var(--color-text-secondary); text-decoration: none; }
  .project-link:hover { color: var(--color-text-primary); }
  .project-desc { font-size: 13px; color: var(--color-text-secondary); line-height: 1.6; margin: 0 0 10px; }
  .project-tags { display: flex; gap: 6px; flex-wrap: wrap; }
  .tag { font-family: 'DM Mono', monospace; font-size: 10px; padding: 2px 7px; border-radius: 3px; background: var(--color-background-secondary); color: var(--color-text-secondary); border: 0.5px solid var(--color-border-tertiary); }
  .stats-row { display: grid; grid-template-columns: repeat(auto-fit, minmax(140px, 1fr)); gap: 8px; }
  .stat-card { background: var(--color-background-secondary); border-radius: var(--border-radius-md); padding: 12px 14px; text-align: center; }
  .stat-num { font-size: 22px; font-weight: 500; margin: 0 0 2px; }
  .stat-lbl { font-family: 'DM Mono', monospace; font-size: 11px; color: var(--color-text-secondary); margin: 0; }
  .contact-row { display: flex; flex-wrap: wrap; gap: 8px; }
  .contact-btn { font-size: 13px; padding: 8px 14px; border-radius: var(--border-radius-md); border: 0.5px solid var(--color-border-tertiary); background: var(--color-background-primary); color: var(--color-text-primary); cursor: pointer; display: flex; align-items: center; gap: 6px; font-family: 'Sora', sans-serif; transition: border-color 0.2s, background 0.2s; }
  .contact-btn:hover { border-color: var(--color-border-secondary); background: var(--color-background-secondary); }
  .fun-bar { background: var(--color-background-secondary); border-radius: var(--border-radius-md); padding: 12px 16px; font-size: 13px; color: var(--color-text-secondary); display: flex; align-items: center; gap: 10px; border-left: 2px solid #7F77DD; border-radius: 0 var(--border-radius-md) var(--border-radius-md) 0; }
  .copy-hint { background: var(--color-background-secondary); border: 0.5px solid var(--color-border-tertiary); border-radius: var(--border-radius-md); padding: 10px 14px; display: flex; justify-content: space-between; align-items: center; margin-top: 1.5rem; }
  .copy-hint p { font-size: 12px; color: var(--color-text-secondary); margin: 0; }
  .copy-btn { font-family: 'DM Mono', monospace; font-size: 11px; padding: 5px 12px; border-radius: 4px; border: 0.5px solid var(--color-border-secondary); background: var(--color-background-primary); color: var(--color-text-primary); cursor: pointer; }
  .copy-btn:hover { background: var(--color-background-secondary); }
</style>

<div class="rm-wrap">
  <h2 class="sr-only">GitHub README preview for Dalha</h2>

  <div class="rm-header">
    <p class="rm-greeting">Hi there, I'm</p>
    <h1 class="rm-name">Dalha <span style="font-weight:300; color:var(--color-text-secondary);">/ dalhaldalha</span></h1>
    <p class="rm-tagline">Full-Stack Developer · Building things for the web</p>
    <div class="rm-badges">
      <span class="badge open">Open to opportunities</span>
      <span class="badge"><i class="ti ti-map-pin" aria-hidden="true" style="font-size:12px;vertical-align:-1px;margin-right:3px"></i>Nigeria</span>
      <span class="badge"><i class="ti ti-book" aria-hidden="true" style="font-size:12px;vertical-align:-1px;margin-right:3px"></i>Sci-fi & Dystopian reader</span>
    </div>
  </div>

  <div class="section">
    <p class="section-label">About me</p>
    <p class="about-text">
      I'm a full-stack developer passionate about crafting clean, functional web experiences — from server-side logic to polished interfaces. I love working across the entire stack, bringing ideas to life with code. <em>When I'm not writing code, you'll likely find me deep in a dystopian or sci-fi novel.</em>
    </p>
  </div>

  <div class="section">
    <p class="section-label">Tech stack</p>
    <div class="stack-grid">
      <div class="stack-item"><span class="stack-dot dot-php"></span>PHP</div>
      <div class="stack-item"><span class="stack-dot dot-js"></span>JavaScript</div>
      <div class="stack-item"><span class="stack-dot dot-py"></span>Python</div>
      <div class="stack-item"><span class="stack-dot dot-cpp"></span>C++</div>
      <div class="stack-item"><span class="stack-dot dot-html"></span>HTML5</div>
      <div class="stack-item"><span class="stack-dot dot-css"></span>CSS3</div>
      <div class="stack-item"><span class="stack-dot dot-sql"></span>SQL</div>
      <div class="stack-item"><span class="stack-dot dot-git"></span>Git</div>
    </div>
  </div>

  <div class="section">
    <p class="section-label">Featured projects</p>
    <div class="projects-grid">
      <div class="project-card">
        <div class="project-top">
          <p class="project-name">HMD Limited</p>
          <a class="project-link" href="https://hmdlimited.com/" target="_blank">hmdlimited.com <i class="ti ti-external-link" aria-hidden="true" style="font-size:11px;vertical-align:-1px"></i></a>
        </div>
        <p class="project-desc">A multi-service website for a firm specialising in construction, real estate, and land surveying — built for clarity and client trust.</p>
        <div class="project-tags">
          <span class="tag">Web Dev</span>
          <span class="tag">Full-Stack</span>
          <span class="tag">Real Estate</span>
        </div>
      </div>
      <div class="project-card">
        <div class="project-top">
          <p class="project-name">Personal Portfolio</p>
          <span class="project-link">dalhaldalha</span>
        </div>
        <p class="project-desc">My personal portfolio — a curated space showcasing my background, skills, and the projects I've built along the way.</p>
        <div class="project-tags">
          <span class="tag">Portfolio</span>
          <span class="tag">Design</span>
          <span class="tag">Frontend</span>
        </div>
      </div>
    </div>
  </div>

  <div class="section">
    <p class="section-label">GitHub stats</p>
    <div class="stats-row">
      <div class="stat-card">
        <p class="stat-num">★</p>
        <p class="stat-lbl">Stars earned</p>
      </div>
      <div class="stat-card">
        <p class="stat-num"><i class="ti ti-git-commit" aria-hidden="true" style="font-size:20px;color:var(--color-text-secondary)"></i></p>
        <p class="stat-lbl">Commits (via badge)</p>
      </div>
      <div class="stat-card">
        <p class="stat-num"><i class="ti ti-flame" aria-hidden="true" style="font-size:20px;color:var(--color-text-secondary)"></i></p>
        <p class="stat-lbl">Streak (via badge)</p>
      </div>
    </div>
    <p style="font-size:12px;color:var(--color-text-secondary);margin:10px 0 0;font-family:'DM Mono',monospace;">Live stats powered by github-readme-stats & streak-stats shields</p>
  </div>

  <div class="section">
    <p class="section-label">Fun fact</p>
    <div class="fun-bar">
      <i class="ti ti-book-2" aria-hidden="true" style="font-size:18px;color:#7F77DD;flex-shrink:0"></i>
      <span>Currently somewhere between a dystopia and a space opera — avid reader of sci-fi and dystopian fiction.</span>
    </div>
  </div>

  <div class="section">
    <p class="section-label">Contact</p>
    <div class="contact-row">
      <button class="contact-btn"><i class="ti ti-mail" aria-hidden="true" style="font-size:15px"></i> Email</button>
      <button class="contact-btn"><i class="ti ti-brand-linkedin" aria-hidden="true" style="font-size:15px"></i> LinkedIn</button>
      <button class="contact-btn"><i class="ti ti-brand-twitter" aria-hidden="true" style="font-size:15px"></i> Twitter</button>
      <button class="contact-btn"><i class="ti ti-globe" aria-hidden="true" style="font-size:15px"></i> Portfolio</button>
    </div>
  </div>

  <div class="copy-hint">
    <p>Ready to generate the <code>.md</code> file? Ask me to create it and I'll output the full Markdown.</p>
    <button class="copy-btn" onclick="sendPrompt('Generate the full Markdown file for this README')">Generate .md file ↗</button>
  </div>
</div>
