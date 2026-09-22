<!DOCTYPE html>
<html lang="it">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Test Attività Sportive — Compilazione</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Fraunces:opsz,wght@9..144,500;9..144,600;9..144,700&family=Inter:wght@400;500;600;700&family=IBM+Plex+Mono:wght@500&display=swap" rel="stylesheet">
<style>
  :root{
    --ink:#14213D;
    --ink-soft:#3C4A66;
    --bg:#F5F6F2;
    --paper:#FFFFFF;
    --line:#E1E2DC;
    --accent:#2F8F6B;
    --accent-soft:#E7F2ED;
    --warn:#C4572A;
    --warn-soft:#FBEBE3;
  }
  *{box-sizing:border-box;}
  body{
    margin:0;
    background:var(--bg);
    color:var(--ink);
    font-family:'Inter',sans-serif;
    line-height:1.5;
  }
  .wrap{max-width:760px;margin:0 auto;padding:0 24px 120px;}
  header.top{
    padding:56px 24px 40px;
    max-width:760px;margin:0 auto;
    border-bottom:1px solid var(--line);
  }
  .eyebrow{
    font-family:'IBM Plex Mono',monospace;
    font-size:12px;letter-spacing:.14em;text-transform:uppercase;
    color:var(--accent);margin-bottom:14px;
  }
  h1{
    font-family:'Fraunces',serif;
    font-weight:600;
    font-size:38px;
    margin:0 0 12px;
    letter-spacing:-.01em;
  }
  .sub{color:var(--ink-soft);font-size:16px;max-width:56ch;}

  .pentagon{
    position:absolute;
    right:40px; top:56px;
    width:64px;height:64px;
    opacity:.9;
  }

  section.card{
    background:var(--paper);
    border:1px solid var(--line);
    border-radius:4px;
    padding:32px;
    margin-top:28px;
  }
  .field-grid{display:grid;grid-template-columns:1fr 1fr;gap:18px 20px;}
  .field{display:flex;flex-direction:column;gap:6px;}
  .field.full{grid-column:1 / -1;}
  label{font-size:13px;font-weight:600;color:var(--ink-soft);}
  input[type=text],input[type=date]{
    font-family:'Inter',sans-serif;
    font-size:15px;
    padding:10px 12px;
    border:1px solid var(--line);
    border-radius:3px;
    background:#fff;
    color:var(--ink);
  }
  input:focus{outline:2px solid var(--accent);outline-offset:1px;}

  .q-block{
    padding:24px 0;
    border-bottom:1px solid var(--line);
  }
  .q-block:last-child{border-bottom:none;}
  .q-num{
    font-family:'IBM Plex Mono',monospace;
    font-size:12px;color:var(--accent);
    margin-bottom:6px;
  }
  .q-text{font-size:16px;font-weight:500;margin:0 0 16px;max-width:58ch;}
  .scale{display:flex;gap:8px;flex-wrap:wrap;}
  .opt{
    flex:1;min-width:88px;
    position:relative;
  }
  .opt input{position:absolute;opacity:0;width:100%;height:100%;cursor:pointer;margin:0;}
  .opt span{
    display:block;
    text-align:center;
    padding:10px 4px 8px;
    border:1px solid var(--line);
    border-radius:3px;
    font-size:12px;
    color:var(--ink-soft);
    line-height:1.3;
  }
  .opt span b{display:block;font-family:'Fraunces',serif;font-size:18px;font-weight:600;color:var(--ink);margin-bottom:2px;}
  .opt input:checked + span{
    border-color:var(--accent);
    background:var(--accent-soft);
    color:var(--ink);
  }
  .opt input:checked + span b{color:var(--accent);}
  .opt input:focus-visible + span{outline:2px solid var(--accent);outline-offset:2px;}

  .progress-bar{
    position:fixed;top:0;left:0;height:3px;background:var(--accent);
    width:0%;transition:width .2s ease;z-index:10;
  }
  .sticky-status{
    position:fixed;bottom:0;left:0;right:0;
    background:var(--paper);border-top:1px solid var(--line);
    padding:14px 24px;
    display:flex;justify-content:center;align-items:center;gap:20px;
    z-index:9;
  }
  .status-inner{max-width:760px;width:100%;display:flex;justify-content:space-between;align-items:center;gap:16px;}
  .status-text{font-size:13px;color:var(--ink-soft);font-family:'IBM Plex Mono',monospace;}
  button.submit{
    font-family:'Inter',sans-serif;
    font-weight:600;font-size:15px;
    padding:12px 26px;
    background:var(--ink);color:#fff;
    border:none;border-radius:3px;
    cursor:pointer;
  }
  button.submit:disabled{background:#B7BCC6;cursor:not-allowed;}
  button.submit:not(:disabled):hover{background:var(--accent);}

  .notice{
    display:flex;gap:10px;align-items:flex-start;
    background:var(--warn-soft);
    border:1px solid #E9C3AE;
    color:var(--warn);
    padding:12px 14px;border-radius:3px;
    font-size:13px;margin-top:16px;
  }

  .done-screen{text-align:center;padding:80px 24px;}
  .done-screen .mark{
    width:56px;height:56px;border-radius:50%;
    background:var(--accent);color:#fff;
    display:flex;align-items:center;justify-content:center;
    margin:0 auto 24px;font-size:26px;
  }
  .done-screen h2{font-family:'Fraunces',serif;font-size:28px;margin:0 0 10px;}
  .done-screen p{color:var(--ink-soft);max-width:46ch;margin:0 auto 28px;}
  .filename{
    font-family:'IBM Plex Mono',monospace;font-size:13px;
    background:var(--paper);border:1px solid var(--line);
    padding:10px 16px;border-radius:3px;display:inline-block;
  }

  @media (max-width:600px){
    .field-grid{grid-template-columns:1fr;}
    h1{font-size:30px;}
    .pentagon{display:none;}
  }
</style>
</head>
<body>

<div class="progress-bar" id="progressBar"></div>

<header class="top" style="position:relative;">
  <div class="eyebrow">Questionario · 50 domande</div>
  <h1>Test Attività Sportive</h1>
  <p class="sub">Rispondi con la prima reazione che ti viene in mente. Non ci sono risposte giuste o sbagliate: il questionario esplora le tue preferenze rispetto allo sport.</p>
  <svg class="pentagon" viewBox="0 0 64 64" fill="none">
    <polygon points="32,4 60,25 49,58 15,58 4,25" stroke="#2F8F6B" stroke-width="1.6"/>
    <polygon points="32,16 49,28 43,48 21,48 15,28" stroke="#2F8F6B" stroke-width="1" opacity=".5"/>
  </svg>
</header>

<div class="wrap">

  <form id="testForm">

    <section class="card" id="personalCard">
      <div class="eyebrow">Dati anagrafici</div>
      <div class="field-grid">
        <div class="field"><label for="nome">Nome</label><input type="text" id="nome" required></div>
        <div class="field"><label for="cognome">Cognome</label><input type="text" id="cognome" required></div>
        <div class="field"><label for="dataNascita">Data di nascita</label><input type="date" id="dataNascita" required></div>
        <div class="field"><label for="azienda">Azienda</label><input type="text" id="azienda"></div>
        <div class="field full"><label for="residenza">Residenza</label><input type="text" id="residenza"></div>
      </div>
    </section>

    <section class="card" id="questionsCard">
      <div class="eyebrow" style="margin-bottom:20px;">Domande</div>
      <div id="questionsHost"></div>
    </section>

  </form>

  <div id="doneScreen" class="done-screen card" style="display:none;">
    <div class="mark">✓</div>
    <h2>File generato</h2>
    <p>Il file con le tue risposte è stato scaricato. Invialo alla persona che deve elaborare i risultati (email, gestionale, PEC…). Nessun punteggio viene calcolato o mostrato qui.</p>
    <div class="filename" id="filenameShown"></div>
  </div>

</div>

<div class="sticky-status" id="stickyStatus">
  <div class="status-inner">
    <div class="status-text" id="statusText">0 / 50 risposte</div>
    <button type="button" class="submit" id="submitBtn" disabled>Genera file risposte</button>
  </div>
</div>

<script>
// Domande nell'ordine del foglio "Risposte e Calcolo" — numero, dimensione, testo
const QUESTIONS = [
[50,"PS","Amo gli sport che combinano abilità fisiche e mentali in modi unici."],
[31,"DS","Amo sperimentare attività sportive insolite o innovative."],
[4,"AF","Cerco sport che mi aiutino a gestire l'ansia o lo stress."],
[5,"AF","Evito attività in cui sento troppa pressione sociale."],
[36,"DS","Evito attività sportive con troppe regole o limiti rigidi."],
[30,"AN","Evito sport che non mi permettono di misurarmi direttamente con gli altri."],
[17,"DI","Evito sport che richiedono un alto grado di interazione sociale."],
[10,"AF","Evito sport con regole complesse o situazioni caotiche."],
[23,"AN","Mi arrabbio facilmente quando perdo in una competizione."],
[6,"AF","Mi capita di rimuginare sugli errori durante una competizione."],
[26,"AN","Mi motiva l'idea di superare gli altri nelle prestazioni sportive."],
[42,"PS","Mi piacciono le attività sportive che stimolano il pensiero non convenzionale."],
[14,"DI","Mi piace condividere i miei risultati sportivi con gli altri."],
[22,"AN","Mi piace dimostrare le mie capacità in uno sport competitivo."],
[46,"PS","Mi piace esplorare discipline sportive fuori dall'ordinario."],
[34,"DS","Mi piace improvvisare durante l'allenamento o la gara."],
[38,"DS","Mi piace provare sport non convenzionali o estremi."],
[32,"DS","Mi piace seguire il mio istinto durante una competizione."],
[28,"AN","Mi piace sfidare gli altri in sport di resistenza o di forza."],
[9,"AF","Mi preoccupa deludere gli altri quando pratico sport."],
[1,"AF","Mi preoccupo molto degli esiti di una gara o di un allenamento."],
[13,"DI","Mi sento a disagio in attività di gruppo o di squadra."],
[45,"PS","Mi sento attratto da sport estremi o poco comuni."],
[19,"DI","Mi sento energizzato quando pratico sport con amici."],
[24,"AN","Mi sento gratificato solo se ottengo il primo posto."],
[16,"DI","Mi sento motivato dal supporto di una squadra o di un gruppo."],
[40,"DS","Mi sento più a mio agio in sport che incoraggiano la creatività."],
[48,"PS","Mi sento più motivato quando pratico sport con una componente mentale sfidante."],
[3,"AF","Mi sento spesso sopraffatto dall'idea di competere."],
[8,"AF","Mi sento teso prima di iniziare una gara o una nuova attività sportiva."],
[49,"PS","Preferisco attività che richiedono fantasia e pensiero divergente."],
[11,"DI","Preferisco praticare sport che mi permettano di stare da solo."],
[35,"DS","Preferisco sport che mi lasciano molta libertà di movimento."],
[43,"PS","Preferisco sport che mi permettano di esprimere il mio lato artistico."],
[25,"AN","Preferisco sport che premiano la competizione diretta con gli avversari."],
[29,"AN","Preferisco sport con un chiaro vincitore e perdente."],
[20,"DI","Preferisco sport individuali in cui posso concentrarmi su me stesso."],
[2,"AF","Tendo a evitare situazioni sportive che percepisco come stressanti."],
[41,"PS","Trovo affascinanti gli sport che richiedono creatività e immaginazione."],
[18,"DI","Trovo difficile collaborare con altri durante l'attività fisica."],
[7,"AF","Trovo difficile rilassarmi durante allenamenti intensi."],
[15,"DI","Trovo gratificante praticare sport senza la presenza di spettatori."],
[47,"PS","Trovo interessante combinare sport tradizionali con elementi creativi."],
[21,"AN","Trovo motivante competere contro gli altri per vincere."],
[33,"DS","Trovo noiose le attività sportive altamente strutturate."],
[39,"DS","Trovo noiose le ripetizioni di esercizi standard."],
[27,"AN","Trovo noiosi gli sport che non includono una componente competitiva."],
[37,"DS","Trovo stimolante esplorare nuovi modi di praticare sport."],
[12,"DI","Trovo stimolante fare sport in un ambiente sociale."],
[44,"PS","Trovo stimolante praticare sport con un alto livello di innovazione."]
];

const SCALE_LABELS = ["Per niente\nd'accordo","Poco\nd'accordo","Neutro","Abbastanza\nd'accordo","Completamente\nd'accordo"];

const host = document.getElementById('questionsHost');
QUESTIONS.forEach((q, idx) => {
  const [numero, dim, testo] = q;
  const block = document.createElement('div');
  block.className = 'q-block';
  block.innerHTML = `
    <div class="q-num">Domanda ${idx+1} / ${QUESTIONS.length}</div>
    <p class="q-text">${testo}</p>
    <div class="scale">
      ${[1,2,3,4,5].map(v => `
        <label class="opt">
          <input type="radio" name="q${numero}" value="${v}" data-numero="${numero}" data-dim="${dim}">
          <span><b>${v}</b>${SCALE_LABELS[v-1]}</span>
        </label>
      `).join('')}
    </div>
  `;
  host.appendChild(block);
});

const form = document.getElementById('testForm');
const statusText = document.getElementById('statusText');
const submitBtn = document.getElementById('submitBtn');
const progressBar = document.getElementById('progressBar');

function countAnswered(){
  return QUESTIONS.filter(([numero]) => form.querySelector(`input[name="q${numero}"]:checked`)).length;
}

function refreshStatus(){
  const answered = countAnswered();
  statusText.textContent = `${answered} / ${QUESTIONS.length} risposte`;
  progressBar.style.width = (answered / QUESTIONS.length * 100) + '%';
  const personalOk = document.getElementById('nome').value.trim() &&
                      document.getElementById('cognome').value.trim() &&
                      document.getElementById('dataNascita').value;
  submitBtn.disabled = !(answered === QUESTIONS.length && personalOk);
}

form.addEventListener('change', refreshStatus);
form.addEventListener('input', refreshStatus);
refreshStatus();

function computeChecksum(risposte){
  // controllo di integrità di base (non crittografico): rileva file corrotti o modificati a mano
  let sum = 0;
  risposte.forEach(r => { sum += r.numero * r.risposta; });
  return (sum % 100000);
}

submitBtn.addEventListener('click', () => {
  if (submitBtn.disabled) return;

  const risposte = QUESTIONS.map(([numero, dim, testo]) => {
    const checked = form.querySelector(`input[name="q${numero}"]:checked`);
    return { numero, dimensione: dim, risposta: parseInt(checked.value, 10) };
  });

  const datiPersonali = {
    nome: document.getElementById('nome').value.trim(),
    cognome: document.getElementById('cognome').value.trim(),
    dataNascita: document.getElementById('dataNascita').value,
    azienda: document.getElementById('azienda').value.trim(),
    residenza: document.getElementById('residenza').value.trim()
  };

  const payload = {
    tipo: "risposte_test_attivita_sportive",
    versione: 1,
    generato: new Date().toISOString(),
    datiPersonali,
    risposte,
    checksum: computeChecksum(risposte)
  };

  const json = JSON.stringify(payload, null, 2);
  const blob = new Blob([json], { type: 'application/json' });
  const url = URL.createObjectURL(blob);

  const safe = (s) => (s || 'utente').replace(/[^a-zA-Z0-9]+/g, '_');
  const filename = `Risposte_${safe(datiPersonali.cognome)}_${safe(datiPersonali.nome)}.json`;

  const a = document.createElement('a');
  a.href = url;
  a.download = filename;
  document.body.appendChild(a);
  a.click();
  document.body.removeChild(a);
  URL.revokeObjectURL(url);

  document.getElementById('testForm').style.display = 'none';
  document.getElementById('stickyStatus').style.display = 'none';
  progressBar.style.width = '100%';
  document.getElementById('doneScreen').style.display = 'block';
  document.getElementById('filenameShown').textContent = filename;
  window.scrollTo({top:0, behavior:'smooth'});
});
</script>

</body>
</html>
