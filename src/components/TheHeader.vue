<template>
  <header class="header">
    <h1 class="header__title">I tested It</h1>
    <TheNav></TheNav>

<!--     <Button></Button>
    <Button></Button> -->
  </header>
</template>

<script lang="ts">
import { Component, Prop, Vue } from 'vue-property-decorator'
import TheNav from '@/components/TheNav.vue'

@Component({
  components: {
  TheNav
  }
  })
export default class TheHeader extends Vue {
  @Prop()
  private msg!: string
}
</script>

<style lang='scss'>
  .header {
    background: green;
    padding: 40px;
  }

  .header__title {
    color: white;
    position: relative;
    &:after {
      content: '';
      width: 120%;
      height: 2px;
      position: absolute;
      top: 100%;
      left: 0;
      background: white;
    }
  }
</style>
