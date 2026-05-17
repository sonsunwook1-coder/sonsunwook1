[kidsnote-observation-integrated.html](https://github.com/user-attachments/files/27898100/kidsnote-observation-integrated.html)
# sonsunwook1<!DOCTYPE html>
<html lang="ko">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width,initial-scale=1,viewport-fit=cover">
<title>키즈노트 + 관찰노트 통합판</title>
<style>
:root{--bg:#f4f7fb;--card:#fff;--line:#dbe5f3;--text:#1f2a44;--muted:#6f7c96;--pri:#3b82f6;--pri2:#6366f1;--soft:#f8fbff;--ok:#16a34a;--warn:#d97706}
*{box-sizing:border-box;-webkit-tap-highlight-color:transparent}
html,body{margin:0;padding:0;background:var(--bg);color:var(--text);font-family:-apple-system,BlinkMacSystemFont,'Apple SD Gothic Neo','Malgun Gothic',sans-serif}
body{padding-bottom:110px}
button,input,select,textarea{font:inherit}
button{cursor:pointer}
.wrap{max-width:820px;margin:0 auto;padding:14px}
.header{position:sticky;top:0;z-index:20;background:rgba(244,247,251,.96);backdrop-filter:blur(10px);border-bottom:1px solid var(--line)}
.header-in{max-width:820px;margin:0 auto;padding:12px 14px;display:flex;align-items:center;gap:10px}
.logo{width:42px;height:42px;border-radius:14px;background:linear-gradient(135deg,var(--pri),var(--pri2));color:#fff;display:grid;place-items:center;font-weight:900}
.title{flex:1}.title h1{margin:0;font-size:17px}.title p{margin:3px 0 0;font-size:12px;color:var(--muted)}
.badge{font-size:11px;font-weight:800;padding:6px 10px;border-radius:999px;border:1px solid #bfdbfe;background:#eff6ff;color:#1d4ed8}
.card{background:var(--card);border:1px solid var(--line);border-radius:18px;padding:16px;margin-bottom:12px;box-shadow:0 3px 14px rgba(30,50,90,.05)}
.row{display:grid;grid-template-columns:1fr 1fr;gap:10px}.row3{display:grid;grid-template-columns:repeat(3,1fr);gap:10px}.row4{display:grid;grid-template-columns:repeat(4,1fr);gap:10px}
@media (max-width:640px){.row,.row3,.row4{grid-template-columns:1fr}}
.label{display:block;margin:0 0 6px;font-size:12px;font-weight:800;color:var(--muted)}
input,select,textarea{width:100%;border:1.5px solid var(--line);background:var(--soft);color:var(--text);padding:12px 13px;border-radius:13px;outline:none}
textarea{min-height:92px;resize:vertical;line-height:1.65}
input:focus,select:focus,textarea:focus{border-color:var(--pri);background:#fff;box-shadow:0 0 0 3px rgba(59,130,246,.12)}
.tabs{display:grid;grid-template-columns:repeat(4,1fr);gap:4px;background:#e8eefb;padding:4px;border-radius:16px;margin-bottom:12px}
.tab{min-height:44px;border:0;border-radius:12px;background:transparent;color:var(--muted);font-weight:900}.tab.active{background:#fff;color:#1d4ed8;box-shadow:0 2px 6px rgba(0,0,0,.06)}
@media (max-width:640px){.tabs{grid-template-columns:repeat(2,1fr)}}
.h{display:flex;align-items:center;gap:10px;margin-bottom:12px}.ico{width:32px;height:32px;border-radius:10px;background:#eef5ff;display:grid;place-items:center}.h h2{margin:0;font-size:15px}.h p{margin:2px 0 0;font-size:12px;color:var(--muted)}
.add-row{display:flex;gap:8px}.add-row input{flex:1}
.btn,.btn-sm{border:0;border-radius:14px;font-weight:900}.btn{min-height:50px}.btn-sm{min-height:42px;padding:0 14px;white-space:nowrap}
.btn-primary{background:linear-gradient(135deg,var(--pri),var(--pri2));color:#fff}.btn-secondary{background:#fff;border:1.5px solid var(--line);color:var(--text)}.btn-ghost{background:#eff6ff;color:#1d4ed8}
.child-list{display:grid;gap:8px}.child{display:flex;align-items:center;gap:10px;padding:12px;border:1.5px solid var(--line);border-radius:14px;background:var(--soft)}.child.active{border-color:var(--pri);background:#eef5ff}.av{width:36px;height:36px;border-radius:50%;display:grid;place-items:center;background:linear-gradient(135deg,var(--pri),var(--pri2));color:#fff;font-weight:900;flex:none}.child-main{flex:1;min-width:0}.child-name{font-weight:900}.child-sub{font-size:12px;color:var(--muted);margin-top:2px;white-space:nowrap;overflow:hidden;text-overflow:ellipsis}.del{width:32px;height:32px;border:0;border-radius:50%;background:transparent;color:#94a3b8}
.chips,.pills{display:flex;flex-wrap:wrap;gap:8px}.chip,.pill{border:1.5px solid var(--line);background:#f8fbff;border-radius:999px;padding:10px 12px;font-size:13px;font-weight:800;min-height:42px;touch-action:manipulation;user-select:none}.chip.on,.pill.on{background:#eff6ff;border-color:var(--pri);color:#1d4ed8}
.progress-top{display:flex;justify-content:space-between;font-size:12px;font-weight:800;color:var(--muted);margin-bottom:6px}.bar{height:6px;background:#dbe5f6;border-radius:999px;overflow:hidden}.fill{height:100%;background:linear-gradient(90deg,var(--pri),var(--pri2));width:0}
.note-list{display:grid;gap:10px}.item{border:1.5px solid var(--line);border-radius:14px;background:#fff;overflow:hidden}.item-h{padding:12px 14px;background:var(--soft);display:flex;justify-content:space-between;align-items:center;font-weight:900}.item-b{display:none;padding:14px}.item-b.open{display:block}.text{white-space:pre-wrap;line-height:1.75;font-size:14px}
.bottom{position:fixed;left:0;right:0;bottom:0;z-index:25;padding:10px 14px calc(10px + env(safe-area-inset-bottom));background:linear-gradient(to bottom,rgba(244,247,251,0),rgba(244,247,251,.98) 24%)}.bottom-in{max-width:820px;margin:0 auto;display:grid;grid-template-columns:1fr 1fr;gap:10px}
.toast{position:fixed;left:50%;bottom:92px;transform:translateX(-50%) translateY(8px);opacity:0;pointer-events:none;background:#111827;color:#fff;padding:10px 16px;border-radius:999px;font-size:13px;font-weight:800;transition:.2s;z-index:99;max-width:90vw;text-align:center}.toast.on{opacity:1;transform:translateX(-50%) translateY(0)}
.empty{text-align:center;padding:28px 8px;color:#94a3b8}.empty .big{font-size:36px;margin-bottom:8px}.hide{display:none !important}
.helper{font-size:12px;color:var(--muted);margin-top:8px}.split{display:grid;grid-template-columns:1fr 1fr;gap:12px}@media (max-width:640px){.split{grid-template-columns:1fr}}
</style>
</head>
<body>
<div class="header"><div class="header-in"><div class="logo">K+</div><div class="title"><h1>키즈노트 + 관찰노트 통합판</h1><p>알림장과 관찰기록을 같은 원아 데이터로 함께 작성합니다</p></div><div class="badge">통합</div></div></div>
<div class="wrap">
  <div class="tabs">
    <button class="tab active" type="button" data-tab="manage">원아/공통</button>
    <button class="tab" type="button" data-tab="kids">키즈노트</button>
    <button class="tab" type="button" data-tab="obs">관찰노트</button>
    <button class="tab" type="button" data-tab="preview">미리보기</button>
  </div>

  <div id="pane-manage">
    <div class="card">
      <div class="h"><div class="ico">👨‍👩‍👧</div><div><h2>원아 목록</h2><p>원아를 한 번 추가하면 키즈노트와 관찰노트에 함께 연동됩니다</p></div></div>
      <div class="child-list" id="childList"></div>
      <div class="add-row"><input id="childNameInput" placeholder="예: 민준, 서연, 하은"><button class="btn-sm btn-primary" type="button" id="addChildBtn">+ 추가</button></div>
      <div class="helper">쉼표로 여러 명을 한 번에 추가할 수 있어요.</div>
    </div>

    <div class="card">
      <div class="h"><div class="ico">📅</div><div><h2>공통 정보</h2><p>오늘 날짜와 반 전체 공통 활동을 입력하세요</p></div></div>
      <div class="row3">
        <div><label class="label">날짜</label><input id="date" type="date"></div>
        <div><label class="label">날씨</label><select id="weather"><option value="">선택 안 함</option><option>맑은</option><option>흐린</option><option>비가 오는</option><option>눈이 오는</option><option>바람이 부는</option></select></div>
        <div><label class="label">관찰 시간대</label><select id="obsTimeBand"><option value="오전">오전</option><option value="점심 전후">점심 전후</option><option value="오후">오후</option><option value="하루 전반">하루 전반</option></select></div>
      </div>
      <div style="height:12px"></div>
      <label class="label">공통 활동</label>
      <div class="chips" id="commonChips">
        <button class="chip" type="button" data-common="미술 활동">🎨 미술</button>
        <button class="chip" type="button" data-common="블록·쌓기 놀이">🧱 블록</button>
        <button class="chip" type="button" data-common="바깥 놀이">🌿 바깥놀이</button>
        <button class="chip" type="button" data-common="음악·율동 활동">🎵 음악/율동</button>
        <button class="chip" type="button" data-common="책 읽기">📚 독서</button>
        <button class="chip" type="button" data-common="역할 놀이">🎭 역할놀이</button>
      </div>
      <div style="height:12px"></div>
      <div class="row">
        <div><label class="label">공통 특이사항</label><input id="commonMemo" placeholder="예: 바깥놀이 후 손씻기 지도가 있었어요"></div>
        <div><label class="label">공통 가정 연계</label><input id="commonHome" placeholder="예: 오늘 놀이 이야기를 집에서도 나눠보세요"></div>
      </div>
    </div>
  </div>

  <div id="pane-kids" class="hide">
    <div class="card">
      <div class="progress-top"><span id="kidsProgressText">0 / 0명 완료</span><span id="kidsProgressPct">0%</span></div>
      <div class="bar"><div class="fill" id="kidsProgressFill"></div></div>
    </div>
    <div id="kidsEmpty" class="empty"><div class="big">👶</div><p>먼저 원아를 추가하고 선택해 주세요</p></div>
    <div id="kidsWrap" class="hide">
      <div class="card">
        <div class="h"><div class="ico">✏️</div><div><h2>키즈노트 작성</h2><p>현재 선택 원아: <span id="activeChildKids"></span></p></div></div>
        <div class="row4">
          <div><label class="label">기분</label><select id="kMood"><option value="">선택</option><option>밝고 활기차게</option><option>차분하고 안정적으로</option><option>조금 피곤한 듯</option><option>다소 예민하게</option></select></div>
          <div><label class="label">식사</label><select id="kMeal"><option value="">선택</option><option>식사를 전반적으로 잘 했어요</option><option>식사를 보통으로 했어요</option><option>식사를 조금 했어요</option><option>식사를 거의 하지 않았어요</option></select></div>
          <div><label class="label">낮잠</label><select id="kSleep"><option value="">선택</option><option>낮잠을 편안하게 잘 잤어요</option><option>낮잠을 조금 잤어요</option><option>자다 깨다를 반복했어요</option><option>낮잠을 자지 않았어요</option></select></div>
          <div><label class="label">사회성</label><select id="kSocial"><option value="">선택</option><option>친구들과 즐겁게 어울렸어요</option><option>차분하게 자신의 놀이에 집중했어요</option><option>친구와 협력하는 모습이 있었어요</option><option>교사의 도움을 받아 상호작용했어요</option></select></div>
        </div>
        <div style="height:12px"></div>
        <div class="row">
          <div><label class="label">건강 메모</label><input id="kHealth" placeholder="예: 콧물이 조금 있었어요"></div>
          <div><label class="label">개별 가정 연계</label><input id="kHome" placeholder="예: 오늘 놀이 이야기를 나눠보세요"></div>
        </div>
        <div style="height:12px"></div>
        <label class="label">오늘의 하이라이트</label>
        <textarea id="kHighlight" placeholder="예: 친구와 블록 기차를 함께 만들며 역할을 나누는 모습이 인상적이었어요."></textarea>
        <div style="height:12px"></div>
        <div class="row"><button class="btn btn-ghost" type="button" id="saveKidsBtn">💾 키즈노트 저장</button><button class="btn btn-primary" type="button" id="goObsBtn">🔗 관찰노트로 이어서 작성</button></div>
      </div>
    </div>
  </div>

  <div id="pane-obs" class="hide">
    <div class="card">
      <div class="progress-top"><span id="obsProgressText">0 / 0명 완료</span><span id="obsProgressPct">0%</span></div>
      <div class="bar"><div class="fill" id="obsProgressFill"></div></div>
    </div>
    <div id="obsEmpty" class="empty"><div class="big">🔎</div><p>먼저 원아를 추가하고 선택해 주세요</p></div>
    <div id="obsWrap" class="hide">
      <div class="card">
        <div class="h"><div class="ico">📝</div><div><h2>관찰노트 작성</h2><p>현재 선택 원아: <span id="activeChildObs"></span></p></div></div>
        <div class="split">
          <div><label class="label">관찰 유형</label><select id="oType"><option>일상생활</option><option>실내놀이</option><option>실외놀이</option></select></div>
          <div><label class="label">연계 영역</label><select id="oArea"><option>사회관계</option><option>의사소통</option><option>신체운동·건강</option><option>예술경험</option><option>자연탐구</option></select></div>
        </div>
        <div style="height:12px"></div>
        <div class="row">
          <div><label class="label">관찰 상황</label><select id="oSituation"><option>자유놀이 중</option><option>활동 참여 중</option><option>식사 시간</option><option>낮잠 전후</option><option>등·하원 전후</option><option>친구와 상호작용 중</option></select></div>
          <div><label class="label">관찰 시간</label><input id="oTime" placeholder="예: 오전 10:20"></div>
        </div>
        <div style="height:12px"></div>
        <label class="label">관찰 사실</label>
        <textarea id="oFact" placeholder="보인 행동과 말, 표정, 상호작용을 객관적으로 적어 주세요."></textarea>
        <div class="row" style="margin-top:10px"><button class="btn btn-secondary" type="button" id="importHighlightBtn">⬇ 키즈노트 하이라이트 가져오기</button><button class="btn btn-secondary" type="button" id="fillObsGuideBtn">🪄 기본 문장 틀 넣기</button></div>
        <div style="height:12px"></div>
        <label class="label">해석 / 평가</label>
        <textarea id="oInterpret" placeholder="관찰 사실이 의미하는 발달 특성이나 현재의 흥미를 간결하게 적어 주세요."></textarea>
        <div style="height:12px"></div>
        <label class="label">교사 지원</label>
        <textarea id="oSupport" placeholder="교사가 제공한 말, 자료, 환경, 도움을 기록하세요."></textarea>
        <div style="height:12px"></div>
        <label class="label">다음 계획</label>
        <textarea id="oPlan" placeholder="다음 놀이 확장, 환경 구성, 상호작용 계획을 적어 주세요."></textarea>
        <div style="height:12px"></div>
        <div class="row"><button class="btn btn-ghost" type="button" id="saveObsBtn">💾 관찰노트 저장</button><button class="btn btn-primary" type="button" id="previewBtn">👁 결과 보기</button></div>
      </div>
    </div>
  </div>

  <div id="pane-preview" class="hide">
    <div class="card">
      <div class="h"><div class="ico">📋</div><div><h2>원아별 결과</h2><p>키즈노트와 관찰노트를 함께 확인하고 복사할 수 있어요</p></div></div>
      <div class="note-list" id="previewList"></div>
    </div>
  </div>
</div>

<div class="bottom"><div class="bottom-in"><button class="btn btn-primary" type="button" id="copyAllBtn">📋 전체 복사</button><button class="btn btn-secondary" type="button" id="resetBtn">🔄 전체 초기화</button></div></div>
<div class="toast" id="toast"></div>

<script>
(function(){
'use strict';
var state = {children:[], current:-1, commonActs:[]};
function $(id){return document.getElementById(id)}
function qa(sel,root){return Array.prototype.slice.call((root||document).querySelectorAll(sel))}
function esc(s){return String(s||'').replace(/&/g,'&amp;').replace(/</g,'&lt;').replace(/>/g,'&gt;')}
function blankKids(){return {mood:'',meal:'',sleep:'',social:'',health:'',highlight:'',home:'',done:false}}
function blankObs(){return {type:'일상생활',area:'사회관계',situation:'자유놀이 중',time:'',fact:'',interpret:'',support:'',plan:'',done:false}}
var toastTimer=null;
function toast(msg){var t=$('toast');t.textContent=msg;t.classList.add('on');clearTimeout(toastTimer);toastTimer=setTimeout(function(){t.classList.remove('on')},2000)}
function today(){var d=new Date(),m=String(d.getMonth()+1).padStart(2,'0'),dd=String(d.getDate()).padStart(2,'0');$('date').value=d.getFullYear()+'-'+m+'-'+dd}
function currentChild(){return state.children[state.current]||null}
function addChildren(){var raw=$('childNameInput').value.trim();if(!raw){toast('원아 이름을 입력해 주세요');return}var names=raw.split(',').map(function(v){return v.trim()}).filter(Boolean), added=0;names.forEach(function(name){if(!state.children.some(function(c){return c.name===name})){state.children.push({id:Date.now()+Math.random(),name:name,kids:blankKids(),obs:blankObs()});added++}});$('childNameInput').value='';renderChildren();updateProgress();if(added){selectChild(state.children.length-added);toast('원아 '+added+'명 추가')}else{toast('같은 이름이 이미 있어요')}}
function renderChildren(){var box=$('childList');if(!state.children.length){box.innerHTML='<div class="empty"><div class="big">👶</div><p>원아를 추가해 주세요</p></div>';toggleForms();return}box.innerHTML=state.children.map(function(c,i){var ks=c.kids.done?'알림장 완료':'알림장 대기';var os=c.obs.done?'관찰 완료':'관찰 대기';return '<div class="child'+(i===state.current?' active':'')+'" data-child="'+i+'"><div class="av">'+esc(c.name.charAt(0))+'</div><div class="child-main"><div class="child-name">'+esc(c.name)+'</div><div class="child-sub">'+ks+' · '+os+'</div></div><button class="del" type="button" data-del="'+i+'">✕</button></div>'}).join('');toggleForms()}
function toggleForms(){var has=currentChild();$('kidsWrap').classList.toggle('hide',!has);$('kidsEmpty').classList.toggle('hide',!!has);$('obsWrap').classList.toggle('hide',!has);$('obsEmpty').classList.toggle('hide',!!has)}
function selectChild(i){if(i<0||i>=state.children.length)return;saveKids(false);saveObs(false);state.current=i;renderChildren();loadKids();loadObs();updateProgress()}
function deleteChild(i){if(!state.children[i])return;if(!confirm(state.children[i].name+' 원아를 삭제할까요?'))return;state.children.splice(i,1);if(!state.children.length) state.current=-1; else if(state.current>=state.children.length) state.current=state.children.length-1;renderChildren();if(state.current>=0){loadKids();loadObs()}updateProgress();toast('삭제했어요')}
function loadKids(){var c=currentChild();if(!c)return;$('activeChildKids').textContent=c.name;$('kMood').value=c.kids.mood;$('kMeal').value=c.kids.meal;$('kSleep').value=c.kids.sleep;$('kSocial').value=c.kids.social;$('kHealth').value=c.kids.health;$('kHighlight').value=c.kids.highlight;$('kHome').value=c.kids.home}
function saveKids(show){var c=currentChild();if(!c)return false;c.kids.mood=$('kMood').value;c.kids.meal=$('kMeal').value;c.kids.sleep=$('kSleep').value;c.kids.social=$('kSocial').value;c.kids.health=$('kHealth').value.trim();c.kids.highlight=$('kHighlight').value.trim();c.kids.home=$('kHome').value.trim();c.kids.done=!!(c.kids.mood||c.kids.highlight||c.kids.meal||c.kids.sleep||c.kids.social);renderChildren();updateProgress();if(show)toast('키즈노트 저장 완료');return true}
function loadObs(){var c=currentChild();if(!c)return;$('activeChildObs').textContent=c.name;$('oType').value=c.obs.type;$('oArea').value=c.obs.area;$('oSituation').value=c.obs.situation;$('oTime').value=c.obs.time;$('oFact').value=c.obs.fact;$('oInterpret').value=c.obs.interpret;$('oSupport').value=c.obs.support;$('oPlan').value=c.obs.plan}
function saveObs(show){var c=currentChild();if(!c)return false;c.obs.type=$('oType').value;c.obs.area=$('oArea').value;c.obs.situation=$('oSituation').value;c.obs.time=$('oTime').value.trim();c.obs.fact=$('oFact').value.trim();c.obs.interpret=$('oInterpret').value.trim();c.obs.support=$('oSupport').value.trim();c.obs.plan=$('oPlan').value.trim();c.obs.done=!!(c.obs.fact||c.obs.interpret||c.obs.support||c.obs.plan);renderChildren();updateProgress();if(show)toast('관찰노트 저장 완료');return true}
function dateText(){var v=$('date').value;var d=v?new Date(v+'T00:00:00'):new Date();var days=['일','월','화','수','목','금','토'];return (d.getMonth()+1)+'월 '+d.getDate()+'일('+days[d.getDay()]+')'}
function buildKids(c){var k=c.kids, lines=[];lines.push('안녕하세요 😊 '+dateText()+( $('weather').value ? ' '+$('weather').value+' 날, ' : ', ')+c.name+' 어린이의 하루를 전해드려요.','');if(k.mood)lines.push('오늘 '+c.name+' 어린이는 '+k.mood+' 하루를 보냈어요.');if(k.meal)lines.push('🍽 '+k.meal);if(k.sleep)lines.push('💤 '+k.sleep);if(k.social)lines.push('🤝 '+k.social);if(k.health)lines.push('🏥 '+k.health);if(state.commonActs.length)lines.push('🎨 오늘은 '+state.commonActs.join(', ')+'에 참여했어요.');if($('commonMemo').value.trim())lines.push('📌 '+$('commonMemo').value.trim());if(k.highlight){lines.push('','✨ 오늘의 하이라이트',k.highlight)}var home=k.home||$('commonHome').value.trim();if(home){lines.push('','📌 가정 연계',home)}lines.push('','오늘도 '+c.name+' 어린이와 함께한 하루가 즐거웠습니다.');return lines.join('\n')}
function buildObs(c){var o=c.obs, lines=[];lines.push('[관찰 기본정보]');lines.push('원아명: '+c.name);lines.push('관찰일: '+dateText());lines.push('관찰유형: '+o.type);lines.push('연계영역: '+o.area);lines.push('관찰시간대: '+$('obsTimeBand').value+(o.time?(' / '+o.time):''));lines.push('관찰상황: '+o.situation);lines.push('');lines.push('[관찰 사실]');lines.push(o.fact||'');lines.push('');lines.push('[해석 / 평가]');lines.push(o.interpret||'');lines.push('');lines.push('[교사 지원]');lines.push(o.support||'');lines.push('');lines.push('[다음 계획]');lines.push(o.plan||'');return lines.join('\n')}
function updateProgress(){var total=state.children.length;var kd=state.children.filter(function(c){return c.kids.done}).length;var od=state.children.filter(function(c){return c.obs.done}).length;var kp=total?Math.round(kd/total*100):0;var op=total?Math.round(od/total*100):0;$('kidsProgressText').textContent=kd+' / '+total+'명 완료';$('kidsProgressPct').textContent=kp+'%';$('kidsProgressFill').style.width=kp+'%';$('obsProgressText').textContent=od+' / '+total+'명 완료';$('obsProgressPct').textContent=op+'%';$('obsProgressFill').style.width=op+'%'}
function switchTab(tab){qa('.tab').forEach(function(b){b.classList.toggle('active',b.getAttribute('data-tab')===tab)});$('pane-manage').classList.toggle('hide',tab!=='manage');$('pane-kids').classList.toggle('hide',tab!=='kids');$('pane-obs').classList.toggle('hide',tab!=='obs');$('pane-preview').classList.toggle('hide',tab!=='preview');if(tab==='preview') renderPreview()}
function renderPreview(){var box=$('previewList');if(!state.children.length){box.innerHTML='<div class="empty"><div class="big">📭</div><p>작성된 원아가 없어요</p></div>';return}box.innerHTML=state.children.map(function(c,i){var kids=esc(buildKids(c));var obs=esc(buildObs(c));return '<div class="item"><div class="item-h" data-open="'+i+'"><span>👶 '+esc(c.name)+'</span><span>▼</span></div><div class="item-b" id="body'+i+'"><div class="split"><div><div class="label">키즈노트</div><div class="text">'+kids+'</div><div style="height:10px"></div><button class="btn-sm btn-primary" type="button" data-copy-k="'+i+'">키즈노트 복사</button></div><div><div class="label">관찰노트</div><div class="text">'+obs+'</div><div style="height:10px"></div><button class="btn-sm btn-secondary" type="button" data-copy-o="'+i+'">관찰노트 복사</button></div></div></div></div>'}).join('')}
function copyText(text,msg){if(navigator.clipboard&&navigator.clipboard.writeText){navigator.clipboard.writeText(text).then(function(){toast(msg)}).catch(function(){fallbackCopy(text,msg)})}else{fallbackCopy(text,msg)}}
function fallbackCopy(text,msg){var ta=document.createElement('textarea');ta.value=text;ta.style.position='fixed';ta.style.left='-9999px';document.body.appendChild(ta);ta.focus();ta.select();ta.setSelectionRange(0,999999);try{document.execCommand('copy');toast(msg)}catch(e){toast('복사가 제한된 환경입니다')}document.body.removeChild(ta)}
function copyAll(){if(!state.children.length){toast('작성된 원아가 없어요');return}var out=state.children.map(function(c){return '[ '+c.name+' ]\n\n[키즈노트]\n'+buildKids(c)+'\n\n[관찰노트]\n'+buildObs(c)}).join('\n\n==============================\n\n');copyText(out,'전체 복사 완료')}
function resetAll(){if(!confirm('전체 내용을 초기화할까요?'))return;state.children=[];state.current=-1;state.commonActs=[];$('childNameInput').value='';today();$('weather').value='';$('obsTimeBand').value='오전';$('commonMemo').value='';$('commonHome').value='';qa('#commonChips .chip').forEach(function(b){b.classList.remove('on')});['kMood','kMeal','kSleep','kSocial','kHealth','kHighlight','kHome','oType','oArea','oSituation','oTime','oFact','oInterpret','oSupport','oPlan'].forEach(function(id){if($(id)) $(id).value='' });renderChildren();updateProgress();switchTab('manage');toast('초기화 완료')}
function importHighlight(){var c=currentChild();if(!c){toast('먼저 원아를 선택해 주세요');return}var text=c.kids.highlight||'';if(!text){toast('가져올 하이라이트가 없어요');return}$('oFact').value = text;toast('하이라이트를 관찰 사실로 가져왔어요')}
function fillObsGuide(){var c=currentChild();if(!c){toast('먼저 원아를 선택해 주세요');return}if(!$('oFact').value.trim()) $('oFact').value = c.name+' 어린이는 '+$('oSituation').value+' 친구 및 교사의 말에 반응하며 자신의 생각을 행동과 말로 표현하였다.';if(!$('oInterpret').value.trim()) $('oInterpret').value = c.name+' 어린이는 현재 활동에 대한 흥미를 보이며 또래와의 상호작용 속에서 자신의 의사를 표현하려는 모습을 보였다.';if(!$('oSupport').value.trim()) $('oSupport').value = '교사는 영아/유아의 시도에 언어적 반응을 제공하고, 필요한 자료를 가까이에 배치하여 놀이가 지속되도록 지원하였다.';if(!$('oPlan').value.trim()) $('oPlan').value = '다음에는 관련 자료를 확장하여 제시하고, 또래와 함께 시도할 수 있는 놀이 기회를 더 제공할 예정이다.';toast('기본 문장 틀을 넣었어요')}
function bind(){ $('addChildBtn').addEventListener('click',addChildren,false); $('childNameInput').addEventListener('keydown',function(e){if(e.key==='Enter'){e.preventDefault();addChildren()}},false); qa('.tab').forEach(function(b){b.addEventListener('click',function(){switchTab(b.getAttribute('data-tab'))},false)}); qa('#commonChips .chip').forEach(function(b){b.addEventListener('click',function(){var v=b.getAttribute('data-common'),idx=state.commonActs.indexOf(v);if(idx>=0){state.commonActs.splice(idx,1);b.classList.remove('on')}else{state.commonActs.push(v);b.classList.add('on')}},false)}); $('childList').addEventListener('click',function(e){var d=e.target.closest('[data-del]');if(d){deleteChild(parseInt(d.getAttribute('data-del'),10));return}var c=e.target.closest('[data-child]');if(c) selectChild(parseInt(c.getAttribute('data-child'),10))},false); $('saveKidsBtn').addEventListener('click',function(){saveKids(true)},false); $('goObsBtn').addEventListener('click',function(){saveKids(false);switchTab('obs')},false); $('saveObsBtn').addEventListener('click',function(){saveObs(true)},false); $('previewBtn').addEventListener('click',function(){saveKids(false);saveObs(false);switchTab('preview')},false); $('importHighlightBtn').addEventListener('click',importHighlight,false); $('fillObsGuideBtn').addEventListener('click',fillObsGuide,false); $('copyAllBtn').addEventListener('click',function(){saveKids(false);saveObs(false);copyAll()},false); $('resetBtn').addEventListener('click',resetAll,false); $('previewList').addEventListener('click',function(e){var op=e.target.closest('[data-open]'); if(op){var i=parseInt(op.getAttribute('data-open'),10); var body=$('body'+i); if(body) body.classList.toggle('open'); return} var ck=e.target.closest('[data-copy-k]'); if(ck){var i1=parseInt(ck.getAttribute('data-copy-k'),10); copyText(buildKids(state.children[i1]), state.children[i1].name+' 키즈노트 복사 완료'); return} var co=e.target.closest('[data-copy-o]'); if(co){var i2=parseInt(co.getAttribute('data-copy-o'),10); copyText(buildObs(state.children[i2]), state.children[i2].name+' 관찰노트 복사 완료'); } },false); }
function init(){today();$('oType').value='일상생활';$('oArea').value='사회관계';$('oSituation').value='자유놀이 중';bind();renderChildren();updateProgress()}
init();
})();
</script>
</body>
</html>
