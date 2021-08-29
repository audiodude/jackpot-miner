<template>
  <div>
    <div class="hello">Hello Jackpot Miner!</div>
    <div>{{ count }}</div>
  </div>
</template>

<script lang="ts">
import { Options, Vue } from 'vue-class-component';

@Options({
  props: {
    msg: String,
  },
})
export default class HelloWorld extends Vue {
  msg!: string;

  get count(): number {
    return this.$store.state.count;
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped></style>
