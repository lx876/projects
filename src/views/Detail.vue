<template>
    <div>
        <my-header></my-header>
        <div class="container">
    <!-- 面包屑导航 -->
    <div class="col-12 bg-transparent  my_breadcrumb pl-0 ">
      <ul class="breadcrumb list-unstyled bg-transparent p-0 mt-2">
        <li class="breadcrumb-item"><a class="text-secondary" href="#">商城首页</a></li>
        <li class="breadcrumb-item"><a class="text-secondary" href="#">"御" Mavic系列</a></li>
        <li class="breadcrumb-item"><a class="text-secondary" href="#">"御" Mavic 2 系列</a></li>
        <li class="breadcrumb-item"><a class="text-secondary" href="#">"御" Mavic 2</a></li>
      </ul>
    </div>
    <!-- 上半部分的布局，左右两个大盒子，分别占一半 -->
    <div class="row">
      <!-- 左边的一个面包屑导航和一个视频和一个图片 -->
      <div class="col-lg-6 col-sm-12 top_left" id="top-left">
        <!-- 视频 -->
        <div class="video_img mt-2" :class="fix" id="searchBar">
          <!-- <div id="img8" class=" abs" ><img class="w-100" src="./imgs/p5.jpeg" alt=""></div> -->
          <div id="img3" class=" abs"  v-show="imgs[0].img"><img  class="w-100"  src="./imgs/p2.jpg" alt=""></div>
          <div id="img2" class="abs"   v-show="imgs[1].img" ><img class="w-100" src="./imgs/p3.jpg" alt=""></div>
          <div id="img4" class=" abs"  v-show="imgs[2].img"><img class="w-100"   src="./imgs/p1.jpg" alt=""></div>
          <div id="img7" class="abs"   v-show="imgs[3].img"><img  class="w-100"  src="./imgs/p6.jpg" alt=""></div>
          <div id="img6" class=" abs"  v-show="imgs[4].img"><img  class="w-100" src="./imgs/p4.jpg" alt=""></div>
          <div id="img1" class="abs"   v-show="imgs[5].img" ><img class="w-100 " src="./imgs/p0.jpg"></div>
          <div id="img5" class="abs"   v-show="imgs[6].img"><img class="w-100"   src="./imgs/p7.jpg" alt=""></div>
          <video class="abs mt-2" id="video" muted controls autoplay v-show="imgs[7].img">
            <source src="../video/720.mp4" type="video/mp4">  
          </video>
          <div id="btns">
            <div class="row left_bottom justify-content-around px-5 abs_bottom">
              <div class="col-1 box_img_1 btn"></div>
              <div class="col-1 box_img_2 btn"  @click="change1"></div>
              <div class="col-1 box_img_3 btn" @click="change2"></div>
              <div  class="col-1 box_img_4 btn" @click="change3"></div>
              <div class="col-1 box_img_5 btn" @click="change4"></div>
              <div class="col-1 box_img_6 btn"  @click="change5"></div>
              <div  class="col-1 box_img_7 btn" @click="change6"></div>
              <div  class="col-1 box_img_8 btn" @click="change7"></div>
            </div>
          </div>
        </div>
        <!-- 视频下面的图片 -->
      </div>
      <div class="col-lg-6 col-sm-12 top_right" id="top-right">
        <div class="card bg-white border-0 ml-5">
          <!-- 头 -->
            <div class="card-header bg-white py-0 text-left">
              <p class="border-0 h2"> "御" Mavic 2 专业版</p> 
              <p class="h3 font-weight-normal my-3">￥9888</p>
              <p class="">邮费：免费</p>
              <a href="javascript:;" >分期最低月付￥453.20起</a>
            </div>
            <!-- 身体 -->
            <div class="card-body ml-2 py-0"> 
              <p class="mt-3 text-left">画质旗舰，变焦先锋。新一代消费级航拍旗舰之作。</p>
              <div class="row mt-4">
                <div class="col-2 "><ul class="list-unstyled">
                  <li >
                    <img class="w-100" src="../image/product_detail/1._哈苏相机.svg" alt="">
                  </li>
                  <li><img class="w-100 my-3" src="../image/product_detail/3._可调光圈.svg" alt=""></li>
                  <li><img class="w-100" src="../image/product_detail/4._10-bit_Dlog-M_色彩模式.svg" alt=""></li>
                </ul></div>
                <div class="col-4"><ul  class="list-unstyled">
                  <li>哈苏相机</li>
                  <li class="my-5">可调光圈</li>
                  <li>10-bit HDR 视频</li>
                </ul></div>
                <div class="col-2"><ul  class="list-unstyled ">
                  <li><img  class="w-100" src="../image/product_detail/2._1_英寸_CMOS.svg" alt=""></li>
                  <li><img class="w-100 my-3" src="../image/product_detail/4._10-bit_Dlog-M_色彩模式.svg" alt=""></li>
                  <li><img class="w-100" src="../image/product_detail/5._10-bit_HDR_视频.svg" alt=""></li>
                </ul></div>
                <div class="col-4"><ul  class="list-unstyled">
                  <li>1 英寸 CMOS</li>
                  <li class="my-5">Dlog-M 色彩模式</li>
                  <li>移动延时视频</li>
                </ul></div>
              </div>
              <!-- <div class=" ">
                <div class="d-flex">
                  <img src="./image/product_detail/1._哈苏相机.svg"class="w-50"  alt="">
                  <div class="w-50">哈苏相机</div>
                </div>
                <div class="d-flex">
                  <div><img src="./image/product_detail/1._哈苏相机.svg"class="w-50"  alt=""></div>
                  <div class="">哈苏相机</div>
                </div>
              </div> -->
            </div>
            <!-- 身体2 -->
            <div class="card-footer bg-white font-weight-normal">
              <h2 class="text-left">版本</h2>
              <div class="form-control mt-4 p-0 "><button class="btn w-100 bg-white p-2">专业版</button></div>
              <div class="form-control my-4 p-0"><button class="btn w-100 bg-white p-2">变焦版专业版</button></div>
              <div class="form-control my-4 p-0"><button class="btn w-100 bg-white p-2">专业版（ DJI带屏遥控器</button></div>
              <div class="form-control p-0 mb-4"><button class="btn w-100 bg-white p-2">变焦版（ DJI带屏遥控器）</button></div>
            </div>
            <!-- 脚 -->
            <div class="card-footer bg-white font-weight-normal mt-2">
              <div class="d-flex justify-content-between">
                <h2 class="">选择套装</h2>
                <a class="mt-2" href="javascript:;">包装清单对比</a>
              </div>
              <div class="form-control my-4 p-3"><button class="btn w-100 bg-white  d-flex">
                <div class="w-25"><img src="../image/product_detail/small_5ff80792-f403-4834-bf05-ac3e8b89be9b.jpg" alt=""></div>
                <p class="w-50 my-2 ml-2" >"御"Mavic 2专业版 <br>￥9888</p>
              </button></div>
              <div class="form-control my-4 p-0"><button class="btn w-100 bg-white  d-flex">
                <div class="w-25"><img class="w-100 ml-2" src="../image/product_detail/small_2c4c7e01-1117-4ada-a9a5-48c7b50432f2.png" alt=""></div>
                <p class="w-50 my-2 ml-2" >"御"Mavic2&DJI飞行眼镜竞速版 <br>￥12847</p>
              </button></div>
            </div>
            <!-- 脚 -->
            <div class="card-footer bg-white  ml-2 mb-4">
              <div class="bg-light py-3 pl-0 text-left">
                <a href="javascript:;">Select会员</a>
                <span>购买此机型可享5折及配件8折优惠</span>
              </div>
              <button class="bg-primary form-control w-50 p-3 my-2 "><router-link class=" text-white" to="/">开始选购</router-link></button>
              <p class="mt-4 text-secondary text-left ">发货时间：订单付款后1个工作日</p>
            </div>
        </div>
      </div>
    </div>
    <!-- 下面是选择卡导航 -->
    <ul class="nav nav-tabs mt-3">
      <li class="nav-item w-25 px-5 ml-4"><a class="nav-link" data-toggle="tab" href="#content1">产品预览</a></li>
      <li class="nav-item w-25 mx-5 px-5"><a class="nav-link" data-toggle="tab" href="#content2">包装清单</a></li>
      <li class="nav-item w-25 mx-5 px-5"><a class="nav-link" data-toggle="tab" href="#">常见问题</a></li>
    </ul>
    <div class="tab-content">
        <!-- content1的盒子 -->
      <div id="content1" class="mt-5 tab-pane active">
        <div class="row">
            <div class="col-9">
            <img src="../image/product_detail/895f41aa-8d5a-4226-8e73-c9119c87052a.jpg" class="w-100" alt="">
            <img src="../image/product_detail/aebbdc1c-1540-4f30-82f8-b264a7d02f90.jpg" class="w-100" alt="">
            <img src="../image/product_detail/710cba26-5ed9-42de-a0c4-0e28eec10b02.jpg" class="w-100" alt="">
            <img class="w-100" src="../image/product_detail/ff6a7d72-23c2-4325-8713-b3f42397f2a3.jpg" alt="">
            <img class="w-100" src="../image/product_detail/123913f6-2e93-4793-80fc-77bac0748444.jpg" alt="">
            <img class="w-100" src="../image/product_detail/647379fc-73a7-47dd-a04e-603f0637433d.jpg" alt="">
            <img class="w-100" src="../image/product_detail/72beba44-67d4-4002-a618-e84eb4a06fc0.jpg" alt="">
            <img class="w-100" src="../image/product_detail/d74b4b0e-dd0b-4e34-b893-88ef2c3cff38.jpg" alt="">
            <img class="w-100" src="../image/product_detail/bbc5983d-0de9-4074-a603-71af42294ab4.jpg" alt="">
            <img class="w-100" src="../image/product_detail/7c449011-9fb1-4967-af86-2bbfac3e987e.jpg" alt="">
            <img class="w-100" src="../image/product_detail/8edd1813-ee15-44de-a501-f6c3300cbe1c.jpg" alt="">
            <img class="w-100" src="../image/product_detail/c5b2064f-edc9-4efb-9d2e-c7f4c70f3bd3.jpg" alt="">
            <img class="w-100" src="../image/product_detail/cdcf7e9c-b190-484b-b7fe-5eeccfa5d4d9.jpg" alt="">
            <img class="w-100" src="../image/product_detail/43b5e123-1938-4f26-bc04-b4eec15152e3.jpg" alt="">
            <img class="w-100" src="../image/product_detail/25c91104-df9d-4564-8a93-e57499b8ae3e.jpg" alt="">
            <img class="w-100" src="../image/product_detail/c4a66d75-9844-4698-91e3-73b7db67e29e.jpg" alt="">
            <img class="w-100" src="../image/product_detail/64f23779-b45d-4a67-94af-c6a6744ec28b.jpg" alt="">
            <img class="w-100" src="../image/product_detail/a3fc375c-9515-4e3d-9f2d-206d90cf1ae1.jpg" alt="">
            <img class="w-100" src="../image/product_detail/6ac4af31-3839-49e9-ac5d-6ec2e6d4cd8e.jpg" alt="">
            <img class="w-100" src="../image/product_detail/0014736e-7115-4147-8e02-a6bb921a3d22.jpg" alt="">
            <img class="w-100" src="../image/product_detail/433ec3f8-780c-4971-a3b7-1416a9c553e3.jpg" alt="">
            <img class="w-100" src="../image/product_detail/7a198b9e-1f1b-4b89-9e6d-bf08f60f1905.jpg" alt="">
            <img class="w-100" src="../image/product_detail/ec20a876-a23f-44c6-b23e-b1c78e18b911.jpg" alt="">
            <img class="w-100" src="../image/product_detail/5170f9cf-3976-4eac-ab7b-e065ca5bb00a.jpg" alt="">
            <img class="w-100" src="../image/product_detail/ac81f46b-18a1-4e9e-b49e-154e5860c35c.jpg" alt="">
            <img class="w-100" src="../image/product_detail/4c1a5bb6-786a-409c-ba6f-9369765175a4.jpg" alt="">
          </div>
          <div class="col-3">
            <div class="row justify-content-between">
              <span class="pl-2 col-6 h3 font-weight-light">视频</span>
              <span class="col-6 mt-2"><a href="#">更多</a></span>
            </div>
            <div class="video1 my-2">
              <video class="w-100" id="video" controls >
                <source src="../video/720.mp4" type="video/mp4">  
              </video>
            </div>
            <div class="video2 my-2">
              <video class="w-100" id="video" controls >
                <source src="../video/720_1.mp4" type="video/mp4">  
              </video>
            </div>
            <!-- <div class="video3 my-2">
              <video class="w-100" id="video" controls autoplay>
                <source src="../video/720_5.mp4" type="video/mp4">  
              </video>
            </div> -->
            <div class="video4 my-2">
              <video class="w-100" id="video" controls >
                <source src="../video/720_3.mp4" type="video/mp4">  
              </video>
            </div>
            <div class="video5 my-2">
              <video class="w-100" id="video" controls autoplay>
                <!-- <source src="./video/720_4.mp4" type="video/mp4">   -->
              </video>
            </div>
            <div class="video6 my-2">
              <video class="w-100" id="video" controls >
                <source src="../video/720_2.mp4" type="video/mp4">  
              </video>
            </div>
          </div>
        </div>
      </div>
      <!-- content2的盒子 -->
      <div id="content2" class="tab-pane">
        <img class="w-100" src="../image/product_detail/3fcaaf7f-9cb2-46cd-a9d1-d28cd918f184.png" alt="">
      </div>
    </div>  
  </div>
        <my-footer></my-footer>
    </div>
