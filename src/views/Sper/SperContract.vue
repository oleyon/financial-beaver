<template>
  <div class="sper-contract">
    <SperLogo class="sper-contract__logo" />
    <div class="sper-contract__border" />
    <div class="sper-contract__text">
      <p>Между банком «Спёрбанк», именуемым в дальнейшем «Банк», и вкладчиком «ФИО вкладчика», именуемым в дальнейшем «Вкладчик», заключен следующий договор о вкладе:</p>
      <p>1. Предмет договора</p>
      <p>1.1. В соответствии с настоящим договором Вкладчик передает Банку финансовые средства в размере «Сумма вклада» («Сумма прописью») .</p>
      <p>1.2. Банк обязуется принять денежные средства во вклад на условиях, предусмотренных настоящим договором, а Вкладчик обязуется внести указанную сумму в соответствии с требованиями Банка.</p>
      <p>2. Условия вклада</p>
      <p>2.1. Срок действия вклада составляет «Срок вклада» («Срок прописью») месяцев/лет.</p>
      <p>2.2. Процентная ставка по вкладу составляет «Процентная ставка»% годовых.</p>
      <p>2.3. Вкладчик вправе получить начисленные проценты по вкладу по истечении срока действия вклада.</p>
      <p>3. Ответственность Банка</p>
      <p>3.1. Банк не несет ответственности за убытки или потери, связанные с вложенными Вкладчиком денежными средствами на вклад. В случае банкротства Банка Вкладчик имеет право на возмещение убытков в порядке, установленном законодательством РФ.</p>
      <p>3.2. Банк не несет ответственности за изменения налогового законодательства, влияющие на сумму налоговых платежей, уплачиваемых Вкладчиком.</p>
      <p>4. Заключительные положения</p>
      <p>4.1. Настоящий договор вступает в силу с момента подписания его сторонами и действует до момента исполнения ими возложенных на них обязательств.</p>
      <p>4.2. Все споры, возникающие при исполнении настоящего договора, будут разрешены в одностороннем порядке, на усмотрение банка</p>
    </div>
    <div class="accept-block">
      <RoundedCheckbox v-model="accept" id="accept" notActiveColor="#2AB514">
        Настоящим подтверждаю что ознакомился с договором
      </RoundedCheckbox>
      <RoundedButton class="accept-block__order-button" :buttonShadow="false" borderRadius="15px">
        Согласен
      </RoundedButton>
    </div>
  </div>
</template>

<script>
import SperLogo from './components/SperLogo.vue'
import RoundedButton from './components/RoundedButton.vue'
import RoundedCheckbox from './components/RoundedCheckbox.vue'

export default {
  name: 'SperContract',
  components: {
    SperLogo,
    RoundedButton,
    RoundedCheckbox
  },
  data () {
    return {
      accept: false
    }
  }
}
</script>

<style lang="less">
@import url('https://fonts.googleapis.com/css2?family=Open+Sans&display=swap');

body {
  background-color: #F2F2F2;
}

.sper-contract {
  padding: 5vmin;

  &__border {
    padding-top: 2vmin;
    border-top: 2px solid #727272;
  }

  &__text {
    font-family: "Open Sans";
    font-size: 3vmin;

    padding: 3vmin;
    background: #D9D9D9;

    margin-bottom: 3vmin;
  }

  &__logo {
    margin-bottom: 2vmin;
  }
}

.accept-block {
  display: flex;
  flex-direction: row;

  &__order-button {
    margin-left: auto;
  }
}
</style>
