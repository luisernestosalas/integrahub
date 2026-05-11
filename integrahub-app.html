<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>IntégraHub — App</title>
<script src="https://js.stripe.com/v3/"></script>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Syne:wght@600;700;800&family=DM+Sans:wght@300;400;500&family=JetBrains+Mono:wght@400;500&display=swap" rel="stylesheet">
<style>
*,*::before,*::after{box-sizing:border-box;margin:0;padding:0}
:root{
  --bg:#08080d;--s1:#0f0f16;--s2:#16161f;--s3:#1e1e2a;
  --border:rgba(255,255,255,0.06);--border2:rgba(255,255,255,0.11);
  --text:#ebebf5;--muted:#5a5a78;--muted2:#3a3a50;
  --volt:#c6ff00;--volt2:#a8e000;--volt-g:rgba(198,255,0,0.1);
  --accent:#6c5fff;--accent-g:rgba(108,95,255,0.12);
  --green:#3ecf8e;--green-g:rgba(62,207,142,0.1);
  --red:#ff4f6d;--amber:#f5a623;
  --sans:'DM Sans',sans-serif;--display:'Syne',sans-serif;--mono:'JetBrains Mono',monospace;
}
html,body{height:100%;font-family:var(--sans);background:var(--bg);color:var(--text);overflow-x:hidden}

/* ── SCREENS ── */
.screen{display:none;min-height:100vh}
.screen.active{display:flex}

