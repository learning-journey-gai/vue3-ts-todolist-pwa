<script setup lang="ts">
  import { ref } from "vue";
  const ALL = '全部'
  const UNDONE = '未完成'
  const DONE = '已完成'

  const tabs = ref<string[]>([ALL, UNDONE, DONE])

</script>

<template>
  <div class="container">
    <div class="header">
      <div class="tabs">
        <div class="tab" v-for="tab of tabs" :key="tab">{{tab}}</div>
      </div>
    </div>
    <div class="content">
      <ul class="list">
        <li class="item">吃饭</li>
        <li class="item">睡觉</li>
      </ul>
    </div>
    <div class="footer"></div>
  </div>
</template>

<style scoped lang="scss">
* {
  margin: 0;
  padding: 0;
  li {
    list-style: none;
  }
}
.container {
  margin: 0 auto;
  width: 340px;
  height: 600px;
  border: 1px solid skyblue;
  .tabs {
    display: flex;
    padding: 10px;
    justify-content: space-evenly;
    .tab {
      font-size: 20px;
      font-weight: 500;
      &:hover {
        cursor: pointer;
      }
    }
  }
  .list {
    padding: 10px 20px;
    text-align: left;
    .item {
      border: 1px solid khaki;
      padding: 8px;
    }
  }
}
</style>
