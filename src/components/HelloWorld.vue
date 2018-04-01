<template>
  <div class="main">
    <el-row :gutter="20">
      <el-col :span="12">
        <div class="card">
          <div class="graph">
            <ul>
              <li v-for="(item,index) in array" :key="index"
                  v-bind:style="{ height: item*5 + 'px' }">{{item}}
              </li>
              <!--<li>1</li>
              <li>1</li>
              <li>1</li>
              <li>1</li>
              <li >1</li>
              <li>1</li>
              <li>1</li>
              <li>1</li>
              <li>1</li>-->
            </ul>
          </div>
        </div>
      </el-col>
      <el-col :span="12">
        <div class="card">
          afeaw
        </div>
      </el-col>
    </el-row>
    <el-row :gutter="20">
      <el-col :span="12">
        <div class="card">
          as
        </div>
      </el-col>
      <el-col :span="12">
        <div class="card">
          af
        </div>
      </el-col>
    </el-row>
  </div>
</template>

<script>
  export default {
    name: 'HelloWorld',
    data() {
      return {
        array: [15, 8, 9, 7, 55, 2, 44, 66, 3, 26]
      }
    },
    methods: {
      sort() {
        for (let i = 0; i < this.array.length - 1; i++) {
          for (let j = 0; j < this.array.length - 1 - i; j++) {
            if (this.array[j] > this.array[j + 1]) {
              let k = j
              let temp = this.array[k];
              this.array[k] = this.array[k + 1];
              this.array[k + 1] = temp;
              this.array.reverse().reverse()
              console.log("joiojio")
            }

          }
        }
      }
    },
    mounted() {
      this.sort()
      /*setInterval(()=>{
        this.array[0] = this.array[0] +10
        this.array.reverse().reverse()
      },1000)*/
    }
  }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  .main {

  }

  .card {
    background: antiquewhite;
    height: 360px;
    margin-top: 10px;
  }

  .graph ul {
    display: inline-flex;
    position: absolute;
    bottom: 10px;
    align-items: flex-end;
    /*transform:rotate(180deg);*/
  }

  .graph ul > li {

    list-style: none;
    width: 20px;
    height: 60px;
    background-color: orangered;
    margin-left: 3px;
    margin-right: 3px;
  }
</style>
