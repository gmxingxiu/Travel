<template>
  <div>
    <div class="title">周末去哪儿</div>
    <ul>
      <li class="item border-bottom" v-for="item of recommendList" :key="item.id">
        <div class="item-wrapper">
          <img class="item-img" :src="item.imgUrl" >
        </div>
        <div class="item-info">
          <p class="item-title">{{item.title}}</p>
          <p class="item-desc">{{item.desc}}</p>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HomeWeekend',
  data () {
    return {
      recommendList: [{
        id: '0001',
        imgUrl: 'http://img1.qunarzz.com/sight/source/1505/85/708da4ab8dba17.jpg_r_640x214_d3d8cfa5.jpg',
        title: '青岛海昌极地海洋世界',
        desc: '最美极地海洋世界'
      }, {
        id: '0002',
        imgUrl: 'http://img1.qunarzz.com/sight/source/1505/85/708da4ab8dba17.jpg_r_640x214_d3d8cfa5.jpg',
        title: '青岛海昌极地海洋世界',
        desc: '最美极地海洋世界'
      }, {
        id: '0003',
        imgUrl: 'http://img1.qunarzz.com/sight/source/1505/85/708da4ab8dba17.jpg_r_640x214_d3d8cfa5.jpg',
        title: '青岛海昌极地海洋世界',
        desc: '最美极地海洋世界'
      }]
    }
  }
}
</script>

<style lang="stylus" scoped>
  @import '~styles/mixins.styl'
  .title
    margin-top: .2rem
    line-height: .8rem
    background: #eee
    text-indent: .2rem
    .item-img-wrapper
      overflow: hidden
      height: 0
      padding-bottom: 37.1%
    .item-img
      width: 100%
  .item-info
    padding: .1rem
    .item-title
      line-height: .54rem
      font-size: .32rem
      ellipsis()
    .item_desc
      line-height: .4rem
      color: #ccc
      ellipsis()
</style>
