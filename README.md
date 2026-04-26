<!DOCTYPE html>
<html lang="pt-BR">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Hernani Lemos — Analista de Negócios, Projetos & Implantação</title>
<link href="https://fonts.googleapis.com/css2?family=Syne:wght@400;500;600;700;800&family=DM+Sans:ital,wght@0,300;0,400;0,500;1,300&display=swap" rel="stylesheet">
<style>
  *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }
  :root {
    --bg: #0a0e1a; --bg2: #111827; --bg3: #1a2235;
    --accent: #3b82f6; --accent2: #06b6d4; --accent3: #8b5cf6;
    --text: #f1f5f9; --text2: #94a3b8; --text3: #64748b;
    --border: rgba(255,255,255,0.07); --card: rgba(255,255,255,0.04);
  }
  html { scroll-behavior: smooth; }
  body { background: var(--bg); color: var(--text); font-family: 'DM Sans', sans-serif; font-size: 16px; line-height: 1.6; overflow-x: hidden; }
  body::before { content: ''; position: fixed; inset: 0; background-image: linear-gradient(rgba(59,130,246,0.03) 1px, transparent 1px), linear-gradient(90deg, rgba(59,130,246,0.03) 1px, transparent 1px); background-size: 60px 60px; pointer-events: none; z-index: 0; }
  .orb { position: fixed; border-radius: 50%; filter: blur(100px); pointer-events: none; z-index: 0; }
  .orb-1 { width: 600px; height: 600px; background: rgba(59,130,246,0.08); top: -200px; right: -100px; }
  .orb-2 { width: 400px; height: 400px; background: rgba(139,92,246,0.06); bottom: 200px; left: -100px; }
  .orb-3 { width: 300px; height: 300px; background: rgba(6,182,212,0.05); top: 50%; left: 50%; }
  nav { position: fixed; top: 0; left: 0; right: 0; z-index: 100; display: flex; align-items: center; justify-content: space-between; padding: 20px 60px; background: rgba(10,14,26,0.8); backdrop-filter: blur(16px); border-bottom: 1px solid var(--border); }
  .nav-logo { font-family: 'Syne', sans-serif; font-weight: 800; font-size: 18px; background: linear-gradient(135deg, var(--accent), var(--accent2)); -webkit-background-clip: text; -webkit-text-fill-color: transparent; }
  .nav-links { display: flex; gap: 32px; list-style: none; }
  .nav-links a { text-decoration: none; color: var(--text2); font-size: 13px; font-weight: 500; letter-spacing: 0.04em; text-transform: uppercase; transition: color 0.2s; }
  .nav-links a:hover { color: var(--text); }
  section { position: relative; z-index: 1; }
  #hero { min-height: 100vh; display: flex; align-items: center; padding: 120px 60px 80px; max-width: 1200px; margin: 0 auto; }
  .hero-inner { max-width: 780px; }
  .hero-badge { display: inline-flex; align-items: center; gap: 8px; padding: 6px 16px; border: 1px solid rgba(59,130,246,0.3); border-radius: 100px; font-size: 12px; color: var(--accent); font-weight: 500; letter-spacing: 0.06em; text-transform: uppercase; margin-bottom: 28px; background: rgba(59,130,246,0.05); }
  .hero-badge::before { content: ''; width: 6px; height: 6px; border-radius: 50%; background: var(--accent); animation: pulse 2s infinite; }
  @keyframes pulse { 0%, 100% { opacity: 1; transform: scale(1); } 50% { opacity: 0.5; transform: scale(1.3); } }
  h1 { font-family: 'Syne', sans-serif; font-size: clamp(48px, 7vw, 80px); font-weight: 800; line-height: 1.0; letter-spacing: -2px; margin-bottom: 24px; }
  h1 .name-line { display: block; }
  h1 .accent-line { display: block; background: linear-gradient(135deg, var(--accent) 0%, var(--accent2) 50%, var(--accent3) 100%); -webkit-background-clip: text; -webkit-text-fill-color: transparent; }
  .hero-desc { font-size: 18px; color: var(--text2); font-weight: 300; line-height: 1.7; max-width: 560px; margin-bottom: 40px; }
  .hero-ctas { display: flex; gap: 16px; flex-wrap: wrap; margin-bottom: 64px; }
  .btn-primary { display: inline-flex; align-items: center; gap: 8px; padding: 14px 28px; background: var(--accent); color: #fff; border-radius: 10px; text-decoration: none; font-weight: 500; font-size: 15px; transition: all 0.2s; border: none; cursor: pointer; }
  .btn-primary:hover { background: #2563eb; transform: translateY(-1px); box-shadow: 0 8px 30px rgba(59,130,246,0.3); }
  .btn-secondary { display: inline-flex; align-items: center; gap: 8px; padding: 14px 28px; background: transparent; color: var(--text); border-radius: 10px; text-decoration: none; font-weight: 500; font-size: 15px; border: 1px solid var(--border); transition: all 0.2s; }
  .btn-secondary:hover { background: var(--card); border-color: rgba(255,255,255,0.15); }
  .hero-stats { display: flex; gap: 48px; padding-top: 40px; border-top: 1px solid var(--border); }
  .stat-num { font-family: 'Syne', sans-serif; font-size: 36px; font-weight: 800; background: linear-gradient(135deg, var(--accent), var(--accent2)); -webkit-background-clip: text; -webkit-text-fill-color: transparent; display: block; }
  .stat-label { font-size: 13px; color: var(--text3); }
  .container { max-width: 1200px; margin: 0 auto; padding: 80px 60px; }
  .section-tag { font-size: 11px; font-weight: 600; letter-spacing: 0.12em; text-transform: uppercase; color: var(--accent); margin-bottom: 12px; display: block; }
  .section-title { font-family: 'Syne', sans-serif; font-size: clamp(32px, 4vw, 46px); font-weight: 700; letter-spacing: -1px; line-height: 1.1; margin-bottom: 16px; }
  .section-sub { font-size: 16px; color: var(--text2); font-weight: 300; max-width: 560px; margin-bottom: 56px; }
  #sobre { background: var(--bg2); }
  .sobre-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 60px; align-items: start; }
  .sobre-text p { color: var(--text2); font-size: 15px; line-height: 1.8; margin-bottom: 20px; }
  .sobre-text p strong { color: var(--text); font-weight: 500; }
  .sobre-info { display: flex; flex-direction: column; gap: 16px; margin-top: 32px; }
  .info-item { display: flex; align-items: center; gap: 12px; font-size: 14px; color: var(--text2); }
  .info-icon { width: 36px; height: 36px; border-radius: 8px; background: var(--card); border: 1px solid var(--border); display: flex; align-items: center; justify-content: center; font-size: 15px; flex-shrink: 0; }
  .sobre-right { display: flex; flex-direction: column; gap: 16px; }
  .skill-category { background: var(--card); border: 1px solid var(--border); border-radius: 12px; padding: 20px 24px; }
  .skill-cat-title { font-size: 11px; font-weight: 600; letter-spacing: 0.1em; text-transform: uppercase; color: var(--text3); margin-bottom: 14px; }
  .skill-tags { display: flex; flex-wrap: wrap; gap: 8px; }
  .skill-tag { padding: 5px 12px; border-radius: 6px; font-size: 12px; font-weight: 500; background: rgba(255,255,255,0.06); color: var(--text2); border: 1px solid var(--border); }
  .skill-tag.blue { background: rgba(59,130,246,0.1); color: #93c5fd; border-color: rgba(59,130,246,0.2); }
  .skill-tag.teal { background: rgba(6,182,212,0.1); color: #67e8f9; border-color: rgba(6,182,212,0.2); }
  .skill-tag.purple { background: rgba(139,92,246,0.1); color: #c4b5fd; border-color: rgba(139,92,246,0.2); }
  #numeros { background: var(--bg); }
  .numeros-grid { display: grid; grid-template-columns: repeat(4, 1fr); gap: 1px; background: var(--border); border: 1px solid var(--border); border-radius: 16px; overflow: hidden; }
  .numero-card { background: var(--bg2); padding: 40px 32px; text-align: center; transition: background 0.2s; }
  .numero-card:hover { background: var(--bg3); }
  .numero-val { font-family: 'Syne', sans-serif; font-size: 52px; font-weight: 800; line-height: 1; margin-bottom: 8px; background: linear-gradient(135deg, var(--accent), var(--accent2)); -webkit-background-clip: text; -webkit-text-fill-color: transparent; }
  .numero-label { font-size: 13px; color: var(--text3); line-height: 1.4; }
  #experiencia { background: var(--bg2); }
  .exp-list { display: flex; flex-direction: column; gap: 2px; }
  .exp-card { background: var(--card); border: 1px solid var(--border); border-radius: 16px; padding: 36px 40px; transition: border-color 0.2s, background 0.2s; position: relative; overflow: hidden; }
  .exp-card::before { content: ''; position: absolute; left: 0; top: 0; bottom: 0; width: 3px; background: linear-gradient(180deg, var(--accent), var(--accent2)); opacity: 0; transition: opacity 0.2s; }
  .exp-card:hover { border-color: rgba(59,130,246,0.3); background: rgba(59,130,246,0.04); }
  .exp-card:hover::before { opacity: 1; }
  .exp-header { display: flex; justify-content: space-between; align-items: flex-start; margin-bottom: 20px; gap: 20px; flex-wrap: wrap; }
  .exp-title { font-family: 'Syne', sans-serif; font-size: 20px; font-weight: 700; color: var(--text); margin-bottom: 4px; }
  .exp-company { font-size: 14px; color: var(--accent); font-weight: 500; }
  .exp-period { font-size: 12px; color: var(--text3); background: var(--card); border: 1px solid var(--border); padding: 6px 14px; border-radius: 100px; white-space: nowrap; }
  .exp-bullets { list-style: none; display: flex; flex-direction: column; gap: 8px; margin-bottom: 24px; }
  .exp-bullets li { display: flex; gap: 12px; font-size: 14px; color: var(--text2); line-height: 1.6; }
  .exp-bullets li::before { content: '→'; color: var(--accent); flex-shrink: 0; font-size: 13px; margin-top: 2px; }
  .exp-result { padding: 14px 18px; background: rgba(6,182,212,0.05); border: 1px solid rgba(6,182,212,0.15); border-radius: 10px; font-size: 13px; color: #67e8f9; }
  .exp-result strong { display: block; font-size: 11px; letter-spacing: 0.08em; text-transform: uppercase; margin-bottom: 6px; opacity: 0.7; }
  .exp-tags { display: flex; flex-wrap: wrap; gap: 6px; margin-top: 18px; }
  .exp-tag { font-size: 11px; padding: 4px 10px; border-radius: 5px; background: rgba(255,255,255,0.05); color: var(--text3); border: 1px solid var(--border); }
  #projetos { background: var(--bg); }
  .projeto-card { background: var(--card); border: 1px solid var(--border); border-radius: 20px; padding: 48px; display: grid; grid-template-columns: 1fr 1fr; gap: 60px; align-items: center; position: relative; overflow: hidden; }
  .projeto-card::after { content: ''; position: absolute; top: -100px; right: -100px; width: 400px; height: 400px; background: radial-gradient(circle, rgba(59,130,246,0.08), transparent 70%); pointer-events: none; }
  .projeto-badge { display: inline-block; padding: 4px 12px; border-radius: 100px; font-size: 11px; font-weight: 600; letter-spacing: 0.08em; text-transform: uppercase; background: rgba(139,92,246,0.15); color: #c4b5fd; border: 1px solid rgba(139,92,246,0.3); margin-bottom: 20px; }
  .projeto-title { font-family: 'Syne', sans-serif; font-size: 32px; font-weight: 800; letter-spacing: -1px; margin-bottom: 16px; }
  .projeto-desc { font-size: 15px; color: var(--text2); line-height: 1.7; margin-bottom: 28px; }
  .projeto-features { list-style: none; display: flex; flex-direction: column; gap: 12px; }
  .projeto-features li { display: flex; align-items: center; gap: 12px; font-size: 14px; color: var(--text2); }
  .feat-dot { width: 8px; height: 8px; border-radius: 50%; background: var(--accent2); flex-shrink: 0; }
  .projeto-visual { background: var(--bg3); border: 1px solid var(--border); border-radius: 14px; padding: 32px; display: flex; flex-direction: column; gap: 16px; }
  .tech-item { display: flex; align-items: center; justify-content: space-between; font-size: 13px; }
  .tech-name { color: var(--text2); }
  .tech-bar-bg { flex: 1; height: 4px; background: rgba(255,255,255,0.05); border-radius: 2px; margin: 0 16px; overflow: hidden; }
  .tech-bar { height: 100%; border-radius: 2px; background: linear-gradient(90deg, var(--accent), var(--accent2)); }
  .tech-val { color: var(--text3); font-size: 12px; }
  #formacao { background: var(--bg2); }
  .form-cert-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 24px; }
  .form-card { background: var(--card); border: 1px solid var(--border); border-radius: 14px; padding: 28px 32px; display: flex; gap: 20px; align-items: flex-start; transition: border-color 0.2s; }
  .form-card:hover { border-color: rgba(59,130,246,0.3); }
  .form-icon { width: 44px; height: 44px; border-radius: 10px; display: flex; align-items: center; justify-content: center; font-size: 20px; flex-shrink: 0; }
  .form-icon.blue { background: rgba(59,130,246,0.1); }
  .form-icon.teal { background: rgba(6,182,212,0.1); }
  .form-icon.purple { background: rgba(139,92,246,0.1); }
  .form-title { font-size: 15px; font-weight: 500; color: var(--text); margin-bottom: 4px; }
  .form-sub { font-size: 13px; color: var(--text2); margin-bottom: 6px; }
  .form-year { font-size: 12px; color: var(--text3); }
  #contato { background: var(--bg); }
  .contato-box { background: linear-gradient(135deg, rgba(59,130,246,0.08), rgba(6,182,212,0.05)); border: 1px solid rgba(59,130,246,0.2); border-radius: 20px; padding: 64px; text-align: center; position: relative; overflow: hidden; }
  .contato-box::before { content: ''; position: absolute; inset: 0; background: radial-gradient(ellipse at center top, rgba(59,130,246,0.1), transparent 60%); pointer-events: none; }
  .contato-title { font-family: 'Syne', sans-serif; font-size: 40px; font-weight: 800; letter-spacing: -1px; margin-bottom: 16px; position: relative; }
  .contato-sub { font-size: 16px; color: var(--text2); margin-bottom: 40px; position: relative; }
  .contato-links { display: flex; justify-content: center; gap: 16px; flex-wrap: wrap; position: relative; }
  .contato-link { display: flex; align-items: center; gap: 10px; padding: 14px 24px; border-radius: 10px; font-size: 14px; font-weight: 500; text-decoration: none; transition: all 0.2s; border: 1px solid var(--border); background: rgba(255,255,255,0.04); color: var(--text); }
  .contato-link:hover { background: rgba(255,255,255,0.08); transform: translateY(-2px); }
  .contato-link .link-icon { font-size: 18px; }
  footer { background: var(--bg2); border-top: 1px solid var(--border); padding: 28px 60px; display: flex; justify-content: space-between; align-items: center; position: relative; z-index: 1; }
  footer p { font-size: 13px; color: var(--text3); }
  .fade-in { opacity: 0; transform: translateY(24px); transition: opacity 0.6s ease, transform 0.6s ease; }
  .fade-in.visible { opacity: 1; transform: translateY(0); }
  @media (max-width: 900px) {
    nav { padding: 16px 24px; } .nav-links { display: none; }
    #hero { padding: 100px 24px 60px; } .container { padding: 60px 24px; }
    .sobre-grid, .projeto-card, .form-cert-grid { grid-template-columns: 1fr; gap: 32px; }
    .numeros-grid { grid-template-columns: repeat(2, 1fr); }
    .hero-stats { gap: 28px; flex-wrap: wrap; }
    .contato-box { padding: 40px 24px; }
    footer { flex-direction: column; gap: 8px; text-align: center; padding: 24px; }
  }
</style>
</head>
<body>

<div class="orb orb-1"></div>
<div class="orb orb-2"></div>
<div class="orb orb-3"></div>

<nav>
  <div class="nav-logo">HL</div>
  <ul class="nav-links">
    <li><a href="#sobre">Sobre</a></li>
    <li><a href="#numeros">Números</a></li>
    <li><a href="#experiencia">Experiência</a></li>
    <li><a href="#projetos">Projetos</a></li>
    <li><a href="#formacao">Formação</a></li>
    <li><a href="#contato">Contato</a></li>
  </ul>
</nav>

<div style="position: relative; z-index: 1;">
<section id="hero">
  <div class="hero-inner fade-in">
    <div class="hero-badge">Disponível para novas oportunidades</div>
    <h1>
      <span class="name-line">Hernani Lemos</span>
      <span class="accent-line">Analista de Negócios,</span>
      <span class="name-line" style="font-size:clamp(32px,4.5vw,54px);color:var(--text2);font-weight:600">Projetos & Implantação</span>
    </h1>
    <p class="hero-desc">
      Mais de 7 anos conectando tecnologia e saúde pública — implantando sistemas em escala nacional, liderando equipes e entregando resultados que impactam municípios reais.
    </p>
    <div class="hero-ctas">
      <a href="#contato" class="btn-primary">Falar comigo →</a>
      <a href="#experiencia" class="btn-secondary">Ver experiência</a>
    </div>
    <div class="hero-stats">
      <div><span class="stat-num">100+</span><span class="stat-label">Municípios implantados</span></div>
      <div><span class="stat-num">15+</span><span class="stat-label">Estados brasileiros</span></div>
      <div><span class="stat-num">5000+</span><span class="stat-label">Profissionais treinados</span></div>
      <div><span class="stat-num">7+</span><span class="stat-label">Anos de experiência</span></div>
    </div>
  </div>
</section>
</div>

<section id="sobre">
  <div class="container">
    <span class="section-tag fade-in">Quem sou</span>
    <h2 class="section-title fade-in">Perfil profissional</h2>
    <div class="sobre-grid fade-in">
      <div class="sobre-text">
        <p>Profissional com <strong>sólida experiência como Analista de Negócios e Sistemas</strong>, com destaque em projetos do setor de saúde pública voltados ao Ministério da Saúde. Graduado em Análise e Desenvolvimento de Sistemas.</p>
        <p>Responsável por <strong>coordenar implantações de sistemas em larga escala</strong> — atuando em mais de 100 municípios espalhados por mais de 15 estados do Brasil — garantindo conformidade técnica, eficiência operacional e satisfação dos clientes.</p>
        <p>Experiência em <strong>licitações, elaboração de propostas técnicas, provas de conceito e negociações</strong>, com foco em soluções personalizadas. <strong>Ex-líder da equipe de suporte técnico</strong>, padronizando processos e desenvolvendo metodologias de atendimento humanizado que se tornaram referência interna.</p>
        <p>Busca oportunidades na área de análise de negócios e projetos, aplicando <strong>versatilidade, visão estratégica e liderança</strong> para conduzir implantações de alto impacto.</p>
        <div class="sobre-info">
          <div class="info-item"><div class="info-icon">📍</div> Salvador, Bahia — Brasil</div>
          <div class="info-item"><div class="info-icon">📞</div> (71) 9.9208-1968</div>
          <div class="info-item"><div class="info-icon">✉️</div> lemosh.ads@gmail.com</div>
        </div>
      </div>
      <div class="sobre-right">
        <div class="skill-category">
          <div class="skill-cat-title">Análise & Negócios</div>
          <div class="skill-tags">
            <span class="skill-tag blue">Análise de Requisitos</span>
            <span class="skill-tag blue">User Stories</span>
            <span class="skill-tag blue">Mapeamento de Processos</span>
            <span class="skill-tag blue">Product Owner</span>
            <span class="skill-tag blue">Stakeholder Management</span>
          </div>
        </div>
        <div class="skill-category">
          <div class="skill-cat-title">Gestão de Projetos</div>
          <div class="skill-tags">
            <span class="skill-tag teal">Scrum</span>
            <span class="skill-tag teal">Kanban</span>
            <span class="skill-tag teal">Cronogramas</span>
            <span class="skill-tag teal">Implantação</span>
            <span class="skill-tag teal">Liderança Técnica</span>
          </div>
        </div>
        <div class="skill-category">
          <div class="skill-cat-title">Ferramentas</div>
          <div class="skill-tags">
            <span class="skill-tag purple">Jira</span>
            <span class="skill-tag purple">Monday</span>
            <span class="skill-tag purple">Trello</span>
            <span class="skill-tag purple">Notion</span>
            <span class="skill-tag purple">SAP</span>
            <span class="skill-tag purple">SQL Server</span>
            <span class="skill-tag purple">Bitrix24</span>
          </div>
        </div>
        <div class="skill-category">
          <div class="skill-cat-title">Sistemas de Saúde</div>
          <div class="skill-tags">
            <span class="skill-tag">PEC</span>
            <span class="skill-tag">SISAB</span>
            <span class="skill-tag">SISPNCD</span>
            <span class="skill-tag">SEI</span>
            <span class="skill-tag">+ACE / Horizon</span>
          </div>
        </div>
      </div>
    </div>
  </div>
</section>

<section id="numeros">
  <div class="container">
    <span class="section-tag fade-in">Impacto em números</span>
    <h2 class="section-title fade-in">Resultados que falam</h2>
    <div class="numeros-grid fade-in">
      <div class="numero-card"><div class="numero-val">100+</div><div class="numero-label">Municípios com sistemas implantados</div></div>
      <div class="numero-card"><div class="numero-val">15+</div><div class="numero-label">Estados brasileiros atendidos</div></div>
      <div class="numero-card"><div class="numero-val">5000+</div><div class="numero-label">Profissionais de saúde treinados</div></div>
      <div class="numero-card"><div class="numero-val">20+</div><div class="numero-label">Cidades com treinamentos presenciais</div></div>
    </div>
  </div>
</section>

<section id="experiencia">
  <div class="container">
    <span class="section-tag fade-in">Trajetória</span>
    <h2 class="section-title fade-in">Experiência profissional</h2>
    <p class="section-sub fade-in">Histórico de atuação com foco em implantação, análise e gestão de projetos de tecnologia no setor público.</p>
    <div class="exp-list">

      <div class="exp-card fade-in">
        <div class="exp-header">
          <div><div class="exp-title">Analista de Negócios Pleno</div><div class="exp-company">Qintess</div></div>
          <div class="exp-period">Jul/2025 – Atual</div>
        </div>
        <ul class="exp-bullets">
          <li>Análise e otimização de processos de negócios, promovendo eficiência operacional e melhores resultados.</li>
          <li>Apresentação do cronograma de implantação do Sistema SEI, detalhando etapas, marcos e prazos.</li>
          <li>Reuniões estratégicas de alinhamento para implantação do Projeto SEI Bahia Municípios.</li>
          <li>Identificação de oportunidades de melhoria, avaliando gaps e propondo ajustes estratégicos.</li>
          <li>Solicitação de estruturação para cadastros de Unidades, Equipes e Usuários no sistema SEI.</li>
        </ul>
        <div class="exp-result">
          <strong>Resultado de destaque</strong>
          Implementação e gestão de fluxo estruturado de prospecção para qualificação de leads e priorização de municípios baianos interessados no Projeto SEI.
        </div>
        <div class="exp-tags">
          <span class="exp-tag">Análise de Processos</span><span class="exp-tag">Avaliação de Gaps</span>
          <span class="exp-tag">Stakeholders</span><span class="exp-tag">SEI</span><span class="exp-tag">Relatórios</span>
        </div>
      </div>

      <div class="exp-card fade-in">
        <div class="exp-header">
          <div><div class="exp-title">Analista de Negócios e Projetos</div><div class="exp-company">Horizon Inovação e Tecnologia</div></div>
          <div class="exp-period">Mai/2018 – Mai/2025</div>
        </div>
        <ul class="exp-bullets">
          <li>Implantação de sistemas em mais de 100 municípios espalhados por mais de 15 estados do Brasil.</li>
          <li><strong style="color:var(--text)">Liderança da equipe de suporte técnico</strong>, padronizando processos e agilizando resolução de problemas.</li>
          <li>Condução de projetos com metodologias ágeis (Scrum e Kanban), organizando demandas e priorizando entregas.</li>
          <li>Levantamento, análise e documentação de requisitos por meio da construção de histórias de usuário.</li>
          <li>Treinamento de mais de 5.000 profissionais da saúde em mais de 20 cidades.</li>
          <li>Gerenciamento dos projetos PEC, SISAB e SISPNCD — planejamento, cronogramas e acompanhamento pós-implantação.</li>
          <li>Representação da empresa em eventos nacionais e consórcios intermunicipais; liderança técnica em licitações e provas de conceito.</li>
        </ul>
        <div class="exp-result">
          <strong>Resultado de destaque</strong>
          Concepção e implantação de metodologia de atendimento humanizado que aumentou a confiança nos sistemas e a adoção das soluções nos municípios — tornando-se base referencial para a equipe.
        </div>
        <div class="exp-tags">
          <span class="exp-tag">Implantação</span><span class="exp-tag">Liderança de Suporte</span>
          <span class="exp-tag">Scrum</span><span class="exp-tag">Kanban</span><span class="exp-tag">PEC</span>
          <span class="exp-tag">SISAB</span><span class="exp-tag">SISPNCD</span><span class="exp-tag">Licitações</span>
        </div>
      </div>

      <div class="exp-card fade-in">
        <div class="exp-header">
          <div><div class="exp-title">Operador de Computador</div><div class="exp-company">Instituto Nacional de Tecnologia e Saúde – INTS</div></div>
          <div class="exp-period">Ago/2017 – Mar/2018</div>
        </div>
        <ul class="exp-bullets">
          <li>Cadastro e validação de dados no sistema Vida, assegurando qualidade das informações enviadas ao Ministério da Saúde.</li>
          <li>Suporte técnico na configuração e manutenção de tablets utilizados nas atividades de campo.</li>
          <li>Treinamento presencial de agentes comunitários de saúde (ACS) no uso de aplicativos móveis.</li>
        </ul>
        <div class="exp-result">
          <strong>Resultado de destaque</strong>
          Desenvolvimento e introdução de método pioneiro de atendimento humanizado no serviço público — base que facilitou a adesão e reduziu resistências à implantação de novos sistemas.
        </div>
        <div class="exp-tags">
          <span class="exp-tag">Atendimento Humanizado</span><span class="exp-tag">Cadastro de Dados</span>
          <span class="exp-tag">Treinamentos</span><span class="exp-tag">Dispositivos Móveis</span>
        </div>
      </div>

    </div>
  </div>
</section>

<section id="projetos">
  <div class="container">
    <span class="section-tag fade-in">Destaque técnico</span>
    <h2 class="section-title fade-in">Projeto em evidência</h2>
    <div class="projeto-card fade-in">
      <div>
        <div class="projeto-badge">Inovação em Saúde Pública</div>
        <h3 class="projeto-title">Sistema +ACE</h3>
        <p class="projeto-desc">Criação dos requisitos do sistema +ACE na Horizon, substituindo fichas físicas por uma solução digital completa para combate ao Aedes aegypti — com coleta em tablets e monitoramento georreferenciado via portal web.</p>
        <ul class="projeto-features">
          <li><div class="feat-dot"></div>Substituição de fichas em papel por app de coleta em tablets</li>
          <li><div class="feat-dot"></div>Portal web de monitoramento com visão georreferenciada</li>
          <li><div class="feat-dot"></div>Facilitação do diagnóstico e combate ao Aedes</li>
          <li><div class="feat-dot"></div>Levantamento completo de requisitos funcionais e técnicos</li>
        </ul>
      </div>
      <div class="projeto-visual">
        <div style="font-size:11px;font-weight:600;letter-spacing:0.1em;text-transform:uppercase;color:var(--text3);margin-bottom:8px;">Áreas de atuação no projeto</div>
        <div class="tech-item"><span class="tech-name">Requisitos</span><div class="tech-bar-bg"><div class="tech-bar" style="width:95%"></div></div><span class="tech-val">95%</span></div>
        <div class="tech-item"><span class="tech-name">UX / Negócio</span><div class="tech-bar-bg"><div class="tech-bar" style="width:85%"></div></div><span class="tech-val">85%</span></div>
        <div class="tech-item"><span class="tech-name">Integração</span><div class="tech-bar-bg"><div class="tech-bar" style="width:75%"></div></div><span class="tech-val">75%</span></div>
        <div class="tech-item"><span class="tech-name">Treinamento</span><div class="tech-bar-bg"><div class="tech-bar" style="width:90%"></div></div><span class="tech-val">90%</span></div>
        <div style="margin-top:16px;padding:16px;background:rgba(6,182,212,0.05);border:1px solid rgba(6,182,212,0.15);border-radius:10px;">
          <div style="font-size:12px;color:#67e8f9;font-weight:500;margin-bottom:4px;">Impacto</div>
          <div style="font-size:13px;color:var(--text2);line-height:1.5;">Visão georreferenciada em tempo real para agentes municipais de saúde pública.</div>
        </div>
      </div>
    </div>
  </div>
</section>

<section id="formacao">
  <div class="container">
    <span class="section-tag fade-in">Educação & Certificações</span>
    <h2 class="section-title fade-in">Formação acadêmica</h2>
    <div class="form-cert-grid fade-in">
      <div class="form-card"><div class="form-icon blue">🎓</div><div><div class="form-title">Análise e Desenvolvimento de Sistemas</div><div class="form-sub">Universidade Estácio de Sá</div><div class="form-year">Graduação — 2023</div></div></div>
      <div class="form-card"><div class="form-icon teal">🗄️</div><div><div class="form-title">SQL Server</div><div class="form-sub">Udemy</div><div class="form-year">Certificação — 2023</div></div></div>
      <div class="form-card"><div class="form-icon purple">🎨</div><div><div class="form-title">Introdução à Linguagem CSS</div><div class="form-sub">Udemy</div><div class="form-year">Certificação — 2023</div></div></div>
      <div class="form-card"><div class="form-icon blue">📋</div><div><div class="form-title">Pacote Office — Intermediário</div><div class="form-sub">Word, Excel, PowerPoint</div><div class="form-year">Habilidade adicional</div></div></div>
    </div>
  </div>
</section>

<section id="contato">
  <div class="container">
    <div class="contato-box fade-in">
      <h2 class="contato-title">Vamos conversar?</h2>
      <p class="contato-sub">Aberto a novas oportunidades em análise de negócios, projetos e implantação de sistemas.</p>
      <div class="contato-links">
        <a href="mailto:lemosh.ads@gmail.com" class="contato-link"><span class="link-icon">✉️</span> lemosh.ads@gmail.com</a>
        <a href="https://www.linkedin.com/in/hernani-lemos/" target="_blank" class="contato-link"><span class="link-icon">💼</span> LinkedIn</a>
        <a href="tel:+5571992081968" class="contato-link"><span class="link-icon">📞</span> (71) 9.9208-1968</a>
      </div>
    </div>
  </div>
</section>

<footer>
  <p>© 2025 Hernani de Oliveira Lemos</p>
  <p>Salvador, Bahia — Brasil</p>
</footer>

<script>
  const observer = new IntersectionObserver((entries) => {
    entries.forEach((entry, i) => {
      if (entry.isIntersecting) {
        setTimeout(() => entry.target.classList.add('visible'), i * 80);
        observer.unobserve(entry.target);
      }
    });
  }, { threshold: 0.1 });
  document.querySelectorAll('.fade-in').forEach(el => observer.observe(el));
</script>
</body>
</html>
