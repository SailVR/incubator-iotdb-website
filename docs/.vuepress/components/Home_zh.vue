<template >
  <div style="background:linear-gradient(top,#A2A2A2,#fff);">

    <gh-btns-fork slug="vuejs/vue" show-count></gh-btns-fork>
    
    <div style="width:100%;margin: 0 auto;position: relative;height:480px;text-align:center;">
      <h2 class="h2">Apache IoTDB</h2>
      <p
        style="font-size: 20px;line-height:23px;margin: 10px 0 20px 0;font-family: 'Arimo', sans-serif;
    text-transform: uppercase;
    font-weight: 700;
    letter-spacing: 0.03em;
    color: #777;
    text-align: center;"
      >(孵化中)物联网数据库</p>
      <p style="font-size: 20px;margin: 50px 0 10px 0;text-align:justify!important;">
Apache IoTDB（孵化中）（物联网数据库）是一个集成数据专为时间序列数据设计的管理引擎。 它为用户提供以下服务数据收集，存储和分析。 由于其轻巧的结构，高性能和丰富的功能集，以及与Apache的深度集成Hadoop和Spark，Apache IoTDB（孵化中）可以满足海量需求物联网中的数据存储，高速数据提取和复杂数据分析工业领域。
      </p>
      <el-row style="margin-top:40px;text-align: center;">
        <el-button
          type="warning"
          round
          style="width:220px;
    font-size: 18px;    letter-spacing: 0.03em;font-family: 'Arimo', sans-serif;"
          @click="addRoutes1"
        >下载</el-button>
        <el-button
          type="info"
          round
          style="width:220px;
    font-size: 18px;    letter-spacing: 0.03em;font-family: 'Arimo', sans-serif;"
          @click="addRoutes2"
        >快速开始</el-button>
      </el-row>
    </div>



    <p class="home-title" style="font-size: 50px;">应用场景</p>

    <div class="block">
        <el-carousel trigger="click" height="700px">
          <el-carousel-item v-for="item in imgBlock" :key="item">
            <img :src="item.src" alt="">
            <h3 style="font-size: 30px;color: #fcac45;text-align: center;line-height: 0px;">{{item.des}}</h3>
            <p style="font-size: 18px;padding:10px;line-height: 22px;text-align:justify!important;font-weight:bold;">{{item.detail}}</p>
          </el-carousel-item>
        </el-carousel>
    </div>

    <p class="home-title" style="font-size: 50px;">主要特点</p>

    <el-row style="margin-top:50px;" :gutter="20">
      <el-col :span="8" style="text-align:center;">
          <el-popover
            placement="top-start"
            title="高吞吐量读写"
            width="350"
            trigger="hover"
            content="Apache IoTDB（孵化中）可以支持数百万个低功耗和智能联网设备的高速写访问。 它还提供闪电读取访问权限以检索数据。"
            >
            <el-button slot="reference" style="text-align:center;width:100%;">
              <img src="/img/home-icon1.png" style="width:40px;height:40px;">
              <p>高吞吐量读写</p>
              </el-button>
          </el-popover>
      </el-col>
      <el-col :span="8" style="text-align:center;">
          <el-popover
            placement="top-start"
            title="高效的目录结构"
            width="350"
            trigger="hover"
            content="Apache IoTDB（孵化中）可以使用模糊搜索策略针对时间序列数据的复杂目录有效地组织来自IoT设备和大量时间序列数据的复杂数据结构。"
            >
            <el-button slot="reference" style="text-align:center;width:100%;">
              <img src="/img/home-icon2.png" style="width:40px;height:40px;">
             <p> 高效的目录结构</p></el-button>
          </el-popover>
      </el-col>
      <el-col :span="8" style="text-align:center;">
          <el-popover
            placement="top-start"
            title="丰富的查询语义"
            width="400"
            trigger="hover"
            content="Apache IoTDB（孵化中）可以支持跨设备和传感器的时间序列数据的时间对齐，时间序列字段中的计算以及时间维度上的丰富聚合功能。"
            >
            <el-button slot="reference" style="text-align:center;width:100%;">
             <img src="/img/home-icon3.png" style="width:40px;height:40px;">
             <p>丰富的查询语义</p></el-button>
          </el-popover>
      </el-col>
    </el-row>

    <el-row style="margin-top:100px;height:300px;" :gutter="20">
      <el-col :span="8" style="text-align:center;">
          <el-popover
            placement="top-start"
            title="硬件成本低"
            width="400"
            trigger="hover"
            content="Apache IoTDB（孵化中）可以达到磁盘存储的高压缩率（将1GB数据存储在硬盘上的成本不到0.23美元）。"
            >
            <el-button slot="reference" style="text-align:center;width:100%;">
             <img src="/img/home-icon4.png" style="width:40px;height:40px;">
             <p>硬件成本低</p></el-button>
          </el-popover>
      </el-col>
      <el-col :span="8" style="text-align:center;">
          <el-popover
            placement="top-start"
            title="灵活的部署"
            width="400"
            trigger="hover"
            content="Apache IoTDB（孵化中）可以为用户提供云上的一键式安装工具，桌面上的终端工具以及云平台与本地计算机之间的桥接工具（数据同步工具）。"
            >
            <el-button slot="reference" style="text-align:center;width:100%;">
             <img src="/img/home-icon5.png" style="width:40px;height:40px;">
             <p>灵活的部署</p></el-button>
          </el-popover>
      </el-col>
      <el-col :span="8" style="text-align:center;">
          <el-popover
            placement="top-start"
            title="与开源生态系统的紧密集成"
            width="400"
            trigger="hover"
            content="Apache IoTDB（孵化中）可以支持分析生态系统，例如Hadoop，Spark和Grafana作为可视化工具。"
            >
            <el-button slot="reference" style="text-align:center;width:100%;">
             <img src="/img/home-icon6.png" style="width:40px;height:40px;">
             <p>与开源生态系统的紧密集成</p>
            </el-button>
          </el-popover>
      </el-col>
    </el-row>

  </div>
