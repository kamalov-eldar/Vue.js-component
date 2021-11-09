<template>
  <div class="wrapper">
    <div class="calculator">
      <h1 class="calculator__title">Калькулятор займа под ПТС</h1>
      <div class="calculator__container">
        <div class="calculator-payment">
          <div class="payment-type">
            <span class="payment-type__title">Тип платежа</span>
            <div class="payment-type__btns">
              <button class="payment-type__differentiated btn" autofocus>Дифференцированный</button>
              <button class="payment-type__annuity btn">Аннуитентный</button>
            </div>
          </div>

          <div class="calculator-sum">
            <span class="calculator-sum__title">Сумма займа</span>
            <input class="calculator-sum__input" type="text" placeholder="138100" />
            <span class="calculator-sum__label">₽</span>
          </div>

          <div class="slider-sum">
            <input
              class="slider-sum__input"
              type="range"
              min="0"
              max="100"
              v-bind:style="{
                background:
                  '-webkit-linear-gradient(left, #68b738 0%, #68b738 ' + inputRangeSum + '%, #cacaca ' + inputRangeSum + '%, #cacaca 0%)',
              }"
              v-model="inputRangeSum"
            />
            <div class="slider__label">
              <span class="slider__text">от 15 000 р</span>
              <span class="slider__text">до 1 000 000 р</span>
            </div>
          </div>

          <div class="calculator-period">
            <span class="calculator-period__title">Срок займа</span>
            <input class="calculator-period__input" type="text" placeholder="8" />
            <span class="calculator-period__months">месяцев</span>
          </div>

          <div class="slider-period">
            <input
              class="slider-period__input"
              type="range"
              min="2"
              max="12"
              v-bind:style="{
                background:
                  '-webkit-linear-gradient(left, #68b738 0%, #68b738 ' +
                  (inputRangePeriod - 2) +
                  '0%, #cacaca ' +
                  (inputRangePeriod - 2) +
                  '0%, #cacaca 0%)',
              }"
              v-model="inputRangePeriod"
            />
            <div class="slider__label">
              <span class="slider__text">от 2 месяцев</span>
              <span class="slider__text">до 12 месяцев</span>
            </div>
          </div>

          <span class="calculator-payment__text">
            Условия выдачи займа могут отличаться, исходя из анализа документов и состояния вашего автомобиля</span
          >
        </div>

        <div class="calculator-result">
          <div class="calculator-result__container">
            <div class="calculator-rate">
              <span class="calculator-rate__title">Ставка</span>
              <p class="calculator-rate__percent">2,7%</p>
            </div>
            <div class="calculator-paying">
              <span class="calculator-paying__title">Ежемесячный платеж</span>
              <div class="calculator-paying__container">
                <p class="calculator-paying__amount">3 729</p>
                <span class="calculator-paying__label">₽</span>
              </div>
            </div>
          </div>
          <button class="calculator-result__btn">Подать заявку</button>
          <span class="calculator-result__text">Расчет займа предварительный</span>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "CalculatorLoan",
  data() {
    return {
      inputRangeSum: 20,
      inputRangePeriod: 8,
    };
  },

  computed: {},

  methods: {},
};
</script>

<style lang="scss"></style>