</template>

<script>
export default {
    data(){
        return{
          s:"./imgs/p0.jpg",
          imgs:[
            {img:false},
            {img:false},
            {img:false},
            {img:false},
            {img:false},
            {img:false},
            {img:false},
            {img:true}
          ],
          fix:"",
        }
    },
    
    methods:{
      //监听滚动事件
      handleScroll(){
          var scrollTop = window.pageYOffset || document.documentElement.scrollTop || document.body.scrollTop;
          var scrollTop = window.pageXOffset || document.documentElement.scrollTop || document.body.scrollTop;
          console.log(scrollTop);
          var offsetTop = document.querySelector('#searchBar').offsetTop
          console.log("这是盒子的高"+offsetTop)
          if(scrollTop>150 && scrollTop<1220){
            this.fix="fixed"
          }else if(scrollTop>1220){
            this.fix="static"
          }else{
            this.fix=""
          }
      },
      change(){
        for(var i of this.imgs){
          if(i.img==true){
            i.img=false
          }
        }
      },
      change1(){
        this.change()
        this.imgs[0].img="true";
        console.log(111111)
      },
      change2(){
        this.change()
        this.imgs[1].img=true
      },
      change3(){
        this.change()
        this.imgs[2].img=true
      },
      change4(){
        this.change()
        this.imgs[3].img=true
      },
      change5(){
        this.change()
        this.imgs[4].img=true
      },
      change6(){
        this.change()
        this.imgs[5].img=true
      },
      change7(){
        this.change()
        this.imgs[6].img=true
      }
    },
    created(){
      window.addEventListener("scroll",this.handleScroll);
      console.log(222222)
    },
    
}
</script>
<style scoped>
.my_header,.my_footer{
  width:100%;
}
.fixed{
  position:fixed;
  top:0
}
.static{
  position: relative;
  top:1100px
}
/* 媒体查询
@media screen and (min-width:992px){
  .my_header{height:7rem;}
  .my_footer{height:30rem;}
}
@media screen and (max-width:991px)and (min-width:768px){
  .my_header{height:18rem;}
  .my_footer{height:30rem;}
}
@media screen and (max-width:767px){
  .my_header{height:27rem;}
  .my_footer{height:34rem;}
} */
.my_breadcrumb{
  font-size: 0.7rem;
}
.top_left,.top_right{
  position: relative;
  height:1517px;
}

