<template>
  <main class="main-content">
    <Text
      title="Simple, traffic-based pricing"
      paragraph="Sign-up for our 30-day trial. No credit card required."
    />
    <div class="main-content--price-module">
      <PriceControl />
      <div class="advantages-and-button">
        <AdvantagesList
          item1="Unlimited websites"
          item2="100% data ownership"
          item3="Email reports"
        />
        <Button text="Start my trial" />
      </div>
    </div>
  </main>
</template>

<script>
import Text from "./components/Text.vue";
import AdvantagesList from "./components/AdvantagesList.vue";
import Button from "./components/Button.vue";
import PriceControl from "./components/PriceControl.vue";


export default {
  components: {
    Text,
  },
};
</script>

<style lang="scss" scoped>
@import "./style.scss";

.main-content {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  width: 100%;
  height: 100vh;
  margin-bottom: 30px;

  .main-content--price-module {
    background-color: $neutral-very-pale-blue;
    width: 100%;
    max-width: 590px;
    border-radius: 10px;
    box-shadow: 0 20px 25px -5px rgba(0, 0, 0, 0.1),
      0 10px 10px -5px rgba(0, 0, 0, 0.04);
  }
}

@media only screen and (max-width: $mobile) {
  .main-content {
    .main-content--price-module {
      max-width: 320px;
      padding: 20px;
    }
  }
}

.advantages-and-button {
  width: 100%;
  max-width: 600px;
  padding: 30px 50px;
  display: flex;
  justify-content: space-between;
  align-items: center;
}

@media only screen and (max-width: $mobile) {
  .advantages-and-button {
    flex-direction: column;
    justify-content: center;
  }
}
</style>