/* ── LOGIN ── */
#screen-login{
  align-items:center;justify-content:center;
  background:var(--bg);position:relative;overflow:hidden;
}
.login-grid{position:absolute;inset:0;background-image:linear-gradient(rgba(198,255,0,.03) 1px,transparent 1px),linear-gradient(90deg,rgba(198,255,0,.03) 1px,transparent 1px);background-size:60px 60px}
.login-glow{position:absolute;top:-20%;left:50%;transform:translateX(-50%);width:600px;height:600px;border-radius:50%;background:radial-gradient(circle,rgba(108,95,255,.12) 0%,transparent 65%);pointer-events:none}
.login-card{position:relative;z-index:1;width:100%;max-width:400px;padding:2rem;text-align:center}
.login-logo{font-family:var(--display);font-weight:800;font-size:1.4rem;letter-spacing:-.04em;margin-bottom:.5rem}
.login-logo b{background:var(--volt);color:var(--bg);padding:0 5px;border-radius:4px}
.login-sub{font-size:.85rem;color:var(--muted);margin-bottom:2.5rem;font-weight:300}
.login-box{background:var(--s1);border:1px solid var(--border2);border-radius:20px;padding:2rem}
.login-title{font-family:var(--display);font-size:1.3rem;font-weight:700;margin-bottom:.4rem;letter-spacing:-.03em}
.login-desc{font-size:.82rem;color:var(--muted);font-weight:300;margin-bottom:2rem;line-height:1.6}
.btn-google{
  width:100%;display:flex;align-items:center;justify-content:center;gap:12px;
  background:var(--text);color:var(--bg);border:none;border-radius:12px;
  padding:13px;font-family:var(--sans);font-size:.9rem;font-weight:600;
  cursor:pointer;transition:background .2s,transform .15s;
}
.btn-google:hover{background:#d0d0e0;transform:translateY(-1px)}
.btn-google svg{flex-shrink:0}
.login-divider{display:flex;align-items:center;gap:10px;margin:1.25rem 0;color:var(--muted2);font-size:.75rem}
.login-divider::before,.login-divider::after{content:'';flex:1;height:1px;background:var(--border)}
.email-input{width:100%;background:var(--s2);border:1px solid var(--border2);border-radius:10px;padding:11px 14px;color:var(--text);font-family:var(--sans);font-size:.875rem;outline:none;transition:border-color .2s;margin-bottom:8px}
.email-input:focus{border-color:var(--accent)}
.btn-email{width:100%;background:var(--accent);color:#fff;border:none;border-radius:10px;padding:12px;font-family:var(--sans);font-size:.875rem;font-weight:500;cursor:pointer;transition:background .2s}
.btn-email:hover{background:#8878ff}
.login-msg{font-size:.78rem;color:var(--green);margin-top:.75rem;min-height:1rem}
.login-fine{font-size:.72rem;color:var(--muted2);margin-top:1.5rem;line-height:1.6}

/* ── APP SHELL ── */
#screen-app{flex-direction:column}
.app-header{
  height:52px;display:flex;align-items:center;justify-content:space-between;
  padding:0 1.5rem;border-bottom:1px solid var(--border);
  background:rgba(8,8,13,.9);backdrop-filter:blur(12px);
  position:sticky;top:0;z-index:100;flex-shrink:0;
}
.app-logo{font-family:var(--display);font-weight:800;font-size:.95rem;letter-spacing:-.03em}
.app-logo b{background:var(--volt);color:var(--bg);padding:0 3px;border-radius:3px}
.header-right{display:flex;align-items:center;gap:12px}
.plan-badge{font-size:.68rem;font-weight:600;letter-spacing:.06em;text-transform:uppercase;padding:3px 10px;border-radius:100px}
.plan-badge.free{background:var(--s2);color:var(--muted);border:1px solid var(--border2)}
.plan-badge.pro{background:var(--volt-g);color:var(--volt);border:1px solid rgba(198,255,0,.2)}
.user-av{width:28px;height:28px;border-radius:50%;background:var(--accent);display:flex;align-items:center;justify-content:center;font-size:.68rem;font-weight:700;cursor:pointer;flex-shrink:0}
.btn-logout{background:none;border:none;color:var(--muted);font-size:.78rem;cursor:pointer;font-family:var(--sans);padding:4px 8px;border-radius:6px;transition:color .2s}
.btn-logout:hover{color:var(--text)}

.app-body{flex:1;display:grid;grid-template-columns:220px 1fr;overflow:hidden;height:calc(100vh - 52px)}

/* ── SIDEBAR ── */
.sidebar{border-right:1px solid var(--border);padding:1.25rem 0;overflow-y:auto;background:var(--s1)}
.nav-section{font-size:.6rem;font-weight:600;letter-spacing:.12em;text-transform:uppercase;color:var(--muted2);padding:0 1.25rem;margin:1rem 0 .4rem}
.nav-item{display:flex;align-items:center;gap:10px;padding:.6rem 1.25rem;font-size:.82rem;color:var(--muted);cursor:pointer;transition:background .15s,color .15s;border-left:2px solid transparent}
.nav-item:hover{background:var(--s2);color:var(--text)}
.nav-item.active{background:var(--accent-g);color:var(--text);border-left-color:var(--accent)}
.nav-item .ni-icon{font-size:1rem;width:18px;text-align:center;flex-shrink:0}
.sidebar-upgrade{margin:1rem;background:var(--volt-g);border:1px solid rgba(198,255,0,.2);border-radius:12px;padding:1rem}
.su-title{font-size:.82rem;font-weight:600;color:var(--volt);margin-bottom:.3rem}
.su-desc{font-size:.72rem;color:var(--muted);font-weight:300;margin-bottom:.75rem;line-height:1.5}
.btn-upgrade{width:100%;background:var(--volt);color:var(--bg);border:none;border-radius:8px;padding:8px;font-family:var(--sans);font-size:.78rem;font-weight:700;cursor:pointer;transition:background .2s}
.btn-upgrade:hover{background:var(--volt2)}

/* ── MAIN CONTENT ── */
.main-content{overflow-y:auto;padding:1.5rem}

/* ── DASHBOARD VIEW ── */
.view{display:none}
.view.active{display:block}
.view-title{font-family:var(--display);font-size:1.4rem;font-weight:700;letter-spacing:-.03em;margin-bottom:.3rem}
.view-sub{font-size:.82rem;color:var(--muted);font-weight:300;margin-bottom:2rem}

.stats-row{display:grid;grid-template-columns:repeat(3,1fr);gap:10px;margin-bottom:2rem}
.stat-card{background:var(--s1);border:1px solid var(--border);border-radius:14px;padding:1.1rem 1.25rem}
.stat-val{font-family:var(--display);font-size:1.8rem;font-weight:700;letter-spacing:-.04em;margin-bottom:.2rem}
.stat-label{font-size:.72rem;color:var(--muted);font-weight:400;text-transform:uppercase;letter-spacing:.06em}

/* ── INTEGRATIONS GRID ── */
.int-grid{display:grid;grid-template-columns:repeat(auto-fill,minmax(200px,1fr));gap:10px}
.int-card{background:var(--s1);border:1px solid var(--border);border-radius:14px;padding:1.1rem;cursor:pointer;transition:border-color .2s,background .15s;position:relative;overflow:hidden}
.int-card:hover{border-color:var(--border2);background:var(--s2)}
.int-card.connected{border-color:rgba(62,207,142,.25);background:rgba(62,207,142,.03)}
.int-card.locked{opacity:.5;cursor:not-allowed}
.int-icon{font-size:1.6rem;margin-bottom:.6rem}
.int-name{font-size:.875rem;font-weight:600;margin-bottom:.2rem;letter-spacing:-.01em}
.int-desc{font-size:.72rem;color:var(--muted);font-weight:300}
.int-status{position:absolute;top:10px;right:10px;font-size:.65rem;font-weight:600;padding:2px 8px;border-radius:100px}
.int-status.on{background:var(--green-g);color:var(--green);border:1px solid rgba(62,207,142,.2)}
.int-status.off{background:var(--s2);color:var(--muted);border:1px solid var(--border)}
.int-status.lock{background:rgba(245,166,35,.1);color:var(--amber);border:1px solid rgba(245,166,35,.2)}

/* ── WIZARD MODAL ── */
.modal-overlay{position:fixed;inset:0;background:rgba(0,0,0,.7);backdrop-filter:blur(4px);z-index:200;display:none;align-items:center;justify-content:center;padding:1rem}
.modal-overlay.open{display:flex}
.modal{background:var(--s1);border:1px solid var(--border2);border-radius:20px;width:100%;max-width:520px;overflow:hidden;max-height:90vh;display:flex;flex-direction:column}
.modal-head{padding:1.25rem 1.5rem;border-bottom:1px solid var(--border);display:flex;align-items:center;gap:12px;flex-shrink:0}
.modal-icon{font-size:1.8rem;flex-shrink:0}
.modal-title{font-family:var(--display);font-size:1rem;font-weight:700;letter-spacing:-.02em;margin-bottom:1px}
.modal-sub{font-size:.72rem;color:var(--muted)}
.modal-close{margin-left:auto;background:none;border:none;color:var(--muted);cursor:pointer;font-size:1.2rem;padding:4px;line-height:1}
.modal-body{padding:1.5rem;overflow-y:auto;flex:1}
.modal-footer{padding:1rem 1.5rem;border-top:1px solid var(--border);display:flex;align-items:center;justify-content:space-between;flex-shrink:0}

/* wizard steps */
.wiz-steps{display:flex;gap:0;margin-bottom:1.5rem}
.wiz-step{flex:1;text-align:center;font-size:.68rem;color:var(--muted);padding-bottom:8px;border-bottom:2px solid var(--border);cursor:pointer;transition:color .2s}
.wiz-step.active{color:var(--accent);border-bottom-color:var(--accent);font-weight:500}
.wiz-step.done{color:var(--green);border-bottom-color:var(--green)}

.tip-box{background:var(--accent-g);border:1px solid rgba(108,95,255,.2);border-radius:10px;padding:.9rem 1.1rem;margin-bottom:1.1rem;font-size:.8rem;color:var(--text);line-height:1.6}
.tip-link{color:var(--accent);text-decoration:none;font-weight:500}
.tip-link:hover{text-decoration:underline}

.field{margin-bottom:1rem}
.field-label{font-size:.7rem;font-weight:500;letter-spacing:.06em;text-transform:uppercase;color:var(--muted);margin-bottom:5px;display:block}
.field-input{width:100%;background:var(--s2);border:1px solid var(--border2);border-radius:9px;padding:10px 13px;color:var(--text);font-family:var(--mono);font-size:.8rem;outline:none;transition:border-color .2s}
.field-input:focus{border-color:var(--accent)}
.field-hint{font-size:.7rem;color:var(--muted);margin-top:4px;line-height:1.5}
.where-btn{font-size:.7rem;color:var(--accent);background:none;border:none;cursor:pointer;font-family:var(--sans);padding:0;margin-bottom:6px;display:inline-flex;align-items:center;gap:4px}
.where-tip{background:var(--s2);border:1px solid var(--border);border-radius:8px;padding:8px 12px;font-size:.72rem;color:var(--muted);line-height:1.6;margin-bottom:8px;display:none}
.where-tip.show{display:block}

.success-body{text-align:center;padding:1.5rem 0}
.success-icon{font-size:2.5rem;margin-bottom:.75rem}
.success-title{font-family:var(--display);font-size:1.1rem;font-weight:700;margin-bottom:.4rem}
.success-desc{font-size:.82rem;color:var(--muted);font-weight:300;line-height:1.6}

/* buttons */
.btn-primary{background:var(--accent);color:#fff;border:none;border-radius:9px;padding:10px 20px;font-family:var(--sans);font-size:.875rem;font-weight:500;cursor:pointer;display:inline-flex;align-items:center;gap:7px;transition:background .2s,transform .15s}
.btn-primary:hover{background:#8878ff;transform:translateY(-1px)}
.btn-secondary{background:var(--s2);color:var(--text);border:1px solid var(--border2);border-radius:9px;padding:10px 16px;font-family:var(--sans);font-size:.875rem;cursor:pointer;transition:border-color .2s}
.btn-secondary:hover{border-color:var(--border2)}
.btn-volt-sm{background:var(--volt);color:var(--bg);border:none;border-radius:9px;padding:10px 20px;font-family:var(--sans);font-size:.875rem;font-weight:700;cursor:pointer;transition:background .2s}
.btn-volt-sm:hover{background:var(--volt2)}
.security-note{font-size:.7rem;color:var(--muted);display:flex;align-items:center;gap:5px}

/* ── UPGRADE VIEW ── */
.upgrade-grid{display:grid;grid-template-columns:repeat(2,1fr);gap:12px;max-width:640px}
.plan-card{background:var(--s1);border:1.5px solid var(--border);border-radius:18px;padding:1.5rem}
.plan-card.featured{background:var(--bg);border-color:var(--volt)}
.plan-name-sm{font-family:var(--display);font-size:1.1rem;font-weight:700;margin-bottom:.3rem}
.plan-price-sm{font-size:2rem;font-weight:800;font-family:var(--display);letter-spacing:-.04em;line-height:1;margin:.4rem 0 .3rem}
.plan-price-sm sub{font-size:.9rem;font-weight:400;opacity:.5}
.plan-desc-sm{font-size:.75rem;color:var(--muted);margin-bottom:1rem;font-weight:300}
.plan-divider-sm{height:1px;background:var(--border);margin:1rem 0}
.plan-feat{font-size:.78rem;display:flex;gap:8px;margin-bottom:.5rem;font-weight:300;color:var(--muted)}
.plan-feat::before{content:'✓';color:var(--green);font-weight:700;flex-shrink:0}
.plan-card.featured .plan-feat{color:var(--text)}
.plan-cta-sm{display:block;text-align:center;width:100%;margin-top:1.25rem;padding:.7rem;border-radius:100px;font-family:var(--sans);font-size:.82rem;font-weight:600;cursor:pointer;border:1.5px solid var(--border2);background:transparent;color:var(--text);transition:all .2s}
.plan-cta-sm:hover{border-color:var(--accent);color:var(--accent)}
.plan-card.featured .plan-cta-sm{background:var(--volt);color:var(--bg);border-color:var(--volt)}
.plan-card.featured .plan-cta-sm:hover{background:var(--volt2)}

/* responsive */
@media(max-width:640px){
  .app-body{grid-template-columns:1fr}
  .sidebar{display:none}
  .stats-row{grid-template-columns:1fr}
  .upgrade-grid{grid-template-columns:1fr}
}
</style>
</head>
<body>

<!-- ══════════════════════════════════
     SCREEN 1: LOGIN
══════════════════════════════════ -->
<div class="screen active" id="screen-login">
  <div class="login-grid"></div>
  <div class="login-glow"></div>
  <div class="login-card">
    <div class="login-logo">íntegra<b>hub</b></div>
    <p class="login-sub">Tu app merece salir al mundo</p>
    <div class="login-box">
      <p class="login-title">Empieza gratis</p>
      <p class="login-desc">Conecta tus integraciones, genera tu backend y despliega — sin DevOps.</p>

      <button class="btn-google" onclick="loginGoogle()">
        <svg width="18" height="18" viewBox="0 0 24 24"><path fill="#4285F4" d="M22.56 12.25c0-.78-.07-1.53-.2-2.25H12v4.26h5.92c-.26 1.37-1.04 2.53-2.21 3.31v2.77h3.57c2.08-1.92 3.28-4.74 3.28-8.09z"/><path fill="#34A853" d="M12 23c2.97 0 5.46-.98 7.28-2.66l-3.57-2.77c-.98.66-2.23 1.06-3.71 1.06-2.86 0-5.29-1.93-6.16-4.53H2.18v2.84C3.99 20.53 7.7 23 12 23z"/><path fill="#FBBC05" d="M5.84 14.09c-.22-.66-.35-1.36-.35-2.09s.13-1.43.35-2.09V7.07H2.18C1.43 8.55 1 10.22 1 12s.43 3.45 1.18 4.93l3.66-2.84z"/><path fill="#EA4335" d="M12 5.38c1.62 0 3.06.56 4.21 1.64l3.15-3.15C17.45 2.09 14.97 1 12 1 7.7 1 3.99 3.47 2.18 7.07l3.66 2.84c.87-2.6 3.3-4.53 6.16-4.53z"/></svg>
        Continuar con Google
      </button>

      <div class="login-divider">o</div>

      <input type="email" class="email-input" id="loginEmail" placeholder="tu@email.com">
      <button class="btn-email" onclick="loginMagicLink()">Recibir link de acceso →</button>
      <p class="login-msg" id="loginMsg"></p>
    </div>
    <p class="login-fine">Al continuar aceptas los términos de servicio · Sin tarjeta de crédito</p>
  </div>
</div>

<!-- ══════════════════════════════════
     SCREEN 2: APP
══════════════════════════════════ -->
<div class="screen" id="screen-app">
  <header class="app-header">
    <div class="app-logo">íntegra<b>hub</b></div>
    <div class="header-right">
      <span class="plan-badge free" id="planBadge">Plan Gratis</span>
      <div class="user-av" id="userAv">?</div>
      <button class="btn-logout" onclick="logout()">Salir</button>
    </div>
  </header>

  <div class="app-body">
    <!-- Sidebar -->
    <nav class="sidebar">
      <p class="nav-section">Principal</p>
      <div class="nav-item active" onclick="showView('dashboard')" id="nav-dashboard">
        <span class="ni-icon">⚡</span> Dashboard
      </div>
      <div class="nav-item" onclick="showView('integrations')" id="nav-integrations">
        <span class="ni-icon">🔌</span> Integraciones
      </div>
      <div class="nav-item" onclick="showView('analyzer')" id="nav-analyzer">
        <span class="ni-icon">🔍</span> Analizar App
      </div>
      <div class="nav-item" onclick="showView('generator')" id="nav-generator">
        <span class="ni-icon">⚙️</span> Generar Backend
      </div>
      <p class="nav-section">Cuenta</p>
      <div class="nav-item" onclick="showView('upgrade')" id="nav-upgrade">
        <span class="ni-icon">🚀</span> Upgrade a Pro
      </div>

      <div class="sidebar-upgrade" id="sidebarUpgrade">
        <p class="su-title">✨ Upgrade a Pro</p>
        <p class="su-desc">Integraciones ilimitadas y deploys sin límite.</p>
        <button class="btn-upgrade" onclick="showView('upgrade')">Ver planes →</button>
      </div>
    </nav>

    <!-- Main -->
    <main class="main-content">

      <!-- DASHBOARD -->
      <div class="view active" id="view-dashboard">
        <p class="view-title">Bienvenido 👋</p>
        <p class="view-sub" id="dashSub">Conecta tus primeras integraciones para empezar.</p>

        <div class="stats-row">
          <div class="stat-card">
            <div class="stat-val" id="statConnected" style="color:var(--green)">0</div>
            <div class="stat-label">Conectadas</div>
          </div>
          <div class="stat-card">
            <div class="stat-val" style="color:var(--volt)">8</div>
            <div class="stat-label">Disponibles</div>
          </div>
          <div class="stat-card">
            <div class="stat-val" id="statLimit" style="color:var(--muted)">3</div>
            <div class="stat-label">Límite del plan</div>
          </div>
        </div>

        <p class="view-sub" style="margin-bottom:1rem;font-size:.85rem;font-weight:500;color:var(--text)">Integraciones rápidas</p>
        <div class="int-grid" id="dashIntGrid"></div>
      </div>

      <!-- INTEGRATIONS -->
      <div class="view" id="view-integrations">
        <p class="view-title">Integraciones</p>
        <p class="view-sub">Conecta los servicios que usa tu app. Tus credenciales se guardan encriptadas.</p>
        <div class="int-grid" id="fullIntGrid"></div>
      </div>

      <!-- ANALYZER -->
      <div class="view" id="view-analyzer">
        <p class="view-title">Analizar tu App</p>
        <p class="view-sub">Pega tu código y Claude detecta qué integraciones necesitas.</p>
        <div style="background:var(--s1);border:1px solid var(--border2);border-radius:14px;padding:1.25rem">
          <textarea id="analyzerCode" style="width:100%;background:var(--s2);border:1px solid var(--border);border-radius:9px;padding:12px;color:var(--text);font-family:var(--mono);font-size:.78rem;min-height:200px;resize:vertical;outline:none;line-height:1.6" placeholder="<!-- Pega aquí tu HTML, JSX o JS -->"></textarea>
          <button class="btn-primary" style="margin-top:1rem" onclick="analyzeApp()">
            🔍 Analizar con IA
          </button>
          <div id="analyzerResult" style="margin-top:1rem"></div>
        </div>
      </div>

      <!-- GENERATOR -->
      <div class="view" id="view-generator">
        <p class="view-title">Generador de Backend</p>
        <p class="view-sub">Selecciona tus integraciones y generamos el código Node.js listo para producción.</p>
        <div style="background:var(--s1);border:1px solid var(--border2);border-radius:14px;padding:1.25rem">
          <p style="font-size:.8rem;color:var(--muted);margin-bottom:1rem">Integraciones a incluir:</p>
          <div id="generatorCheckboxes" style="display:flex;flex-wrap:wrap;gap:8px;margin-bottom:1.5rem"></div>
          <button class="btn-primary" onclick="generateBackend()">⚡ Generar backend</button>
          <div id="generatorResult" style="margin-top:1rem"></div>
        </div>
      </div>

      <!-- UPGRADE -->
      <div class="view" id="view-upgrade">
        <p class="view-title">Elige tu plan</p>
        <p class="view-sub">Empieza gratis. Actualiza cuando estés listo para escalar.</p>
        <div class="upgrade-grid">
          <div class="plan-card">
            <p class="plan-name-sm">Gratis</p>
            <p class="plan-price-sm">$0 <sub>/mes</sub></p>
            <p class="plan-desc-sm">Para empezar y validar</p>
            <div class="plan-divider-sm"></div>
            <p class="plan-feat">3 integraciones</p>
            <p class="plan-feat">Generador de backend</p>
            <p class="plan-feat">1 deploy a Railway</p>
            <p class="plan-feat">Analizador de app</p>
            <button class="plan-cta-sm" disabled style="opacity:.4;cursor:not-allowed">Plan actual</button>
          </div>
          <div class="plan-card featured">
            <p style="font-size:.68rem;font-weight:700;background:var(--volt);color:var(--bg);padding:2px 10px;border-radius:100px;display:inline-block;margin-bottom:.75rem;letter-spacing:.06em">MÁS POPULAR</p>
            <p class="plan-name-sm">Pro</p>
            <p class="plan-price-sm">$19 <sub>/mes</sub></p>
            <p class="plan-desc-sm">Para builders que ya generan ingresos</p>
            <div class="plan-divider-sm"></div>
            <p class="plan-feat" style="color:var(--text)">Integraciones ilimitadas</p>
            <p class="plan-feat" style="color:var(--text)">Deploys ilimitados</p>
            <p class="plan-feat" style="color:var(--text)">Soporte prioritario</p>
            <p class="plan-feat" style="color:var(--text)">Nuevas integraciones primero</p>
            <button class="plan-cta-sm" onclick="startCheckout()">Upgrade a Pro →</button>
          </div>
        </div>
        <div id="checkoutMsg" style="margin-top:1rem;font-size:.82rem;color:var(--muted)"></div>
      </div>

    </main>
  </div>
</div>

<!-- ══════════════════════════════════
     WIZARD MODAL
══════════════════════════════════ -->
<div class="modal-overlay" id="wizardModal">
  <div class="modal">
    <div class="modal-head">
      <span class="modal-icon" id="wizIcon"></span>
      <div>
        <p class="modal-title" id="wizTitle"></p>
        <p class="modal-sub" id="wizSub"></p>
      </div>
      <button class="modal-close" onclick="closeWizard()">×</button>
    </div>
    <div class="modal-body" id="wizBody"></div>
    <div class="modal-footer">
      <span class="security-note">🔒 Encriptación AES-256</span>
      <div style="display:flex;gap:8px">
        <button class="btn-secondary" id="wizBtnBack" onclick="wizPrev()" style="display:none">← Atrás</button>
        <button class="btn-primary" id="wizBtnNext" onclick="wizNext()">Siguiente →</button>
      </div>
    </div>
  </div>
</div>

<script>
// ════════════════════════════════════
//  CONFIG
// ════════════════════════════════════
const SUPABASE_URL = 'https://ameubkwhvhywazxpeyay.supabase.co';
const SUPABASE_KEY = 'eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJzdXBhYmFzZSIsInJlZiI6ImFtZXVia3dodmh5d2F6eHBleWF5Iiwicm9sZSI6ImFub24iLCJpYXQiOjE3Nzg1MjM2MTAsImV4cCI6MjA5NDA5OTYxMH0.mFc5Mk5IJ1uMlz4hLV2-is_SdlyOipAXI-0o6UHWbxE';
const STRIPE_PK    = 'pk_test_51QS4eiH5hboqtBoO3CzG8F7x5keJiupMXYrojCRx1nU7I1hUyt9EseGdh4Q7Hpiiooosej0TxilLRYTS2HUHatx200DIz90y5v';
const STRIPE_PRICE = 'price_1TW30rH5hboqtBoOIBQ84hld';

// ════════════════════════════════════
//  STATE
// ════════════════════════════════════
let currentUser  = null;
let userPlan     = 'free';
let connections  = {};  // { stripe: true, openai: false, ... }
let wizService   = null;
let wizStep      = 0;
let wizValues    = {};

// ════════════════════════════════════
//  SERVICES CONFIG
// ════════════════════════════════════
const SERVICES = {
  stripe:      { icon:'💳', name:'Stripe',          desc:'Cobros y suscripciones',    color:'#635BFF' },
  resend:      { icon:'✉️', name:'Resend',           desc:'Emails transaccionales',    color:'#000' },
  openai:      { icon:'🤖', name:'OpenAI',           desc:'GPT-4o e inteligencia IA',  color:'#10a37f' },
  whatsapp:    { icon:'💬', name:'WhatsApp',         desc:'Mensajes automáticos',      color:'#25D366' },
  supabase:    { icon:'🗄️', name:'Supabase',         desc:'Base de datos PostgreSQL',  color:'#3ECF8E' },
  twilio:      { icon:'📱', name:'Twilio',           desc:'SMS a cualquier número',    color:'#F22F46' },
  sheets:      { icon:'📊', name:'Google Sheets',    desc:'Lee y escribe hojas',       color:'#34A853' },
  anthropic:   { icon:'🧠', name:'Anthropic',        desc:'Claude para tu app',        color:'#cc785c' },
};

const WIZARD_STEPS = {
  stripe:    [{ title:'Clave secreta', fields:[{ key:'secret_key', label:'Secret Key', hint:'Empieza con sk_live_ o sk_test_', ph:'sk_live_...', where:'Dashboard → Developers → API keys → Secret key' },{ key:'webhook_secret', label:'Webhook Secret', hint:'Empieza con whsec_', ph:'whsec_...', where:'Dashboard → Developers → Webhooks → Signing secret' }] }],
  resend:    [{ title:'API Key', fields:[{ key:'api_key', label:'API Key', hint:'Empieza con re_', ph:'re_...', where:'resend.com → API Keys → Create API Key' },{ key:'from_email', label:'Email de origen', hint:'El email desde donde envías', ph:'hola@tudominio.com', where:'Cualquier email que hayas verificado en Resend' }] }],
  openai:    [{ title:'API Key', fields:[{ key:'api_key', label:'API Key', hint:'Empieza con sk-proj-', ph:'sk-proj-...', where:'platform.openai.com → API keys → Create new secret key' },{ key:'model', label:'Modelo (opcional)', hint:'Ej: gpt-4o-mini', ph:'gpt-4o-mini', where:'Déjalo en blanco para usar gpt-4o-mini por defecto' }] }],
  whatsapp:  [{ title:'Credenciales Jelou', fields:[{ key:'token', label:'Bearer Token', hint:'Token largo que empieza con eyJ', ph:'eyJhbGci...', where:'app.jelou.ai → Configuración → API → Bearer Token' },{ key:'bot_id', label:'Bot ID', hint:'Número del ID de tu bot', ph:'12345', where:'app.jelou.ai → Bots → tu bot → URL del navegador' }] }],
  supabase:  [{ title:'Credenciales', fields:[{ key:'url', label:'Project URL', hint:'URL de tu proyecto Supabase', ph:'https://xxxx.supabase.co', where:'supabase.com → Settings → API → Project URL' },{ key:'anon_key', label:'Anon Key', hint:'Clave pública del proyecto', ph:'eyJhbGci...', where:'supabase.com → Settings → API → anon public' }] }],
  twilio:    [{ title:'Credenciales', fields:[{ key:'account_sid', label:'Account SID', hint:'Empieza con AC', ph:'ACxxxx...', where:'console.twilio.com → página principal → Account Info' },{ key:'auth_token', label:'Auth Token', hint:'Token de autenticación', ph:'••••••••••••', where:'console.twilio.com → página principal → Auth Token' },{ key:'from_number', label:'Número Twilio', hint:'Formato E.164: +15551234567', ph:'+15551234567', where:'console.twilio.com → Phone Numbers → Active Numbers' }] }],
  sheets:    [{ title:'Service Account', fields:[{ key:'service_account', label:'JSON de Service Account', hint:'Pega el contenido del archivo JSON descargado de Google Cloud', ph:'{"type":"service_account",...}', where:'Google Cloud → IAM → Service Accounts → Keys → Add Key → JSON', textarea:true }] }],
  anthropic: [{ title:'API Key', fields:[{ key:'api_key', label:'API Key', hint:'Empieza con sk-ant-', ph:'sk-ant-...', where:'console.anthropic.com → API Keys → Create Key' }] }],
};

// ════════════════════════════════════
//  SUPABASE HELPERS
// ════════════════════════════════════
async function sbFetch(path, opts={}) {
  const res = await fetch(SUPABASE_URL + path, {
    ...opts,
    headers: {
      'Content-Type':'application/json',
      'apikey': SUPABASE_KEY,
      'Authorization': 'Bearer ' + (currentUser?.access_token || SUPABASE_KEY),
      ...(opts.headers||{})
    }
  });
  return res;
}

// ════════════════════════════════════
//  AUTH
// ════════════════════════════════════
async function loginGoogle() {
  const res = await sbFetch('/auth/v1/authorize?provider=google&redirect_to=' + encodeURIComponent(location.href), { method:'GET' });
  // Redirect via link
  const { url } = await res.json().catch(()=>({}));
  if(url) location.href = url;
  else {
    // fallback: direct redirect
    location.href = SUPABASE_URL + '/auth/v1/authorize?provider=google&redirect_to=' + encodeURIComponent(location.href);
  }
}

async function loginMagicLink() {
  const email = document.getElementById('loginEmail').value.trim();
  const msg   = document.getElementById('loginMsg');
  if(!email || !email.includes('@')) { msg.textContent='Ingresa un email válido'; msg.style.color='var(--red)'; return; }
  msg.textContent='⏳ Enviando link...'; msg.style.color='var(--muted)';
  const res = await sbFetch('/auth/v1/otp', {
    method:'POST',
    body: JSON.stringify({ email, create_user:true })
  });
  if(res.ok){
    msg.textContent='✓ Revisa tu correo — te enviamos el link de acceso.';
    msg.style.color='var(--green)';
  } else {
    msg.textContent='Error al enviar. Intenta de nuevo.';
    msg.style.color='var(--red)';
  }
}

async function checkSession() {
  // Check hash params (OAuth callback)
  const hash = location.hash;
  if(hash.includes('access_token')) {
    const params = new URLSearchParams(hash.replace('#',''));
    const token  = params.get('access_token');
    if(token) {
      const res  = await fetch(SUPABASE_URL + '/auth/v1/user', {
        headers:{ 'Authorization':'Bearer '+token, 'apikey':SUPABASE_KEY }
      });
      const user = await res.json();
      if(user.id){ currentUser = { ...user, access_token: token }; history.replaceState(null,'',location.pathname); enterApp(); return; }
    }
  }
  // Check stored session
  const stored = localStorage.getItem('ih_user');
  if(stored) {
    try {
      currentUser = JSON.parse(stored);
      // verify token still valid
      const res = await fetch(SUPABASE_URL + '/auth/v1/user', {
        headers:{ 'Authorization':'Bearer '+currentUser.access_token, 'apikey':SUPABASE_KEY }
      });
      if(res.ok){ enterApp(); return; }
      else { localStorage.removeItem('ih_user'); }
    } catch(e){ localStorage.removeItem('ih_user'); }
  }
}

function enterApp() {
  localStorage.setItem('ih_user', JSON.stringify(currentUser));
  document.getElementById('screen-login').classList.remove('active');
  document.getElementById('screen-app').classList.add('active');
  const name  = currentUser.user_metadata?.full_name || currentUser.email || 'U';
  const initials = name.split(' ').map(n=>n[0]).join('').slice(0,2).toUpperCase();
  document.getElementById('userAv').textContent = initials;
  document.getElementById('dashSub').textContent = `Hola, ${name.split(' ')[0]}. Conecta tus integraciones para empezar.`;
  loadConnections();
  renderIntGrids();
  renderGeneratorCheckboxes();
}

function logout() {
  localStorage.removeItem('ih_user');
  currentUser = null; connections = {};
  document.getElementById('screen-app').classList.remove('active');
  document.getElementById('screen-login').classList.add('active');
}

// ════════════════════════════════════
//  CONNECTIONS (stored in Supabase)
// ════════════════════════════════════
async function loadConnections() {
  try {
    const res  = await sbFetch('/rest/v1/integrations?select=service,active&user_id=eq.'+currentUser.id);
    if(res.ok){
      const data = await res.json();
      connections = {};
      data.forEach(r => { if(r.active) connections[r.service] = true; });
    }
  } catch(e){}
  updateStats();
  renderIntGrids();
}

function updateStats() {
  const n = Object.values(connections).filter(Boolean).length;
  document.getElementById('statConnected').textContent = n;
  const limit = userPlan === 'pro' ? '∞' : '3';
  document.getElementById('statLimit').textContent = limit;
  const badge = document.getElementById('planBadge');
  if(userPlan === 'pro'){ badge.textContent='Plan Pro ✨'; badge.className='plan-badge pro'; document.getElementById('sidebarUpgrade').style.display='none'; }
}

// ════════════════════════════════════
//  RENDER INTEGRATION CARDS
// ════════════════════════════════════
function renderIntGrids() {
  renderGrid('dashIntGrid', true);
  renderGrid('fullIntGrid', false);
}

function renderGrid(id, limit4) {
  const el = document.getElementById(id);
  if(!el) return;
  const keys = Object.keys(SERVICES);
  const show = limit4 ? keys.slice(0,4) : keys;
  el.innerHTML = show.map(svc => {
    const s   = SERVICES[svc];
    const on  = connections[svc];
    const locked = userPlan==='free' && !on && Object.values(connections).filter(Boolean).length >= 3;
    return `<div class="int-card ${on?'connected':''} ${locked?'locked':''}" onclick="${locked?'showView(\'upgrade\')':'openWizard(\''+svc+'\')'}">
      <span class="int-status ${on?'on':locked?'lock':'off'}">${on?'✓ Activa':locked?'🔒 Pro':'Sin conectar'}</span>
      <div class="int-icon">${s.icon}</div>
      <div class="int-name">${s.name}</div>
      <div class="int-desc">${s.desc}</div>
    </div>`;
  }).join('');
}

// ════════════════════════════════════
//  WIZARD
// ════════════════════════════════════
function openWizard(svc) {
  wizService = svc; wizStep = 0; wizValues = {};
  const s = SERVICES[svc];
  document.getElementById('wizIcon').textContent  = s.icon;
  document.getElementById('wizTitle').textContent = s.name;
  document.getElementById('wizSub').textContent   = s.desc;
  document.getElementById('wizardModal').classList.add('open');
  renderWizStep();
}

function closeWizard() {
  document.getElementById('wizardModal').classList.remove('open');
  wizService = null;
}

function renderWizStep() {
  const steps = WIZARD_STEPS[wizService];
  if(!steps) return;
  const step  = steps[wizStep];
  const last  = wizStep === steps.length - 1;
  const body  = document.getElementById('wizBody');

  // steps tabs
  let tabs = '';
  steps.forEach((s,i) => {
    const cls = i===wizStep?'active':i<wizStep?'done':'';
    tabs += `<div class="wiz-step ${cls}">${i<wizStep?'✓ ':i+1+'. '}${s.title}</div>`;
  });

  if(step.done) {
    body.innerHTML = `<div class="success-body"><div class="success-icon">✅</div><p class="success-title">${SERVICES[wizService].name} conectado</p><p class="success-desc">Tus credenciales se guardaron encriptadas y están listas para usar.</p></div>`;
    document.getElementById('wizBtnNext').textContent = 'Cerrar';
    document.getElementById('wizBtnBack').style.display = 'none';
    return;
  }

  let fieldsHtml = '';
  (step.fields||[]).forEach(f => {
    const whereId = 'where-'+f.key;
    fieldsHtml += `<div class="field">
      <label class="field-label">${f.label}</label>
      ${f.where?`<button class="where-btn" onclick="toggleWhere('${f.key}')">📍 ¿Dónde lo encuentro?</button><div class="where-tip" id="${whereId}">${f.where}</div>`:''}
      ${f.textarea
        ? `<textarea class="field-input" id="f-${f.key}" rows="4" placeholder="${f.ph||''}" style="resize:vertical">${wizValues[f.key]||''}</textarea>`
        : `<input class="field-input" type="text" id="f-${f.key}" placeholder="${f.ph||''}" value="${wizValues[f.key]||''}">`
      }
      <p class="field-hint">${f.hint||''}</p>
    </div>`;
  });

  body.innerHTML = `<div class="wiz-steps">${tabs}</div>${fieldsHtml}`;

  document.getElementById('wizBtnNext').textContent  = last ? '💾 Guardar y conectar' : 'Siguiente →';
  document.getElementById('wizBtnBack').style.display = wizStep > 0 ? 'block' : 'none';
}

function toggleWhere(key) {
  const el = document.getElementById('where-'+key);
  if(el) el.classList.toggle('show');
}

async function wizNext() {
  const steps = WIZARD_STEPS[wizService];
  const step  = steps[wizStep];

  if(step.done) { closeWizard(); return; }

  // collect values
  (step.fields||[]).forEach(f => {
    const el = document.getElementById('f-'+f.key);
    if(el) wizValues[f.key] = el.value.trim();
  });

  if(wizStep < steps.length - 1) {
    wizStep++;
    // if last real step done, save
    if(wizStep === steps.length - 1) {
      await saveIntegration();
      steps[wizStep] = { title:'Listo', done:true };
    }
    renderWizStep();
  } else {
    await saveIntegration();
    closeWizard();
  }
}

function wizPrev() {
  if(wizStep > 0){ wizStep--; renderWizStep(); }
}

async function saveIntegration() {
  if(!currentUser) return;
  try {
    await sbFetch('/rest/v1/integrations', {
      method: 'POST',
      headers:{ 'Prefer':'resolution=merge-duplicates' },
      body: JSON.stringify({
        user_id: currentUser.id,
        service: wizService,
        encrypted_credentials: btoa(JSON.stringify(wizValues)),
        active: true,
        updated_at: new Date().toISOString()
      })
    });
    connections[wizService] = true;
    updateStats();
    renderIntGrids();
  } catch(e){ console.error(e); }
}

// ════════════════════════════════════
//  ANALYZER (calls Claude API)
// ════════════════════════════════════
async function analyzeApp() {
  const code   = document.getElementById('analyzerCode').value.trim();
  const result = document.getElementById('analyzerResult');
  if(!code){ result.innerHTML = '<p style="color:var(--red);font-size:.8rem">Pega tu código primero.</p>'; return; }
  result.innerHTML = '<p style="color:var(--muted);font-size:.8rem">⏳ Analizando con Claude...</p>';
  try {
    const res = await fetch('https://api.anthropic.com/v1/messages', {
      method:'POST',
      headers:{ 'Content-Type':'application/json' },
      body: JSON.stringify({
        model:'claude-sonnet-4-20250514', max_tokens:800,
        messages:[{ role:'user', content:`Analiza este código y dime en JSON qué integraciones necesita. Responde SOLO JSON con este formato: {"integrations":["stripe","openai",...], "missing":["descripción corta de qué falta"], "score":75}. Integraciones posibles: stripe, resend, openai, whatsapp, supabase, twilio, sheets, anthropic.\n\nCódigo:\n${code.slice(0,5000)}` }]
      })
    });
    const data = await res.json();
    const text = data.content?.[0]?.text || '{}';
    const json = JSON.parse(text.replace(/```json|```/g,'').trim());
    result.innerHTML = `
      <div style="background:var(--s2);border:1px solid var(--border2);border-radius:10px;padding:1rem;margin-top:1rem">
        <p style="font-size:.82rem;font-weight:600;margin-bottom:.75rem">Resultado del análisis — Score: <span style="color:var(--volt)">${json.score||'?'}/100</span></p>
        <p style="font-size:.75rem;color:var(--muted);margin-bottom:.5rem">Integraciones detectadas:</p>
        <div style="display:flex;flex-wrap:wrap;gap:6px;margin-bottom:.75rem">
          ${(json.integrations||[]).map(i=>`<span style="background:var(--accent-g);color:var(--accent);border:1px solid rgba(108,95,255,.2);border-radius:100px;padding:2px 10px;font-size:.72rem;font-weight:500">${SERVICES[i]?.icon||'🔌'} ${SERVICES[i]?.name||i}</span>`).join('')}
        </div>
        ${(json.missing||[]).length ? `<p style="font-size:.75rem;color:var(--amber)">⚠ ${json.missing.join(' · ')}</p>` : ''}
      </div>`;
  } catch(e){
    result.innerHTML = '<p style="color:var(--red);font-size:.8rem">Error al analizar. Intenta de nuevo.</p>';
  }
}

// ════════════════════════════════════
//  GENERATOR
// ════════════════════════════════════
function renderGeneratorCheckboxes() {
  const el = document.getElementById('generatorCheckboxes');
  if(!el) return;
  el.innerHTML = Object.entries(SERVICES).map(([k,s]) =>
    `<label style="display:inline-flex;align-items:center;gap:7px;background:var(--s2);border:1px solid var(--border2);border-radius:8px;padding:6px 12px;cursor:pointer;font-size:.8rem">
      <input type="checkbox" id="gen-${k}" ${connections[k]?'checked':''} style="accent-color:var(--accent)">
      ${s.icon} ${s.name}
    </label>`
  ).join('');
}

function generateBackend() {
  const selected = Object.keys(SERVICES).filter(k => document.getElementById('gen-'+k)?.checked);
  const result   = document.getElementById('generatorResult');
  if(!selected.length){ result.innerHTML='<p style="color:var(--red);font-size:.8rem">Selecciona al menos una integración.</p>'; return; }
  result.innerHTML = `
    <div style="background:var(--s2);border:1px solid var(--green-g);border-radius:10px;padding:1rem;margin-top:1rem">
      <p style="font-size:.82rem;color:var(--green);font-weight:600;margin-bottom:.5rem">✓ Backend generado — ${selected.length} integraciones</p>
      <p style="font-size:.75rem;color:var(--muted);margin-bottom:.75rem">server.js · ${selected.map(s=>'routes/'+s+'.js').join(' · ')} · .env.example · package.json</p>
      <p style="font-family:var(--mono);font-size:.72rem;color:var(--muted2);background:var(--bg);border-radius:6px;padding:8px 12px">
        npm install<br>
        node server.js<br>
        # Listo en http://localhost:3000
      </p>
      <p style="font-size:.72rem;color:var(--muted);margin-top:.75rem">💡 Ve al generador completo para descargar el código.</p>
    </div>`;
}

// ════════════════════════════════════
//  STRIPE CHECKOUT
// ════════════════════════════════════
async function startCheckout() {
  const msg = document.getElementById('checkoutMsg');
  msg.textContent = '⏳ Creando sesión de pago...';
  try {
    const stripe = Stripe(STRIPE_PK);
    // Create checkout session via Supabase Edge Function (or direct Stripe)
    // For demo: redirect to Stripe payment link
    const res = await fetch('https://api.stripe.com/v1/checkout/sessions', {
      method:'POST',
      headers:{
        'Authorization':'Bearer '+STRIPE_PK,
        'Content-Type':'application/x-www-form-urlencoded'
      },
      body: new URLSearchParams({
        'mode':'subscription',
        'line_items[0][price]': STRIPE_PRICE,
        'line_items[0][quantity]':'1',
        'success_url': location.href+'?upgrade=success',
        'cancel_url':  location.href,
        'customer_email': currentUser?.email || ''
      })
    });
    const session = await res.json();
    if(session.url){ location.href = session.url; }
    else { msg.textContent = 'Error al crear sesión. Intenta de nuevo.'; }
  } catch(e){
    msg.textContent = 'Error de conexión. Intenta de nuevo.';
  }
}

// ════════════════════════════════════
//  NAV
// ════════════════════════════════════
function showView(view) {
  document.querySelectorAll('.view').forEach(v => v.classList.remove('active'));
  document.querySelectorAll('.nav-item').forEach(n => n.classList.remove('active'));
  document.getElementById('view-'+view)?.classList.add('active');
  document.getElementById('nav-'+view)?.classList.add('active');
  if(view==='integrations') renderIntGrids();
  if(view==='generator') renderGeneratorCheckboxes();
}

// ════════════════════════════════════
//  INIT
// ════════════════════════════════════
// Check upgrade success
if(location.search.includes('upgrade=success')){
  userPlan = 'pro';
  history.replaceState(null,'',location.pathname);
}

checkSession();
</script>
</body>
</html>
