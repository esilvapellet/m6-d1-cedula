<template>
  <div id="app">
    <header>
      <h1>Cédula de Identidad</h1>
    </header>

    <div class="carnet">
      <aside>
        <div>
          <span>CEDULA DE IDENTIDAD</span>
          <img width="40" src="./assets/bandera.png" alt="" />
        </div>

        <img src="./assets/foto.jpg" alt="" />
        <p>RUN {{ run }}</p>
      </aside>

      <main>
        <header>
          <p>REPUBLICA DE CHILE</p>
          <span>SERVICIO DE REGISTRO CIVIL E IDENTIFICACIÓN</span>
        </header>
        <section>
          <article>
            <header>APELLIDOS</header>
            <span>{{ apellidos }}</span>
          </article>
          <article>
            <header>NOMBRES</header>
            <span>{{ nombres }}</span>
          </article>

          <div class="grid-2-colums">
            <article>
              <header>NACIONALIDAD</header>
              <span>{{ nacionalidad }}</span>
            </article>
            <article>
              <header>SEXO</header>
              <span>M</span>
            </article>
          </div>
          <div class="grid-2-colums">
            <article>
              <header>FECHA DE NACIMIENTO</header>
              <span>{{ fechaNac }}</span>
            </article>
            <article>
              <header>NÙMERO DOCUMENTO</header>
              <span>{{ numeroDoc }}</span>
            </article>
          </div>
          <div class="grid-2-colums">
            <article>
              <header>FECHA DE EMISIÒN</header>
              <span>{{ fechaEmi }}</span>
            </article>
            <article>
              <header>FECHA DE VENCIMIENTO</header>
              <span>{{ fechaVen }}</span>
            </article>
          </div>
          <article>
            <header>FIRMA DEL TITULAR</header>
            <!-- <span>X Æ A-12</span> -->
            <span><img src="./assets/firma.png" style="width: 75px" /></span>
          </article>
        </section>
      </main>
    </div>
  </div>
</template>

<script>
export default {
  name: "App",
  components: {},
  data() {
    return {
      run: "12.345.678-9",
      apellidos: "MUSK",
      nombres: "ELON REEVE",
      nacionalidad: "SUDAFRICANO",
      genero: "M",
      fechaNac: "28 JUN 1971",
      numeroDoc: "123.456.789",
      fechaEmi: "08 MAY 2024",
      fechaVen: "28 JUN 2034",
    };
  },
  methods: {
    emitirCi: function () {
      alert(
        `Cédula del ciudadano: ${this.nombres} ${this.apellidos} Run: ${this.run} emitida con éxito`
      );
    },
  },
};
</script>

<style>
body {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 60vh;
  font-size: 10px;
  font-family: sans-serif;
  background: url("./assets/background.jpeg");
  background-size: cover;
}

h1 {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  text-align: center;
  font-weight: bold;
  text-transform: uppercase;
  color: #ffffff;
  font-size: 24px;
}

.container-form {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  color: #ffffff;
  padding: 25px;
}

.container-form label {
  font-size: 18px;
}

.carnet {
  width: 400px;
  height: 230px;
  background: #c8deed;
  border-radius: 20px;
  display: grid;
  grid-template-columns: 30% 1fr;
  padding: 15px;
  box-shadow: 0px 0px 10px 2px black;
}

aside div {
  display: flex;
}

aside > img {
  margin-top: 15px;
  width: 100%;
}

aside p {
  text-align: center;
  font-size: 12px;
  font-weight: bold;
}

main {
  padding: 0px 14px;
}

main article {
  margin: 4px 0px;
}

main article header {
  font-weight: bold;
  color: #0235a4;
  font-size: 8px;
}

main header p {
  font-size: 20px;
  margin: 0;
  font-weight: bold;
  color: #0235a4;
}

main header span {
  font-size: 8px;
  color: #399be1;
}

main section {
  margin-top: 10px;
}

main section article span {
  font-size: 13px;
  font-weight: 600;
}

main section .grid-2-colums {
  display: grid;
  grid-template-columns: 50% 50%;
}
</style>
