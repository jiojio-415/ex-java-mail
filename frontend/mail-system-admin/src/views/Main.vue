<template>
  <el-container>
    <el-header>
      <Header/>
    </el-header>
    <el-aside>
      <Navbar/>
    </el-aside>
  </el-container>
</template>

<script>
  import Navbar from "../components/Navbar";
  import Header from "../components/Header";
    export default {
        name: "Main",
        components: {Header, Navbar},
        data() {
            return {
                activeIndex: '1',
                activeIndex2: '1',
                navList:[
                    {name:'/client',navItem:'客户管理'},
                    {name:'/server',navItem:'服务管理'},
                    {name:'/system',navItem:'系统参数设置'},
                ]
            };
        },
        methods: {
            handleSelect(key, keyPath) {
                console.log(key, keyPath);
            },
        }
    }
</script>

<style scoped>

</style>
