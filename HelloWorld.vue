<template>
  <div class="cv">
    
    
    <h1>{{ name }}</h1>
    <hr>
    <h2>Pendidikan</h2>
    <p><strong>{{ education.degree }}</strong><br>{{ education.university }}<br>{{ education.duration }}</p>
    <hr>
    <h2>Pengalaman Kerja</h2>
    <p><strong>{{ experience[0].title }}</strong><br>{{ experience[0].company }}<br>{{ experience[0].duration }}<br>{{ experience[0].responsibilities }}</p>
    <hr>
    <h2>Proyek</h2>
    <p><strong>{{ projects[0].name }}</strong><br>{{ projects[0].duration }}<br>{{ projects[0].description }}</p>
    <hr>
    <h2>Keahlian</h2>
    <ul>
      <li v-for="skill in skills">{{ skill }}</li>
    </ul>
    <hr>
    <h2>Kontak</h2>
    <p>Email: {{ contact.email }}</p>
    <p>LinkedIn: <a :href="'https://www.linkedin.com/in/' + contact.linkedin">{{ contact.linkedin }}</a></p>
    <hr>
  </div>
</template>

<script setup>
const name = 'Nadia Anak Ampun';
const education = {
  degree: 'S1 Teknik Informatika',
  university: 'Universitas Islam Riau',
  duration: '2022'
};
const experience = [
  {
    title: 'Praktikum Pengembangan Web',
    company: 'Perusahaan ABC',
    duration: 'Januari 2022 - Mei 2022',
    responsibilities: 'Mengembangkan fitur frontend menggunakan Vue 3. Berkontribusi dalam pengoptimalan kinerja aplikasi dengan menggunakan Vite.'
  }
];
const projects = [
  {
    name: 'Sistem Manajemen Tugas',
    duration: 'Januari 2023 - Mei 2023',
    description: 'Mengembangkan aplikasi manajemen tugas berbasis web menggunakan Vue 3. Mengimplementasikan fungsionalitas drag-and-drop untuk mengatur tugas.'
  }
];
const skills = [
  'Bahasa Pemrograman: JavaScript, HTML, CSS',
  'Framework: Vue.js',
  'Pengembangan Web: Vite',
  'Responsive Web Design'
];
const extracurriculars = [
  'Anggota aktif klub pengembangan perangkat lunak di kampus.',
  'Menjadi mentor dalam workshop pengembangan web untuk mahasiswa tingkat awal.'
];
const contact = {
  email: 'anakampunnadia@gmail.com',
  linkedin: 'nadiaanakampun'
};
</script>

<style scoped>
h1 {
  font-weight: 500;
  font-size: 2.6rem;
  position: relative;
  top: -10px;
}
h2 {
  font-size: 1.6rem;
}
.cv p {
  margin-bottom: 10px;
}
.cv ul {
  list-style-type: disc;
  margin-left: 20px;
}
</style>
