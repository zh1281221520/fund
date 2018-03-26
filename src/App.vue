<template>
  <div id="app">
        <!-- 头部 -->
        <div id="top">
          <!-- 中间文字需要修改未做 -->
          <mt-header fixed >
                <router-link to="/" slot="left" >
                <mt-button icon="back">返回</mt-button>
                </router-link>
                <h1 class="mint-header-title">{{title1}}</h1>
                <mt-button icon="more" slot="right" >
                </mt-button>
          </mt-header>
                <!-- 选项卡 -->
                <!-- navbar -->  
                <mt-navbar class="page-part" v-model="selected">  
                  <mt-tab-item id="客户管理">
                    <router-link to="/f_conMage" >客户管理
                    </router-link>
                  </mt-tab-item>  
                  <mt-tab-item id="基金产品管理">
                    <router-link to="/f_prodect" >基金产品管理
                    </router-link>                
                  </mt-tab-item>  
                  <mt-tab-item id="基金经理管理">
                    <router-link to="/f_manager" >基金经理管理
                    </router-link>
                  </mt-tab-item>
                  <mt-tab-item id="客户基金交易">
                    <router-link to="/f_transaction" >客户基金交易
                    </router-link>
                  </mt-tab-item>  
                </mt-navbar>        
        </div>
        <!-- 中部 -->
        <div class="middle">
              <router-view/>
        </div>
        <!-- 底部 -->
        <div class="bottom_one">
                  <div class="footer_container">
                  <div class="footer_list">
                    <p data-skipsinglepage="aboutus">关于我们</p>
                    <span></span>
                    <p data-skipsinglepage="contactus">联系我们</p>
                    <span></span>
                    <p data-skipsinglepage="feedback">意见反馈</p>
                    
                    
                  </div>
                  
                  
                  <p class="footer_hotline">
                    客服热线：<a href="tel:95021">18119340274</a>
                    
                  </p>
                  <p class="footer_tips">工作日：7:30-21:30 双休日：9:00-21:00</p>
                </div>
        </div>
  </div>
</template>

<script>
export default {
  name: 'App',
  data: function(){
    return {
      title1:'测试'
  };
  }
}
</script>

<style scoped>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
  font-size:18px;
}
div,body,span,p
  {
    margin: 0;
    padding: 0;
    border: 0;
    vertical-align: baseline;
    font: inherit;
    -webkit-touch-callout: none;
    -webkit-user-select: none;
    -moz-user-select: none;
    -ms-user-select: none;
    user-select: none;
}

  .mint-header{
    height: 3em;
    line-height: 2em;
    font-size:18px;
  }
  /*头部*/
  
.router-link-active {
    text-decoration: none;
}

  /*底部*/
  .bottom_one{
    
    position:absolute;
    left:0;
    right:0;
    bottom:0;
    height:2em;
    line-height:2em;
    text-align:center;
    color:#FFFFFF;
  }
  .footer_list{
           display:flex;
           padding: 0.5em 0;
           border-top: 1px solid #dfdfdf;
           border-bottom: 1px solid #dfdfdf;

  }
  .footer_list p {
    -webkit-flex: 1;
    -ms-flex: 1;
    flex: 1;
    color: #959595;
    font-size: 14px;
    text-align: center;
    line-height: 20px;
}
.footer_list span {
    width: 1px;
    background: #D7CFCF;
    display: block;
}
p {
    display: block;
    -webkit-margin-before: 1em;
    -webkit-margin-after: 1em;
    -webkit-margin-start: 0px;
    -webkit-margin-end: 0px;
}
 .footer_hotline {
    text-align: center;
    font-size: 14px;
    color: #959595;
    margin-bottom: 8px;
}
 .footer_tips {
    text-align: center;
    font-size: 12px;
    color: #959595;
    margin: 7px 0;
}

</style>
