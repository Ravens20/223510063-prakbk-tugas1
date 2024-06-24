<template>
  <div id="app">
    <div class="container">
      <header>
        <h1>Portofolio Saya</h1>
      </header>
      <main class="main-content">
        <div class="profile">
          <img src="./assets/img/profile.png" alt="Profile Picture" class="profile-picture">
          <h2>Dindra Desvantio</h2>
          <h3>Mahasiswa Teknik Informatika</h3>
          <div class="social-icons">
            <div class="icon-box facebook"><i class="fab fa-facebook-f"></i></div>
            <div class="icon-box twitter"><i class="fab fa-twitter"></i></div>
            <div class="icon-box instagram"><i class="fab fa-instagram"></i></div>
            <div class="icon-box linkedin"><i class="fab fa-linkedin-in"></i></div>
          </div>
          <ul class="contact-info">
            <li>
              <div class="icon-box phone"><i class="fas fa-phone"></i></div>+62 831 8567 5743
            </li>
            <li>
              <div class="icon-box email"><i class="fas fa-envelope"></i></div>dindradesvantio@student.uir.ac.id
            </li>
            <li>
              <div class="icon-box location"><i class="fas fa-map-marker-alt"></i></div>Pekanbaru, Riau
            </li>
            <li>
              <div class="icon-box birthday"><i class="fas fa-birthday-cake"></i></div>06 Desember 2003
            </li>
          </ul>
        </div>
        <div class="projects">
          <div class="project">
            <h2>Pengenalan</h2>
            <p>Nama saya Dindra Desvantio. Saya adalah seorang mahasiswa yang penuh semangat dan berdedikasi tinggi yang sedang menempuh pendidikan di bidang Teknik Informatika di Universitas Islam Riau. Saya memiliki minat yang mendalam dalam teknologi informasi dan selalu berusaha untuk terus belajar dan berkembang dalam bidang ini.</p>
          </div>
          <div class="project">
            <h2>Status</h2>
            <p>Saat ini, saya berstatus sebagai mahasiswa aktif di Universitas Islam Riau. Selama masa studi saya, saya telah memperoleh dasar yang kuat dalam berbagai aspek ilmu komputer, baik teori maupun praktik. Saya selalu berusaha untuk mencapai prestasi akademis yang tinggi serta aktif berpartisipasi dalam kegiatan ekstrakurikuler untuk mengembangkan keterampilan kepemimpinan dan kerja sama tim.</p>
          </div>
          <div class="project">
            <h2>Keterampilan</h2>
            <p>Saya telah mengembangkan berbagai keterampilan yang diperlukan dalam industri teknologi informasi. Beberapa keterampilan utama yang saya kuasai meliputi:</p>
            <ul>
              <li>HTML: Memahami dasar-dasar pembuatan struktur halaman web.</li>
              <li>CSS: Mengerti bagaimana membuat tampilan halaman web yang menarik dan responsif.</li>
              <li>JavaScript: Mampu membuat interaksi dinamis pada halaman web.</li>
              <li>Vue.js: Berpengalaman dalam menggunakan framework ini untuk membangun aplikasi web interaktif.</li>
              <li>Node.js: Memiliki pengetahuan dalam pengembangan server-side menggunakan Node.js.</li>
              <li>Express.js: Familiar dengan framework ini untuk membuat aplikasi web back-end.</li>
              <li>MongoDB: Mengerti penggunaan basis data NoSQL ini untuk penyimpanan data yang efisien.</li>
            </ul>
          </div>
          <div class="project">
            <h2>Pengalaman</h2>
            <p>Selama menempuh pendidikan di Universitas Islam Riau, saya telah terlibat dalam berbagai proyek dan tugas yang membantu mengasah kemampuan saya dalam memecahkan masalah dan bekerja dalam tim. Beberapa pengalaman saya antara lain:</p>
            <ul>
              <li>Proyek Pengembangan Web: Membuat beberapa aplikasi web menggunakan teknologi seperti HTML, CSS, JavaScript, dan Vue.js.</li>
              <li>Magang: Mengikuti program magang di perusahaan teknologi untuk mendapatkan pengalaman praktis dalam industri IT.</li>
              <li>Kegiatan Ekstrakurikuler: Aktif dalam berbagai kegiatan organisasi mahasiswa untuk mengembangkan keterampilan kepemimpinan dan manajemen proyek.</li>
            </ul>
          </div>
        </div>
      </main>
      <div class="skills">
        <h3>Keterampilan:</h3>
        <ul>
          <li v-for="(skill, index) in skills" :key="index" class="skill">
            <div class="icon-box" @click="showSkillInfo(skill)">
              <i :class="getSkillIconClass(skill)" :style="{ color: getColor(skill) }"></i>
            </div>
            <span>{{ skill }}</span>
          </li>
        </ul>
      </div>
      <footer>
        <p>&copy; 2024 Portofolio Saya</p>
      </footer>
    </div>
  </div>
</template>

