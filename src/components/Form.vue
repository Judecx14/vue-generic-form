<script>
export default {
  methods: {
    showAlert() {
      this.$swal(
        "Saved data",
        "You can answer the survey again by clicking on the button",
        "success"
      ).then(() => {
        window.location.reload();
      });
    },
  },
};
</script>

<template>
  <section>
    <article>
      <h1>Developer survey</h1>
      <form @submit.prevent="showAlert">
        <div class="container-form">
          <div class="container-input" id="first-part">
            <label for="name">What's your name?</label>
            <input type="text" id="name" />
            <label for="age">How old are you?</label>
            <input type="text" id="age" />
            <label for="country">Where are you from?</label>
            <select id="country">
              <option value="">Select a country</option>
              <option value="us">United States</option>
              <option value="uk">United Kingdom</option>
              <option value="au">Australia</option>
              <option value="ca">Canada</option>
              <option value="nz">New Zealand</option>
            </select>
            <label for="position"
              >What is your current professional position?</label
            >
            <div>
              <input
                type="radio"
                id="employee"
                value="employee"
                name="position"
              />
              <label for="employee">Employee</label>
            </div>
            <div>
              <input
                type="radio"
                id="unemployed"
                value="unemployed"
                name="position"
              />
              <label for="unemployed">Unemployed</label>
            </div>
          </div>
          <div class="container-input">
            <label for="front-end"
              >Select the programming areas you like.</label
            >
            <label>
              <input type="checkbox" id="front-end" value="front-end" />
              Front-end
            </label>
            <label>
              <input type="checkbox" id="back-end" value="back-end" />
              Back-end
            </label>
            <label>
              <input type="checkbox" id="data-science" value="data-science" />
              Data sciencie
            </label>
            <label>
              <input type="checkbox" id="mobile" value="mobile" />
              Mobile development
            </label>
            <label>
              <input type="checkbox" id="iot" value="iot" />
              IOT
            </label>
            <label for="framework">Select your favorite framework</label>
            <select id="framework">
              <option value="">Select a framework</option>
              <option value="vue" id="vue">Vue</option>
              <option value="react" id="react">React</option>
              <option value="angular" id="angular">Angular</option>
              <option value="ionic" id="ionic">Ionic</option>
              <option value="flutter" id="flutter">Flutter</option>
            </select>
          </div>
        </div>
        <button type="submit">Send</button>
      </form>
    </article>
  </section>
</template>

<style scoped>
section {
  min-height: 100vh;
  display: flex;
  flex-direction: column;
  align-items: center;
  background: rgb(247, 247, 247);
}
h1 {
  padding-top: 60px;
  margin-block: 20px;
  font-size: 4em;
  font-family: "Red Hat Display", sans-serif;
  font-weight: 900;
  background: #08bbcf;
  background: linear-gradient(to right, #08bbcf 0%, #cf11a3 100%);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
}
form {
  background: white;
  border-radius: 20px;
  display: flex;
  flex-direction: column;
  align-items: center;
  padding: 20px;
  box-shadow: 0px 0px 18px 1px rgba(0, 0, 0, 0.123);
}
label {
  margin-bottom: 5px;
  font-weight: 500;
}
input,
select {
  margin-bottom: 15px;
  border-radius: 10px;
  border: 1px solid grey;
}
input {
  padding-inline: 10px;
}
input:focus {
  outline: none;
}
.container-form {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  align-items: center;
}
.container-input {
  display: flex;
  flex-direction: column;
}
#first-part {
  padding-right: 10px;
}
button {
  width: 100%;
  background: transparent;
  border: 1px solid #08bbcf;
  border-radius: 20px;
  height: 30px;
  color: #08bbcf;
  font-weight: 500;
  font-size: 1.2em;
}
button:focus {
  outline: none;
  background: #08bbcf;
  color: white;
}
</style>
