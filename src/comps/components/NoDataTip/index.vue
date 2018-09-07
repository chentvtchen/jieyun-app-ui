<template>
    <!--没有数据时显示-->
    <div class="noDataTip" v-show="showFlag == true" :style="{ marginTop: top ? top+'px' : '40%'}">
        <img :src="imgUrl"/>
        <br/>{{msg}}
    </div>
</template>

<script>
    export default{
      name: 'noDataTip',
      props: {
        showFlag: {
          type: Boolean,
          default: false
        },
        msg: {
          type: String,
          default: '暂无数据'
        },
        top: {
          type: Number
        },
        imgUrl: {
          type: String,
          default: '../../../assets/myyy.png'
        }
      }
    }
</script>


<style lang="scss">
    .noDataTip {
        margin-top: 250px;
        text-align: center;
        font-size: 18px;
        color: #888;
        img {
            height: 80px;
        }
    }
</style>