</template>

<script>
export default {
  name: "Home",
  data() {
    return {
      msg: "Welcome to Home Page",
      imgBlock:[
        {
          src: "/img/home-Slide1.png",
          des:"高端设备",
          detail:"在高端制造业中，有很多设备配备有传感器来收集工作状态数据，气象站，风力涡轮机是常见的高端设备，这些设备如果支持Java或Go（正在开发中），则可以运行TsFile在本地存储数据 通过这种方式，TsFile可以提供具有高吞吐量，高压缩率和毫秒查询的数据保存功能。结合TsFile-Sync工具，可以将TsFiles传输到数据中心。"
        },
        {
          src: "/img/home-Slide2.png",
          des:"本地控制器",
          detail:"在工厂现场，LAN网络下有数十台设备。 IoTDB可以安装在工厂的本地控制器服务器上，以从这些设备接收数据。 具有IoTDB的本地控制器服务器（普通PC或工作站）可以使用类似于SQL的界面保留数据和查询数据。 此外，使用TsFile-Sync工具，可以将本地控制器上的TsFiles传输到云中配备IoTDB实例的数据中心。"
        },
        {
          src: "/img/home-Slide3.png",
          des:"云数据管理",
          detail:"在高速网络（车联网等）的场景中，安装有传感器的汽车可以以一定频率收集自身的监视信息（行驶状态等）。 通常，这些汽车设备的硬件配置有限，并且难以进行复杂的应用。 轻量级的IoTDB（IoTDB客户端）应运而生。 借助JDBC API，它可以使窄带IoT或4G发送数据。 这样，设备和云连接在一起。"
        },
      ],
      isHover: false
    };
  },
  methods: {
    hover: function(e) {
      e.currentTarget.style.boxShadow = "2px 2px 10px #909090";
      e.currentTarget.firstElementChild.style.marginTop = "0px";
      e.currentTarget.firstElementChild.nextElementSibling.style.display =
        "block";
    },
    unhover: function(e) {
      e.currentTarget.style.boxShadow = "";
      e.currentTarget.firstElementChild.style.marginTop = "60px";
      e.currentTarget.firstElementChild.nextElementSibling.style.display =
        "none";
    },

    addRoutes1() {
      this.$router.push("/zh/download/");
    },
    addRoutes2() {
      this.$router.push("/zh/document/V0.9.x/UserGuide/1-Overview/1-What%20is%20IoTDB.html");
    }
  }
};
</script>

<style scoped>

  .el-row {
    margin-bottom: 20px;
    height: 50px;
    &:last-child {
      margin-bottom: 0;
    }
  }
  .el-row p{
    font-size: 18px;
  }
  .el-col {
    border-radius: 4px;

  }
  .bg-purple-dark {
    background: #99a9bf;
  }
  .bg-purple {
    background: #d3dce6;
  }
  .bg-purple-light {
    background: #e5e9f2;
  }
  .grid-content {
    border-radius: 4px;
    min-height: 36px;
  }
  .row-bg {
    padding: 10px 0;
    background-color: #f9fafc;
  }

  .el-carousel__item:nth-child(2n) {
     background-color: #99a9bf;
  }
  
  .el-carousel__item:nth-child(2n+1) {
     background-color: #d3dce6;
  }


@media (min-width: 200px) {
  .carousel-inner {
    min-height: 530px;
  }
}

@media (min-width: 768px) {
  .feature-item {
    min-height: 220px;
  }
  .carousel-inner {
    min-height: 520px;
  }
}

@media (min-width: 992px) {
  .feature-item {
    min-height: 240px;
  }
  .carousel-inner {
    min-height: 580px;
  }
}

@media (min-width: 1200px) {
  .feature-item {
    min-height: 210px;
  }
  .carousel-inner {
    min-height: 650px;
  }
}


.Scenarios {
  padding: 5px 10px;
  color: white;
  margin-left: 10px;
  margin-right: 10px;
}

h2 {
  margin: 0 auto;
  padding: 0 5%;
  opacity: 0.9;
  color: #3f3b3f;
  font-size: 108px;
  text-align: center;
  text-transform: none;
  font-weight: 700;
  letter-spacing: 0.03em;
}

  .home-title {
    color: #ffa500;
    font-size: x-large;
    font-weight: 600;
    text-align: center;
  }
</style>
