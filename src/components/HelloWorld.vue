<template>
  <div class="hello">

    <vxe-table resizable row-id="id" :data="tableData" :tree-config="{children: 'children'}" :checkbox-config="{labelField: 'name', checkRowKeys: [10053, 23666]}" @checkbox-change="selectChangeEvent">
      <vxe-table-column type="checkbox" title="Sex" width="400" tree-node></vxe-table-column>
      <vxe-table-column field="size" title="Size"></vxe-table-column>
      <vxe-table-column field="type" title="Type"></vxe-table-column>
      <vxe-table-column field="date" title="Date"></vxe-table-column>
    </vxe-table>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App',

      tableData: [
        {
          date: '2016-05-02',
          name: '王小虎',
          address: '上海市普陀区金沙江路 1518 弄'
        },
        {
          date: '2016-05-04',
          name: '王小虎',
          address: '上海市普陀区金沙江路 1517 弄'
        },
        {
          date: '2016-05-01',
          name: '王小虎',
          address: '上海市普陀区金沙江路 1519 弄'
        },
        {
          date: '2016-05-03',
          name: '王小虎',
          address: '上海市普陀区金沙江路 1516 弄'
        }
      ],
      tableData: [
        { id: 1000, name: 'vxe-table 从入门到放弃1', type: 'mp3', size: 1024, date: '2020-08-01' },
        {
          id: 1005,
          name: 'Test2',
          type: 'mp4',
          size: null,
          date: '2021-04-01',
          children: [
            { id: 24300, name: 'Test3', type: 'avi', size: 1024, date: '2020-03-01' },
            { id: 20045, name: 'vxe-table 从入门到放弃4', type: 'html', size: 600, date: '2021-04-01' },
            {
              id: 10053,
              name: 'vxe-table 从入门到放弃96',
              type: 'avi',
              size: null,
              date: '2021-04-01',
              children: [
                { id: 24330, name: 'vxe-table 从入门到放弃5', type: 'txt', size: 25, date: '2021-10-01' },
                { id: 21011, name: 'Test6', type: 'pdf', size: 512, date: '2020-01-01' },
                { id: 22200, name: 'Test7', type: 'js', size: 1024, date: '2021-06-01' }
              ]
            }
          ]
        },
        { id: 23666, name: 'Test8', type: 'xlsx', size: 2048, date: '2020-11-01' },
        { id: 24555, name: 'vxe-table 从入门到放弃9', type: 'avi', size: 224, date: '2020-10-01' }
      ]
    }
  },
  methods: {
    selectChangeEvent ({ records }) {
      console.info(`勾选${records.length}个树形节点`, records)
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1,
h2 {
  font-weight: normal;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