.top_left>div{
  height:320px;
}
.left_bottom>div{
  height:35px;
  border:1px solid gray;
}
.box_img_1{
  background: url("../image/product_detail/small_e98ea3db-7910-4928-882a-757ee5b4f4ae.jpeg") no-repeat center;
  background-size: cover;
}
.box_img_2{
  background: url("../image/product_detail/small_547a09b9-1137-46e4-b806-8f9278ca84a1\ \(1\).jpg")no-repeat center;
  background-size: cover;
}
.box_img_3{
  background: url("../image/product_detail/small_258e3965-b6d4-4598-a7bc-ee4733c02410.jpg")no-repeat center;
  background-size: cover;
}

.box_img_4{
  background: url("../image/product_detail/small_4cb68b06-1b31-4369-9951-82b8f818b8c3.jpg")no-repeat center;
  background-size: cover;
}
.box_img_5{
  background: url("../image/product_detail/small_f732da2a-df74-4e81-acd3-23dde94846b8.jpg")no-repeat center;
  background-size: cover;
}
.box_img_6{
  background: url("../image/product_detail/small_547a09b9-1137-46e4-b806-8f9278ca84a1.jpg")no-repeat center;
  background-size: cover;
}
.box_img_7{
  background: url("../image/product_detail/small_2ea117f5-f9fe-4471-b03a-74427f065f2f.jpg")no-repeat center;
  background-size: cover;
}
.box_img_8{
  background: url("../image/product_detail/small_8e06abed-16b6-40b4-8f56-caf0ad88c584.png")no-repeat center;
  background-size: cover;
}
.btn{
  border-radius: 0;
}
.abs_bottom{
  margin-left: 15px;
  position: absolute;
  top: 360px;
  left: 5px;
  width: 511px;
  height: 30px;
}
.abs{
  margin-left: 15px;
  position: absolute;
  top: 0px;
  left: 0px;
  width: 540px;
  height: 312px;
}
.float{
  float:both;
}
</style>
