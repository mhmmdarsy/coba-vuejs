<template>
  <div>
    <h1>Vue JS</h1>

    <!-- implementasi interpolation -->
    <h2>{{ nama }}</h2>
    <!-- contoh attribute binding -->
    <img
      :src="gambar"
      :alt="`Foto profil ${nama}`"
      title="Foto profil"
      width="250px"
      height="250px"
    />
    <p>Umur: {{ umur }}</p>

    <br /><br />

    <!-- contoh event binding -->
    <button @click="tambahUmur">Tambah Umur</button>

    <br /><br />

    <!-- contoh conditional rendering -->
    <p v-if="umur >= 18">Status: Dewasa</p>
    <p v-else>Status: Anak-anak</p>

    <br />

    <!-- implementasi two-way binding menggunakan v-model -->
    <label>Masukkan pesan:</label>
    <input type="text" v-model="pesan" />
    <!-- implementasi interpolation -->
    <p>Pesan kamu: {{ pesan }}</p>

    <br />

    <h3>Wishlist:</h3>
    <!-- contoh implementasi v-for -->
    <ul>
      <li v-for="(hobi, index) in daftarHobi" :key="index">
        {{ hobi }}
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      nama: "Muhammad Arsy Al-Fahd",
      umur: 20,
      gambar: "../assets/pfp.jpg",
      pesan: "",
      daftarHobi: ["Adizero EVO SL White Black", "Speedcat White Pink"],
    };
  },
  methods: {
    tambahUmur() {
      this.umur++;
    },
  },
};
</script>
