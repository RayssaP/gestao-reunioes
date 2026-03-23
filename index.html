<!DOCTYPE html>
<html lang="pt-BR">
<head>
<meta charset="UTF-8"/>
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>
<title>Gestão de Reuniões</title>
<link href="https://fonts.googleapis.com/css2?family=Crimson+Pro:wght@300;400;500;600;700&family=DM+Mono:wght@300;400;500&display=swap" rel="stylesheet"/>
<script src="https://accounts.google.com/gsi/client" async defer></script>
<style>
  *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }
  :root {
    --bg: #F1F5F9; --bg2: #FFFFFF; --bg3: #E2E8F0;
    --text: #1E293B; --text2: #475569; --text3: #94A3B8;
    --accent: #F59E0B; --accent2: #D97706;
    --blue: #1D4ED8; --green: #15803D;
    --font-body: 'Crimson Pro', Georgia, serif;
    --font-mono: 'DM Mono', monospace;
  }
  body.dark {
    --bg: #0F172A; --bg2: #1E293B; --bg3: #334155;
    --text: #F1F5F9; --text2: #CBD5E1; --text3: #64748B;
    --blue: #3B82F6; --green: #22C55E;
  }
  body.dark #header { background: linear-gradient(135deg, #1E293B 0%, #0F172A 100%) !important; }
  body.dark .modal { background: #1E293B !important; }
  body.dark input, body.dark textarea, body.dark select { background: #0F172A !important; color: var(--text) !important; border-color: var(--bg3) !important; }
  body.dark .search-input { background: #0F172A !important; }
  body.dark .inp { background: #0F172A !important; }
  body.dark .add-form, body.dark .item-card { background: #0F172A !important; }
  body.dark .participant-card { background: #0F172A !important; }
  body.dark .ref-item { background: #0F172A !important; }
  body.dark .od-user-card { background: #14532D33 !important; }
  body, html { transition: background 0.3s, color 0.3s; }
  html, body { height: 100%; overflow: hidden; }
  body { font-family: var(--font-body); background: var(--bg); color: var(--text); display: flex; flex-direction: column; }
  ::-webkit-scrollbar { width: 6px; height: 6px; }
  ::-webkit-scrollbar-track { background: var(--bg); }
  ::-webkit-scrollbar-thumb { background: #CBD5E1; border-radius: 3px; }
  input, select, textarea, button { font-family: var(--font-body); }
  button { cursor: pointer; }

  /* HEADER */
  #header {
    background: linear-gradient(135deg, #FFFFFF 0%, #F8FAFC 100%);
    border-bottom: 1px solid var(--bg3); box-shadow: 0 1px 4px rgba(0,0,0,0.08);
    padding: 0 24px; height: 64px;
    display: flex; align-items: center; justify-content: space-between;
    flex-shrink: 0; z-index: 10;
  }
  .header-left { display: flex; align-items: center; gap: 14px; }
  .logo { width: 36px; height: 36px; background: linear-gradient(135deg, #F59E0B, #D97706); border-radius: 8px; display: flex; align-items: center; justify-content: center; font-size: 18px; flex-shrink: 0; }
  .header-title { font-weight: 700; font-size: 18px; color: #1E293B; letter-spacing: -0.3px; }
  .header-sub { font-size: 11px; color: var(--text3); font-family: var(--font-mono); letter-spacing: 0.05em; }
  .header-right { display: flex; gap: 10px; align-items: center; }

  /* BUTTONS */
  .btn { padding: 8px 16px; border-radius: 8px; font-size: 13px; display: inline-flex; align-items: center; gap: 6px; transition: all 0.15s; border: none; color: var(--text); }
  .btn-ghost { background: var(--bg2); border: 1px solid var(--bg3) !important; }
  .btn-ghost:hover { background: var(--bg3); }
  .btn-primary { background: linear-gradient(135deg, #F59E0B, #D97706); color: #0F172A; font-weight: 700; }
  .btn-primary:hover { opacity: 0.9; }
  .btn-blue { background: var(--blue); color: #fff; }
  .btn-blue:hover { opacity: 0.9; }
  .btn-green { background: var(--green); color: #fff; }
  .btn-green:hover { opacity: 0.9; }
  .btn-danger { background: #DC2626; color: #fff; font-weight: 700; }
  .btn-sm { padding: 5px 10px; font-size: 12px; }
  .btn-icon { background: none; border: none; color: #EF4444; font-size: 18px; padding: 2px 6px; }

  /* AI DOT */
  .ai-dot { display: none; }

  /* LAYOUT */
  #app { display: flex; flex: 1; overflow: hidden; }
  #sidebar { width: 300px; min-width: 300px; background: var(--bg2); border-right: 1px solid var(--bg3); display: flex; flex-direction: column; overflow: hidden; }
  #main { flex: 1; overflow: auto; display: flex; }
  #content { flex: 1; }

  /* SIDEBAR */
  .sidebar-filters { padding: 16px 16px 12px; }
  .sidebar-list { flex: 1; overflow-y: auto; padding: 0 8px 16px; }
  .search-input { width: 100%; background: #F8FAFC; border: 1px solid var(--bg3); border-radius: 8px; padding: 8px 12px; color: var(--text); font-size: 13px; outline: none; }
  .search-input:focus { border-color: var(--accent); }
  .filter-chips { display: flex; gap: 6px; margin-top: 10px; flex-wrap: wrap; }
  .chip { font-size: 11px; padding: 3px 10px; border-radius: 20px; border: 1px solid var(--bg3); background: transparent; color: var(--text2); font-family: var(--font-mono); transition: all 0.15s; cursor: pointer; }
  .chip.active { background: var(--accent); color: #fff; border-color: var(--accent); }

  .meeting-card { padding: 12px; border-radius: 10px; margin-bottom: 4px; cursor: pointer; transition: all 0.15s; border: 1px solid transparent; }
  .meeting-card:hover { background: rgba(0,0,0,0.03); }
  .meeting-card.active { background: var(--bg); border-color: var(--bg3); }
  .card-title { font-weight: 600; font-size: 14px; color: #475569; line-height: 1.3; margin-bottom: 4px; }
  .meeting-card.active .card-title { color: #1E293B; }
  .card-date { font-size: 12px; color: var(--text3); font-family: var(--font-mono); }
  .card-participants { font-size: 12px; color: var(--text2); margin-top: 3px; }
  .card-top { display: flex; justify-content: space-between; align-items: flex-start; gap: 8px; }

  /* STATUS BADGE */
  .badge { font-size: 11px; padding: 2px 8px; border-radius: 10px; font-family: var(--font-mono); display: inline-flex; align-items: center; gap: 4px; white-space: nowrap; }
  .badge-dot { width: 6px; height: 6px; border-radius: 50%; display: inline-block; }
  .badge-Agendada { background: #EFF6FF; color: #1D4ED8; }
  .badge-Agendada .badge-dot { background: #3B82F6; }
  .badge-Realizada { background: #F0FDF4; color: #15803D; }
  .badge-Realizada .badge-dot { background: #22C55E; }
  .badge-Cancelada { background: #FEF2F2; color: #B91C1C; }
  .badge-Cancelada .badge-dot { background: #EF4444; }
  .badge-Adiada { background: #FFFBEB; color: #B45309; }
  .badge-Adiada .badge-dot { background: #F59E0B; }

  /* DASHBOARD */
  #view-empty { height: 100%; overflow-y: auto; }
  .dash { padding: 32px 40px; max-width: 960px; margin: 0 auto; }
  .dash-greeting { margin-bottom: 28px; }
  .dash-greeting h1 { font-size: 26px; font-weight: 700; color: #1E293B; margin-bottom: 4px; }
  .dash-greeting p { font-size: 14px; color: var(--text3); font-family: var(--font-mono); }
  .kpi-grid { display: grid; grid-template-columns: repeat(4, 1fr); gap: 14px; margin-bottom: 24px; }
  .kpi { background: var(--bg2); border: 1px solid var(--bg3); border-radius: 12px; padding: 18px 20px; position: relative; overflow: hidden; }
  .kpi::before { content:''; position:absolute; inset:0; opacity:0.04; }
  .kpi-label { font-size: 11px; font-family: var(--font-mono); color: var(--text3); letter-spacing: 0.05em; text-transform: uppercase; margin-bottom: 10px; }
  .kpi-value { font-size: 36px; font-weight: 700; color: #1E293B; line-height: 1; margin-bottom: 4px; }
  .kpi-sub { font-size: 12px; color: var(--text3); }
  .kpi-icon { position: absolute; right: 16px; top: 14px; font-size: 22px; opacity: 0.6; }
  .kpi-bar { height: 3px; border-radius: 2px; margin-top: 12px; background: var(--bg3); overflow: hidden; }
  .kpi-bar-fill { height: 100%; border-radius: 2px; transition: width 0.6s ease; }

  .dash-row { display: grid; grid-template-columns: 1fr 1fr; gap: 20px; margin-bottom: 20px; }
  .dash-row-3 { display: grid; grid-template-columns: 1fr 1fr 1fr; gap: 20px; margin-bottom: 20px; }
  .dash-card { background: var(--bg2); border: 1px solid var(--bg3); border-radius: 12px; overflow: hidden; }
  .dash-card-head { padding: 14px 18px; border-bottom: 1px solid var(--bg3); font-size: 13px; font-family: var(--font-mono); color: var(--text2); font-weight: 600; letter-spacing: 0.03em; display: flex; justify-content: space-between; align-items: center; }
  .dash-card-body { padding: 16px 18px; }
  .dash-list-item { display: flex; align-items: center; gap: 10px; padding: 8px 0; border-bottom: 1px solid rgba(0,0,0,0.07); }
  .dash-list-item:last-child { border-bottom: none; }
  .dash-list-bar-wrap { flex: 1; }
  .dash-list-label { font-size: 13px; color: #475569; margin-bottom: 4px; display: flex; justify-content: space-between; }
  .dash-list-bar { height: 5px; background: var(--bg3); border-radius: 3px; overflow: hidden; }
  .dash-list-bar-fill { height: 100%; border-radius: 3px; }
  .dash-pill { font-size: 11px; font-family: var(--font-mono); padding: 3px 10px; border-radius: 20px; }
  .dash-empty { color: var(--text3); font-size: 13px; font-style: italic; text-align: center; padding: 16px 0; }

  .status-chart { display: flex; gap: 8px; align-items: stretch; height: 60px; border-radius: 8px; overflow: hidden; margin-bottom: 14px; }
  .status-bar-seg { display: flex; align-items: center; justify-content: center; font-size: 11px; font-weight: 700; color: rgba(0,0,0,0.7); transition: all 0.4s ease; font-family: var(--font-mono); border-radius: 6px; min-width: 0; overflow: hidden; }
  .status-legend { display: flex; gap: 14px; flex-wrap: wrap; }
  .status-legend-item { display: flex; align-items: center; gap: 5px; font-size: 12px; color: var(--text2); }
  .status-legend-dot { width: 8px; height: 8px; border-radius: 50%; flex-shrink: 0; }

  .recent-item { display: flex; gap: 12px; align-items: flex-start; padding: 10px 0; border-bottom: 1px solid rgba(0,0,0,0.07); cursor: pointer; transition: background 0.15s; border-radius: 6px; }
  .recent-item:last-child { border-bottom: none; }
  .recent-item:hover { background: rgba(0,0,0,0.04); }
  .recent-dot { width: 8px; height: 8px; border-radius: 50%; margin-top: 5px; flex-shrink: 0; }
  .recent-title { font-size: 13px; font-weight: 600; color: #334155; margin-bottom: 2px; }
  .recent-meta { font-size: 11px; color: var(--text3); font-family: var(--font-mono); }

  .action-item { display: flex; gap: 10px; align-items: flex-start; padding: 8px 0; border-bottom: 1px solid rgba(0,0,0,0.07); }
  .action-item:last-child { border-bottom: none; }
  .action-text { font-size: 13px; color: #475569; flex: 1; }
  .action-meta { font-size: 11px; color: var(--text3); margin-top: 2px; font-family: var(--font-mono); }
  .overdue { color: #FCA5A5 !important; }

  @keyframes fadeUp { from{opacity:0;transform:translateY(12px)} to{opacity:1;transform:translateY(0)} }
  .dash > * { animation: fadeUp 0.35s ease both; }
  .dash > *:nth-child(2) { animation-delay: 0.05s; }
  .dash > *:nth-child(3) { animation-delay: 0.1s; }
  .dash > *:nth-child(4) { animation-delay: 0.15s; }
  .dash > *:nth-child(5) { animation-delay: 0.2s; }

  /* INPUTS */
  .inp { background: #F8FAFC; border: 1px solid var(--bg3); border-radius: 8px; padding: 9px 12px; color: var(--text); font-size: 14px; font-family: var(--font-body); outline: none; width: 100%; transition: border 0.15s; }
  .inp:focus { border-color: var(--accent); }
  textarea.inp { resize: vertical; }
  select.inp { cursor: pointer; }
  label.lbl { display: block; font-size: 11px; font-family: var(--font-mono); color: var(--text3); margin-bottom: 5px; letter-spacing: 0.05em; text-transform: uppercase; }

  /* GRID HELPERS */
  .grid2 { display: grid; grid-template-columns: 1fr 1fr; gap: 14px; }
  .grid2auto { display: grid; grid-template-columns: repeat(auto-fill, minmax(240px, 1fr)); gap: 10px; }

  /* SECTION CARD */
  .section-card { background: var(--bg2); border-radius: 12px; border: 1px solid var(--bg3); overflow: hidden; margin-bottom: 20px; }
  .section-head { padding: 12px 18px; border-bottom: 1px solid var(--bg3); font-weight: 600; font-size: 14px; color: var(--text2); font-family: var(--font-mono); letter-spacing: 0.03em; }
  .section-body { padding: 14px 18px; }
  .section-empty { color: var(--text3); font-size: 13px; font-style: italic; }

  /* DETAIL */
  #detail-view { padding: 32px 40px; max-width: 860px; margin: 0 auto; }
  .detail-header { display: flex; justify-content: space-between; align-items: flex-start; margin-bottom: 28px; }
  .detail-title { font-size: 28px; font-weight: 700; color: #1E293B; line-height: 1.2; margin: 8px 0 0; }
  .detail-location { font-size: 14px; color: var(--text3); margin-top: 6px; }
  .detail-actions { display: flex; gap: 8px; }

  /* FORM */
  #form-view { padding: 28px 40px; max-width: 860px; margin: 0 auto; }
  .form-header { display: flex; justify-content: space-between; align-items: center; margin-bottom: 24px; }
  .form-title { font-size: 24px; font-weight: 700; color: #1E293B; }
  .form-header-btns { display: flex; gap: 10px; }

  /* TABS */
  .tabs { display: flex; gap: 4px; border-bottom: 1px solid var(--bg3); margin-bottom: 20px; }
  .tab { padding: 8px 14px; background: none; border: none; color: var(--text3); font-family: var(--font-body); font-size: 14px; cursor: pointer; border-bottom: 2px solid transparent; margin-bottom: -1px; transition: all 0.15s; }
  .tab.active { color: var(--accent); border-bottom-color: var(--accent); }
  .tab-panel { display: none; }
  .tab-panel.active { display: block; }

  /* ITEM CARDS */
  .item-card { display: flex; gap: 12px; padding: 12px 16px; background: #F8FAFC; border-radius: 10px; border: 1px solid var(--bg3); margin-bottom: 8px; align-items: flex-start; }
  .item-card-ref { cursor: pointer; }
  .item-card-ref:hover { border-color: #3B82F6; }
  .item-num { width: 24px; height: 24px; border-radius: 50%; background: var(--bg3); display: flex; align-items: center; justify-content: center; font-size: 12px; flex-shrink: 0; margin-top: 2px; font-family: var(--font-mono); }
  .item-num.done { background: var(--green); }
  .item-body { flex: 1; }
  .item-title { font-size: 14px; color: var(--text); font-weight: 500; }
  .item-meta { display: flex; gap: 16px; margin-top: 4px; font-size: 12px; color: var(--text3); }
  .item-status-pending { color: #F59E0B; }
  .item-status-done { color: #4ADE80; }

  /* PARTICIPANT CARD */
  .participant-card { padding: 12px 14px; background: #F8FAFC; border-radius: 10px; border: 1px solid var(--bg3); }
  .participant-name { font-weight: 600; font-size: 14px; color: #1E293B; margin-bottom: 4px; }
  .participant-org { font-size: 12px; color: var(--accent); font-family: var(--font-mono); margin-bottom: 6px; }
  .participant-contact { font-size: 12px; color: var(--text2); }

  /* ADD FORM */
  .add-form { padding: 16px; background: #F8FAFC; border-radius: 10px; border: 1px solid var(--bg3); margin-bottom: 12px; }
  .add-form-row { display: grid; grid-template-columns: 1fr 1fr; gap: 10px; margin-top: 10px; }
  .add-form-full { grid-column: 1/-1; }

  /* REFERENCE ITEM */
  .ref-item { display: flex; gap: 12px; align-items: center; padding: 12px 16px; background: #F8FAFC; border-radius: 8px; border: 1px solid var(--bg3); margin-bottom: 6px; cursor: pointer; transition: border-color 0.15s; }
  .ref-item.checked { border-color: var(--blue); }
  .ref-checkbox { width: 18px; height: 18px; border-radius: 4px; border: 2px solid #475569; background: transparent; display: flex; align-items: center; justify-content: center; font-size: 11px; color: #fff; flex-shrink: 0; transition: all 0.15s; }
  .ref-checkbox.checked { background: #3B82F6; border-color: #3B82F6; }
  .ref-title { font-size: 14px; font-weight: 600; color: var(--text); }
  .ref-date { font-size: 12px; color: var(--text3); font-family: var(--font-mono); margin-top: 2px; }

  /* MODAL */
  .modal-overlay { position: fixed; inset: 0; background: rgba(0,0,0,0.3); display: flex; align-items: center; justify-content: center; z-index: 1000; backdrop-filter: blur(4px); }
  .modal-overlay.hidden { display: none; }
  .modal { background: var(--bg2); border-radius: 14px; padding: 28px 32px; min-width: 420px; max-width: 520px; border: 1px solid var(--bg3); box-shadow: 0 20px 60px rgba(0,0,0,0.18); }
  .modal-header { display: flex; justify-content: space-between; align-items: center; margin-bottom: 20px; }
  .modal-title { font-weight: 700; font-size: 18px; color: #1E293B; }
  .modal-close { background: none; border: none; color: var(--text3); font-size: 22px; }
  .modal-body { display: flex; flex-direction: column; gap: 16px; }
  .modal-text { color: #475569; margin-bottom: 8px; }
  .modal-btns { display: flex; gap: 10px; justify-content: flex-end; }

  /* TOAST */
  #toast { position: fixed; bottom: 24px; right: 24px; padding: 12px 20px; border-radius: 10px; font-size: 14px; font-weight: 500; box-shadow: 0 4px 20px rgba(0,0,0,0.4); z-index: 9999; border: 1px solid rgba(0,0,0,0.08); animation: slideIn 0.3s ease; display: none; }
  #toast.success { background: #15803D; color: #fff; }
  #toast.info { background: var(--bg2); color: var(--text); }

  /* DOC ITEM */
  .doc-item { display: flex; gap: 10px; align-items: center; padding: 10px 14px; background: #F8FAFC; border-radius: 8px; border: 1px solid var(--bg3); margin-bottom: 6px; }
  .doc-icon { font-size: 20px; }
  .doc-name { font-size: 14px; color: #475569; overflow: hidden; text-overflow: ellipsis; white-space: nowrap; }
  .doc-desc { font-size: 12px; color: var(--text3); }

  /* DASHBOARD */
  .dash { padding: 32px 40px; max-width: 960px; margin: 0 auto; overflow-y: auto; }
  .dash-greeting { margin-bottom: 28px; }
  .dash-greeting h2 { font-size: 26px; font-weight: 700; color: #1E293B; margin-bottom: 4px; }
  .dash-greeting p { font-size: 14px; color: var(--text3); font-family: var(--font-mono); }
  .kpi-grid { display: grid; grid-template-columns: repeat(4, 1fr); gap: 14px; margin-bottom: 28px; }
  .kpi-card { background: var(--bg2); border: 1px solid var(--bg3); border-radius: 14px; padding: 18px 20px; position: relative; overflow: hidden; transition: border-color 0.2s; }
  .kpi-card:hover { border-color: var(--accent); }
  .kpi-card::before { content:''; position:absolute; inset:0; background: linear-gradient(135deg, rgba(0,0,0,0.01), transparent); pointer-events:none; }
  .kpi-icon { font-size: 22px; margin-bottom: 10px; }
  .kpi-value { font-size: 32px; font-weight: 700; color: #1E293B; line-height: 1; margin-bottom: 4px; font-family: var(--font-mono); }
  .kpi-label { font-size: 12px; color: var(--text3); font-family: var(--font-mono); letter-spacing: 0.04em; text-transform: uppercase; }
  .kpi-sub { font-size: 11px; color: var(--text2); margin-top: 6px; }
  .kpi-accent-green { border-left: 3px solid #22C55E; }
  .kpi-accent-blue { border-left: 3px solid #3B82F6; }
  .kpi-accent-amber { border-left: 3px solid #F59E0B; }
  .kpi-accent-purple { border-left: 3px solid #A78BFA; }
  .dash-row { display: grid; grid-template-columns: 1fr 1fr; gap: 20px; margin-bottom: 24px; }
  .dash-row3 { display: grid; grid-template-columns: 1fr 1fr 1fr; gap: 20px; margin-bottom: 24px; }
  .dash-card { background: var(--bg2); border: 1px solid var(--bg3); border-radius: 14px; overflow: hidden; }
  .dash-card-head { padding: 14px 18px; border-bottom: 1px solid var(--bg3); font-weight: 600; font-size: 13px; color: var(--text2); font-family: var(--font-mono); letter-spacing: 0.04em; text-transform: uppercase; display: flex; justify-content: space-between; align-items: center; }
  .dash-card-body { padding: 16px 18px; }
  .dash-card-empty { color: var(--text3); font-size: 13px; font-style: italic; text-align: center; padding: 20px 0; }
  /* Status bars */
  .status-bar-row { display: flex; flex-direction: column; gap: 10px; }
  .status-bar-item { display: flex; flex-direction: column; gap: 4px; }
  .status-bar-top { display: flex; justify-content: space-between; align-items: center; font-size: 13px; }
  .status-bar-label { color: var(--text2); }
  .status-bar-count { font-family: var(--font-mono); font-size: 12px; color: var(--text3); }
  .status-bar-track { height: 6px; background: var(--bg3); border-radius: 3px; overflow: hidden; }
  .status-bar-fill { height: 100%; border-radius: 3px; transition: width 0.6s ease; }
  /* Org list */
  .org-item { display: flex; justify-content: space-between; align-items: center; padding: 8px 0; border-bottom: 1px solid rgba(0,0,0,0.07); }
  .org-item:last-child { border-bottom: none; }
  .org-name { font-size: 13px; color: var(--text); font-weight: 500; white-space: nowrap; overflow: hidden; text-overflow: ellipsis; max-width: 180px; }
  .org-pill { font-size: 11px; font-family: var(--font-mono); background: var(--bg3); color: var(--text2); padding: 2px 8px; border-radius: 10px; white-space: nowrap; }
  /* Recent list */
  .recent-item { display: flex; gap: 12px; padding: 10px 0; border-bottom: 1px solid rgba(0,0,0,0.07); cursor: pointer; transition: background 0.15s; }
  .recent-item:last-child { border-bottom: none; }
  .recent-item:hover { opacity: 0.85; }
  .recent-dot { width: 8px; height: 8px; border-radius: 50%; flex-shrink: 0; margin-top: 5px; }
  .recent-title { font-size: 13px; color: var(--text); font-weight: 500; line-height: 1.4; }
  .recent-meta { font-size: 11px; color: var(--text3); font-family: var(--font-mono); margin-top: 2px; }
  /* Action items */
  .action-item { display: flex; gap: 10px; padding: 9px 0; border-bottom: 1px solid rgba(0,0,0,0.07); align-items: flex-start; }
  .action-item:last-child { border-bottom: none; }
  .action-check { width: 16px; height: 16px; border-radius: 50%; border: 2px solid #F59E0B; flex-shrink: 0; margin-top: 2px; }
  .action-text { font-size: 13px; color: var(--text2); flex: 1; line-height: 1.4; }
  .action-who { font-size: 11px; color: var(--text3); margin-top: 2px; font-family: var(--font-mono); }
  /* Timeline donut / progress ring */
  .donut-wrap { display: flex; align-items: center; gap: 20px; }
  .donut-legend { display: flex; flex-direction: column; gap: 8px; flex: 1; }
  .donut-legend-item { display: flex; align-items: center; gap: 8px; font-size: 12px; color: var(--text2); }
  .donut-legend-dot { width: 10px; height: 10px; border-radius: 50%; flex-shrink: 0; }
  /* Upcoming badge */
  .upcoming-item { display: flex; gap: 12px; align-items: center; padding: 10px 0; border-bottom: 1px solid rgba(0,0,0,0.07); cursor: pointer; }
  .upcoming-item:last-child { border-bottom: none; }
  .upcoming-item:hover { opacity: 0.85; }
  .upcoming-date-box { background: #F8FAFC; border: 1px solid var(--bg3); border-radius: 8px; padding: 6px 10px; text-align: center; min-width: 46px; }
  .upcoming-day { font-size: 18px; font-weight: 700; color: #1E293B; font-family: var(--font-mono); line-height: 1; }
  .upcoming-mon { font-size: 10px; color: var(--text3); font-family: var(--font-mono); text-transform: uppercase; }
  .upcoming-title { font-size: 13px; font-weight: 500; color: var(--text); line-height: 1.4; }
  .upcoming-loc { font-size: 11px; color: var(--text3); margin-top: 2px; }

  /* ── HAMBURGER ── */
  .btn-hamburger {
    display: none; flex-direction: column; justify-content: center; gap: 5px;
    background: none; border: none; padding: 6px; cursor: pointer;
    width: 34px; height: 34px; border-radius: 8px; flex-shrink: 0;
  }
  @media (max-width: 768px) { .btn-hamburger { display: flex; } }
  .btn-hamburger span {
    display: block; width: 20px; height: 2px;
    background: var(--text2); border-radius: 2px; transition: all 0.25s;
  }
  .btn-hamburger.open span:nth-child(1) { transform: translateY(7px) rotate(45deg); }
  .btn-hamburger.open span:nth-child(2) { opacity: 0; }
  .btn-hamburger.open span:nth-child(3) { transform: translateY(-7px) rotate(-45deg); }

  /* Sidebar overlay backdrop */
  #sidebar-overlay {
    display: none; position: fixed; inset: 0; background: rgba(0,0,0,0.55);
    z-index: 99; backdrop-filter: blur(2px);
  }
  #sidebar-overlay.show { display: block; }

  /* ── TABLET LANDSCAPE  ≤ 1100px ── */
  @media (max-width: 1100px) {
    #sidebar { width: 260px; min-width: 260px; }
    .dash { padding: 24px 28px; }
    #detail-view { padding: 24px 28px; }
    #form-view  { padding: 22px 28px; }
    .kpi-value  { font-size: 28px; }
    .kpi-grid   { gap: 10px; }
    .modal      { min-width: 360px; }
  }

  /* ── TABLET PORTRAIT  ≤ 768px ── */
  @media (max-width: 768px) {
    /* Header — duas linhas no mobile */
    #header {
      padding: 0 12px;
      height: auto;
      min-height: 56px;
      flex-wrap: wrap;
      gap: 6px;
      padding-top: 8px;
      padding-bottom: 8px;
    }
    .header-left { flex: 1; min-width: 0; gap: 8px; }
    .header-title { font-size: 14px; white-space: nowrap; overflow: hidden; text-overflow: ellipsis; }
    .header-sub   { display: none; }
    .logo { width: 28px; height: 28px; font-size: 14px; flex-shrink: 0; }
    .header-right {
      width: 100%;
      justify-content: flex-end;
      gap: 6px;
      flex-wrap: nowrap;
      overflow-x: auto;
      -webkit-overflow-scrolling: touch;
      padding-bottom: 2px;
    }
    .header-right::-webkit-scrollbar { display: none; }

    /* Botões do header — compactos */
    .od-btn        { padding: 5px 8px; font-size: 11px; gap: 4px; }
    #od-indicator  { width: 6px; height: 6px; }
    #btn-ai-search { padding: 5px 8px; font-size: 11px; gap: 4px; }
    .btn-label-search { font-size: 11px; }
    #btn-settings  { padding: 5px 8px; font-size: 13px; }
    .btn-label-cfg { display: none; }
    .btn-label-search { display: none; }
    #btn-new       { padding: 6px 10px; font-size: 18px; font-weight: 700; line-height: 1; }
    .btn-label-new { display: none; }

    /* Sidebar — drawer */
    #sidebar {
      position: fixed; top: 0; left: 0; bottom: 0;
      width: 280px; min-width: 0;
      z-index: 200; transform: translateX(-100%);
      transition: transform 0.28s cubic-bezier(.4,0,.2,1);
      box-shadow: 4px 0 24px rgba(0,0,0,0.15);
    }
    #sidebar.open { transform: translateX(0); }
    #sidebar-overlay { z-index: 199; }

    /* Main fills full width */
    #main { flex-direction: column; overflow: hidden; }
    #content { overflow-y: auto; flex: 1; }

    /* Dashboard */
    #view-empty { height: calc(100vh - 96px); }
    .dash { padding: 14px 12px 80px; }
    .dash-greeting h1 { font-size: 18px; }
    .dash-greeting p  { font-size: 11px; }
    .kpi-grid { grid-template-columns: 1fr 1fr; gap: 8px; margin-bottom: 14px; }
    .kpi { padding: 12px 14px; }
    .kpi-value { font-size: 28px; }
    .kpi-label { font-size: 10px; }
    .kpi-sub   { font-size: 10px; }
    .kpi-icon  { font-size: 18px; top: 10px; right: 10px; }
    .dash-row  { grid-template-columns: 1fr; gap: 12px; margin-bottom: 12px; }
    .dash-row-3 { grid-template-columns: 1fr; gap: 12px; margin-bottom: 12px; }
    .dash-card-head { font-size: 11px; padding: 10px 12px; }
    .dash-card-body { padding: 10px 12px; }
    .dash-list-label { font-size: 12px; }

    /* Detail view */
    #view-detail { overflow-y: auto; height: calc(100vh - 96px); }
    #detail-view { padding: 14px 12px 80px; max-width: 100%; }
    .detail-header { flex-direction: column; gap: 12px; margin-bottom: 16px; }
    .detail-title  { font-size: 20px; }
    .detail-actions { width: 100%; justify-content: flex-end; }
    .grid2 { grid-template-columns: 1fr; }
    .grid2auto { grid-template-columns: 1fr; }
    .section-card { margin-bottom: 12px; }
    .section-head { font-size: 12px; padding: 10px 12px; }
    .section-body { padding: 10px 12px; }

    /* Form view */
    #view-form { overflow-y: auto; height: calc(100vh - 96px); }
    #form-view { padding: 14px 12px 80px; max-width: 100%; }
    .form-header { flex-direction: column; gap: 10px; align-items: flex-start; margin-bottom: 14px; }
    .form-title  { font-size: 18px; }
    .form-header-btns { width: 100%; justify-content: flex-end; }
    .tabs { overflow-x: auto; -webkit-overflow-scrolling: touch; padding-bottom: 2px; }
    .tabs::-webkit-scrollbar { display: none; }
    .tab { white-space: nowrap; padding: 8px 10px; font-size: 12px; }
    .add-form-row { grid-template-columns: 1fr; }

    /* Modals */
    .modal { min-width: 0; width: calc(100vw - 24px); padding: 18px 14px; }
    .modal-title { font-size: 15px; }

    /* Toast */
    #toast { left: 12px; right: 12px; bottom: 12px; text-align: center; font-size: 13px; }
  }

  /* ── MINI PORTRAIT  ≤ 480px ── */
  @media (max-width: 480px) {
    .kpi-grid  { grid-template-columns: 1fr 1fr; gap: 8px; }
    .kpi-value { font-size: 24px; }
    .header-title { max-width: 120px; }
  }

  /* ── ONEDRIVE ── */
  .od-btn { display:inline-flex; align-items:center; gap:7px; padding:7px 13px; border-radius:8px; font-size:13px; border:1px solid var(--bg3); background:var(--bg2); color:var(--text2); cursor:pointer; transition:all .15s; white-space:nowrap; }
  .od-btn:hover { background:var(--bg3); }
  .od-btn.connected { border-color:#86efac; background:#f0fdf4; color:#15803d; }
  .od-btn.syncing   { border-color:#93c5fd; background:#eff6ff; color:#1d4ed8; }
  .od-btn.error     { border-color:#fca5a5; background:#fef2f2; color:#b91c1c; }
  .od-indicator { width:8px; height:8px; border-radius:50%; flex-shrink:0; }
  .od-indicator.off      { background:#475569; }
  .od-indicator.on       { background:#22c55e; box-shadow:0 0 6px #22c55e88; }
  .od-indicator.spin     { background:#3b82f6; animation:pulse 1s infinite; }
  .od-indicator.err      { background:#ef4444; }
  @keyframes pulse { 0%,100%{opacity:1} 50%{opacity:.4} }

  .od-setup { background:var(--bg); border:1px solid var(--bg3); border-radius:10px; padding:16px; display:flex; flex-direction:column; gap:12px; }
  .od-setup-title { font-size:14px; font-weight:600; color:#1E293B; display:flex; align-items:center; gap:8px; }
  .od-step { display:flex; gap:10px; font-size:13px; color:var(--text2); line-height:1.6; }
  .od-step-num { width:20px; height:20px; border-radius:50%; background:var(--bg3); color:var(--text2); font-family:var(--font-mono); font-size:11px; display:flex; align-items:center; justify-content:center; flex-shrink:0; margin-top:2px; }
  .od-user-card { display:flex; align-items:center; gap:12px; padding:12px 14px; background:#f0fdf4; border:1px solid #86efac; border-radius:10px; }
  .od-avatar { width:36px; height:36px; border-radius:50%; background:linear-gradient(135deg,#1d4ed8,#7c3aed); display:flex; align-items:center; justify-content:center; font-size:15px; flex-shrink:0; }
  .od-user-name { font-weight:600; font-size:14px; color:#1E293B; }
  .od-user-email { font-size:12px; color:#15803d; font-family:var(--font-mono); }
  .od-last-sync { font-size:11px; color:var(--text3); margin-top:2px; font-family:var(--font-mono); }

@keyframes bounce { 0%,80%,100%{transform:translateY(0)} 40%{transform:translateY(-6px)} }
@keyframes slideIn { from{transform:translateX(20px);opacity:0} to{transform:translateX(0);opacity:1} }
@keyframes fadeUp { from{opacity:0;transform:translateY(12px)} to{opacity:1;transform:translateY(0)} }
.dash-animate { animation: fadeUp 0.4s ease forwards; }
.dash-animate:nth-child(2) { animation-delay: 0.05s; }
.dash-animate:nth-child(3) { animation-delay: 0.1s; }
.dash-animate:nth-child(4) { animation-delay: 0.15s; }

/* ===== PRINT / PDF ===== */
@media print {
  * { -webkit-print-color-adjust: exact !important; print-color-adjust: exact !important; }

  body, html { overflow: visible !important; height: auto !important; background: #fff !important; }
  #header, #sidebar, #sidebar-overlay, #toast,
  .detail-actions, #detail-back,
  .action-toggle-btn, .action-edit-btn,
  .participant-edit-btn,
  .modal-overlay { display: none !important; }

  #app { display: block !important; }
  #main { display: block !important; overflow: visible !important; }
  #content { overflow: visible !important; }
  #view-detail { display: block !important; overflow: visible !important; height: auto !important; }
  #view-empty, #view-form { display: none !important; }

  #detail-view {
    padding: 0 !important; max-width: 100% !important;
    font-family: Georgia, serif !important;
    color: #1E293B !important;
  }

  /* Cabeçalho do PDF */
  .print-header {
    display: flex !important;
    justify-content: space-between;
    align-items: flex-start;
    padding-bottom: 16px;
    border-bottom: 3px solid #F59E0B;
    margin-bottom: 24px;
  }
  .print-logo {
    display: flex !important;
    align-items: center; gap: 10px;
    font-size: 13px; color: #64748B;
  }
  .print-logo-icon {
    width: 36px; height: 36px;
    background: linear-gradient(135deg, #F59E0B, #D97706);
    border-radius: 8px;
    display: flex !important;
    align-items: center; justify-content: center;
    font-size: 18px; color: #fff;
  }

  .detail-title { font-size: 22px !important; color: #1E293B !important; margin-bottom: 4px !important; }
  .detail-location { font-size: 13px !important; color: #64748B !important; }
  .badge { font-size: 11px !important; padding: 3px 10px !important; }

  .section-card {
    border: 1px solid #E2E8F0 !important;
    border-radius: 10px !important;
    break-inside: avoid;
    margin-bottom: 16px !important;
    background: #fff !important;
  }
  .section-head {
    background: #F8FAFC !important;
    padding: 10px 16px !important;
    font-size: 11px !important;
    font-weight: 700 !important;
    color: #475569 !important;
    letter-spacing: .05em !important;
    text-transform: uppercase !important;
    border-bottom: 1px solid #E2E8F0 !important;
  }
  .section-body { padding: 14px 16px !important; }
  .section-empty { color: #94A3B8 !important; font-style: italic !important; font-size: 13px !important; }

  .grid2 { display: grid !important; grid-template-columns: 1fr 1fr !important; gap: 16px !important; }
  .grid2auto { display: grid !important; grid-template-columns: repeat(auto-fill, minmax(200px, 1fr)) !important; gap: 10px !important; }

  .item-card {
    background: #F8FAFC !important;
    border: 1px solid #E2E8F0 !important;
    border-radius: 8px !important;
    padding: 10px 14px !important;
    margin-bottom: 8px !important;
    break-inside: avoid;
  }
  .item-title { font-size: 13px !important; color: #1E293B !important; }
  .item-meta { font-size: 11px !important; color: #64748B !important; margin-top: 4px !important; display: flex; gap: 12px; flex-wrap: wrap; }
  .item-status-pending { color: #F59E0B !important; }
  .item-status-done    { color: #22C55E !important; }

  .participant-card {
    background: #F8FAFC !important;
    border: 1px solid #E2E8F0 !important;
    border-radius: 8px !important;
    padding: 10px 12px !important;
    break-inside: avoid;
  }
  .participant-name { font-size: 13px !important; font-weight: 700 !important; color: #1E293B !important; }
  .participant-org  { font-size: 11px !important; color: #F59E0B !important; }
  .participant-contact { font-size: 11px !important; color: #475569 !important; margin-top: 4px !important; }

  .doc-item {
    background: #F8FAFC !important;
    border: 1px solid #E2E8F0 !important;
    border-radius: 8px !important;
    padding: 8px 12px !important;
    margin-bottom: 6px !important;
  }
  .doc-name { font-size: 13px !important; }
  .doc-desc { font-size: 11px !important; color: #64748B !important; }

  .print-footer {
    display: block !important;
    margin-top: 32px;
    padding-top: 12px;
    border-top: 1px solid #E2E8F0;
    font-size: 11px;
    color: #94A3B8;
    text-align: center;
  }
}
</style>
</head>
<body>

<!-- HEADER -->
<header id="header">
  <div class="header-left">
    <button class="btn-hamburger" id="btn-sidebar-toggle" aria-label="Menu">
      <span></span><span></span><span></span>
    </button>
    <div class="logo">📋</div>
    <div>
      <div class="header-title">Gestão de Reuniões</div>
      <div class="header-sub" id="meeting-count">0 REGISTROS</div>
    </div>
  </div>
  <div class="header-right">
    <button class="od-btn" id="btn-onedrive" title="Google Drive">
      <span class="od-indicator off" id="od-indicator"></span>
      <span id="od-btn-label">Drive</span>
    </button>
    <button class="btn btn-ghost" id="btn-ai-search" style="gap:6px">🔎 <span class="btn-label-search">Busca IA</span></button>    <button class="btn btn-ghost" id="btn-settings">⚙️ <span class="btn-label-cfg">Config</span></button>
    <button class="btn btn-primary" id="btn-new">+ <span class="btn-label-new">Nova Reunião</span></button>
  </div>
</header>

<div id="sidebar-overlay"></div>
<div id="app">
  <!-- SIDEBAR -->
  <aside id="sidebar">
    <div class="sidebar-filters">
      <input class="search-input" id="search" placeholder="🔍 Buscar reuniões..."/>
      <div class="filter-chips" id="filter-chips">
        <button class="chip active" data-status="Todas">Todas</button>
        <button class="chip" data-status="Agendada">Agendada</button>
        <button class="chip" data-status="Realizada">Realizada</button>
        <button class="chip" data-status="Cancelada">Cancelada</button>
        <button class="chip" data-status="Adiada">Adiada</button>
      </div>
    </div>
    <div class="sidebar-list" id="sidebar-list"></div>
  </aside>

  <!-- MAIN -->
  <main id="main">
    <div id="content">
      <!-- DASHBOARD -->
      <div id="view-empty" style="overflow-y:auto;height:100%">
        <div class="dash" id="dashboard-content"></div>
      </div>

      <!-- DETAIL VIEW -->
      <div id="view-detail" style="display:none">
        <div id="detail-view"></div>
      </div>

      <!-- FORM VIEW -->
      <div id="view-form" style="display:none">
        <div id="form-view"></div>
      </div>
    </div>

    <!-- AI PANEL -->
  </main>
</div>

<!-- AI SEARCH MODAL -->
<div class="modal-overlay hidden" id="modal-ai-search">
  <div class="modal" style="max-width:620px;width:calc(100vw - 32px);max-height:85vh;display:flex;flex-direction:column">
    <div class="modal-header" style="flex-shrink:0">
      <div class="modal-title">🔎 Busca Inteligente</div>
      <button class="modal-close" id="btn-ai-search-close">×</button>
    </div>
    <div style="flex-shrink:0;padding:0 0 14px">
      <div style="display:flex;gap:8px">
        <input class="inp" id="ai-search-input" placeholder="Ex: reuniões sobre licitação, encaminhamentos do João, reuniões de março..." style="flex:1;font-size:14px"/>
        <button class="btn btn-primary" id="btn-ai-search-send" style="flex-shrink:0;padding:9px 18px;font-size:14px">Buscar</button>
      </div>
      <div style="display:flex;gap:6px;flex-wrap:wrap;margin-top:10px" id="ai-search-suggestions">
        <button class="chip" data-sq="Quais reuniões tiveram encaminhamentos vencidos?">encaminhamentos vencidos</button>
        <button class="chip" data-sq="Liste as reuniões realizadas com mais participantes">mais participantes</button>
        <button class="chip" data-sq="Quais pautas se repetiram em mais de uma reunião?">pautas recorrentes</button>
        <button class="chip" data-sq="Mostre os encaminhamentos pendentes por responsável">pendentes por responsável</button>
        <button class="chip" data-sq="Qual foi a reunião mais recente?">última reunião</button>
      </div>
    </div>
    <div id="ai-search-result" style="flex:1;overflow-y:auto;padding:14px 16px;background:var(--bg);border-radius:10px;border:1px solid var(--bg3);font-size:14px;line-height:1.8;color:var(--text);min-height:80px;white-space:pre-wrap">
      <span style="color:var(--text3);font-style:italic">Faça uma pergunta sobre suas reuniões...</span>
    </div>
    <div style="flex-shrink:0;margin-top:12px;display:flex;justify-content:flex-end">
      <button class="btn btn-ghost" id="btn-ai-search-cancel">Fechar</button>
    </div>
  </div>
</div>

<!-- SETTINGS MODAL -->
<div class="modal-overlay hidden" id="modal-settings">
  <div class="modal" style="max-width:520px;width:calc(100vw - 32px);max-height:90vh;overflow-y:auto">
    <div class="modal-header">
      <div class="modal-title">⚙️ Configurações</div>
      <button class="modal-close" id="btn-settings-close">×</button>
    </div>
    <div class="modal-body">

      <!-- ONEDRIVE SECTION -->
      <div>
        <div style="font-size:12px;font-family:var(--font-mono);color:var(--text3);letter-spacing:.05em;text-transform:uppercase;margin-bottom:10px">☁️ Google Drive — sincronização em qualquer dispositivo</div>

        <!-- CONNECTED -->
        <div id="od-connected" style="display:none">
          <div class="od-user-card">
            <div class="od-avatar">☁️</div>
            <div style="flex:1;min-width:0">
              <div class="od-user-name" id="od-user-name-el">—</div>
              <div class="od-user-email" id="od-user-email-el">—</div>
              <div class="od-last-sync" id="od-last-sync-display">—</div>
            </div>
          </div>
          <div style="font-size:11px;color:var(--text3);padding:8px 10px;background:var(--bg);border-radius:6px;font-family:var(--font-mono);margin-top:8px;line-height:1.6">
            📁 Cada reunião é salva como arquivo separado em:<br>
            <span style="color:#93c5fd">Google Drive/GestaoReunioes/reunioes.json</span>
          </div>
          <div style="display:flex;gap:8px;margin-top:10px;flex-wrap:wrap">
            <button class="btn btn-green btn-sm" id="btn-od-sync-now" style="flex:1;justify-content:center;min-width:110px">🔄 Sincronizar agora</button>
            <button class="btn btn-ghost btn-sm" id="btn-od-import" style="flex:1;justify-content:center;min-width:110px">⬇️ Carregar do Drive</button>
            <button class="btn btn-ghost btn-sm" id="btn-od-disconnect" style="border-color:#7f1d1d;color:#fca5a5">Sair</button>
          </div>
        </div>

        <!-- NOT CONNECTED: setup -->
        <div id="od-disconnected">
          <div style="padding:12px 14px;background:#eff6ff;border:1px solid #bfdbfe;border-radius:10px;font-size:13px;color:#1d4ed8;line-height:1.8;margin-bottom:14px">
            🌐 Para funcionar bem, hospede este arquivo como site <strong>https://</strong> (Cloudflare Pages, GitHub Pages etc.).<br>
            Depois conecte sua conta Google e sincronize tudo pelo Drive.
          </div>

          <details style="margin-bottom:14px">
            <summary style="cursor:pointer;font-size:13px;color:var(--accent);font-weight:600;padding:8px 0;list-style:none">
              🔧 Como obter o Client ID do Google (apenas 1 vez)
            </summary>
            <div style="margin-top:10px;display:flex;flex-direction:column;gap:8px;font-size:13px">
              <div class="od-step"><div class="od-step-num">1</div><div>Acesse <a href="https://console.cloud.google.com/apis/credentials" target="_blank" style="color:#93c5fd">console.cloud.google.com</a> → <strong>APIs e serviços</strong> → <strong>Credenciais</strong></div></div>
              <div class="od-step"><div class="od-step-num">2</div><div>Crie ou selecione um projeto. Depois clique em <strong>Criar credenciais</strong> → <strong>ID do cliente OAuth</strong> → tipo <strong>Aplicativo da Web</strong>.</div></div>
              <div class="od-step"><div class="od-step-num">3</div><div>Em <strong>Origens JavaScript autorizadas</strong>, adicione a URL onde o sistema ficará publicado, por exemplo <strong>https://seusite.pages.dev</strong>.</div></div>
              <div class="od-step"><div class="od-step-num">4</div>
                <div>Ative a <strong>Google Drive API</strong>. Depois copie o <strong>Client ID OAuth</strong> e cole abaixo.
                  <div style="margin-top:6px;padding:8px 10px;background:#fffbeb;border:1px solid #fde68a;border-radius:6px;font-size:11px;color:#92400e">
                    ⚠️ Se você abrir este HTML como arquivo local (<code>file://</code> ou <code>content://</code>), o login do Google não ficará estável. Publique como site.
                  </div>
                </div>
              </div>
            </div>
          </details>

          <label class="lbl">Client ID OAuth do Google</label>
          <input class="inp" id="od-client-id-input" placeholder="1234567890-abcdefg.apps.googleusercontent.com" style="font-family:var(--font-mono);font-size:13px"/>
          <div style="font-size:11px;color:var(--text3);margin-top:4px;margin-bottom:12px">O Client ID não é segredo. Ele identifica seu app web no Google Cloud.</div>
          <button class="btn btn-blue" id="btn-od-connect" style="width:100%;justify-content:center;padding:10px;font-size:14px">
            🔐 Entrar com Google
          </button>
        </div>

        <!-- DEVICE CODE DIALOG (shown after requesting code) -->
        <div id="od-device-code-box" style="display:none;margin-top:12px;padding:16px;background:#fffbeb;border:2px solid var(--accent);border-radius:12px;text-align:center">
          <div style="font-size:13px;color:var(--text2);margin-bottom:10px">Acesse no seu navegador:</div>
          <a id="od-code-url" href="https://accounts.google.com" target="_blank" style="font-size:15px;font-weight:700;color:#93c5fd;display:block;margin-bottom:12px">accounts.google.com</a>
          <div style="font-size:13px;color:var(--text2);margin-bottom:8px">E digite o código:</div>
          <div id="od-code-display" style="font-size:28px;font-weight:800;letter-spacing:6px;color:#F59E0B;font-family:var(--font-mono);background:var(--bg);padding:12px 20px;border-radius:8px;display:inline-block;margin-bottom:12px">——————</div>
          <div id="od-code-status" style="font-size:12px;color:var(--text3);margin-top:6px">Aguardando login…</div>
          <button id="btn-od-cancel-code" class="btn btn-ghost btn-sm" style="margin-top:10px;width:100%;justify-content:center">Cancelar</button>
        </div>
      </div>

      <hr style="border:none;border-top:1px solid var(--bg3)"/>

      <!-- TEMA -->
      <div>
        <div style="font-size:12px;font-family:var(--font-mono);color:var(--text3);letter-spacing:.05em;text-transform:uppercase;margin-bottom:10px">🎨 Aparência</div>
        <div style="display:flex;gap:8px">
          <button class="theme-btn" data-theme="light" style="flex:1;padding:10px 8px;border-radius:10px;border:2px solid var(--bg3);background:var(--bg2);cursor:pointer;display:flex;flex-direction:column;align-items:center;gap:6px;transition:all .2s">
            <span style="font-size:20px">☀️</span>
            <span style="font-size:12px;font-family:var(--font-mono);color:var(--text2)">Claro</span>
          </button>
          <button class="theme-btn" data-theme="dark" style="flex:1;padding:10px 8px;border-radius:10px;border:2px solid var(--bg3);background:var(--bg2);cursor:pointer;display:flex;flex-direction:column;align-items:center;gap:6px;transition:all .2s">
            <span style="font-size:20px">🌙</span>
            <span style="font-size:12px;font-family:var(--font-mono);color:var(--text2)">Escuro</span>
          </button>
          <button class="theme-btn" data-theme="auto" style="flex:1;padding:10px 8px;border-radius:10px;border:2px solid var(--bg3);background:var(--bg2);cursor:pointer;display:flex;flex-direction:column;align-items:center;gap:6px;transition:all .2s">
            <span style="font-size:20px">🖥️</span>
            <span style="font-size:12px;font-family:var(--font-mono);color:var(--text2)">Sistema</span>
          </button>
        </div>
      </div>

      <hr style="border:none;border-top:1px solid var(--bg3)"/>

      <!-- AUTO-SYNC -->
      <div>
        <div style="font-size:12px;font-family:var(--font-mono);color:var(--text3);letter-spacing:.05em;text-transform:uppercase;margin-bottom:10px">🔄 Sincronização automática</div>
        <div style="display:flex;align-items:center;justify-content:space-between;gap:12px;padding:12px 14px;background:var(--bg);border-radius:10px;border:1px solid var(--bg3)">
          <div>
            <div style="font-size:13px;font-weight:600;color:var(--text)">Sincronizar em segundo plano</div>
            <div style="font-size:11px;color:var(--text3);font-family:var(--font-mono);margin-top:2px">Busca dados do Drive automaticamente</div>
          </div>
          <label style="position:relative;display:inline-block;width:44px;height:24px;flex-shrink:0">
            <input type="checkbox" id="toggle-autosync" style="opacity:0;width:0;height:0;position:absolute"/>
            <span id="autosync-slider" style="position:absolute;inset:0;border-radius:24px;background:#CBD5E1;cursor:pointer;transition:.3s">
              <span style="position:absolute;left:3px;top:3px;width:18px;height:18px;border-radius:50%;background:#fff;transition:.3s;display:block" id="autosync-knob"></span>
            </span>
          </label>
        </div>
        <div id="autosync-interval-row" style="margin-top:8px;display:flex;align-items:center;gap:10px;padding:10px 14px;background:var(--bg);border-radius:10px;border:1px solid var(--bg3)">
          <span style="font-size:13px;color:var(--text2)">Intervalo:</span>
          <select class="inp" id="autosync-interval" style="flex:1;padding:7px 10px;font-size:13px">
            <option value="1">A cada 1 minuto</option>
            <option value="5">A cada 5 minutos</option>
            <option value="10">A cada 10 minutos</option>
            <option value="30" selected>A cada 30 minutos</option>
          </select>
        </div>
      </div>

      <hr style="border:none;border-top:1px solid var(--bg3)"/>

      <hr style="border:none;border-top:1px solid var(--bg3)"/>

      <hr style="border:none;border-top:1px solid var(--bg3)"/>

      <button class="btn btn-ghost" id="btn-settings-save" style="width:100%;justify-content:center;padding:10px">Fechar</button>
    </div>
  </div>
</div>

<!-- EDIT PARTICIPANT MODAL -->
<div class="modal-overlay hidden" id="modal-edit-participant">
  <div class="modal" style="max-width:480px;width:calc(100vw - 32px)">
    <div class="modal-header">
      <div class="modal-title">✏️ Editar Participante</div>
      <button class="modal-close" id="btn-edit-participant-close">×</button>
    </div>
    <div class="modal-body">
      <div>
        <label class="lbl">Nome *</label>
        <input class="inp" id="edit-p-name" placeholder="Nome completo"/>
      </div>
      <div>
        <label class="lbl">Órgão / Instituição</label>
        <input class="inp" id="edit-p-org" placeholder="Ex: Secretaria de Saúde"/>
      </div>
      <div class="grid2">
        <div>
          <label class="lbl">E-mail</label>
          <input class="inp" id="edit-p-email" type="email" placeholder="email@exemplo.com"/>
        </div>
        <div>
          <label class="lbl">Telefone</label>
          <input class="inp" id="edit-p-phone" placeholder="(00) 00000-0000"/>
        </div>
      </div>
      <div class="modal-btns">
        <button class="btn btn-danger btn-sm" id="btn-edit-participant-delete">🗑️ Remover</button>
        <div style="flex:1"></div>
        <button class="btn btn-ghost" id="btn-edit-participant-cancel">Cancelar</button>
        <button class="btn btn-primary" id="btn-edit-participant-save">💾 Salvar</button>
      </div>
    </div>
  </div>
</div>

<!-- EDIT ACTION MODAL -->
<div class="modal-overlay hidden" id="modal-edit-action">
  <div class="modal" style="max-width:480px;width:calc(100vw - 32px)">
    <div class="modal-header">
      <div class="modal-title">✏️ Editar Encaminhamento</div>
      <button class="modal-close" id="btn-edit-action-close">×</button>
    </div>
    <div class="modal-body">
      <div>
        <label class="lbl">Encaminhamento *</label>
        <textarea class="inp" id="edit-action-text" style="min-height:80px" placeholder="Descreva o encaminhamento..."></textarea>
      </div>
      <div class="grid2">
        <div>
          <label class="lbl">Responsável</label>
          <input class="inp" id="edit-action-resp" placeholder="Nome do responsável"/>
        </div>
        <div>
          <label class="lbl">Prazo</label>
          <input class="inp" type="date" id="edit-action-deadline"/>
        </div>
      </div>
      <div style="display:flex;align-items:center;gap:10px">
        <input type="checkbox" id="edit-action-done" style="width:16px;height:16px;accent-color:#22C55E"/>
        <label for="edit-action-done" style="font-size:14px;color:var(--text2);cursor:pointer">Marcar como concluído</label>
      </div>
      <div class="modal-btns">
        <button class="btn btn-ghost" id="btn-edit-action-cancel">Cancelar</button>
        <button class="btn btn-primary" id="btn-edit-action-save">💾 Salvar</button>
      </div>
    </div>
  </div>
</div>

<!-- DELETE CONFIRM MODAL -->
<div class="modal-overlay hidden" id="modal-delete">
  <div class="modal">
    <div class="modal-header">
      <div class="modal-title">🗑️ Confirmar exclusão</div>
      <button class="modal-close" id="btn-delete-close">×</button>
    </div>
    <p class="modal-text" id="delete-msg"></p>
    <div class="modal-btns">
      <button class="btn btn-ghost" id="btn-delete-cancel">Cancelar</button>
      <button class="btn btn-danger" id="btn-delete-confirm">Excluir</button>
    </div>
  </div>
</div>

<!-- TOAST -->
<div id="toast"></div>

<input type="file" id="file-input" style="display:none"/>

<script>
// ===== STATE =====
let meetings = JSON.parse(localStorage.getItem('reunioes-data') || '[]');
let settings = JSON.parse(localStorage.getItem('reunioes-settings') || '{}');
let selectedId = null;
let currentView = 'empty';
let filterStatus = 'Todas';
let searchText = '';
let formData = {};
let formTab = 'geral';
let deleteTarget = null;

// ===== GOOGLE DRIVE — GOOGLE IDENTITY SERVICES + DRIVE API =====
// Requer hospedagem em https:// com Client ID OAuth de Aplicativo da Web.
// Os dados são salvos em Google Drive/GestaoReunioes/reunioes.json

const GD_FOLDER = 'GestaoReunioes';
const GD_FILENAME = 'reunioes.json';
const GD_SCOPES = 'https://www.googleapis.com/auth/drive.file https://www.googleapis.com/auth/userinfo.profile https://www.googleapis.com/auth/userinfo.email';
const DRIVE_API = 'https://www.googleapis.com/drive/v3';
const DRIVE_UPLOAD = 'https://www.googleapis.com/upload/drive/v3/files';

let odTokenData = null;   // mantive os nomes para minimizar mudanças no restante do app
let odUserInfo = null;
let odPollTimer = null;
let googleTokenClient = null;

function odSaveTokens(data) {
  odTokenData = data;
  localStorage.setItem('gd-tokens', JSON.stringify(data));
}
function odLoadTokens() {
  try { odTokenData = JSON.parse(localStorage.getItem('gd-tokens') || 'null'); } catch { odTokenData = null; }
}
function odClearTokens() {
  odTokenData = null;
  odUserInfo = null;
  localStorage.removeItem('gd-tokens');
  localStorage.removeItem('gd-userinfo');
  delete settings.gdFolderId;
  delete settings.gdFileId;
  saveSettings();
}

function hasValidGoogleToken() {
  return !!(odTokenData && odTokenData.access_token && odTokenData.expires_at && Date.now() < odTokenData.expires_at - 60000);
}

async function ensureGoogleAccess(interactive = false) {
  if (hasValidGoogleToken()) return odTokenData.access_token;
  const clientId = settings.odClientId || (document.getElementById('od-client-id-input')?.value || '').trim();
  if (!clientId) throw new Error('Informe o Client ID OAuth do Google.');
  if (!window.google?.accounts?.oauth2) throw new Error('Biblioteca do Google não carregou. Abra o sistema já hospedado em HTTPS.');
  settings.odClientId = clientId;
  saveSettings();
  if (!googleTokenClient) {
    googleTokenClient = google.accounts.oauth2.initTokenClient({
      client_id: clientId,
      scope: GD_SCOPES,
      callback: () => {}
    });
  }
  return await new Promise((resolve, reject) => {
    googleTokenClient.callback = async (resp) => {
      if (resp?.error) { reject(new Error(resp.error)); return; }
      if (!resp?.access_token) { reject(new Error('Google não retornou token de acesso.')); return; }
      const expiresIn = Number(resp.expires_in || 3600);
      odSaveTokens({ access_token: resp.access_token, expires_at: Date.now() + expiresIn * 1000 });
      try { await odFetchUser(); } catch {}
      updateOdUI();
      resolve(resp.access_token);
    };
    try {
      googleTokenClient.requestAccessToken({ prompt: interactive ? 'consent' : '' });
    } catch (e) { reject(e); }
  });
}

async function odAccessToken(interactive = false) {
  return await ensureGoogleAccess(interactive);
}

async function gfetch(url, opts = {}) {
  const token = await odAccessToken(false);
  const res = await fetch(url, {
    ...opts,
    headers: { Authorization: 'Bearer ' + token, ...(opts.headers || {}) }
  });
  if (res.status === 401 && !opts.__retried) {
    await ensureGoogleAccess(true);
    return gfetch(url, { ...opts, __retried: true });
  }
  return res;
}

async function gdFindFolder() {
  if (settings.gdFolderId) return settings.gdFolderId;
  const q = encodeURIComponent(`name='${GD_FOLDER}' and mimeType='application/vnd.google-apps.folder' and trashed=false`);
  const r = await gfetch(`${DRIVE_API}/files?q=${q}&fields=files(id,name)&pageSize=10`);
  if (!r.ok) throw new Error('Falha ao localizar pasta no Drive.');
  const data = await r.json();
  const id = data.files?.[0]?.id || null;
  if (id) { settings.gdFolderId = id; saveSettings(); }
  return id;
}

async function ensureFolder() {
  let folderId = await gdFindFolder();
  if (folderId) return folderId;
  const r = await gfetch(`${DRIVE_API}/files`, {
    method: 'POST',
    headers: { 'Content-Type': 'application/json' },
    body: JSON.stringify({ name: GD_FOLDER, mimeType: 'application/vnd.google-apps.folder' })
  });
  if (!r.ok) throw new Error('Não foi possível criar a pasta no Drive.');
  const data = await r.json();
  settings.gdFolderId = data.id;
  saveSettings();
  return data.id;
}

async function gdFindDataFile(folderId) {
  if (settings.gdFileId) return settings.gdFileId;
  const q = encodeURIComponent(`name='${GD_FILENAME}' and '${folderId}' in parents and trashed=false`);
  const r = await gfetch(`${DRIVE_API}/files?q=${q}&fields=files(id,name)&pageSize=10`);
  if (!r.ok) throw new Error('Falha ao localizar arquivo principal no Drive.');
  const data = await r.json();
  const id = data.files?.[0]?.id || null;
  if (id) { settings.gdFileId = id; saveSettings(); }
  return id;
}

async function uploadDriveJson(fileId, folderId, payloadObj) {
  const metadata = fileId
    ? { name: GD_FILENAME }
    : { name: GD_FILENAME, parents: [folderId] };

  const boundary = '-------314159265358979323846';
  const body = [
    `--${boundary}`,
    'Content-Type: application/json; charset=UTF-8',
    '',
    JSON.stringify(metadata),
    `--${boundary}`,
    'Content-Type: application/json; charset=UTF-8',
    '',
    JSON.stringify(payloadObj, null, 2),
    `--${boundary}--`
  ].join('\r\n');

  const endpoint = fileId
    ? `${DRIVE_UPLOAD}/${fileId}?uploadType=multipart&supportsAllDrives=false`
    : `${DRIVE_UPLOAD}?uploadType=multipart&supportsAllDrives=false`;

  const method = fileId ? 'PATCH' : 'POST';

  const r = await gfetch(endpoint, {
    method,
    headers: { 'Content-Type': `multipart/related; boundary=${boundary}` },
    body
  });

  if (!r.ok) {
    const text = await r.text().catch(() => '');
    throw new Error(`Falha ao salvar no Google Drive (${r.status}). ${text.slice(0,160)}`);
  }

  const data = await r.json();
  settings.gdFileId = data.id;
  saveSettings();
  return data.id;
}
 
async function odSaveIndex() {
  const folderId = await ensureFolder();
  const fileId = await gdFindDataFile(folderId);
  await uploadDriveJson(fileId, folderId, {
    version: 1,
    updatedAt: new Date().toISOString(),
    meetings
  });
}

async function odSaveMeeting(meeting) {
  if (!meeting) return;
  setOdStatus('syncing', 'Salvando…');
  try {
    const idx = meetings.findIndex(m => m.id === meeting.id);
    if (idx >= 0) meetings[idx] = meeting;
    await odSaveIndex();
    settings.odLastSync = new Date().toISOString();
    saveSettings();
    setOdStatus('on', 'Drive ✓');
    updateLastSync();
  } catch (e) {
    setOdStatus('err', 'Erro');
    showToast('Erro Google Drive: ' + e.message, 'info');
  }
}

async function odDeleteMeeting(id) {
  try {
    await odSaveIndex();
  } catch(e) {}
}

async function odSyncAll() {
  setOdStatus('syncing', 'Sincronizando…');
  try {
    await odSaveIndex();
    settings.odLastSync = new Date().toISOString();
    saveSettings();
    setOdStatus('on', 'Drive ✓');
    updateLastSync();
    showToast(`☁️ ${meetings.length} reuniões salvas no Google Drive!`);
  } catch (e) {
    setOdStatus('err', 'Erro');
    showToast('Erro: ' + e.message, 'info');
  }
}

async function odLoadAll() {
  setOdStatus('syncing', 'Baixando…');
  try {
    const folderId = await ensureFolder();
    const fileId = await gdFindDataFile(folderId);
    if (!fileId) {
      await odSyncAll();
      return;
    }
    const r = await gfetch(`${DRIVE_API}/files/${fileId}?alt=media`);
    if (!r.ok) throw new Error('Não foi possível baixar as reuniões do Drive.');
    const data = await r.json();
    meetings = Array.isArray(data) ? data : (data.meetings || []);
    localStorage.setItem('reunioes-data', JSON.stringify(meetings));
    renderSidebar();
    renderDashboard();
    settings.odLastSync = new Date().toISOString();
    saveSettings();
    setOdStatus('on', 'Drive ✓');
    updateLastSync();
    showToast(`☁️ ${meetings.length} reuniões carregadas do Google Drive!`);
  } catch (e) {
    setOdStatus('err', 'Erro ao baixar');
    showToast('Erro: ' + e.message, 'info');
  }
}

async function odFetchUser() {
  const token = await odAccessToken(false);
  const r = await fetch('https://www.googleapis.com/oauth2/v2/userinfo', {
    headers: { Authorization: 'Bearer ' + token }
  });
  if (r.ok) {
    const d = await r.json();
    odUserInfo = { name: d.name || 'Conta Google', email: d.email || '—' };
    localStorage.setItem('gd-userinfo', JSON.stringify(odUserInfo));
  }
}

async function odConnect() {
  const clientId = (document.getElementById('od-client-id-input')?.value || '').trim();
  if (!clientId) { showToast('Cole o Client ID OAuth do Google', 'info'); return; }
  if (location.protocol === 'file:' || location.protocol === 'content:') {
    showToast('Publique este HTML como site HTTPS antes de usar o login Google.', 'info');
    return;
  }
  settings.odClientId = clientId;
  saveSettings();
  const codeBox = document.getElementById('od-device-code-box');
  const setupArea = document.getElementById('od-disconnected');
  const statusEl = document.getElementById('od-code-status');
  const codeEl = document.getElementById('od-code-display');
  codeBox.style.display = 'block';
  setupArea.style.display = 'none';
  codeEl.textContent = 'GOOGLE';
  statusEl.textContent = 'Abrindo login do Google…';
  const link = document.getElementById('od-code-url');
  link.href = 'https://accounts.google.com/';
  link.textContent = 'accounts.google.com';
  try {
    await ensureGoogleAccess(true);
    codeBox.style.display = 'none';
    updateOdUI();
    document.getElementById('modal-settings').classList.add('hidden');
    showToast('✅ Google Drive conectado! Carregando reuniões…');
    await odLoadAll();
  } catch (e) {
    codeBox.style.display = 'none';
    setupArea.style.display = 'block';
    showToast('Erro: ' + e.message, 'info');
  }
}

function odDisconnect() {
  try {
    const token = odTokenData?.access_token;
    if (token && window.google?.accounts?.oauth2?.revoke) {
      google.accounts.oauth2.revoke(token, () => {});
    }
  } catch {}
  odClearTokens();
  updateOdUI();
  showToast('Google Drive desconectado.', 'info');
  document.getElementById('modal-settings').classList.add('hidden');
}

function setOdStatus(state, label) {
  const btn = document.getElementById('btn-onedrive');
  const ind = document.getElementById('od-indicator');
  const lbl = document.getElementById('od-btn-label');
  if (!btn) return;
  btn.className = 'od-btn' + (state==='on'?' connected': state==='syncing'?' syncing': state==='err'?' error':'');
  if (ind) ind.className = 'od-indicator' + (state==='on'?' on': state==='syncing'?' spin': state==='err'?' err':' off');
  if (lbl) lbl.textContent = label || 'Drive';
}

function updateLastSync() {
  const el = document.getElementById('od-last-sync-display');
  if (el && settings.odLastSync) el.textContent = 'Último sync: ' + fmtDateTime(settings.odLastSync);
}

function updateOdUI() {
  const connected = hasValidGoogleToken();
  document.getElementById('od-connected').style.display = connected ? 'block' : 'none';
  document.getElementById('od-disconnected').style.display = connected ? 'none' : 'block';
  document.getElementById('od-device-code-box').style.display = 'none';
  if (connected) {
    if (!odUserInfo) { try { odUserInfo = JSON.parse(localStorage.getItem('gd-userinfo')); } catch {} }
    const ne = document.getElementById('od-user-name-el');
    const ee = document.getElementById('od-user-email-el');
    if (ne) ne.textContent = odUserInfo?.name || 'Conta Google';
    if (ee) ee.textContent = odUserInfo?.email || '—';
    updateLastSync();
    setOdStatus('on', 'Drive ✓');
  } else {
    setOdStatus('off', 'Drive');
    const inp = document.getElementById('od-client-id-input');
    if (inp && settings.odClientId) inp.value = settings.odClientId;
  }
}

// ── Override save ──
function save() { localStorage.setItem('reunioes-data', JSON.stringify(meetings)); }
function saveSettings() { localStorage.setItem('reunioes-settings', JSON.stringify(settings)); }

// ===== TEMA (claro / escuro / sistema) =====
function applyTheme(theme) {
  const prefersDark = window.matchMedia('(prefers-color-scheme: dark)').matches;
  const isDark = theme === 'dark' || (theme === 'auto' && prefersDark);
  document.body.classList.toggle('dark', isDark);
  document.querySelectorAll('.theme-btn').forEach(btn => {
    const active = btn.dataset.theme === theme;
    btn.style.borderColor = active ? 'var(--accent)' : 'var(--bg3)';
    btn.style.background   = active ? 'var(--accent)18' : 'var(--bg2)';
  });
}
function setTheme(theme) {
  settings.theme = theme;
  saveSettings();
  applyTheme(theme);
}
window.matchMedia('(prefers-color-scheme: dark)').addEventListener('change', () => {
  if (settings.theme === 'auto') applyTheme('auto');
});

// ===== AUTO-SYNC CONFIGURÁVEL =====
let autoSyncTimer = null;
function startAutoSync() {
  if (autoSyncTimer) clearInterval(autoSyncTimer);
  if (!settings.autoSync) return;
  const mins = parseInt(settings.autoSyncInterval || 30);
  autoSyncTimer = setInterval(async () => {
    if (hasValidGoogleToken() || settings.odClientId) {
      try { await odLoadAll(); } catch(e) {}
    }
  }, mins * 60 * 1000);
}
function initAutoSyncUI() {
  const toggle = document.getElementById('toggle-autosync');
  const slider = document.getElementById('autosync-slider');
  const knob   = document.getElementById('autosync-knob');
  const row    = document.getElementById('autosync-interval-row');
  const sel    = document.getElementById('autosync-interval');
  if (!toggle) return;

  function updateSliderUI(on) {
    slider.style.background = on ? '#F59E0B' : '#CBD5E1';
    knob.style.left = on ? '23px' : '3px';
    row.style.opacity = on ? '1' : '0.4';
    row.style.pointerEvents = on ? 'auto' : 'none';
  }

  toggle.checked = !!settings.autoSync;
  sel.value = String(settings.autoSyncInterval || 30);
  updateSliderUI(!!settings.autoSync);

  toggle.onchange = () => {
    settings.autoSync = toggle.checked;
    saveSettings();
    updateSliderUI(toggle.checked);
    startAutoSync();
  };
  sel.onchange = () => {
    settings.autoSyncInterval = parseInt(sel.value);
    saveSettings();
    startAutoSync();
  };
}

// ── Auto-sync inicial (usa configuração salva, padrão: ligado, 30 min) ──
if (settings.autoSync === undefined) { settings.autoSync = true; settings.autoSyncInterval = 30; saveSettings(); }

// ── Restore session on page load ──
async function restoreOdSession() {
  odLoadTokens();
  // Carrega userinfo salvo para exibir nome/email mesmo antes de validar token
  try { if (!odUserInfo) odUserInfo = JSON.parse(localStorage.getItem('gd-userinfo')); } catch {}
  updateOdUI();

  const hasToken = !!odTokenData;
  const hasClientId = !!settings.odClientId;

  if (hasToken || hasClientId) {
    // Tenta carregar do Drive (renovação silenciosa automática se token expirou)
    try {
      await odLoadAll();
    } catch(e) {
      // Falhou — tenta renovação silenciosa forçada
      try {
        await ensureGoogleAccess(false);
        await odLoadAll();
      } catch(e2) {
        // Renovação silenciosa falhou — usuário precisa reconectar manualmente
        setOdStatus('off', 'Reconectar');
        updateOdUI();
      }
    }
  }
}

function genId() { return Date.now().toString(36) + Math.random().toString(36).slice(2); }

function fmtDate(iso) {
  if (!iso) return '—';
  // Datas no formato YYYY-MM-DD são interpretadas como UTC meia-noite,
  // o que no fuso de Brasília (UTC-3) vira o dia anterior. Parseamos manualmente.
  if (/^\d{4}-\d{2}-\d{2}$/.test(iso)) {
    const [y, m, d] = iso.split('-').map(Number);
    return new Date(y, m - 1, d).toLocaleDateString('pt-BR', { day:'2-digit', month:'short', year:'numeric' });
  }
  return new Date(iso).toLocaleDateString('pt-BR', { day:'2-digit', month:'short', year:'numeric' });
}
function fmtDateTime(iso) {
  if (!iso) return '—';
  const d = new Date(iso);
  return d.toLocaleString('pt-BR', { day:'2-digit', month:'short', year:'numeric', hour:'2-digit', minute:'2-digit' });
}

function docIcon(name='') {
  const ext = (name.split('.').pop()||'').toLowerCase();
  const icons = {pdf:'📄',doc:'📝',docx:'📝',xls:'📊',xlsx:'📊',ppt:'📑',pptx:'📑',jpg:'🖼️',jpeg:'🖼️',png:'🖼️',zip:'🗜️',mp4:'🎥'};
  return icons[ext] || '📎';
}

function showToast(msg, type='success') {
  const t = document.getElementById('toast');
  t.textContent = msg;
  t.className = type;
  t.style.display = 'block';
  setTimeout(() => { t.style.display = 'none'; }, 3000);
}

function badge(status) {
  return `<span class="badge badge-${status||'Agendada'}"><span class="badge-dot"></span>${status||'Agendada'}</span>`;
}

// ===== RENDER SIDEBAR =====
function renderSidebar() {
  document.getElementById('meeting-count').textContent = meetings.length + ' REGISTROS';
  const filtered = meetings.filter(m => {
    const s = !searchText || (m.title||'').toLowerCase().includes(searchText.toLowerCase()) ||
      (m.participants||[]).some(p => (p.name||'').toLowerCase().includes(searchText.toLowerCase()));
    const f = filterStatus === 'Todas' || m.status === filterStatus;
    return s && f;
  });
  const list = document.getElementById('sidebar-list');
  if (filtered.length === 0) {
    list.innerHTML = '<div style="text-align:center;color:var(--text3);padding:40px 20px;font-size:14px"><div style="font-size:32px;margin-bottom:8px">📭</div>Nenhuma reunião encontrada</div>';
    return;
  }
  list.innerHTML = filtered.map(m => `
    <div class="meeting-card${selectedId===m.id?' active':''}" data-id="${m.id}">
      <div class="card-top">
        <div class="card-title">${escHtml(m.title||'Sem título')}</div>
        ${badge(m.status)}
      </div>
      <div class="card-date">${fmtDate(m.date)}</div>
      ${m.participants&&m.participants.length>0?`<div class="card-participants">👥 ${m.participants.length} participante${m.participants.length>1?'s':''}</div>`:''}
    </div>
  `).join('');
  list.querySelectorAll('.meeting-card').forEach(el => {
    el.addEventListener('click', () => selectMeeting(el.dataset.id));
  });
}

function escHtml(s) {
  return String(s||'').replace(/&/g,'&amp;').replace(/</g,'&lt;').replace(/>/g,'&gt;').replace(/"/g,'&quot;');
}

function selectMeeting(id) {
  selectedId = id;
  const m = meetings.find(m=>m.id===id);
  if (m) renderDetail(m);
  renderSidebar();
}

// ===== DETAIL =====
function renderDetail(m) {
  showView('detail');
  const refs = meetings.filter(r => (m.references||[]).includes(r.id));
  const actions = m.actions || [];
  const participants = m.participants || [];
  const docs = m.documents || [];

  document.getElementById('detail-view').innerHTML = `
    <div class="print-header">
      <div class="print-logo">
        <div class="print-logo-icon">📋</div>
        <div><div style="font-weight:700;color:#1E293B;font-size:14px">Gestão de Reuniões</div><div style="font-size:11px;color:#94A3B8">Documento gerado em ${new Date().toLocaleDateString('pt-BR',{day:'2-digit',month:'long',year:'numeric'})}</div></div>
      </div>
      <div style="text-align:right;font-size:12px;color:#94A3B8">
        ${fmtDate(m.date)} ${m.date?new Date(m.date+'T'+(m.time||'00:00')).toLocaleTimeString('pt-BR',{hour:'2-digit',minute:'2-digit'}):''}
      </div>
    </div>
    <div class="detail-header">
      <div>
        <button class="btn btn-ghost btn-sm" id="detail-back" style="margin-bottom:12px;gap:6px;font-size:12px;color:var(--text3)">← Painel</button>
        <div style="display:flex;gap:10px;align-items:center;margin-bottom:8px">
          ${badge(m.status)}
          <span style="font-size:12px;font-family:var(--font-mono);color:var(--text3)">${fmtDateTime(m.date)}</span>
        </div>
        <h1 class="detail-title">${escHtml(m.title||'Sem título')}</h1>
        ${m.location?`<div class="detail-location">📍 ${escHtml(m.location)}</div>`:''}
      </div>
      <div class="detail-actions">
        <button class="btn btn-ghost btn-sm" id="detail-export-csv" title="Exportar contatos em CSV">📊 Contatos</button>
        <button class="btn btn-ghost btn-sm" id="detail-export-pdf" title="Exportar reunião em PDF">📄 PDF</button>
        <button class="btn btn-ghost" id="detail-edit">✏️ Editar</button>
        <button class="btn btn-ghost" id="detail-delete" style="border-color:#7F1D1D;color:#FCA5A5">🗑️</button>
      </div>
    </div>

    <div class="grid2" style="margin-bottom:20px">
      <div class="section-card" style="margin-bottom:0">
        <div class="section-head">📋 Pauta / Objetivos</div>
        <div class="section-body">${m.agenda?`<div style="font-size:15px;line-height:1.8;color:#475569;white-space:pre-wrap">${escHtml(m.agenda)}</div>`:'<div class="section-empty">Nenhuma pauta registrada</div>'}</div>
      </div>
      <div class="section-card" style="margin-bottom:0">
        <div class="section-head">📝 Anotações e Discussões</div>
        <div class="section-body">${m.notes?`<div style="font-size:15px;line-height:1.8;color:#475569;white-space:pre-wrap">${escHtml(m.notes)}</div>`:'<div class="section-empty">Nenhuma anotação</div>'}</div>
      </div>
    </div>

    <div class="section-card">
      <div class="section-head" style="display:flex;justify-content:space-between;align-items:center">
        <span>✅ Encaminhamentos</span>
        ${actions.length>0?`<span style="font-size:11px;font-weight:400;color:var(--text3);font-family:var(--font-mono)">${actions.filter(a=>a.done).length}/${actions.length} concluídos</span>`:''}
      </div>
      <div class="section-body">
        ${actions.length===0?'<div class="section-empty">Nenhum encaminhamento registrado</div>':
          actions.map((a,i)=>`
            <div class="item-card" style="align-items:center">
              <button class="action-toggle-btn" data-action-idx="${i}" title="${a.done?'Marcar como pendente':'Marcar como concluído'}"
                style="width:28px;height:28px;border-radius:50%;border:2px solid ${a.done?'#22C55E':'#475569'};background:${a.done?'#14532D':'transparent'};
                display:flex;align-items:center;justify-content:center;cursor:pointer;flex-shrink:0;transition:all .2s;font-size:13px;color:${a.done?'#4ADE80':'#64748B'}">
                ${a.done?'✓':'○'}
              </button>
              <div class="item-body" style="${a.done?'opacity:.65':''}">
                <div class="item-title" style="${a.done?'text-decoration:line-through;color:var(--text3)':''}">${escHtml(a.text)}</div>
                <div class="item-meta">
                  ${a.responsible?`<span>👤 ${escHtml(a.responsible)}</span>`:''}
                  ${(() => {
                    const hoje = new Date(); hoje.setHours(0,0,0,0);
                    const vencido = a.deadline && new Date(a.deadline+'T00:00:00') < hoje && !a.done;
                    return a.deadline
                      ? `<span style="color:${vencido?'#EF4444':'#F59E0B'}">📅 ${vencido?'Vencido: ':'Prazo: '}${fmtDate(a.deadline)}</span>`
                      : `<span style="color:var(--text3)">📅 Sem prazo</span>`;
                  })()}
                  <span class="${a.done?'item-status-done':'item-status-pending'}">${a.done?'Concluído':'Pendente'}</span>
                </div>
              </div>
              <button class="btn btn-ghost btn-sm action-edit-btn" data-action-idx="${i}" style="flex-shrink:0;font-size:13px" title="Editar encaminhamento">✏️</button>
            </div>`).join('')}
      </div>
    </div>

    <div class="section-card">
      <div class="section-head">👥 Participantes</div>
      <div class="section-body">
        ${participants.length===0?'<div class="section-empty">Nenhum participante registrado</div>':
          `<div class="grid2auto">${participants.map((p,i)=>`
            <div class="participant-card" style="position:relative">
              <button class="participant-edit-btn btn btn-ghost btn-sm" data-p-idx="${i}"
                style="position:absolute;top:8px;right:8px;padding:3px 7px;font-size:12px" title="Editar participante">✏️</button>
              <div class="participant-name">${escHtml(p.name)}</div>
              ${p.org?`<div class="participant-org">${escHtml(p.org)}</div>`:''}
              <div class="participant-contact">
                ${p.email?`<div>✉️ ${escHtml(p.email)}</div>`:''}
                ${p.phone?`<div>📱 ${escHtml(p.phone)}</div>`:''}
              </div>
            </div>`).join('')}</div>`}
      </div>
    </div>

    <div class="grid2">
      <div class="section-card" style="margin-bottom:0">
        <div class="section-head">📎 Documentos Anexados</div>
        <div class="section-body">
          ${docs.length===0?'<div class="section-empty">Nenhum documento</div>':
            docs.map(d=>{
              const hasFile = !!d.data;
              const hasUrl  = !!d.url;
              const actionBtn = hasFile
                ? `<a href="${d.data}" download="${escHtml(d.name)}" class="btn btn-ghost btn-sm" style="flex-shrink:0;text-decoration:none">⬇️ Baixar</a>`
                : hasUrl
                  ? `<a href="${escHtml(d.url)}" target="_blank" rel="noopener" class="btn btn-ghost btn-sm" style="flex-shrink:0;text-decoration:none">🔗 Abrir</a>`
                  : `<span style="font-size:11px;color:var(--text3);padding:4px 8px">sem arquivo</span>`;
              return `<div class="doc-item">
                <span class="doc-icon">${docIcon(d.name)}</span>
                <div style="flex:1;min-width:0">
                  <div class="doc-name">${escHtml(d.name)}</div>
                  ${d.description?`<div class="doc-desc">${escHtml(d.description)}</div>`:''}
                </div>
                ${actionBtn}
              </div>`;
            }).join('')}
        </div>
      </div>
      <div class="section-card" style="margin-bottom:0">
        <div class="section-head">🔗 Reuniões Relacionadas</div>
        <div class="section-body">
          ${refs.length===0?'<div class="section-empty">Nenhuma referência</div>':
            refs.map(r=>`<div class="item-card item-card-ref" data-ref-id="${r.id}" style="cursor:pointer"><div style="flex:1"><div style="font-size:13px;font-weight:600;color:#93C5FD">${escHtml(r.title)}</div><div style="font-size:11px;color:var(--text3);font-family:var(--font-mono);margin-top:2px">${fmtDate(r.date)}</div></div>${badge(r.status)}</div>`).join('')}
        </div>
      </div>
    </div>
    <div class="print-footer">
      Gestão de Reuniões · Documento gerado em ${new Date().toLocaleString('pt-BR')} · Confidencial
    </div>
  `;

  document.getElementById('detail-back').onclick = () => {
    selectedId = null;
    renderSidebar();
    showView('empty');
  };
  document.getElementById('detail-edit').onclick   = () => openForm(m);
  document.getElementById('detail-delete').onclick = () => confirmDelete(m);

  document.getElementById('detail-export-pdf').onclick = () => exportMeetingPDF(m);
  document.getElementById('detail-export-csv').onclick = () => exportContactsCSV(m);
  document.querySelectorAll('[data-ref-id]').forEach(el => {
    el.addEventListener('click', () => selectMeeting(el.dataset.refId));
  });

  // Toggle encaminhamento done/pending directly from detail view
  document.querySelectorAll('.action-toggle-btn').forEach(btn => {
    btn.addEventListener('click', () => {
      const idx = parseInt(btn.dataset.actionIdx);
      const meeting = meetings.find(x => x.id === m.id);
      if (!meeting || !meeting.actions[idx]) return;
      meeting.actions[idx].done = !meeting.actions[idx].done;
      localStorage.setItem('reunioes-data', JSON.stringify(meetings));
      if (odTokenData) odSaveMeeting(meeting);
      renderSidebar();
      renderDetail(meeting);
    });
  });

  // Editar participante
  document.querySelectorAll('.participant-edit-btn').forEach(btn => {
    btn.addEventListener('click', () => {
      const idx = parseInt(btn.dataset.pIdx);
      const meeting = meetings.find(x => x.id === m.id);
      if (!meeting) return;
      const p = meeting.participants[idx];
      document.getElementById('edit-p-name').value  = p.name  || '';
      document.getElementById('edit-p-org').value   = p.org   || '';
      document.getElementById('edit-p-email').value = p.email || '';
      document.getElementById('edit-p-phone').value = p.phone || '';
      document.getElementById('modal-edit-participant').classList.remove('hidden');

      document.getElementById('btn-edit-participant-save').onclick = () => {
        const name = document.getElementById('edit-p-name').value.trim();
        if (!name) { showToast('Preencha o nome do participante.', 'info'); return; }
        meeting.participants[idx] = {
          ...meeting.participants[idx],
          name,
          org:   document.getElementById('edit-p-org').value.trim(),
          email: document.getElementById('edit-p-email').value.trim(),
          phone: document.getElementById('edit-p-phone').value.trim()
        };
        localStorage.setItem('reunioes-data', JSON.stringify(meetings));
        if (odTokenData) odSaveMeeting(meeting);
        document.getElementById('modal-edit-participant').classList.add('hidden');
        renderSidebar();
        renderDetail(meeting);
        showToast('✅ Participante atualizado!');
      };

      document.getElementById('btn-edit-participant-delete').onclick = () => {
        if (!confirm(`Remover "${p.name}" da reunião?`)) return;
        meeting.participants.splice(idx, 1);
        localStorage.setItem('reunioes-data', JSON.stringify(meetings));
        if (odTokenData) odSaveMeeting(meeting);
        document.getElementById('modal-edit-participant').classList.add('hidden');
        renderSidebar();
        renderDetail(meeting);
        showToast('Participante removido.', 'info');
      };
    });
  });
  document.querySelectorAll('.action-edit-btn').forEach(btn => {
    btn.addEventListener('click', () => {
      const idx = parseInt(btn.dataset.actionIdx);
      const meeting = meetings.find(x => x.id === m.id);
      if (!meeting) return;
      const a = meeting.actions[idx];
      document.getElementById('edit-action-text').value     = a.text || '';
      document.getElementById('edit-action-resp').value     = a.responsible || '';
      document.getElementById('edit-action-deadline').value = a.deadline || '';
      document.getElementById('edit-action-done').checked   = !!a.done;
      document.getElementById('modal-edit-action').classList.remove('hidden');

      document.getElementById('btn-edit-action-save').onclick = () => {
        const text = document.getElementById('edit-action-text').value.trim();
        if (!text) { showToast('Preencha o encaminhamento.', 'info'); return; }
        meeting.actions[idx] = {
          ...meeting.actions[idx],
          text,
          responsible: document.getElementById('edit-action-resp').value.trim(),
          deadline:    document.getElementById('edit-action-deadline').value,
          done:        document.getElementById('edit-action-done').checked
        };
        localStorage.setItem('reunioes-data', JSON.stringify(meetings));
        if (odTokenData) odSaveMeeting(meeting);
        document.getElementById('modal-edit-action').classList.add('hidden');
        renderSidebar();
        renderDetail(meeting);
        showToast('✅ Encaminhamento atualizado!');
      };
    });
  });
}

// Fechar modal de edição de encaminhamento
document.getElementById('btn-edit-action-close').onclick  = () => document.getElementById('modal-edit-action').classList.add('hidden');
document.getElementById('btn-edit-action-cancel').onclick = () => document.getElementById('modal-edit-action').classList.add('hidden');

// Fechar modal de edição de participante
document.getElementById('btn-edit-participant-close').onclick  = () => document.getElementById('modal-edit-participant').classList.add('hidden');
document.getElementById('btn-edit-participant-cancel').onclick = () => document.getElementById('modal-edit-participant').classList.add('hidden');

function confirmDelete(m) {
  deleteTarget = m.id;
  document.getElementById('delete-msg').innerHTML = `Tem certeza que deseja excluir a reunião <strong>"${escHtml(m.title)}"</strong>? Esta ação não pode ser desfeita.`;
  document.getElementById('modal-delete').classList.remove('hidden');
}

// ===== FORM =====
function openForm(meeting) {
  formData = meeting ? JSON.parse(JSON.stringify(meeting)) : {
    title:'', date:'', location:'', status:'Agendada',
    agenda:'', notes:'', participants:[], actions:[], documents:[], references:[]
  };
  formTab = 'geral';
  renderForm();
  showView('form');
}

function renderForm() {
  const isEdit = !!formData.id;
  const el = document.getElementById('form-view');
  el.innerHTML = `
    <div class="form-header">
      <h2 class="form-title">${isEdit?'Editar Reunião':'Nova Reunião'}</h2>
      <div class="form-header-btns">
        <button class="btn btn-ghost" id="form-cancel">Cancelar</button>
        <button class="btn btn-primary" id="form-save">💾 Salvar</button>
      </div>
    </div>
    <div class="tabs">
      ${[['geral','📋 Geral'],['pauta','📝 Pauta'],['participantes','👥 Participantes'],['encaminhamentos','✅ Encaminhamentos'],['documentos','📎 Documentos'],['referencias','🔗 Referências']].map(([k,l])=>`<button class="tab${formTab===k?' active':''}" data-tab="${k}">${l}</button>`).join('')}
    </div>
    <div id="tab-content"></div>
  `;

  el.querySelectorAll('.tab').forEach(t => {
    t.addEventListener('click', () => { formTab = t.dataset.tab; renderTabContent(); updateTabBar(); });
  });
  document.getElementById('form-cancel').onclick = () => {
    if (selectedId) { const m = meetings.find(m=>m.id===selectedId); if(m) renderDetail(m); showView('detail'); }
    else showView('empty');
  };
  document.getElementById('form-save').onclick = saveForm;
  renderTabContent();
}

function updateTabBar() {
  document.querySelectorAll('.tab').forEach(t => t.classList.toggle('active', t.dataset.tab===formTab));
}

function renderTabContent() {
  const c = document.getElementById('tab-content');
  if (!c) return;

  if (formTab === 'geral') {
    c.innerHTML = `
      <div class="grid2" style="margin-bottom:14px">
        <div>
          <label class="lbl">Título da Reunião *</label>
          <input class="inp" id="f-title" value="${escHtml(formData.title||'')}" placeholder="Ex: Reunião de Planejamento Anual"/>
        </div>
        <div>
          <label class="lbl">Status</label>
          <select class="inp" id="f-status">
            ${['Agendada','Realizada','Cancelada','Adiada'].map(s=>`<option value="${s}"${formData.status===s?' selected':''}>${s}</option>`).join('')}
          </select>
        </div>
      </div>
      <div class="grid2">
        <div>
          <label class="lbl">Data e Hora</label>
          <input type="datetime-local" class="inp" id="f-date" value="${formData.date||''}"/>
        </div>
        <div>
          <label class="lbl">Local / Link</label>
          <input class="inp" id="f-location" value="${escHtml(formData.location||'')}" placeholder="Ex: Sala de reuniões A / Meet"/>
        </div>
      </div>
    `;
    c.querySelector('#f-title').oninput = e => { formData.title = e.target.value; };
    c.querySelector('#f-status').onchange = e => { formData.status = e.target.value; };
    c.querySelector('#f-date').onchange = e => { formData.date = e.target.value; };
    c.querySelector('#f-location').oninput = e => { formData.location = e.target.value; };
  }

  else if (formTab === 'pauta') {
    c.innerHTML = `
      <div style="margin-bottom:16px">
        <label class="lbl">Pauta / Objetivos</label>
        <textarea class="inp" id="f-agenda" rows="6" placeholder="Descreva os tópicos da pauta, objetivos e ordem do dia...">${escHtml(formData.agenda||'')}</textarea>
      </div>
      <div>
        <label class="lbl">Anotações e Discussões</label>
        <textarea class="inp" id="f-notes" rows="8" placeholder="Registre as discussões, decisões tomadas e observações...">${escHtml(formData.notes||'')}</textarea>
      </div>
    `;
    c.querySelector('#f-agenda').oninput = e => { formData.agenda = e.target.value; };
    c.querySelector('#f-notes').oninput = e => { formData.notes = e.target.value; };
  }

  else if (formTab === 'participantes') {
    renderParticipantTab(c);
  }

  else if (formTab === 'encaminhamentos') {
    renderActionsTab(c);
  }

  else if (formTab === 'documentos') {
    renderDocsTab(c);
  }

  else if (formTab === 'referencias') {
    renderRefsTab(c);
  }
}

function renderParticipantTab(c) {
  c.innerHTML = `
    <div class="add-form">
      <div class="grid2">
        <div><label class="lbl">Nome *</label><input class="inp" id="p-name" placeholder="Nome completo"/></div>
        <div><label class="lbl">Órgão / Empresa</label><input class="inp" id="p-org" placeholder="Ex: Secretaria de Saúde"/></div>
        <div><label class="lbl">E-mail</label><input type="email" class="inp" id="p-email" placeholder="email@exemplo.com"/></div>
        <div><label class="lbl">Celular</label><input class="inp" id="p-phone" placeholder="(61) 9 0000-0000"/></div>
        <div class="add-form-full"><button class="btn btn-blue" id="p-add" style="width:100%;justify-content:center">+ Adicionar Participante</button></div>
      </div>
    </div>
    <div id="p-list"></div>
  `;
  renderPList();
  c.querySelector('#p-add').onclick = () => {
    const name = c.querySelector('#p-name').value.trim();
    if (!name) return;
    formData.participants = formData.participants || [];
    formData.participants.push({ name, org: c.querySelector('#p-org').value, email: c.querySelector('#p-email').value, phone: c.querySelector('#p-phone').value });
    c.querySelector('#p-name').value=''; c.querySelector('#p-org').value=''; c.querySelector('#p-email').value=''; c.querySelector('#p-phone').value='';
    renderPList();
  };
  function renderPList() {
    const pl = c.querySelector('#p-list');
    const ps = formData.participants || [];
    if (ps.length===0) { pl.innerHTML='<div style="text-align:center;color:var(--text3);padding:20px">Nenhum participante adicionado</div>'; return; }
    pl.innerHTML = ps.map((p,i)=>`
      <div class="item-card" style="justify-content:space-between">
        <div>
          <div style="font-weight:600;color:#1E293B;font-size:14px">${escHtml(p.name)}</div>
          ${p.org?`<div style="font-size:12px;color:var(--accent);font-family:var(--font-mono)">${escHtml(p.org)}</div>`:''}
          <div style="font-size:12px;color:var(--text2)">${p.email||''}${p.phone?` · ${p.phone}`:''}</div>
        </div>
        <button class="btn-icon" data-pi="${i}">×</button>
      </div>`).join('');
    pl.querySelectorAll('[data-pi]').forEach(b => b.onclick = () => { formData.participants.splice(+b.dataset.pi,1); renderPList(); });
  }
}

function renderActionsTab(c) {
  c.innerHTML = `
    <div class="add-form">
      <div><label class="lbl">Encaminhamento *</label><input class="inp" id="a-text" placeholder="Descreva o encaminhamento ou ação a ser tomada"/></div>
      <div class="add-form-row">
        <div><label class="lbl">Responsável</label><input class="inp" id="a-resp" placeholder="Nome do responsável"/></div>
        <div><label class="lbl">Prazo</label><input type="date" class="inp" id="a-deadline"/></div>
      </div>
      <button class="btn btn-green" id="a-add" style="width:100%;justify-content:center;margin-top:10px">+ Adicionar Encaminhamento</button>
    </div>
    <div id="a-list"></div>
  `;
  renderAList();
  c.querySelector('#a-add').onclick = () => {
    const text = c.querySelector('#a-text').value.trim();
    if (!text) return;
    formData.actions = formData.actions || [];
    formData.actions.push({ text, responsible: c.querySelector('#a-resp').value, deadline: c.querySelector('#a-deadline').value, done: false });
    c.querySelector('#a-text').value=''; c.querySelector('#a-resp').value=''; c.querySelector('#a-deadline').value='';
    renderAList();
  };
  function renderAList() {
    const al = c.querySelector('#a-list');
    const acts = formData.actions || [];
    if (acts.length===0) { al.innerHTML='<div style="text-align:center;color:var(--text3);padding:20px">Nenhum encaminhamento adicionado</div>'; return; }
    al.innerHTML = acts.map((a,i)=>{
      const hoje = new Date(); hoje.setHours(0,0,0,0);
      const vencido = a.deadline && new Date(a.deadline + 'T00:00:00') < hoje && !a.done;
      const deadlineLabel = a.deadline
        ? `<span style="color:${vencido?'#EF4444':'#F59E0B'}">📅 ${vencido?'Vencido: ':'Prazo: '}${fmtDate(a.deadline)}</span>`
        : `<span style="color:var(--text3)">📅 Sem prazo definido</span>`;
      return `
      <div class="item-card">
        <input type="checkbox" ${a.done?'checked':''} data-ai="${i}" style="accent-color:#22C55E;width:16px;height:16px;margin-top:3px;flex-shrink:0"/>
        <div class="item-body">
          <div class="item-title">${escHtml(a.text)}</div>
          <div class="item-meta">
            ${a.responsible?`<span>👤 ${escHtml(a.responsible)}</span>`:''}
            ${deadlineLabel}
          </div>
        </div>
        <button class="btn-icon" data-adel="${i}">×</button>
      </div>`;
    }).join('');
    al.querySelectorAll('[data-ai]').forEach(cb => cb.onchange = () => { formData.actions[+cb.dataset.ai].done = cb.checked; });
    al.querySelectorAll('[data-adel]').forEach(b => b.onclick = () => { formData.actions.splice(+b.dataset.adel,1); renderAList(); });
  }
}

function renderDocsTab(c) {
  c.innerHTML = `
    <div class="add-form">
      <label class="lbl">Descrição</label>
      <input class="inp" id="d-desc" placeholder="Ex: Apresentação de slides, relatório..." style="margin-bottom:10px"/>
      <div class="grid2" style="margin-bottom:8px">
        <button class="btn btn-blue" id="d-file" style="justify-content:center">📁 Selecionar Arquivo</button>
        <button class="btn btn-ghost" id="d-name-add" style="justify-content:center">+ Adicionar por Nome</button>
      </div>
      <input class="inp" id="d-name" placeholder="Ou digite o nome/link do documento"/>
    </div>
    <div id="d-list"></div>
  `;
  renderDList();
  c.querySelector('#d-file').onclick = () => {
    const fi = document.getElementById('file-input');
    fi.onchange = e => {
      const file = e.target.files[0];
      if (!file) return;
      const reader = new FileReader();
      reader.onload = ev => {
        formData.documents = formData.documents || [];
        formData.documents.push({
          name: file.name,
          description: c.querySelector('#d-desc').value,
          size: file.size,
          type: file.type,
          data: ev.target.result  // base64 dataURL
        });
        c.querySelector('#d-desc').value = '';
        renderDList();
        fi.value = '';
      };
      reader.readAsDataURL(file);
    };
    fi.click();
  };
  c.querySelector('#d-name-add').onclick = () => {
    const name = c.querySelector('#d-name').value.trim();
    if (!name) return;
    formData.documents = formData.documents || [];
    // Se for URL, salva como link
    const isUrl = /^https?:\/\//i.test(name);
    formData.documents.push({ name: isUrl ? name : name, description: c.querySelector('#d-desc').value, url: isUrl ? name : null });
    c.querySelector('#d-name').value=''; c.querySelector('#d-desc').value='';
    renderDList();
  };
  function renderDList() {
    const dl = c.querySelector('#d-list');
    const docs = formData.documents || [];
    if (docs.length===0) { dl.innerHTML='<div style="text-align:center;color:var(--text3);padding:20px">Nenhum documento anexado</div>'; return; }
    dl.innerHTML = docs.map((d,i)=>`
      <div class="doc-item">
        <span class="doc-icon">${docIcon(d.name)}</span>
        <div style="flex:1;min-width:0">
          <div class="doc-name">${escHtml(d.url || d.name)}</div>
          ${d.description?`<div class="doc-desc">${escHtml(d.description)}</div>`:''}
          <div class="doc-desc">${d.data ? '✅ Arquivo carregado' : d.url ? '🔗 Link externo' : '📎 Referência por nome'}</div>
        </div>
        <button class="btn-icon" data-di="${i}">×</button>
      </div>`).join('');
    dl.querySelectorAll('[data-di]').forEach(b => b.onclick = () => { formData.documents.splice(+b.dataset.di,1); renderDList(); });
  }
}

function renderRefsTab(c) {
  const others = meetings.filter(r => r.id !== formData.id);
  c.innerHTML = `
    <div style="margin-bottom:12px;font-size:13px;color:var(--text3)">Selecione reuniões relacionadas a esta:</div>
    <div id="r-list"></div>
  `;
  if (others.length===0) {
    c.querySelector('#r-list').innerHTML='<div style="text-align:center;color:var(--text3);padding:20px">Nenhuma outra reunião disponível</div>';
    return;
  }
  const rl = c.querySelector('#r-list');
  rl.innerHTML = others.map(r => {
    const checked = (formData.references||[]).includes(r.id);
    return `<div class="ref-item${checked?' checked':''}" data-rid="${r.id}">
      <div class="ref-checkbox${checked?' checked':''}">${checked?'✓':''}</div>
      <div style="flex:1">
        <div class="ref-title">${escHtml(r.title)}</div>
        <div class="ref-date">${fmtDate(r.date)}</div>
      </div>
      ${badge(r.status)}
    </div>`;
  }).join('');
  rl.querySelectorAll('[data-rid]').forEach(el => {
    el.addEventListener('click', () => {
      const id = el.dataset.rid;
      formData.references = formData.references || [];
      if (formData.references.includes(id)) formData.references = formData.references.filter(x=>x!==id);
      else formData.references.push(id);
      renderRefsTab(c);
    });
  });
}

function saveForm() {
  if (!formData.title || !formData.title.trim()) {
    showToast('Informe o título da reunião', 'info'); return;
  }
  if (formData.id) {
    meetings = meetings.map(m => m.id===formData.id ? formData : m);
    selectedId = formData.id;
  } else {
    formData.id = genId();
    formData.createdAt = new Date().toISOString();
    meetings.unshift(formData);
    selectedId = formData.id;
  }
  save();
  if (odTokenData) odSaveMeeting(formData);
  renderSidebar();
  const m = meetings.find(m=>m.id===selectedId);
  if (m) renderDetail(m);
  showView('detail');
  showToast('Reunião salva com sucesso!');
}

// ===== DASHBOARD =====
function renderDashboard() {
  const el = document.getElementById('dashboard-content');
  if (!el) return;

  const total = meetings.length;
  const realizadas = meetings.filter(m => m.status === 'Realizada').length;
  const agendadas  = meetings.filter(m => m.status === 'Agendada').length;
  const canceladas = meetings.filter(m => m.status === 'Cancelada').length;
  const adiadas    = meetings.filter(m => m.status === 'Adiada').length;

  // Órgãos únicos
  const orgsMap = {};
  meetings.forEach(m => {
    (m.participants || []).forEach(p => {
      if (p.org && p.org.trim()) {
        const k = p.org.trim();
        orgsMap[k] = (orgsMap[k] || 0) + 1;
      }
    });
  });
  const orgs = Object.entries(orgsMap).sort((a,b) => b[1]-a[1]);

  // Participantes únicos
  const partSet = new Set();
  meetings.forEach(m => (m.participants||[]).forEach(p => { if(p.email) partSet.add(p.email); else if(p.name) partSet.add(p.name); }));

  // Encaminhamentos pendentes
  const pendentes = [];
  meetings.forEach(m => {
    (m.actions||[]).filter(a => !a.done).forEach(a => pendentes.push({ ...a, meeting: m.title, meetingId: m.id }));
  });

  // Próximas reuniões (agendadas, com data futura ou recente)
  const now = new Date();
  const upcoming = meetings
    .filter(m => m.status === 'Agendada' && m.date)
    .sort((a,b) => new Date(a.date) - new Date(b.date))
    .slice(0, 5);

  // Reuniões recentes (realizadas)
  const recent = meetings
    .filter(m => m.status === 'Realizada')
    .sort((a,b) => new Date(b.date||b.createdAt) - new Date(a.date||a.createdAt))
    .slice(0, 5);

  // Status bar colors
  const statusColors2 = {
    'Realizada': '#22C55E', 'Agendada': '#3B82F6',
    'Adiada': '#F59E0B', 'Cancelada': '#EF4444'
  };

  // Donut SVG helper
  function donutSVG(data) {
    const size = 88, cx = 44, cy = 44, r = 34, stroke = 10;
    const circ = 2 * Math.PI * r;
    let offset = 0;
    const colors = ['#22C55E','#3B82F6','#F59E0B','#EF4444'];
    const slices = data.filter(d=>d.v>0).map((d,i) => {
      const frac = total > 0 ? d.v / total : 0;
      const dash = frac * circ;
      const gap = circ - dash;
      const s = `<circle cx="${cx}" cy="${cy}" r="${r}" fill="none" stroke="${colors[i]}" stroke-width="${stroke}" stroke-dasharray="${dash.toFixed(2)} ${gap.toFixed(2)}" stroke-dashoffset="${(-offset).toFixed(2)}" transform="rotate(-90 ${cx} ${cy})"/>`;
      offset += frac * circ;
      return s;
    });
    return `<svg width="${size}" height="${size}" viewBox="0 0 ${size} ${size}">
      <circle cx="${cx}" cy="${cy}" r="${r}" fill="none" stroke="#334155" stroke-width="${stroke}"/>
      ${slices.join('')}
      <text x="${cx}" y="${cy+5}" text-anchor="middle" fill="#F1F5F9" font-size="16" font-family="DM Mono,monospace" font-weight="700">${total}</text>
    </svg>`;
  }

  const donutData = [
    { label:'Realizadas', v: realizadas },
    { label:'Agendadas',  v: agendadas  },
    { label:'Adiadas',    v: adiadas    },
    { label:'Canceladas', v: canceladas },
  ];
  const donutColors = ['#22C55E','#3B82F6','#F59E0B','#EF4444'];

  function bar(v, color) {
    const pct = total > 0 ? Math.round(v/total*100) : 0;
    return `<div class="status-bar-track"><div class="status-bar-fill" style="width:${pct}%;background:${color}"></div></div>`;
  }

  // Greeting
  const hora = new Date().getHours();
  const saud = hora < 12 ? 'Bom dia' : hora < 18 ? 'Boa tarde' : 'Boa noite';
  const dateStr = new Date().toLocaleDateString('pt-BR', { weekday:'long', day:'numeric', month:'long', year:'numeric' });

  el.innerHTML = `
  <div class="dash-greeting dash-animate">
    <h2>📋 Painel de Reuniões</h2>
    <p>${dateStr}</p>
  </div>

  <!-- KPIs -->
  <div class="kpi-grid dash-animate">
    <div class="kpi-card kpi-accent-green">
      <div class="kpi-icon">✅</div>
      <div class="kpi-value">${realizadas}</div>
      <div class="kpi-label">Realizadas</div>
      <div class="kpi-sub">${total > 0 ? Math.round(realizadas/total*100) : 0}% do total</div>
    </div>
    <div class="kpi-card kpi-accent-blue">
      <div class="kpi-icon">🗓️</div>
      <div class="kpi-value">${agendadas}</div>
      <div class="kpi-label">Agendadas</div>
      <div class="kpi-sub">${upcoming.length} com data definida</div>
    </div>
    <div class="kpi-card kpi-accent-purple">
      <div class="kpi-icon">👥</div>
      <div class="kpi-value">${partSet.size}</div>
      <div class="kpi-label">Participantes</div>
      <div class="kpi-sub">${orgs.length} órgão${orgs.length!==1?'s':''} envolvido${orgs.length!==1?'s':''}</div>
    </div>
    <div class="kpi-card kpi-accent-amber">
      <div class="kpi-icon">⏳</div>
      <div class="kpi-value">${pendentes.length}</div>
      <div class="kpi-label">Encaminhamentos</div>
      <div class="kpi-sub">pendentes de conclusão</div>
    </div>
  </div>

  <!-- Row 1: Status + Órgãos -->
  <div class="dash-row dash-animate">
    <div class="dash-card">
      <div class="dash-card-head">Distribuição por Status</div>
      <div class="dash-card-body">
        ${total === 0 ? '<div class="dash-card-empty">Nenhuma reunião registrada</div>' : `
        <div class="donut-wrap">
          ${donutSVG(donutData)}
          <div class="donut-legend">
            ${donutData.map((d,i) => `
              <div class="donut-legend-item">
                <div class="donut-legend-dot" style="background:${donutColors[i]}"></div>
                <span>${d.label}</span>
                <span style="margin-left:auto;font-family:var(--font-mono);font-size:11px;color:var(--text3)">${d.v}</span>
              </div>`).join('')}
          </div>
        </div>`}
      </div>
    </div>
    <div class="dash-card">
      <div class="dash-card-head">Órgãos Envolvidos <span style="font-size:11px;font-weight:400">${orgs.length}</span></div>
      <div class="dash-card-body">
        ${orgs.length === 0 ? '<div class="dash-card-empty">Nenhum órgão registrado</div>' :
          orgs.slice(0, 7).map(([name, count]) => `
            <div class="org-item">
              <span class="org-name" title="${escHtml(name)}">🏛️ ${escHtml(name)}</span>
              <span class="org-pill">${count} reunião${count>1?'ões':''}</span>
            </div>`).join('')}
        ${orgs.length > 7 ? `<div style="font-size:11px;color:var(--text3);text-align:center;margin-top:8px;font-family:var(--font-mono)">+${orgs.length-7} outros</div>` : ''}
      </div>
    </div>
  </div>

  <!-- Row 2: Próximas + Encaminhamentos -->
  <div class="dash-row dash-animate">
    <div class="dash-card">
      <div class="dash-card-head">Próximas Reuniões</div>
      <div class="dash-card-body">
        ${upcoming.length === 0 ? '<div class="dash-card-empty">Nenhuma reunião agendada</div>' :
          upcoming.map(m => {
            const d = m.date ? new Date(m.date) : null;
            const day = d ? d.toLocaleDateString('pt-BR',{day:'2-digit'}) : '—';
            const mon = d ? d.toLocaleDateString('pt-BR',{month:'short'}).replace('.','') : '';
            return `<div class="upcoming-item" data-goto="${m.id}">
              <div class="upcoming-date-box">
                <div class="upcoming-day">${day}</div>
                <div class="upcoming-mon">${mon}</div>
              </div>
              <div style="flex:1;min-width:0">
                <div class="upcoming-title">${escHtml(m.title||'Sem título')}</div>
                <div class="upcoming-loc">${m.location ? '📍 '+escHtml(m.location) : (m.participants&&m.participants.length ? '👥 '+m.participants.length+' participantes' : '')}</div>
              </div>
            </div>`;
          }).join('')}
      </div>
    </div>
    <div class="dash-card">
      <div class="dash-card-head">Encaminhamentos Pendentes <span style="font-size:11px;font-weight:400">${pendentes.length}</span></div>
      <div class="dash-card-body">
        ${pendentes.length === 0 ? '<div class="dash-card-empty">Nenhum encaminhamento pendente 🎉</div>' :
          pendentes.slice(0, 6).map(a => `
            <div class="action-item" style="cursor:pointer" data-goto="${a.meetingId}">
              <div class="action-check"></div>
              <div>
                <div class="action-text">${escHtml(a.text)}</div>
                <div class="action-who">${a.responsible ? '👤 '+escHtml(a.responsible)+' · ' : ''}📋 ${escHtml(a.meeting)}</div>
              </div>
            </div>`).join('')}
        ${pendentes.length > 6 ? `<div style="font-size:11px;color:var(--text3);text-align:center;margin-top:8px;font-family:var(--font-mono)">+${pendentes.length-6} pendentes</div>` : ''}
      </div>
    </div>
  </div>

  <!-- Row 3: Recentes -->
  <div class="dash-card dash-animate" style="margin-bottom:32px">
    <div class="dash-card-head">Reuniões Realizadas Recentemente</div>
    <div class="dash-card-body" style="display:grid;grid-template-columns:1fr 1fr;gap:0 24px">
      ${recent.length === 0 ? '<div class="dash-card-empty" style="grid-column:1/-1">Nenhuma reunião realizada ainda</div>' :
        recent.map(m => `
          <div class="recent-item" data-goto="${m.id}">
            <div class="recent-dot" style="background:#22C55E"></div>
            <div>
              <div class="recent-title">${escHtml(m.title||'Sem título')}</div>
              <div class="recent-meta">${fmtDate(m.date)} ${m.participants&&m.participants.length ? '· 👥 '+m.participants.length : ''} ${m.actions&&m.actions.length ? '· ✅ '+m.actions.length : ''}</div>
            </div>
          </div>`).join('')}
    </div>
  </div>
  `;

  // Click handlers to navigate
  el.querySelectorAll('[data-goto]').forEach(item => {
    item.addEventListener('click', () => selectMeeting(item.dataset.goto));
  });
}


function showView(v) {
  currentView = v;
  document.getElementById('view-empty').style.display = v==='empty' ? 'block' : 'none';
  document.getElementById('view-detail').style.display = v==='detail' ? 'block' : 'none';
  document.getElementById('view-form').style.display = v==='form' ? 'block' : 'none';
  if (v==='empty') renderDashboard();
}

// ===== IA — CHAMADA UNIFICADA (Anthropic ou OpenAI) =====
async function callAI(systemPrompt, userMessage, history = []) {
  const provider = settings.aiProvider || 'anthropic';

  if (provider === 'openai') {
    const apiKey = settings.openaiKey || '';
    if (!apiKey) throw new Error('NOKEY_openai');
    const messages = [
      { role: 'system', content: systemPrompt },
      ...history,
      { role: 'user', content: userMessage }
    ];
    const res = await fetch('https://api.openai.com/v1/chat/completions', {
      method: 'POST',
      headers: { 'Content-Type': 'application/json', 'Authorization': 'Bearer ' + apiKey },
      body: JSON.stringify({ model: 'gpt-4o', max_tokens: 1500, messages })
    });
    const data = await res.json();
    if (data.error) throw new Error(data.error.message);
    return data.choices?.[0]?.message?.content || '';

  } else {
    const apiKey = settings.anthropicKey || '';
    if (!apiKey) throw new Error('NOKEY_anthropic');
    const res = await fetch('https://api.anthropic.com/v1/messages', {
      method: 'POST',
      headers: {
        'Content-Type': 'application/json',
        'x-api-key': apiKey,
        'anthropic-version': '2023-06-01',
        'anthropic-dangerous-direct-browser-access': 'true'
      },
      body: JSON.stringify({
        model: 'claude-sonnet-4-20250514',
        max_tokens: 1500,
        system: systemPrompt,
        messages: [...history, { role: 'user', content: userMessage }]
      })
    });
    const data = await res.json();
    if (data.error) throw new Error(data.error.message);
    return data.content.map(b => b.type === 'text' ? b.text : '').join('');
  }
}

function noKeyMessage(err) {
  if (err.message === 'NOKEY_openai')
    return '⚙️ Configure sua chave da <strong>OpenAI</strong> nas Configurações para usar o assistente.';
  if (err.message === 'NOKEY_anthropic')
    return '⚙️ Configure sua chave da <strong>Anthropic</strong> nas Configurações para usar o assistente.';
  const msg = err.message.includes('fetch') ? 'Não foi possível conectar. Verifique sua conexão e a chave configurada.' : err.message;
  return '❌ Erro: ' + msg;
}

// ===== EXPORTAÇÕES =====

function exportMeetingPDF(m) {
  // Guarda título original
  const origTitle = document.title;
  document.title = (m.title || 'Reunião') + ' — ' + fmtDate(m.date);
  window.print();
  document.title = origTitle;
}

function exportContactsCSV(m) {
  const participants = m.participants || [];
  if (participants.length === 0) {
    showToast('Nenhum participante para exportar.', 'info');
    return;
  }
  const header = ['Nome', 'Órgão / Instituição', 'E-mail', 'Telefone', 'Reunião', 'Data'];
  const rows = participants.map(p => [
    p.name  || '',
    p.org   || '',
    p.email || '',
    p.phone || '',
    m.title || '',
    fmtDate(m.date)
  ]);
  const csvContent = [header, ...rows]
    .map(row => row.map(cell => `"${String(cell).replace(/"/g, '""')}"`).join(';'))
    .join('\n');

  // BOM para abrir corretamente no Excel com acentos
  const blob = new Blob(['\uFEFF' + csvContent], { type: 'text/csv;charset=utf-8;' });
  const url  = URL.createObjectURL(blob);
  const a    = document.createElement('a');
  a.href     = url;
  a.download = `contatos_${(m.title||'reuniao').replace(/\s+/g,'_')}_${m.date||'sem_data'}.csv`;
  a.click();
  URL.revokeObjectURL(url);
  showToast(`📊 ${participants.length} contato(s) exportados!`);
}

// ===== BUSCA IA =====
async function aiSearch(query) {
  const resultEl = document.getElementById('ai-search-result');
  if (!query.trim()) return;

  resultEl.innerHTML = '<span style="color:var(--text3)">🔎 Analisando suas reuniões...</span>';

  const resumo = meetings.map(m => ({
    id: m.id,
    titulo: m.title || 'Sem título',
    data: m.date || '',
    status: m.status || '',
    local: m.location || '',
    participantes: (m.participants||[]).map(p=>p.name).join(', '),
    pauta: m.agenda || '',
    notas: m.notes || '',
    encaminhamentos: (m.actions||[]).map(a =>
      `${a.text}${a.responsible?' (resp: '+a.responsible+')':''}${a.deadline?' prazo: '+a.deadline:''}${a.done?' [concluído]':' [pendente]'}`
    ).join('; ')
  }));

  const systemPrompt = `Você é um assistente especializado em análise de reuniões institucionais.
O usuário tem ${meetings.length} reunião(ões) cadastrada(s) no sistema.
Aqui estão os dados completos em JSON:
${JSON.stringify(resumo, null, 2)}

Responda em português brasileiro. Seja direto, objetivo e bem organizado.
Quando listar reuniões, use formato de lista. Quando fizer análises, destaque pontos importantes.
Se a pergunta não tiver relação com os dados, diga educadamente.`;

  try {
    const reply = await callAI(systemPrompt, query);
    resultEl.textContent = reply;
  } catch(e) {
    resultEl.innerHTML = `<span style="color:#EF4444">${noKeyMessage(e)}</span>`;
  }
}

// ===== EVENTS =====
document.getElementById('btn-new').onclick = () => openForm(null);

document.getElementById('search').oninput = e => { searchText = e.target.value; renderSidebar(); };

document.getElementById('filter-chips').addEventListener('click', e => {
  if (e.target.classList.contains('chip')) {
    filterStatus = e.target.dataset.status;
    document.querySelectorAll('.chip').forEach(c=>c.classList.remove('active'));
    e.target.classList.add('active');
    renderSidebar();
  }
});

document.getElementById('btn-settings').onclick = () => {
  updateOdUI();
  document.getElementById('modal-settings').classList.remove('hidden');
};
document.getElementById('btn-settings-close').onclick = () => document.getElementById('modal-settings').classList.add('hidden');
document.getElementById('btn-settings-save').onclick  = () => document.getElementById('modal-settings').classList.add('hidden');

document.getElementById('btn-od-connect').onclick    = odConnect;
document.getElementById('btn-od-disconnect').onclick = odDisconnect;
document.getElementById('btn-od-sync-now').onclick   = () => { odLoadAll(); document.getElementById('modal-settings').classList.add('hidden'); };
document.getElementById('btn-od-import').onclick     = () => { odLoadAll(); document.getElementById('modal-settings').classList.add('hidden'); };

document.getElementById('btn-onedrive').onclick = () => {
  updateOdUI();
  document.getElementById('modal-settings').classList.remove('hidden');
};

document.getElementById('btn-delete-close').onclick = () => { document.getElementById('modal-delete').classList.add('hidden'); deleteTarget=null; };
document.getElementById('btn-delete-cancel').onclick = () => { document.getElementById('modal-delete').classList.add('hidden'); deleteTarget=null; };
document.getElementById('btn-delete-confirm').onclick = () => {
  if (deleteTarget) {
    const idToDelete = deleteTarget;
    meetings = meetings.filter(m=>m.id!==idToDelete);
    save();
    if (odTokenData) odDeleteMeeting(idToDelete);
    selectedId=null;
    deleteTarget=null;
    document.getElementById('modal-delete').classList.add('hidden');
    renderSidebar();
    showView('empty');
    showToast('Reunião removida.', 'info');
  }
};

// Close modals on overlay click
document.querySelectorAll('.modal-overlay').forEach(o => {
  o.addEventListener('click', e => { if(e.target===o) o.classList.add('hidden'); });
});

// ===== DASHBOARD =====
function renderDashboard() {
  const el = document.getElementById('dashboard-content');
  if (!el) return;

  const total = meetings.length;
  const realizadas = meetings.filter(m => m.status === 'Realizada').length;
  const agendadas = meetings.filter(m => m.status === 'Agendada').length;
  const canceladas = meetings.filter(m => m.status === 'Cancelada').length;
  const adiadas = meetings.filter(m => m.status === 'Adiada').length;

  // Órgãos únicos
  const orgSet = new Set();
  meetings.forEach(m => (m.participants||[]).forEach(p => { if(p.org && p.org.trim()) orgSet.add(p.org.trim()); }));
  const totalOrgs = orgSet.size;

  // Participantes únicos (por nome)
  const peopleSet = new Set();
  meetings.forEach(m => (m.participants||[]).forEach(p => { if(p.name && p.name.trim()) peopleSet.add(p.name.trim().toLowerCase()); }));
  const totalPeople = peopleSet.size;

  // Encaminhamentos pendentes
  const pendentes = meetings.reduce((acc, m) => acc + (m.actions||[]).filter(a => !a.done).length, 0);
  const totalActions = meetings.reduce((acc, m) => acc + (m.actions||[]).length, 0);
  const concluidos = totalActions - pendentes;

  // Encaminhamentos vencidos
  const hoje = new Date(); hoje.setHours(0,0,0,0);
  const vencidos = meetings.reduce((acc, m) => acc + (m.actions||[]).filter(a => !a.done && a.deadline && new Date(a.deadline) < hoje).length, 0);

  // Top órgãos
  const orgCount = {};
  meetings.forEach(m => (m.participants||[]).forEach(p => {
    if (p.org && p.org.trim()) orgCount[p.org.trim()] = (orgCount[p.org.trim()]||0) + 1;
  }));
  const topOrgs = Object.entries(orgCount).sort((a,b)=>b[1]-a[1]).slice(0,6);
  const maxOrg = topOrgs[0]?.[1] || 1;

  // Palavras-chave da pauta (temas)
  const stopwords = new Set(['de','a','o','e','em','para','da','do','com','que','uma','um','as','os','por','se','na','no','ao','não','é','como','sua','seu','mais','ser','dos','das','foram','para','esta','este','isso','essa','esse']);
  const wordCount = {};
  meetings.forEach(m => {
    const text = ((m.title||'') + ' ' + (m.agenda||'')).toLowerCase();
    text.replace(/[^a-záàãâéêíóôõúüçñ\s]/gi,'').split(/\s+/).forEach(w => {
      if (w.length > 3 && !stopwords.has(w)) wordCount[w] = (wordCount[w]||0) + 1;
    });
  });
  const topWords = Object.entries(wordCount).sort((a,b)=>b[1]-a[1]).slice(0,10);

  // Reuniões por mês (últimos 6 meses)
  const monthData = {};
  for (let i = 5; i >= 0; i--) {
    const d = new Date(); d.setDate(1); d.setMonth(d.getMonth() - i);
    const key = d.toLocaleDateString('pt-BR', { month:'short', year:'2-digit' });
    monthData[key] = 0;
  }
  meetings.forEach(m => {
    if (!m.date) return;
    const d = new Date(m.date);
    const key = d.toLocaleDateString('pt-BR', { month:'short', year:'2-digit' });
    if (key in monthData) monthData[key]++;
  });
  const monthEntries = Object.entries(monthData);
  const maxMonth = Math.max(...monthEntries.map(e=>e[1]), 1);

  // Reuniões recentes
  const recentes = [...meetings].sort((a,b) => new Date(b.date||b.createdAt||0) - new Date(a.date||a.createdAt||0)).slice(0, 5);

  // Próximas encaminhamentos pendentes
  const proximosEnc = [];
  meetings.forEach(m => {
    (m.actions||[]).filter(a => !a.done).forEach(a => {
      proximosEnc.push({ text: a.text, responsible: a.responsible, deadline: a.deadline, meeting: m.title, meetingId: m.id });
    });
  });
  proximosEnc.sort((a,b) => {
    if (!a.deadline && !b.deadline) return 0;
    if (!a.deadline) return 1;
    if (!b.deadline) return -1;
    return new Date(a.deadline) - new Date(b.deadline);
  });

  const statusColors2 = { 'Agendada':'#3B82F6','Realizada':'#22C55E','Cancelada':'#EF4444','Adiada':'#F59E0B' };

  const now = new Date();
  const hour = now.getHours();
  const greeting = hour < 12 ? 'Bom dia' : hour < 18 ? 'Boa tarde' : 'Boa noite';
  const dateStr = now.toLocaleDateString('pt-BR', { weekday:'long', day:'numeric', month:'long', year:'numeric' });

  const pct = t => total > 0 ? Math.round((t/total)*100) : 0;

  el.innerHTML = `
    <div class="dash-greeting">
      <h1>📋 ${greeting}! Visão geral das reuniões</h1>
      <p>${dateStr.charAt(0).toUpperCase()+dateStr.slice(1)}</p>
    </div>

    <!-- KPIs -->
    <div class="kpi-grid">
      <div class="kpi">
        <div class="kpi-icon">🗓️</div>
        <div class="kpi-label">Total de reuniões</div>
        <div class="kpi-value">${total}</div>
        <div class="kpi-sub">${realizadas} realizadas</div>
        <div class="kpi-bar"><div class="kpi-bar-fill" style="width:${pct(realizadas)}%;background:#22C55E"></div></div>
      </div>
      <div class="kpi">
        <div class="kpi-icon">🏛️</div>
        <div class="kpi-label">Órgãos envolvidos</div>
        <div class="kpi-value">${totalOrgs}</div>
        <div class="kpi-sub">${totalPeople} pessoa${totalPeople!==1?'s':''} únicas</div>
        <div class="kpi-bar"><div class="kpi-bar-fill" style="width:${Math.min(100,totalOrgs*10)}%;background:#F59E0B"></div></div>
      </div>
      <div class="kpi">
        <div class="kpi-icon">✅</div>
        <div class="kpi-label">Encaminhamentos</div>
        <div class="kpi-value">${totalActions}</div>
        <div class="kpi-sub">${concluidos} concluídos · ${pendentes} pendentes</div>
        <div class="kpi-bar"><div class="kpi-bar-fill" style="width:${totalActions>0?Math.round((concluidos/totalActions)*100):0}%;background:#3B82F6"></div></div>
      </div>
      <div class="kpi">
        <div class="kpi-icon">⚠️</div>
        <div class="kpi-label">Vencidos</div>
        <div class="kpi-value" style="color:${vencidos>0?'#FCA5A5':'#F1F5F9'}">${vencidos}</div>
        <div class="kpi-sub">encaminhamento${vencidos!==1?'s':''} em atraso</div>
        <div class="kpi-bar"><div class="kpi-bar-fill" style="width:${pendentes>0?Math.round((vencidos/pendentes)*100):0}%;background:#EF4444"></div></div>
      </div>
    </div>

    <!-- STATUS + MESES -->
    <div class="dash-row">
      <div class="dash-card">
        <div class="dash-card-head">📊 Status das reuniões</div>
        <div class="dash-card-body">
          ${total === 0 ? '<div class="dash-empty">Nenhuma reunião registrada ainda</div>' : `
          <div class="status-chart">
            ${[['Realizada','#22C55E',realizadas],['Agendada','#3B82F6',agendadas],['Adiada','#F59E0B',adiadas],['Cancelada','#EF4444',canceladas]].filter(s=>s[2]>0).map(([label,color,count])=>`
              <div class="status-bar-seg" style="background:${color};flex:${count};min-width:${count>0?'36px':'0'}">${count>0&&(count/total)>0.1?count:''}</div>
            `).join('')}
          </div>
          <div class="status-legend">
            ${[['Realizada','#22C55E',realizadas],['Agendada','#3B82F6',agendadas],['Adiada','#F59E0B',adiadas],['Cancelada','#EF4444',canceladas]].map(([label,color,count])=>`
              <div class="status-legend-item"><span class="status-legend-dot" style="background:${color}"></span>${label}: <strong>${count}</strong> (${pct(count)}%)</div>
            `).join('')}
          </div>`}
        </div>
      </div>

      <div class="dash-card">
        <div class="dash-card-head">📅 Reuniões por mês <span style="font-size:11px;color:var(--text3)">últimos 6 meses</span></div>
        <div class="dash-card-body">
          ${meetings.length === 0 ? '<div class="dash-empty">Nenhum dado disponível</div>' : `
          <div style="display:flex;align-items:flex-end;gap:8px;height:80px;margin-bottom:10px">
            ${monthEntries.map(([month,count])=>`
              <div style="flex:1;display:flex;flex-direction:column;align-items:center;gap:4px">
                <div style="font-size:10px;color:var(--text3);font-family:var(--font-mono)">${count||''}</div>
                <div style="width:100%;background:${count>0?'#3B82F6':'var(--bg3)'};border-radius:4px 4px 0 0;height:${count>0?Math.max(8,Math.round((count/maxMonth)*56)):4}px;transition:height 0.5s ease;opacity:${count>0?1:0.4}"></div>
              </div>
            `).join('')}
          </div>
          <div style="display:flex;gap:8px">
            ${monthEntries.map(([month])=>`<div style="flex:1;text-align:center;font-size:10px;color:var(--text3);font-family:var(--font-mono)">${month}</div>`).join('')}
          </div>`}
        </div>
      </div>
    </div>

    <!-- ÓRGÃOS + TEMAS + RECENTES -->
    <div class="dash-row">
      <div class="dash-card">
        <div class="dash-card-head">🏛️ Principais órgãos <span style="font-size:11px;color:var(--text3)">por participações</span></div>
        <div class="dash-card-body">
          ${topOrgs.length === 0 ? '<div class="dash-empty">Nenhum órgão registrado ainda</div>' :
            topOrgs.map(([org,count])=>`
              <div class="dash-list-item">
                <div class="dash-list-bar-wrap">
                  <div class="dash-list-label"><span style="overflow:hidden;text-overflow:ellipsis;white-space:nowrap;max-width:200px">${escHtml(org)}</span><span style="font-family:var(--font-mono);font-size:11px;color:var(--accent);flex-shrink:0;margin-left:8px">${count}</span></div>
                  <div class="dash-list-bar"><div class="dash-list-bar-fill" style="width:${Math.round((count/maxOrg)*100)}%;background:linear-gradient(90deg,#F59E0B,#D97706)"></div></div>
                </div>
              </div>`).join('')}
        </div>
      </div>

      <div class="dash-card">
        <div class="dash-card-head">🏷️ Palavras-chave / Temas</div>
        <div class="dash-card-body">
          ${topWords.length === 0 ? '<div class="dash-empty">Adicione pautas e títulos para ver temas</div>' : `
          <div style="display:flex;flex-wrap:wrap;gap:8px">
            ${topWords.map(([word,count],i)=>{
              const size = i < 3 ? 15 : i < 6 ? 13 : 12;
              const opacity = 1 - (i * 0.07);
              const colors = ['#F59E0B','#3B82F6','#22C55E','#A78BFA','#F472B6','#34D399','#60A5FA','#FBBF24'];
              const color = colors[i % colors.length];
              return `<span style="font-size:${size}px;color:${color};opacity:${opacity};background:${color}18;padding:4px 10px;border-radius:20px;border:1px solid ${color}33;cursor:default" title="${count} ocorrência${count!==1?'s':''}">${word} <span style="font-size:10px;opacity:0.7">${count}</span></span>`;
            }).join('')}
          </div>`}
        </div>
      </div>
    </div>

    <!-- RECENTES + ENCAMINHAMENTOS -->
    <div class="dash-row">
      <div class="dash-card">
        <div class="dash-card-head">🕒 Reuniões recentes</div>
        <div class="dash-card-body">
          ${recentes.length === 0 ? '<div class="dash-empty">Nenhuma reunião registrada</div>' :
            recentes.map(m=>`
              <div class="recent-item" data-open="${m.id}">
                <span class="recent-dot" style="background:${statusColors2[m.status]||'#3B82F6'}"></span>
                <div style="flex:1;min-width:0">
                  <div class="recent-title">${escHtml(m.title||'Sem título')}</div>
                  <div class="recent-meta">${fmtDate(m.date)}${m.participants?.length?` · 👥 ${m.participants.length}`:''}</div>
                </div>
                ${badge(m.status)}
              </div>`).join('')}
        </div>
      </div>

      <div class="dash-card">
        <div class="dash-card-head">📌 Encaminhamentos pendentes <span style="font-size:11px;color:${vencidos>0?'#FCA5A5':'var(--text3)'}">${vencidos>0?`⚠️ ${vencidos} vencido${vencidos>1?'s':''}`:'todos no prazo'}</span></div>
        <div class="dash-card-body">
          ${proximosEnc.length === 0 ? '<div class="dash-empty">Nenhum encaminhamento pendente 🎉</div>' :
            proximosEnc.slice(0,6).map(a=>{
              const isOverdue = a.deadline && new Date(a.deadline) < hoje;
              return `<div class="action-item">
                <span style="font-size:14px;margin-top:1px">${isOverdue?'🔴':'🟡'}</span>
                <div style="flex:1;min-width:0">
                  <div class="action-text">${escHtml(a.text)}</div>
                  <div class="action-meta ${isOverdue?'overdue':''}">${a.responsible?`👤 ${escHtml(a.responsible)} · `:''}${a.deadline?`📅 ${fmtDate(a.deadline)}`:'Sem prazo'} — <span style="color:var(--text2)">${escHtml(a.meeting)}</span></div>
                </div>
                <button class="btn btn-ghost btn-sm" data-open="${a.meetingId}" style="flex-shrink:0;font-size:11px">Ver</button>
              </div>`;
            }).join('')}
          ${proximosEnc.length > 6 ? `<div style="text-align:center;padding-top:8px;font-size:12px;color:var(--text3)">+ ${proximosEnc.length-6} outros pendentes</div>` : ''}
        </div>
      </div>
    </div>
  `;

  // Events: click to open meeting
  el.querySelectorAll('[data-open]').forEach(e => {
    e.addEventListener('click', ev => {
      ev.stopPropagation();
      selectMeeting(e.dataset.open);
    });
  });
}

// ===== RESPONSIVE SIDEBAR =====
function isMobile() { return window.innerWidth <= 768; }

function openSidebar() {
  document.getElementById('sidebar').classList.add('open');
  document.getElementById('sidebar-overlay').classList.add('show');
  document.getElementById('btn-sidebar-toggle').classList.add('open');
}
function closeSidebar() {
  document.getElementById('sidebar').classList.remove('open');
  document.getElementById('sidebar-overlay').classList.remove('show');
  document.getElementById('btn-sidebar-toggle').classList.remove('open');
}
function toggleSidebar() {
  const open = document.getElementById('sidebar').classList.contains('open');
  open ? closeSidebar() : openSidebar();
}

document.getElementById('btn-ai-search').onclick = () => {
  document.getElementById('modal-ai-search').classList.remove('hidden');
  document.getElementById('ai-search-input').focus();
};
document.getElementById('btn-ai-search-close').onclick  = () => document.getElementById('modal-ai-search').classList.add('hidden');
document.getElementById('btn-ai-search-cancel').onclick = () => document.getElementById('modal-ai-search').classList.add('hidden');
document.getElementById('btn-ai-search-send').onclick   = () => aiSearch(document.getElementById('ai-search-input').value);
document.getElementById('ai-search-input').addEventListener('keydown', e => { if (e.key==='Enter') aiSearch(e.target.value); });
document.querySelectorAll('[data-sq]').forEach(b => {
  b.addEventListener('click', () => {
    document.getElementById('ai-search-input').value = b.dataset.sq;
    aiSearch(b.dataset.sq);
  });
});
document.getElementById('modal-ai-search').addEventListener('click', e => {
  if (e.target === document.getElementById('modal-ai-search')) document.getElementById('modal-ai-search').classList.add('hidden');
});
document.getElementById('btn-sidebar-toggle').onclick = toggleSidebar;
document.getElementById('sidebar-overlay').onclick = closeSidebar;

// Close sidebar when a meeting is selected on mobile
const _origSelect = selectMeeting;
selectMeeting = function(id) {
  _origSelect(id);
  if (isMobile()) closeSidebar();
};

// ===== INIT =====
renderSidebar();
renderDashboard();
restoreOdSession();

// Tema
applyTheme(settings.theme || 'light');
document.querySelectorAll('.theme-btn').forEach(btn => {
  btn.onclick = () => setTheme(btn.dataset.theme);
});

// Auto-sync configurável
startAutoSync();

function updateProviderUI() {}

// Inicializa UI quando settings for aberto
document.getElementById('btn-settings').addEventListener('click', () => {
  initAutoSyncUI();
  applyTheme(settings.theme || 'light');
});
</script>
</body>
</html>
