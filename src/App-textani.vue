<template>
  <div>
  <animated-number :value="value"  :duration="500"  :formatValue="formatToPrice" v-if="this.animateDisplayFlag" />
  <br>
  <input v-model="value" type="number" />
  <br>
  <br>
  <button type="button" @click="test"> dkslfk숫자 애니메이션</button>
  </div>
</template>
<script>
import AnimatedNumber from "animated-number-vue";
 
export default {
  components: {
    AnimatedNumber
  },
  data() {
    return {
      value: 0,
      animateDisplayFlag: false
    };
  },
  methods: {
    formatToPrice(value) {
      return `${Number(value).toFixed(0)}`;
    },
    test(){
      this.animateDisplayFlag = true;
    }
  }
};
</script>