<template>
  <el-select v-model="value" placeholder="请选择">
    <el-option-group
      v-for="group in options"
      :key="group.label"
      :label="group.label">
      <el-option
        v-for="item in group.options"
        :key="item.value"
        :value="item.value">
        <div class="flex flex-between">
          <span>item.label</span>
          <i class="el-icon-star-on" @click=""></i>
        </div>
      </el-option>
    </el-option-group>
  </el-select>
</template>

<script>
export default {
  data() {
    return {
      options: [{
        label: '热门城市',
        options: [{
          value: 'Shanghai',
          label: '上海'
        }, {
          value: 'Beijing',
          label: '北京'
        }]
      }, {
        label: '城市名',
        options: [{
          value: 'Chengdu',
          label: '成都'
        }, {
          value: 'Shenzhen',
          label: '深圳'
        }, {
          value: 'Guangzhou',
          label: '广州'
        }, {
          value: 'Dalian',
          label: '大连'
        }]
      }],
      value: ''
    }
  }
}
</script>
<style scoped>

</style>
