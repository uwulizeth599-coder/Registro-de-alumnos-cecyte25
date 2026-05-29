# Registro-de-alumnos-cecyte25
<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>CECyTE 25 – Registro de Alumnos</title>
<link href="https://fonts.googleapis.com/css2?family=Bebas+Neue&family=Nunito:wght@400;500;600;700;800;900&display=swap" rel="stylesheet">
<style>
:root {
  --verde:   #006a07;
  --verde2:  #024c1a;
  --rojo:    #b91c1c;
  --oro:     #f59e0b;
  --bg:      #f0f4f8;
  --card:    #ffffff;
  --border:  #8aa1c4;
  --texto:   #1e293b;
  --muted:   #64748b;
  --r:       14px;
  --sh:      0 4px 24px rgba(0,0,0,.09);
}
*{margin:0;padding:0;box-sizing:border-box;}
body{font-family:'Nunito',sans-serif;background:var(--bg);color:var(--texto);min-height:100vh;}
 
/* ── HEADER ── */
header{
  background:linear-gradient(160deg,#08014a 0%,#820202 55%,#460541 100%);
  position:relative;overflow:hidden;
}
header::after{
  content:'';position:absolute;inset:0;
  background:repeating-linear-gradient(45deg,black,transparent 20px,rgba(255,255,255,.03) 20px,rgba(255,255,255,.03) 40px);
  pointer-events:none;
}
 
.hdr-main{
  display:flex;align-items:center;justify-content:space-between;
  padding:1.1rem 2rem;position:relative;z-index:2;gap:1rem;flex-wrap:wrap;
}
 
/* LOGO */
.logo-box{
  width:80px;height:80px;
  background:#fff;border-radius:14px;
  border:3px solid var(--oro);
  box-shadow:0 4px 16px rgba(0,0,0,.25);
  display:flex;flex-direction:column;align-items:center;justify-content:center;
  flex-shrink:0;padding:6px;
  position:relative;
}
.logo-box::before{
  content:'';position:absolute;inset:4px;
  border:1.5px dashed rgba(0,104,71,.15);border-radius:10px;
}
.lc{ font-family:'Bebas Neue',sans-serif;font-size:1.55rem;color:var(--verde);line-height:1;letter-spacing:.06em; }
.ln{ font-family:'Bebas Neue',sans-serif;font-size:2.2rem;color:var(--rojo);line-height:1; }
.lt{ font-size:.42rem;font-weight:900;color:var(--muted);text-transform:uppercase;letter-spacing:.08em; }
 
.hdr-info{ flex:1;min-width:200px; }
.hdr-info h1{
  font-family:'Bebas Neue',sans-serif;font-size:2.1rem;
  color:#028c99;letter-spacing:.08em;line-height:1;
  text-shadow:0 2px 8px rgba(0,0,0,.3);
}
.hdr-info .sub{ font-size:.78rem;color:rgba(255,255,255,.72);font-weight:700;letter-spacing:.04em;margin-top:.2rem; }
.badge-6to{
  display:inline-flex;align-items:center;gap:.35rem;
  background:rgba(245,158,11,.18);
  border:1px solid rgba(245,158,11,.4);
  border-radius:999px;padding:.28rem .85rem;
  font-size:.71rem;color:var(--oro);font-weight:800;
  letter-spacing:.04em;margin-top:.5rem;
}
 
.hdr-stats{display:flex;gap:.75rem;flex-shrink:0;}
.hst{
  text-align:center;
  background:rgba(255,255,255,.1);
  border:1px solid rgba(255,255,255,.18);
  border-radius:10px;padding:.55rem .9rem;min-width:62px;
}
.hst-n{font-family:'Bebas Neue',sans-serif;font-size:1.9rem;color:var(--oro);line-height:1;}
.hst-l{font-size:.6rem;color:rgba(223, 212, 2, 0.68);font-weight:800;text-transform:uppercase;letter-spacing:.05em;}
 
.hdr-stripe{
  background:var(--rojo);padding:.32rem 2rem;
  display:flex;align-items:center;gap:.5rem;
  position:relative;z-index:2;flex-wrap:wrap;
}
.hdr-stripe span{font-size:.72rem;color:rgb(255, 255, 255);font-weight:800;letter-spacing:.06em;text-transform:uppercase;}
.dot{width:5px;height:5px;border-radius:50%;background:var(--oro);flex-shrink:0;}
 
/* ── TABS ── */
.tabs{
  background:#2e0169d2;border-bottom:2px solid #ffffff;
  padding:0 2rem;display:flex;gap:0;
}
.tab{
  padding:.85rem 1.4rem;background:none;border:none;
  font-family:'Nunito',sans-serif;font-size:.875rem;font-weight:800;
  color:var(--texto);cursor:pointer;
  border-bottom:3px solid transparent;margin-bottom:-2px;
  transition:all .2s;display:flex;align-items:center;gap:.35rem;
}
.tab:hover{color:var(--bg);}
.tab.active{color:var(--bg);border-bottom-color:var(--bg);}
 
/* ── MAIN ── */
main{max-width:1140px;margin:0 auto;padding:1.75rem 1.25rem 3rem;}
 
/* ── CARD ── */
.card{
  background:var(--card);border-radius:var(--r);
  box-shadow:var(--sh);border:1px solid #ffffff;
  padding:1.75rem;margin-bottom:1.5rem;
  animation:up .4s ease both;
}
@keyframes up{from{opacity:0;transform:translateY(14px)}to{opacity:1;transform:translateY(0)}}
 
.card-title{
  font-family:'Bebas Neue',sans-serif;font-size:1.25rem;
  color:var(--texto);letter-spacing:.06em;
  display:flex;align-items:center;gap:.5rem;
  padding-bottom:.75rem;border-bottom:2px solid var(--bg);
  margin-bottom:1.35rem;
}
.card-title::before{content:'';width:4px;height:1.2rem;background:var(--texto);border-radius:99px;}
 
/* ── FORM ── */
.fgrid{display:grid;grid-template-columns:repeat(auto-fill,minmax(185px,1fr));gap:1rem;}
.field{display:flex;flex-direction:column;gap:.35rem;}
.field.full{grid-column:1/-1;}
.field.half{grid-column:span 2;}
 
label{font-size:.7rem;font-weight:900;text-transform:uppercase;letter-spacing:.07em;color:var(--verde);}
 
input,select{
  background:#fefeff;border:1.5px solid var(--rojo);
  border-radius:8px;color:var(--texto);
  font-family:'Nunito',sans-serif;font-size:.9rem;font-weight:600;
  padding:.6rem .9rem;transition:border-color .2s,box-shadow .2s,background .2s;
  width:100%;appearance:none;
}
input:focus,select:focus{
  outline:none;border-color:var(--texto);
  box-shadow:0 0 0 3px rgb(255, 255, 255);background:#fff;
}
select{
  background-image:url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='12' height='8'%3E%3Cpath d='M1 1l5 5 5-5' stroke='%2364748b' stroke-width='1.5' fill='none'/%3E%3C/svg%3E");
  background-repeat:no-repeat;background-position:right .85rem center;padding-right:2.2rem;
}
 
.btn-row{display:flex;gap:.75rem;margin-top:1.35rem;flex-wrap:wrap;}
.btn{
  padding:.65rem 1.5rem;border-radius:8px;border:none;
  font-family:'Nunito',sans-serif;font-size:.9rem;font-weight:800;
  cursor:pointer;transition:all .2s;display:flex;align-items:center;gap:.4rem;
}
.btn-p{background:var(--texto);color:#ffffff;}
.btn-p:hover{background:#ffffff;transform:translateY(-1px);box-shadow:0 6px 18px rgba(255, 255, 255, 0.28);}
.btn-s{background:transparent;border:1.5px solid var(--texto);color:var(--texto);}
.btn-s:hover{border-color:var(--verde2);color:var(--verde);}
.btn-d{background:rgba(185,28,28,.08);border:1.5px solid rgba(185,28,28,.22);color:var(--rojo);}
.btn-d:hover{background:rgba(185,28,28,.16);}
 
/* ── TABLE ── */
.tbl-hdr{display:flex;align-items:center;justify-content:space-between;margin-bottom:1rem;flex-wrap:wrap;gap:.5rem;}
.srch{
  display:flex;align-items:center;gap:.4rem;
  background:#ffffff;border:1.5px solid var(--border);
  border-radius:8px;padding:.4rem .85rem;width:230px;
}
.srch input{border:none;background:transparent;padding:0;font-size:.85rem;width:100%;}
.srch input:focus{box-shadow:none;background:transparent;}
 
.tbl-wrap{overflow-x:auto;}
table{width:100%;border-collapse:collapse;font-size:.84rem;}
thead tr{background:var(--verde);}
th{
  padding:.75rem .9rem;text-align:left;
  font-size:.68rem;font-weight:900;text-transform:uppercase;
  letter-spacing:.07em;color:#ffffffe8;white-space:nowrap;
}
th:first-child{border-radius:8px 0 0 0;}
th:last-child{border-radius:0 8px 0 0;}
tbody tr{border-bottom:1px solid #fafafa;transition:background .15s;}
tbody tr:hover{background:#ffffff;}
tbody tr:last-child{border-bottom:none;}
td{padding:.78rem .9rem;vertical-align:middle;}
 
.badge{display:inline-flex;align-items:center;padding:.2rem .6rem;border-radius:999px;font-size:.71rem;font-weight:800;letter-spacing:.04em;}
.bg-A{background:#dbeafe;color:#1d4ed8;border:1px solid #bfdbfe;}
.bg-B{background:#fef3c7;color:#92400e;border:1px solid #fde68a;}
.bg-C{background:#dcfce7;color:#166534;border:1px solid #bbf7d0;}
 
.grd-badge{display:inline-block;background:rgba(252, 255, 254, 0.1);color:var(--verde);border:1px solid rgb(255, 255, 255);border-radius:6px;padding:.2rem .55rem;font-size:.71rem;font-weight:800;}
.pc-badge{display:inline-block;background:#ffffff;color:var(--texto);border:1px solid #cbd5e1;border-radius:6px;padding:.2rem .55rem;font-size:.71rem;font-weight:800;font-family:monospace;}
 
.hora-e{color:#ffffff;font-weight:700;}
.hora-s{color:#d97706;font-weight:700;}
 
.acts{display:flex;gap:.3rem;}
.ibtn{width:29px;height:29px;border-radius:7px;border:none;cursor:pointer;transition:all .2s;display:flex;align-items:center;justify-content:center;font-size:.83rem;}
.ie{background:rgba(255, 252, 252, 0.771);color:var(--verde);}
.ie:hover{background:rgba(0,104,71,.22);}
.id{background:rgba(185,28,28,.09);color:var(--rojo);}
.id:hover{background:rgba(185,28,28,.2);}
 
.empty{text-align:center;padding:2.5rem;}
.empty-i{font-size:2.8rem;margin-bottom:.5rem;opacity:.35;}
.empty p{color:var(--muted);font-size:.9rem;}
 
/* ── RESUMEN ── */
.res-tiles{display:grid;grid-template-columns:repeat(auto-fill,minmax(130px,1fr));gap:1rem;margin-bottom:1.5rem;}
.rtile{background:var(--bg);border:1.5px solid var(--border);border-radius:10px;padding:.9rem;text-align:center;}
.rtile-n{font-family:'Bebas Neue',sans-serif;font-size:2.2rem;color:var(--verde);line-height:1;}
.rtile-l{font-size:.68rem;font-weight:800;text-transform:uppercase;letter-spacing:.06em;color:var(--muted);margin-top:.2rem;}
 
/* ── SECTION ── */
.sec{display:none;}
.sec.active{display:block;}
 
/* ── MODAL ── */
.ov{position:fixed;inset:0;z-index:300;background:rgba(0,0,0,.5);backdrop-filter:blur(3px);display:flex;align-items:center;justify-content:center;padding:1rem;opacity:0;pointer-events:none;transition:opacity .25s;}
.ov.open{opacity:1;pointer-events:all;}
.modal{background:#ffffff;border-radius:var(--r);padding:1.75rem;width:100%;max-width:560px;box-shadow:0 20px 60px rgba(0,0,0,.2);transform:scale(.95);transition:transform .25s;}
.ov.open .modal{transform:scale(1);}
.modal-t{font-family:'Bebas Neue',sans-serif;font-size:1.2rem;color:var(--verde);letter-spacing:.05em;display:flex;justify-content:space-between;align-items:center;margin-bottom:1.25rem;}
.xbtn{background:none;border:none;font-size:1.3rem;cursor:pointer;color:var(--muted);transition:color .2s;}
.xbtn:hover{color:var(--rojo);}
 
/* ── TOAST ── */
.toast{position:fixed;bottom:1.5rem;right:1.5rem;z-index:999;background:#ffffff;border:1px solid var(--border);border-radius:10px;padding:.8rem 1.2rem;font-size:.875rem;font-weight:700;box-shadow:0 8px 30px rgba(0,0,0,.12);display:flex;align-items:center;gap:.5rem;transform:translateY(80px);opacity:0;transition:all .35s cubic-bezier(.34,1.56,.64,1);max-width:300px;}
.toast.show{transform:translateY(0);opacity:1;}
.toast.ok{border-left:4px solid var(--verde2);}
.toast.err{border-left:4px solid var(--rojo);}
.toast.inf{border-left:4px solid var(--oro);}
 
/* ── FOOTER ── */
footer{background:linear-gradient(135deg,#34026a,#7b0202);text-align:center;padding:1rem 1.5rem;}
footer p{font-size:.72rem;color:rgba(255,255,255,.7);font-weight:700;letter-spacing:.04em;}
footer strong{color:var(--oro);}
 
@media(max-width:640px){
  .hdr-stats{display:none;}
  .fgrid{grid-template-columns:1fr;}
  .field.half{grid-column:1/-1;}
  .hdr-main{padding:1rem;}
  .tabs{padding:0 .75rem;}
  .tab{padding:.75rem .8rem;font-size:.8rem;}
  .srch{width:160px;}
}
</style>
</head>
<body>
 
<!-- ═══ HEADER ═══ -->
<header>
  <div class="hdr-main">
    <!-- LOGO -->
    <div style="display:flex;align-items:center;gap:1rem;">
      <div class="logo-box">
        <div class="lc">CECyTE</div>
        <div class="ln">25</div>
        <div class="lt">Tlaxcala</div>
      </div>
      <div class="hdr-info">
        <h1>Registro de Alumnos</h1>
        <div class="sub">Control de Asistencia y Laboratorio de Cómputo</div>
        <div class="badge-6to">🎓 Proyecto De Titulacion · 6° Semestre</div>
      </div>
    </div>
    <!-- STATS -->
    <div class="hdr-stats">
      <div class="hst"><div class="hst-n" id="hT">0</div><div class="hst-l">Total</div></div>
      <div class="hst"><div class="hst-n" id="hA">0</div><div class="hst-l">Grupo A</div></div>
      <div class="hst"><div class="hst-n" id="hB">0</div><div class="hst-l">Grupo B</div></div>
      <div class="hst"><div class="hst-n" id="hC">0</div><div class="hst-l">Grupo C</div></div>
    </div>
  </div>
  <div class="hdr-stripe">
    <div class="dot"></div><span>CECyTE Plantel 25</span>
    <div class="dot"></div><span>Ciclo Escolar 2023–2026</span>
    <div class="dot"></div><span>Programacion · 6° Semestre</span>
    <div class="dot"></div>
  </div>
</header>
 
<!-- ═══ TABS ═══ -->
<div class="tabs">
  <button class="tab active" id="t-reg"   onclick="goTab('reg')">  ✏️ Registrar</button>
  <button class="tab"        id="t-lista" onclick="goTab('lista')">📋 Lista</button>
  <button class="tab"        id="t-res"   onclick="goTab('res')">  📊 Resumen</button>
</div>
 
<!-- ═══ MAIN ═══ -->
<main>
 
  <!-- ── REGISTRO ── -->
  <div class="sec active" id="s-reg">
    <div class="card">
      <div class="card-title">Datos del Alumno</div>
      <div class="fgrid">
        <div class="field">
          <label>Nombre completo</label>
          <input id="f-nom" type="text" placeholder="Apellidos, Nombre" />
        </div>
        <div class="field">
          <label>Matrícula</label>
          <input id="f-mat" type="text" placeholder="CECyTE25-001" />
        </div>
        <div class="field">
          <label>Grado</label>
          <select id="f-grado">
            <option value="">— Seleccionar —</option>
            <option>1°</option><option>2°</option><option>3°</option>
            <option>4°</option><option>5°</option><option>6°</option>
          </select>
        </div>
        <div class="field">
          <label>Grupo</label>
          <select id="f-grupo">
            <option value="">— Seleccionar —</option>
            <option value="A">A</option>
            <option value="B">B</option>
            <option value="C">C</option>
          </select>
        </div>
        <div class="field">
          <label>Hora de entrada</label>
          <input id="f-ent" type="time" value="07:00" />
        </div>
        <div class="field">
          <label>Hora de salida</label>
          <input id="f-sal" type="time" value="14:00" />
        </div>
        <div class="field">
          <label>N° de PC</label>
          <input id="f-pc" type="text" placeholder="Ej. PC-07" />
        </div>
        <div class="field">
          <label>Docente a cargo</label>
          <input id="f-doc" type="text" placeholder="Nombre del docente" />
        </div>
      </div>
      <div class="btn-row">
        <button class="btn btn-p" onclick="guardar()">💾 Guardar alumno</button>
        <button class="btn btn-s" onclick="limpiar()">🗑️ Limpiar</button>
      </div>
    </div>
  </div>
 
  <!-- ── LISTA ── -->
  <div class="sec" id="s-lista">
    <div class="card">
      <div class="tbl-hdr">
        <div class="card-title" style="margin-bottom:0;padding-bottom:0;border-bottom:none">Alumnos registrados</div>
        <div class="srch">
          <span>🔍</span>
          <input type="text" id="buscar" placeholder="Buscar…" oninput="renderTabla()" />
        </div>
      </div>
      <div class="tbl-wrap">
        <table>
          <thead>
            <tr>
              <th>#</th>
              <th>Nombre</th>
              <th>Matrícula</th>
              <th>Grado</th>
              <th>Grupo</th>
              <th>Entrada</th>
              <th>Salida</th>
              <th>N° PC</th>
              <th>Docente</th>
              <th>Acciones</th>
            </tr>
          </thead>
          <tbody id="tbody"></tbody>
        </table>
        <div class="empty" id="emptyMsg" style="display:none">
          <div class="empty-i">🖥️</div>
          <p>No hay alumnos registrados aún.</p>
        </div>
      </div>
    </div>
  </div>
 
  <!-- ── RESUMEN ── -->
  <div class="sec" id="s-res">
    <div class="card">
      <div class="card-title">Resumen general</div>
      <div class="res-tiles" id="resTiles"></div>
      <div id="resTbl"></div>
      <div id="resDoc" style="margin-top:1.25rem"></div>
      <div id="resPc"  style="margin-top:1.25rem"></div>
    </div>
  </div>
 
</main>
 
<!-- ═══ MODAL EDITAR ═══ -->
<div class="ov" id="ov">
  <div class="modal">
    <div class="modal-t">
      ✏️ Editar alumno
      <button class="xbtn" onclick="closeModal()">✕</button>
    </div>
    <div class="fgrid">
      <div class="field"><label>Nombre</label><input id="e-nom" type="text"/></div>
      <div class="field"><label>Matrícula</label><input id="e-mat" type="text"/></div>
      <div class="field">
        <label>Grado</label>
        <select id="e-grado">
          <option>1°</option><option>2°</option><option>3°</option>
          <option>4°</option><option>5°</option><option>6°</option>
        </select>
      </div>
      <div class="field">
        <label>Grupo</label>
        <select id="e-grupo">
          <option value="A">A</option>
          <option value="B">B</option>
          <option value="C">C</option>
        </select>
      </div>
      <div class="field"><label>Hora entrada</label><input id="e-ent" type="time"/></div>
      <div class="field"><label>Hora salida</label><input id="e-sal" type="time"/></div>
      <div class="field"><label>N° de PC</label><input id="e-pc" type="text"/></div>
      <div class="field"><label>Docente a cargo</label><input id="e-doc" type="text"/></div>
    </div>
    <div class="btn-row">
      <button class="btn btn-p" onclick="saveEdit()">💾 Guardar cambios</button>
      <button class="btn btn-s" onclick="closeModal()">Cancelar</button>
    </div>
  </div>
</div>
 
<div class="toast" id="toast"></div>
 
<!-- ═══ FOOTER ═══ -->
<footer>
  <p>
    <strong>CECyTE Plantel 25</strong> &nbsp;·&nbsp;
     Proyecto de Desarrollo De Aplicacion Web &nbsp;·&nbsp;
    <strong>6° Semestre</strong> &nbsp;·&nbsp; Ciclo 2023–2026
  </p>
</footer>
 
<script>
// ── DB ──
const KEY = 'cecyte25v2';
let db = (()=>{ try{ return JSON.parse(localStorage.getItem(KEY))||[]; }catch{ return []; }})();
let editId = null;
function saveDB(){ localStorage.setItem(KEY, JSON.stringify(db)); }
 
// ── TABS ──
function goTab(id){
  ['reg','lista','res'].forEach(t=>{
    document.getElementById('s-'+t).classList.toggle('active',t===id);
    document.getElementById('t-'+t).classList.toggle('active',t===id);
  });
  if(id==='lista') renderTabla();
  if(id==='res')   renderRes();
}
 
// ── GUARDAR ──
function guardar(){
  const v={
    nom:   g('f-nom').trim(),
    mat:   g('f-mat').trim(),
    grado: g('f-grado'),
    grupo: g('f-grupo'),
    ent:   g('f-ent'),
    sal:   g('f-sal'),
    pc:    g('f-pc').trim(),
    doc:   g('f-doc').trim(),
  };
  if(Object.values(v).some(x=>!x)){ toast('⚠️ Completa todos los campos','err'); return; }
  if(db.some(a=>a.mat===v.mat)){ toast('⚠️ Matrícula ya registrada','err'); return; }
  db.push({id:Date.now(),...v});
  saveDB(); stats(); limpiar();
  toast('✅ Alumno registrado correctamente','ok');
}
 
function limpiar(){
  ['f-nom','f-mat','f-pc','f-doc'].forEach(i=>set(i,''));
  set('f-grado',''); set('f-grupo','');
  set('f-ent','07:00'); set('f-sal','14:00');
}
 
// ── TABLA ──
function renderTabla(){
  const q=(document.getElementById('buscar').value||'').toLowerCase();
  const rows=db.filter(a=>
    a.nom.toLowerCase().includes(q)||
    a.mat.toLowerCase().includes(q)||
    a.doc.toLowerCase().includes(q)||
    a.pc.toLowerCase().includes(q)
  );
  const tbody=document.getElementById('tbody');
  const empty=document.getElementById('emptyMsg');
  if(!rows.length){ tbody.innerHTML=''; empty.style.display='block'; return; }
  empty.style.display='none';
  tbody.innerHTML=rows.map((a,i)=>`
    <tr>
      <td style="color:var(--muted);font-weight:800">${i+1}</td>
      <td style="font-weight:700">${a.nom}</td>
      <td style="font-family:monospace;font-size:.81rem;color:var(--verde);font-weight:700">${a.mat}</td>
      <td><span class="grd-badge">${a.grado}</span></td>
      <td><span class="badge bg-${a.grupo}">${a.grupo}</span></td>
      <td class="hora-e">${fmt(a.ent)}</td>
      <td class="hora-s">${fmt(a.sal)}</td>
      <td><span class="pc-badge">💻 ${a.pc}</span></td>
      <td style="font-size:.81rem;color:var(--muted)">${a.doc}</td>
      <td><div class="acts">
        <button class="ibtn ie" onclick="openEdit(${a.id})" title="Editar">✏️</button>
        <button class="ibtn id" onclick="del(${a.id})"     title="Eliminar">🗑️</button>
      </div></td>
    </tr>`).join('');
}
 
function fmt(t){
  if(!t) return '—';
  const [h,m]=t.split(':'); const H=+h;
  return `${H%12||12}:${m} ${H>=12?'PM':'AM'}`;
}
 
// ── ELIMINAR ──
function del(id){
  if(!confirm('¿Eliminar este alumno del registro?')) return;
  db=db.filter(a=>a.id!==id);
  saveDB(); stats(); renderTabla();
  toast('🗑️ Alumno eliminado','inf');
}
 
// ── EDITAR ──
function openEdit(id){
  const a=db.find(x=>x.id===id); if(!a) return;
  editId=id;
  set('e-nom',a.nom); set('e-mat',a.mat);
  set('e-grado',a.grado); set('e-grupo',a.grupo);
  set('e-ent',a.ent); set('e-sal',a.sal);
  set('e-pc',a.pc); set('e-doc',a.doc);
  document.getElementById('ov').classList.add('open');
}
 
function closeModal(){ document.getElementById('ov').classList.remove('open'); editId=null; }
 
function saveEdit(){
  const idx=db.findIndex(a=>a.id===editId); if(idx<0) return;
  db[idx]={...db[idx],
    nom:g('e-nom').trim(), mat:g('e-mat').trim(),
    grado:g('e-grado'), grupo:g('e-grupo'),
    ent:g('e-ent'), sal:g('e-sal'),
    pc:g('e-pc').trim(), doc:g('e-doc').trim(),
  };
  saveDB(); stats(); renderTabla(); closeModal();
  toast('✅ Cambios guardados','ok');
}
 
// ── RESUMEN ──
function renderRes(){
  const grupos=['A','B','C'];
  const grados=[...new Set(db.map(a=>a.grado))].sort();
 
  const colores={A:'#1d4ed8',B:'#92400e',C:'#166534'};
  document.getElementById('resTiles').innerHTML=
    `<div class="rtile"><div class="rtile-n">${db.length}</div><div class="rtile-l">Total alumnos</div></div>`+
    grupos.map(g=>`<div class="rtile"><div class="rtile-n" style="color:${colores[g]}">${db.filter(a=>a.grupo===g).length}</div><div class="rtile-l">Grupo ${g}</div></div>`).join('');
 
  if(!db.length){ document.getElementById('resTbl').innerHTML='<p style="color:var(--muted);font-size:.9rem">Sin datos.</p>'; return; }
 
  // tabla grado x grupo
  let t=`<table style="width:100%;border-collapse:collapse;font-size:.85rem">
    <thead><tr style="background:var(--verde)">
      <th style="padding:.6rem .9rem;color:#fff;font-size:.68rem;border-radius:8px 0 0 0">Grado</th>
      ${grupos.map(g=>`<th style="padding:.6rem .9rem;color:#fff;font-size:.68rem;text-align:center">Grupo ${g}</th>`).join('')}
      <th style="padding:.6rem .9rem;color:#fff;font-size:.68rem;text-align:center;border-radius:0 8px 0 0">Total</th>
    </tr></thead><tbody>`;
  grados.forEach(gr=>{
    let tot=0; t+=`<tr style="border-bottom:1px solid #f1f5f9"><td style="padding:.6rem .9rem;font-weight:700">${gr}</td>`;
    grupos.forEach(gp=>{ const n=db.filter(a=>a.grado===gr&&a.grupo===gp).length; tot+=n; t+=`<td style="text-align:center;padding:.6rem .9rem;color:${n?'var(--texto)':'var(--muted)'}">${n||'—'}</td>`; });
    t+=`<td style="text-align:center;padding:.6rem .9rem;font-weight:800;color:var(--verde)">${tot}</td></tr>`;
  });
  t+=`</tbody></table>`;
  document.getElementById('resTbl').innerHTML=t;
 
  // docentes
  const docs=[...new Set(db.map(a=>a.doc))];
  document.getElementById('resDoc').innerHTML=
    `<div style="font-family:'Bebas Neue',sans-serif;font-size:1rem;color:var(--verde);letter-spacing:.05em;margin-bottom:.6rem">👩‍🏫 Docentes registrados</div>
     <div style="display:flex;flex-wrap:wrap;gap:.5rem">
       ${docs.map(d=>`<span style="background:rgba(0,104,71,.08);border:1px solid rgba(0,104,71,.2);border-radius:7px;padding:.3rem .8rem;font-size:.8rem;font-weight:700">${d}</span>`).join('')}
     </div>`;
 
  // pcs usadas
  const pcs=[...new Set(db.map(a=>a.pc))].sort();
  document.getElementById('resPc').innerHTML=
    `<div style="font-family:'Bebas Neue',sans-serif;font-size:1rem;color:var(--verde);letter-spacing:.05em;margin-bottom:.6rem">💻 PCs asignadas</div>
     <div style="display:flex;flex-wrap:wrap;gap:.5rem">
       ${pcs.map(p=>`<span style="background:#f1f5f9;border:1px solid #cbd5e1;border-radius:7px;padding:.3rem .8rem;font-size:.8rem;font-weight:700;font-family:monospace">${p}</span>`).join('')}
     </div>`;
}
 
// ── STATS ──
function stats(){
  document.getElementById('hT').textContent=db.length;
  ['A','B','C'].forEach(g=>document.getElementById('h'+g).textContent=db.filter(a=>a.grupo===g).length);
}
 
// ── HELPERS ──
function g(id){ return document.getElementById(id).value; }
function set(id,v){ document.getElementById(id).value=v; }
 
// ── TOAST ──
function toast(msg,tipo='inf'){
  const el=document.getElementById('toast');
  el.textContent=msg; el.className=`toast ${tipo} show`;
  setTimeout(()=>el.classList.remove('show'),3000);
}
 
// INIT
stats();
</script>
</body>
</html>
