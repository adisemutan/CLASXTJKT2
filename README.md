<!DOCTYPE html>
<html lang="id">
<head>
<meta charset="utf-8" />
<meta name="viewport" content="width=device-width,initial-scale=1" />
<title>Kelas X TJKT - SMK Asta Mitra Purwodadi</title>

<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600;700&display=swap" rel="stylesheet">

<style>
  :root{
    --bg:#0b0f14;
    --card:#0f1720;
    --muted:#9aa4b2;
    --accent:#00ffd1;
    --accent-2:#2ea8ff;
    --glass: rgba(255,255,255,0.03);
    --radius:12px;
  }
  *{box-sizing:border-box;margin:0;padding:0}
  body{
    margin:0;
    font-family:"Poppins",system-ui,-apple-system,Segoe UI,Roboto,"Helvetica Neue",Arial;
    background: linear-gradient(180deg, #05070a 0%, #071025 100%);
    color:#e6eef8;
    line-height:1.45;
  }

  /* --- Splash screen --- */
  #splash{
    position:fixed;
    top:0;left:0;width:100%;height:100%;
    background:#05070a;
    display:flex;align-items:center;justify-content:center;
    z-index:9999;
    animation: fadeOut 1s ease 3.8s forwards;
  }
  #splash h1{
    font-size:64px;
    font-weight:800;
    background: linear-gradient(90deg, var(--accent-2), var(--accent));
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    text-shadow: 0 0 12px rgba(46,168,255,0.7), 0 0 20px rgba(0,255,209,0.6);
    opacity:0;
    animation: zoomIn 1.2s ease forwards, glowPulse 1.8s ease-in-out 1.2s infinite alternate;
  }
  @keyframes zoomIn{
    from{opacity:0;transform:scale(0.5);}
    to{opacity:1;transform:scale(1);}
  }
  @keyframes glowPulse{
    from{text-shadow:0 0 8px rgba(46,168,255,0.5), 0 0 12px rgba(0,255,209,0.4);}
    to{text-shadow:0 0 16px rgba(46,168,255,1), 0 0 28px rgba(0,255,209,0.9);}
  }
  @keyframes fadeOut{
    to{opacity:0;visibility:hidden;}
  }

  header{
    padding:28px 20px;
    text-align:center;
    background: linear-gradient(90deg, rgba(46,168,255,0.06), rgba(0,255,209,0.03));
    border-bottom:1px solid rgba(255,255,255,0.03);
    position:sticky;
    top:0;
    z-index:10;
    backdrop-filter: blur(6px);
  }
  .title{
    display:flex;
    gap:16px;
    align-items:center;
    justify-content:center;
    flex-wrap:wrap;
  }
  .logo{
    width:64px;height:64px;
    border-radius:10px;
    background:linear-gradient(135deg,var(--accent-2),var(--accent));
    display:flex;align-items:center;justify-content:center;
    box-shadow: 0 6px 18px rgba(46,168,255,0.08), inset 0 -6px 18px rgba(0,255,209,0.06);
    font-weight:700;
    color:#021;
    font-size:22px;
  }
  h1{margin:0;font-size:20px;letter-spacing:0.2px}
  h2{margin:0;font-weight:600;color:var(--accent-2);font-size:13px}
  nav{
    display:flex;gap:8px;justify-content:center;padding:14px 10px;margin-top:14px;
  }
  .nav-btn{
    background:transparent;border:1px solid rgba(255,255,255,0.04);
    padding:8px 12px;border-radius:999px;color:var(--muted);
    text-decoration:none;font-weight:500;font-size:13px;
    transition: all .18s ease;
  }
  .nav-btn:hover{transform:translateY(-3px); box-shadow:0 6px 18px rgba(46,168,255,0.04); color:var(--accent)}
  main{max-width:1100px;margin:24px auto;padding:0 18px;}
  .top-row{display:grid;grid-template-columns:1fr;gap:18px;align-items:start}
  .card{
    background:linear-gradient(180deg, rgba(255,255,255,0.01), rgba(255,255,255,0.02));
    border:1px solid rgba(255,255,255,0.03);
    padding:16px;border-radius:var(--radius);
    box-shadow: 0 8px 30px rgba(2,6,23,0.6);
  }
  .struktur h3{color:var(--accent);margin-bottom:8px}
  .roles{display:grid;grid-template-columns:1fr 1fr;gap:8px}
  .role{
    background:var(--glass);padding:10px;border-radius:10px;border:1px solid rgba(255,255,255,0.02);
    display:flex;align-items:center;gap:10px;font-size:14px;
  }
  .role .badge{
    width:44px;height:44px;border-radius:8px;background:linear-gradient(135deg,var(--accent-2),var(--accent));
    display:flex;align-items:center;justify-content:center;color:#021;font-weight:700;
  }
  .muted{color:var(--muted);font-size:13px}
  .list-students{max-height:340px;overflow:auto;padding-right:6px}
  .student{
    display:flex;align-items:center;gap:12px;padding:8px;border-radius:10px;margin-bottom:8px;background:linear-gradient(180deg, rgba(255,255,255,0.01), transparent);
    border:1px solid rgba(255,255,255,0.02)
  }
  .avatar{width:44px;height:44px;border-radius:8px;background:linear-gradient(135deg,#0b1220,#071a2a);display:flex;align-items:center;justify-content:center;color:var(--accent);font-weight:600}
  .subject{font-weight:600;color:#dff;letter-spacing:0.2px}
  .schedule{display:flex;flex-direction:column;gap:8px}
  .sched-item{padding:10px;border-radius:10px;background:linear-gradient(90deg, rgba(46,168,255,0.04), rgba(0,255,209,0.02));border:1px solid rgba(46,168,255,0.06)}
  footer{max-width:1100px;margin:24px auto;padding:18px;color:var(--muted);text-align:center;font-size:13px}
</style>
</head>
<body>

<!-- Splash Screen -->
<div id="splash">
  <h1>X TJKT 2</h1>
</div>

<header>
  <div class="title">
    <div class="logo">TJ</div>
    <div>
      <h1>Kelas X TJKT</h1>
      <h2>SMK Asta Mitra Purwodadi</h2>
    </div>
  </div>

  <nav>
    <a class="nav-btn" href="#struktur">Struktur</a>
    <a class="nav-btn" href="#murid">Murid</a>
    <a class="nav-btn" href="#piket">Piket</a>
    <a class="nav-btn" href="#pelajaran">Pelajaran</a>
  </nav>
</header>

<main>
  <div class="top-row">
    <div class="card struktur" id="struktur">
      <h3>Struktur Kelas</h3>
      <div class="roles">
        <div class="role"><div class="badge">WK</div><div><strong>Wali Kelas</strong><div class="muted">Bu Rining</div></div></div>
        <div class="role"><div class="badge">KT</div><div><strong>Ketua Kelas</strong><div class="muted">Fahri</div></div></div>
        <div class="role"><div class="badge">WK</div><div><strong>Wakil Ketua</strong><div class="muted">Fahri</div></div></div>
        <div class="role"><div class="badge">S1</div><div><strong>Sekretaris 1</strong><div class="muted">Inesa</div></div></div>
        <div class="role"><div class="badge">S2</div><div><strong>Sekretaris 2</strong><div class="muted">Salma</div></div></div>
        <div class="role"><div class="badge">B1</div><div><strong>Bendahara 1</strong><div class="muted">Syifa</div></div></div>
        <div class="role"><div class="badge">B2</div><div><strong>Bendahara 2</strong><div class="muted">Bintang</div></div></div>
      </div>
    </div>
  </div>

  <div class="grid">
    <div class="card">
      <h3 id="murid" style="color:var(--accent)">Daftar Murid</h3>
      <div class="list-students">
        <!-- 31 murid asli -->
        <div class="student"><div class="avatar">A</div><div><strong>Adly Prasetyo</strong><div class="muted">No. 1</div></div></div>
        <div class="student"><div class="avatar">A</div><div><strong>Alfian Tri Widodo</strong><div class="muted">No. 2</div></div></div>
        <div class="student"><div class="avatar">A</div><div><strong>Alya Nur Amiroh</strong><div class="muted">No. 3</div></div></div>
        <div class="student"><div class="avatar">A</div><div><strong>Anom Fathasena</strong><div class="muted">No. 4</div></div></div>
        <div class="student"><div class="avatar">B</div><div><strong>Bagus Prasetyo</strong><div class="muted">No. 5</div></div></div>
        <div class="student"><div class="avatar">B</div><div><strong>Bayu Samudra</strong><div class="muted">No. 6</div></div></div>
        <div class="student"><div class="avatar">B</div><div><strong>Bayu Seto Anggoro</strong><div class="muted">No. 7</div></div></div>
        <div class="student"><div class="avatar">D</div><div><strong>Dewi Ambar</strong><div class="muted">No. 8</div></div></div>
        <div class="student"><div class="avatar">D</div><div><strong>Dimas Ega Putra (S)</strong><div class="muted">No. 9</div></div></div>
        <div class="student"><div class="avatar">F</div><div><strong>Fahri Fajar Pepriyanto</strong><div class="muted">No. 10</div></div></div>
        <div class="student"><div class="avatar">F</div><div><strong>Farid Yudistira</strong><div class="muted">No. 11</div></div></div>
        <div class="student"><div class="avatar">F</div><div><strong>Firdausa Ramadhan (Ws)</strong><div class="muted">No. 12</div></div></div>
        <div class="student"><div class="avatar">G</div><div><strong>Gibran Wafia Dzakwan</strong><div class="muted">No. 13</div></div></div>
        <div class="student"><div class="avatar">I</div><div><strong>Inesa Atufuniza</strong><div class="muted">No. 14</div></div></div>
        <div class="student"><div class="avatar">J</div><div><strong>Junion Richo Rizaldo</strong><div class="muted">No. 15</div></div></div>
        <div class="student"><div class="avatar">M</div><div><strong>M. Safrizal Abdul Ghoni</strong><div class="muted">No. 16</div></div></div>
        <div class="student"><div class="avatar">M</div><div><strong>M. Bintang Fernando</strong><div class="muted">No. 17</div></div></div>
        <div class="student"><div class="avatar">M</div><div><strong>Melinda Audri Ananda Putri</strong><div class="muted">No. 18</div></div></div>
        <div class="student"><div class="avatar">M</div><div><strong>Mohamad Reza Ardiansyah</strong><div class="muted">No. 19</div></div></div>
        <div class="student"><div class="avatar">M</div><div><strong>Muhamad Hafiz Febriawan</strong><div class="muted">No. 20</div></div></div>
        <div class="student"><div class="avatar">M</div><div><strong>Muhamad Syukri Ar'Rouf</strong><div class="muted">No. 21</div></div></div>
        <div class="student"><div class="avatar">N</div><div><strong>Natan Damara Putra</strong><div class="muted">No. 22</div></div></div>
        <div class="student"><div class="avatar">N</div><div><strong>Nugroho Dwi Prasetyo</strong><div class="muted">No. 23</div></div></div>
        <div class="student"><div class="avatar">O</div><div><strong>Olivia Zalianti</strong><div class="muted">No. 24</div></div></div>
        <div class="student"><div class="avatar">R</div><div><strong>Rafa Yuda Eka Pratama</strong><div class="muted">No. 25</div></div></div>
        <div class="student"><div class="avatar">S</div><div><strong>Salma Aulia Dewy</strong><div class="muted">No. 26</div></div></div>
        <div class="student"><div class="avatar">S</div><div><strong>Surya Pratama Muza</strong><div class="muted">No. 27</div></div></div>
        <div class="student"><div class="avatar">U</div><div><strong>Uut Meisa Kalisa Putri</strong><div class="muted">No. 28</div></div></div>
        <div class="student"><div class="avatar">V</div><div><strong>Vino Pratama Nugroho</strong><div class="muted">No. 29</div></div></div>
        <div class="student"><div class="avatar">Y</div><div><strong>Yuan Rama Yudistira</strong><div class="muted">No. 30</div></div></div>
        <div class="student"><div class="avatar">Z</div><div><strong>Zahratus Syifa Al-Maulida</strong><div class="muted">No. 31</div></div></div>
      </div>
    </div>

    <div class="card">
      <h3 id="piket" style="color:var(--accent)">Jadwal Piket</h3>
      <div class="schedule">
        <div class="sched-item"><strong>Senin</strong><div class="muted">Ani, Budi</div></div>
        <div class="sched-item"><strong>Selasa</strong><div class="muted">Citra, Dedi</div></div>
        <div class="sched-item"><strong>Rabu</strong><div class="muted">Eka, Fajar</div></div>
        <div class="sched-item"><strong>Kamis</strong><div class="muted">Gita, Hana</div></div>
        <div class="sched-item"><strong>Jumat</strong><div class="muted">Indra, Joko</div></div>
      </div>

      <h3 id="pelajaran" style="margin-top:14px;color:var(--accent)">Jadwal Pelajaran (Ringkas)</h3>
      <div style="margin-top:8px">
        <div class="sched-item"><span class="subject">Senin</span><div class="muted">Matematika • IPA</div></div>
        <div class="sched-item"><span class="subject">Selasa</span><div class="muted">Bahasa Indonesia • PKN</div></div>
        <div class="sched-item"><span class="subject">Rabu</span><div class="muted">Produktif TKJ • Inggris</div></div>
        <div class="sched-item"><span class="subject">Kamis</span><div class="muted">Sejarah • Seni Budaya</div></div>
        <div class="sched-item"><span class="subject">Jumat</span><div class="muted">Agama • Penjas</div></div>
      </div>
    </div>
  </div>
</main>

<footer>
  © 2025 Kelas X TJKT – SMK Asta Mitra Purwodadi
</footer>

</body>
</html>
