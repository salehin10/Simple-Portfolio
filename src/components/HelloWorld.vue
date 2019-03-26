<template>
  <div class="hello">
    <div class="container header-container">
      <div class="row">
        <div class="col-12">
          <div class="card">
            <div class="card-header" id="portfolio-card-header">
              <h1 v-bind:title="text">Portfolio</h1>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="container body-container">
      <div class="row">
        <div class="col-sm-4">
          <div class="card portfolio-img-card" style="width: 18rem">
            <img src="salehinjpg.jpg" class="card-img-top" alt="...">
            <div class="card-body">
              <h5 class="card-title">Siraj Uz Salehin</h5>
              <p class="card-text">
                <img  height="30rem" width="30rem" src="html.png">Full Stack Web Developer
              </p>
              <div class="row">
                <div class="col-sm-4">
                  <a href="https://www.facebook.com/salehin.merchant">
                    <img height="30rem" width="30rem" src="facebook.png">
                  </a>
                </div>
                <div class="col-sm-4">
                  <a href="https://www.instagram.com/m_e_r_c_h_a_n_t/">
                    <img height="30rem" width="30rem" src="instagram.png">
                  </a>
                </div>
                <div class="col-sm-4">
                  <a href="https://github.com/salehin10/">
                    <img height="30rem" width="30rem" src="github.png">
                  </a>
                </div>
              </div>
            </div>
          </div>
        </div>
        <div class="col-sm-8">
          <div class="accordion" id="accordionExample">
            <div class="card">
              <div class="card-header" id="headingOne">
                <h2 class="mb-0">
                  <button
                    class="btn btn-link"
                    type="button"
                    data-toggle="collapse"
                    data-target="#collapseOne"
                    aria-expanded="true"
                    aria-controls="collapseOne"
                  >About</button>
                </h2>
              </div>

              <div
                id="collapseOne"
                class="collapse show"
                aria-labelledby="headingOne"
                data-parent="#accordionExample"
              >
                <div class="card-body" style="color:forestgreen">{{about}}</div>
              </div>
            </div>
            <div class="card">
              <div class="card-header" id="headingTwo">
                <h2 class="mb-0">
                  <button
                    class="btn btn-link collapsed"
                    type="button"
                    data-toggle="collapse"
                    data-target="#collapseTwo"
                    aria-expanded="false"
                    aria-controls="collapseTwo"
                  >Skills</button>
                </h2>
              </div>
              <div
                id="collapseTwo"
                class="collapse"
                aria-labelledby="headingTwo"
                data-parent="#accordionExample"
              >
                <div class="card-body">
                  <ul>
                    <li style="color:forestgreen" v-for="skill in skills" v-bind:key="skill">{{ skill.name }}</li>
                  </ul>
                </div>
              </div>
            </div>
            <div class="card">
              <div class="card-header" id="headingThree">
                <h2 class="mb-0">
                  <button
                    class="btn btn-link collapsed"
                    type="button"
                    data-toggle="collapse"
                    data-target="#collapseThree"
                    aria-expanded="false"
                    aria-controls="collapseThree"
                  >Projects</button>
                </h2>
              </div>
              <div
                id="collapseThree"
                class="collapse"
                aria-labelledby="headingThree"
                data-parent="#accordionExample"
              >
                <div class="card-body">
                  <ul>
                    <li v-for="link in links" v-bind:key="link">
                      <p v-html="link.name"></p>
                    </li>
                  </ul>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>

    </div>
</template>

<script>
export default {
  name: "Helloworld",
  data() {
   return{
     img:[
       {img1:'./assets/facebook.png'}
     ],
     skills: [
      { name: "PHP (Laravel Faramework)" },
      { name: "Java" },
      { name: "C/C#" },
      { name: "Html,CSS,Javascript(Vue.js,React.js)" }
    ],
    links: [
      {
        name:
          "<a style='color:forestgreen', href='https://github.com/salehin10/University-Website-Management'> University Website Management</a>"
      },
      {
        name:
          "<a style='color:forestgreen', href='https://github.com/salehin10/CNG-Merter'>CNG Meter</a>"
      },
      {
        name:
          "<a style='color:forestgreen', href='https://github.com/salehin10/Beverage-Management'>Beverage Management</a>"
      }
    ],
    about:
      "I am a Fullstack Web developer. I am from Bangladesh. I am tech. lover.I am belongto a muslim family I am always try to learn new things to up-to-date with world.Since it's fourth industrial revolution running, so alwasys i want to train myself to compete with this generation."
   }
    
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.container.header-container{
    margin-top:1.5rem;
}
.container.header-container h1{
    text-align: center;
    text-decoration: underline wavy;
    color: rgb(128, 210, 235);
}

.card.portfolio-img-card{
    margin-top: 8rem;
}
#html-img{
    height: 3rem;
    width: 2rem;

}
#accordionExample{
    margin-top:8rem;
}

</style>
