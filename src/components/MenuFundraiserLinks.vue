<template>
  <div class="mf-links">
    <a class="mf-link" :href="config.FUNDRAISER_URL">
      <i class="fa fa-external-link"></i> <strong>Open Fundraiser</strong>
    </a>
    <router-link class="mf-link" to="/blog/fundraiser-results">
      <i class="fa fa-hourglass-end"></i>
      Fundraiser Results
    </router-link>
    <!--
    <a class="mf-link" :href="docs.btc">
      <i class="fa fa-file-pdf-o"></i> BTC Tutorial
    </a>
    <a class="mf-link" :href="docs.ethWeb">
      <i class="fa fa-file-pdf-o"></i> ETH Web Tutorial
    </a>
    <a class="mf-link" :href="docs.ethMist">
      <i class="fa fa-file-pdf-o"></i> ETH Mist Tutorial
    </a>
    -->
    <a class="mf-link" :href="docs.terms">
      <i class="fa fa-file-pdf-o"></i> Contribution Terms
    </a>
    <a class="mf-link" href="http://slack.cosmos.network">
      <i class="fa fa-slick"></i>
      Discuss on Slack
    </a>
  </div>
</template>

<script>
import { mapGetters } from 'vuex'
export default {
  name: 'menu-fundraiser-links',
  computed: {
    ...mapGetters(['config', 'docs'])
  }
}
</script>

<style lang="stylus">
@require '../styles/variables.styl'

.mf-link
  padding 0.75rem 0
  color txt
  border-bottom 1px solid bc
  display flex
  align-items center
  user-select none
  &.disabled
    color light
    cursor not-allowed
    i.fa
      color light
    &:hover
      color light
  &:hover
    color link
  i.fa
    margin-right 0.5rem
    color dim
  .alert
    display flex
    align-items center
    background link
    color c-app-fg
    font-size 0.75rem
    padding 0 0.5rem
    border-radius 0.25rem
    height 1.5rem
    i.fa
      color c-app-fg
    i.fa + .ni-time-left
      margin-left 0.25rem
</style>
