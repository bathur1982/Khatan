<!DOCTYPE html>
<html lang="ms">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Khatan Perdana 2026 - Countdown Live</title>
<style>
  *{margin:0;padding:0;box-sizing:border-box;font-family:Arial, sans-serif}
  body{height:100vh;overflow:hidden;background:#000}
  .poster{
    position:relative;width:100vw;height:100vh;
    background:#041a3a url('khatan.jpg') center center / contain no-repeat;
    display:flex;align-items:flex-end;justify-content:center;
  }
  .overlay{
    position:relative;z-index:2;width:100%;
    padding:0 3vw 2.5vh;text-align:center;
    background:linear-gradient(to top, rgba(0,8,25,0.95) 0%, rgba(0,8,25,0.75) 60%, transparent 100%);
  }
  .top{color:#f5c86b;font-size:2vw;font-weight:900;letter-spacing:2px;text-shadow:0 2px 10px #000}
  .top span{color:#fff;font-size:1.3vw;font-weight:400;letter-spacing:1px}
  .countdown{display:flex;justify-content:center;gap:1.5vw;margin:1.5vh 0}
  .box{
    background:rgba(6,42,85,0.95);border:3px solid #f5c86b;
    width:12vw;height:12vw;max-width:185px;max-height:185px;min-width:110px;min-height:110px;
    border-radius:16px;display:flex;flex-direction:column;align-items:center;justify-content:center;
    box-shadow:0 10px 25px rgba(0,0,0,0.6);
  }
  .box span{font-size:4vw;font-weight:900;color:#f5c86b;line-height:1}
  .box small{font-size:1.1vw;letter-spacing:3px;color:#fff;margin-top:6px}
  .info{display:inline-block;background:#f5c86b;color:#041a3a;padding:0.8vh 2.5vw;border-radius:50px;font-size:1.4vw;font-weight:bold}
  .contact{margin-top:1vh;color:#fff;font-size:1.3vw;text-shadow:0 2px 8px #000}
  .contact b{color:#f5c86b}
</style>
</head>
<body>
<div class="poster">
  <div class="overlay">
    <div class="top">COUNTDOWN KE ACARA<br><span>KHATAN PERDANA 2026 &nbsp;|&nbsp; 6 DIS 2026 (AHAD) &nbsp;|&nbsp; MASJID AL MUHAJIRIN</span></div>
    <div class="countdown">
      <div class="box"><span id="hari">00</span><small>HARI</small></div>
      <div class="box"><span id="jam">00</span><small>JAM</small></div>
      <div class="box"><span id="minit">00</span><small>MINIT</small></div>
      <div class="box"><span id="saat">00</span><small>SAAT</small></div>
    </div>
    <div class="info">YURAN RM50.00 &nbsp;•&nbsp; TERHAD 30 ORANG SAHAJA</div>
    <div class="contact">Sebarang pertanyaan : <b>Shahabudin 017 575 8950</b></div>
  </div>
</div>
<script>
  const target = new Date("2026-12-06T08:00:00+08:00").getTime();
  function update(){
    const now = new Date().getTime();
    let diff = target - now; if(diff<0) diff=0;
    const h=Math.floor(diff/(1000*60*60*24));
    const j=Math.floor((diff%(1000*60*60*24))/(1000*60*60));
    const m=Math.floor((diff%(1000*60*60))/(1000*60));
    const s=Math.floor((diff%(1000*60))/1000);
    document.getElementById("hari").textContent=String(h).padStart(2,"0");
    document.getElementById("jam").textContent=String(j).padStart(2,"0");
    document.getElementById("minit").textContent=String(m).padStart(2,"0");
    document.getElementById("saat").textContent=String(s).padStart(2,"0");
  }
  update(); setInterval(update,1000);
</script>
</body>
</html>