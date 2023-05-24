<script>
  export default {
    data() {
      return {
        data_images: [
          {
            id: 1,
            logo_name: "FC BARCELONA",
            logo_file: "barcelona.png",
            palyed: 2,
            scores: 7,
            lose: 2,
            rating: 3,
          },
          {
            id: 2,
            logo_name: "ATLETICO MADRID",
            logo_file: "Atletico.png",
            palyed: 3,
            scores: 6,
            lose: 3,
            rating: 4,
          },
          {
            id: 3,
            logo_name: "RCD ESPANYOL",
            logo_file: "espanyol.gif",
            palyed: 4,
            scores: 5,
            lose: 3,
            rating: 5,
          },
          {
            id: 4,
            logo_name: "ATHLETIC CLUB",
            logo_file: "Bilbao.png",
            palyed: 5,
            scores: 4,
            lose: 4,
            rating: 6,
          },
          {
            id: 5,
            logo_name: "SEVILLA FC",
            logo_file: "Sevilla.png",
            palyed: 1,
            scores: 9,
            lose: 3,
            rating: 2,
          },
          {
            id: 6,
            logo_name: "GIRONA FC",
            logo_file: "Girona.png",
            palyed: 6,
            scores: 2,
            lose: 1,
            rating: 7,
          },
          {
            id: 7,
            logo_name: "RAYO VALLECANO",
            logo_file: "Rayo.png",
            palyed: 6,
            scores: 2,
            lose: 1,
            rating: 6,
          },
          {
            id: 8,
            logo_name: "REAL MADRID",
            logo_file: "Madrid.png",
            palyed: 7,
            scores: 12,
            lose: 1,
            rating: 1,
          },
          {
            id: 9,
            logo_name: "REAL BETIS",
            logo_file: "betis.png",
            palyed: 8,
            scores: 2,
            lose: 7,
            rating: 8,
          },
          {
            id: 10,
            logo_name: "CA OSASUNA",
            logo_file: "osasuna.png",
            palyed: 9,
            scores: 1,
            lose: 8,
            rating: 10,
          },
        ],
      };
    },
  };
</script>
<template>
  <div>
    <div class="row row-cols-1 row-cols-md-5 g-4">
      <div v-for="data_images in data_images" class="col">
        <a class="btn btn-link btn-block">
          <router-link :to="'/detail/' + data_images.id">
            <div class="col">
              <div class="card h-100">
                <div class="card-body">
                  <img
                    :src="'/src/assets/logo_bola/' + data_images.logo_file"
                    class="card-img-top"
                    alt="404"
                  />
                </div>
                <h5 id="text__decotation" class="text-center">
                  {{ data_images.logo_name }}
                </h5>
              </div>
            </div>
          </router-link>
        </a>
      </div>
    </div>
  </div>
</template>

<style>
  img {
    width: 100px;
    height: 150px;
  }
</style>