<script>
export default {
  name: 'App',
  data() {
    return {
      skills: ['HTML', 'CSS', 'JavaScript', 'Vue.js', 'Node.js', 'Express.js', 'MongoDB'],
    }
  },
  methods: {
    getSkillIconClass(skill) {
      switch (skill) {
        case 'HTML':
          return 'fab fa-html5 fa-lg html-color';
        case 'CSS':
          return 'fab fa-css3-alt fa-lg css-color';
        case 'JavaScript':
          return 'fab fa-js-square fa-lg js-color';
        case 'Vue.js':
          return 'fab fa-vuejs fa-lg vue-color';
        case 'Node.js':
          return 'fab fa-node-js fa-lg node-color';
        case 'Express.js':
          return 'fab fa-node-js fa-lg express-color';
        case 'MongoDB':
          return 'fas fa-database fa-lg mongodb-color';
        default:
          return '';
      }
    },
    showSkillInfo(skill) {
      // Add your logic to show skill info
      console.log(`Klik pada ${skill}`);
    },
    getColor(skill) {
      switch (skill) {
        case 'HTML':
          return '#E44D26';
        case 'CSS':
          return '#264DE4'; 
        case 'JavaScript':
          return '#F7DF1E';
        case 'Vue.js':
          return '#41B883';
        case 'Node.js':
          return '#68A063';
        case 'Express.js':
          return '#000000'; 
        case 'MongoDB':
          return '#4DB33D';
        default:
          return '';
      }
    }
  }
}
</script>

<style scoped>
@import url('https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.15.4/css/all.min.css');

body {
  background-color: #f3f4f6;
  margin: 0;
  padding: 0;
  font-family: Arial, sans-serif;
}

#app {
  max-width: 1200px;
  margin: 0 auto;
  padding: 20px;
  box-sizing: border-box;
}

.container {
  background-color: #fad68a;
  border-radius: 10px;
  padding: 20px;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
}

header {
  text-align: center;
  margin-bottom: 30px;
}

.main-content {
  display: flex;
  gap: 20px;
}

.profile {
  flex: 1;
  max-width: 350px;
  padding: 20px;
  border: 1px solid #ddd;
  border-radius: 10px;
  background-color: #f9f9f9;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
  text-align: center;
}

.profile-picture {
  width: 120px;
  height: 120px;
  border-radius: 50%;
  margin-bottom: 20px;
  border: 2px solid #fff;
}

.profile h2 {
  margin: 10px 0 5px;
  font-size: 24px;
  color: #333;
}

.profile h3 {
  margin: 0 0 20px;
  font-weight: normal;
  color: #777;
}

.social-icons {
  display: flex;
  justify-content: center;
  margin-bottom: 20px;
}

.icon-box {
  background-color: #f0f0f0;
  border-radius: 50%;
  padding: 12px;
  margin: 0 5px;
  transition: transform 0.3s;
  cursor: pointer;
}

.icon-box i {
  color: #555;
  font-size: 18px;
}

.icon-box:hover {
  transform: translateY(-5px);
}

.contact-info {
  list-style: none;
  padding: 0;
  margin: 20px 0;
  text-align: center;
  justify-content: center;
}

.contact-info li {
  margin-bottom: 10px;
  display: flex;
  align-items: center;
}

.contact-info li .icon-box {
  margin-right: 10px;
  transition: transform 0.3s;
}

.contact-info li .icon-box:hover {
  transform: translateY(-5px);
}

.contact-info i {
  margin-right: 10px;
}

.projects {
  flex: 3;
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  gap: 20px;
}

.project {
  background-color: #f9f9f9;
  padding: 20px;
  border-radius: 10px;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
  transition: transform 0.3s;
}

.project:hover {
  transform: translateY(-5px);
}

.project h2 {
  margin-top: 0;
}

.skills {
  margin-top: 30px;
  text-align: center;
  padding: 5px;
  background-color: #f9f9f9;
  border-radius: 10px;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
}

.skills h3 {
  margin-bottom: 20px;
}

.skills ul {
  list-style-type: none;
  padding: 0;
  display: flex;
  justify-content: center;
  flex-wrap: wrap;
}

.skills li {
  display: flex;
  align-items: center;
  margin: 10px;
  font-size: 18px;
}

.skills li .icon-box {
  background-color: #f0f0f0;
  border-radius: 50%;
  padding: 12px;
  margin-right: 10px;
  transition: transform 0.3s;
}

.skills li .icon-box i {
  color: #555;
  font-size: 18px;
}

.skills li .icon-box:hover {
  transform: translateY(-5px);
}

.skills li span {
  margin-left: 5px;
}

footer {
  text-align: center;
  margin-top: 30px;
}

.icon-box.phone i { color: #007bff; } 
.icon-box.email i { color: #D44638; } 
.icon-box.location i { color: #4caf50; }
.icon-box.birthday i { color: #ff9800; }

.icon-box.facebook i { color: #3b5998; }
.icon-box.twitter i { color: #1da1f2; }
.icon-box.instagram i { color: #e1306c; } 
.icon-box.linkedin i { color: #0077b5; }
</style>
