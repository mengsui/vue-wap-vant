<template>
  <div class="about">
    <van-search
      v-model="value"
      placeholder="请输入搜索关键词"
      show-action
      shape="round"
      @search="onSearch"
    >
      <div slot="action" @click="onSearch">搜索</div>
    </van-search>
  </div>
</template>

<script>
export default {
  data() {

    return {
      value: '哈哈',
    };
  },
  mounted(){
    console.log('交集');
    var arr1 = [1,3,4,5,6];
    var arr2 = [2,5];
    var arr = arr1.filter(item => {
      return !arr2.includes(item);
    });
    console.log(arr)
  },
  methods: {
    onSearch(event) {
      console.log(event);
    },
  }
};
</script>
