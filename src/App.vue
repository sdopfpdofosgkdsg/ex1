<script>
export default {
  data() {
    return {
      email: ""
    }
  },
  methods: {
    sendFeedback() {
      //Проверка на валидность E-Mail
      if (!this.validateEmail(this.email)) {
        alert("Некорректный E-Mail");
        return;
      }
      
      //Отправка email на сервер
      //Код для отправки данных на сервер
      
      //Уведомление в тг
      //Kод для отправки уведомления в тг
    },
    validateEmail(email) {
        //Регулярное выражение (для проверки валидности email)
        const reg = /^(([^<>()[\]\\.,;:\s@"]+(\.[^<>()[\]\\.,;:\s@"]+)*)|(".+"))@((\[[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}\])|(([a-zA-Z\-0-9]+\.)+[a-zA-Z]{2,}))$/;
        return reg.test(email);
    }
  }
}
</script>

<template>

  <section class="sign-up">
        <div class="container">
            <h1 class="title">Don’t forget to sign up</h1>
            <div class="line"></div>
            <p class="description">Find out early about all upcoming promotions and new product releases with 
                our newsletter.</p>
            <div class="subscribe">
                <input type="email" class="text-field" v-model="email" id="email" placeholder="Enter your email address.....">
                <a href="#" class="btn" id="btn_email" @click="sendFeedback">subscribe</a>
            </div>
        </div>
  </section>

</template>

<style scoped>
.sign-up {
  padding-top: 197px;
  text-align: center;
}

.container {
  width: 1346px;
  margin: auto;
}

.title {
  font-family: 'Poppins', sans-serif;
  font-size: 48px;
  font-weight: 500;
  line-height: 28px;
  letter-spacing: 3.84px;
  text-transform: uppercase;
}

.line {
  margin: auto;
  max-width: 470px;
  margin-top: 37px;
  border-bottom: 1px solid #C4C4C4;
}
.description {
  margin: auto;
  max-width: 665px;
  color: #646464;
  font-size: 18px;
  line-height: 30px;
  padding-top: 40px;
}

.subscribe {
  display: inline-table;
  align-items: baseline;
}

.text-field {
  font-family: 'Poppins', sans-serif;
  width: 590px;
  height: 50px;
  border-radius: 20px 0px 0px 0px;
  background: #EEE;
  color: #646464;
  font-size: 18px;
  line-height: 55px;
  border: #EEE;
  padding-left: 30px;
  margin-top: 30px;
  margin-bottom: 195px;
  outline: none;
}

.btn {
  color: #ffffff;
  font-size: 18px;
  font-weight: 700;
  padding: 14px 40px;
  border-radius: 0px 0px 20px 0px;
  background: #37806B;
  text-transform: uppercase;
  text-decoration: none;
}
</style>
