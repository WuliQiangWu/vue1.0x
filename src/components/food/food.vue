<template>
  <div v-show="showFlag" class="food" transition="move">
  </div>
</template>
<script>
  export default {
    props: {
      food: {
        type: Object
      }
    },
    computed: {},
    data () {
      return {
        showFlag: false
      };
    },
    methods: {
      show () {
        this.showFlag = true;
      }
    },
    components: {}
  };
</script>
<style lang="stylus" rel="stylesheet/stylus">
  .food
    position: fixed;
    left: 0
    top: 0
    bottom: 48px
    z-index: 30
    width: 100%
    background: #fff
    &.move-transition
      transform :translate3d(0, 0, 0)
      transition :all 0.3s linear
    &.move-enter, &.move-leave
      transform :translate3d(100%, 0, 0)
</style>
