<template>
    <el-row :gutter="10" class="nav" type="flex" justify="space-between">
        <el-col :xs="12" :sm="6" :md="4" :lg="3" :xl="1">
            <div class="grid-content logo ">
                <img src="../assets/images/min-logo.png"/>
                <img src="../assets/images/logo.png" class="hidden-xs-only"/>
            </div>
        </el-col>
        <el-col :xs="6" :sm="13" :md="8" :lg="9" :xl="11" class="hidden-xs-only">
            <div class="grid-content nav-menu">
                <router-link to="/"  class="nav-router">首页</router-link>
                <router-link to="/images"  class="nav-router">发现</router-link>
                <router-link to="/hub"  class="nav-router">社区</router-link>
                <router-link to="/blog"  class="nav-router">博客</router-link>
            </div>
        </el-col>
        <el-col :xs="6" :sm="2" :md="8" :lg="9" :xl="11" class="hidden-sm-and-down">
            <div class="grid-content search-input">
                <search-input></search-input>
            </div>
        </el-col>
        <el-col :xs="12" :sm="5" :md="4" :lg="3" :xl="1">
            <div class="grid-content   nav-menu-account">
                <el-row  span="24"  type="flex" justify="end">
                    <!--<el-col :span="6">-->
                        <div class="grid-content ">
                            <img class="account-logo" src="../assets/images/face.png"/>
                        </div>
                    <!--</el-col>-->
                    <!--<el-col :span="18">-->
                        <div class="grid-content  ">
                            <el-dropdown>
                    <span class="el-dropdown-link">
                    邵泽明
                        <i class="el-icon-arrow-down el-icon--right"></i></span>
                                <el-dropdown-menu slot="dropdown">
                                    <el-dropdown-item>个人中心</el-dropdown-item>
                                    <el-dropdown-item>我的账户</el-dropdown-item>
                                    <el-dropdown-item>我的博客</el-dropdown-item>
                                    <el-dropdown-item disabled>双皮奶</el-dropdown-item>
                                    <el-dropdown-item divided>蚵仔煎</el-dropdown-item>
                                </el-dropdown-menu>
                            </el-dropdown>
                        </div>
                    <!--</el-col>-->
                </el-row>
            </div>
        </el-col>
    </el-row>
</template>

<script>


    import SearchInput from '../components/Input/SearchInput.vue';

    export default {
        name: 'Nav',
        components: {
            SearchInput,
        }
    }
</script>


<style>
    .nav {
        margin-top: 15px;
    }

    .logo{
        text-align: left;
        margin-top: -5px;
    }
    .logo img {
        height: 40px;
    }

    .nav-menu{
        text-align: left;
        margin-top: -10px;
    }

    .nav-menu>a,.nav-router{
        display: inline-block;
        color: #100c0c;
        font-size: 18px;
        margin-left: 10%;
    }

    .nav-menu-account {
        text-align: right;
        margin-top: -10px;
        color: #100c0c;
    }



    .el-dropdown-link{
        font-size: 18px;
    }


    .account-logo {
        width: 40px;
        margin: 8px;
        border-radius: 50%;
    }




    .el-header {
        position: fixed;
        width: 100%;
        z-index: 1001;
        font-size: 12px;
        background-color: #409EFF;
        color: #606266;
        line-height: 60px;
    }


    .search-input{
        margin-top: -12px;
        text-align: right;
    }
</style>
