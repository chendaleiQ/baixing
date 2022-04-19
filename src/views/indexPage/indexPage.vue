<template>
  <div class="indexPage">
    <el-row class="my-affix">
      <el-col class="my-icon">
        <el-image src="images/dizhi.png" fit="contain" alt=""/>
        门店地址
      </el-col>
      <el-col class="my-icon">
        <el-image src="images/zixun.png" fit="contain" alt=""/>
        植发咨询
      </el-col>
      <el-col class="my-icon">
        <el-image src="images/jiage.png" fit="contain" alt=""/>
        植发价格
      </el-col>
      <el-col class="my-icon">
        <el-image src="images/anli.png" fit="contain" alt=""/>
        索要案例
      </el-col>
      <el-col class="my-icon">
        <el-image src="images/fangansheji.png" fit="contain" alt=""/>
        方案设计
      </el-col>
      <el-col style="display: flex;justify-content: center">
        <div class="my-top" @click="backTop">
          TOP
        </div>
      </el-col>
    </el-row>
    <el-container>
      <el-header class="my-header">
        <el-row>
          <el-col :span="12">
            <img src="images/logo.png">
          </el-col>
          <el-col :span="12">
            <el-row>
              <el-col :span="16">
                <el-row>
                  <el-col :offset="10" :span="10">
                    <div class="my-tele">
                      <img src="images/tele.png" alt="">
                      <span>
                         400-888-6666
                      </span>
                    </div>
                  </el-col>
                </el-row>
                <el-row>
                  <el-col :span="4">首页</el-col>
                  <el-col :span="4">医院介绍</el-col>
                  <el-col :span="4">植发项目</el-col>
                  <el-col :span="4">医师团队</el-col>
                  <el-col :span="4">植发技术</el-col>
                  <el-col :span="4">全国连锁</el-col>
                </el-row>
              </el-col>
            </el-row>
          </el-col>
        </el-row>
      </el-header>
      <el-main>
        <el-row>
          <el-col>
            <img src="images/banner.png" class="my-banner" alt="">
          </el-col>
        </el-row>
        <!--        <el-carousel trigger="click" height="750px">-->
        <!--          <el-carousel-item v-for="item in 1" :key="item">-->
        <!--          </el-carousel-item>-->
        <!--        </el-carousel>-->
        <el-row class="my-product">
          <el-col :span="24">
            <h3>植发项目</h3>
            <h5>毛发终止有效解决您的毛发问题</h5>
            <el-row justify="center" class="my-product-content">
              <el-col :span="2" class="my-icon-content">
                <div class="my-icon">
                  <img src="images/meirenjian.png" alt="">
                </div>
                <p>美人尖种植</p>
              </el-col>
              <el-col :span="2" class="my-icon-content">
                <div class="my-icon">
                  <img src="images/fajixian.png" alt="">
                </div>
                <p>前额发际线</p>
              </el-col>
              <el-col :span="2" class="my-icon-content">
                <div class="my-icon">
                  <img src="images/dingbu.png" alt="">
                </div>
                <p>前额顶部</p>
              </el-col>
              <el-col :span="2" class="my-icon-content">
                <div class="my-icon">
                  <img src="images/xishu.png" alt="">
                </div>
                <p>稀疏</p>
              </el-col>
              <el-col :span="2" class="my-icon-content">
                <div class="my-icon">
                  <img src="images/bahen.png" alt="">
                </div>
                <p>疤痕</p>
              </el-col>
              <el-col :span="2" class="my-icon-content">
                <div class="my-icon">
                  <img src="images/meimao.png" alt="">
                </div>
                <p>眉毛种植</p>
              </el-col>
              <el-col :span="2" class="my-icon-content">
                <div class="my-icon">
                  <img src="images/huxu.png" alt="">
                </div>
                <p>胡须种植</p>
              </el-col>
              <el-col :span="2" class="my-icon-content">
                <div class="my-icon">
                  <img src="images/yishu.png" alt="">
                </div>
                <p>艺术种植</p>
              </el-col>
            </el-row>
          </el-col>

        </el-row>
        <el-row class="jishu">
          <el-col :span="24">
            <h3>百星六大技术</h3>
            <h5>百姓技术 匠心种植</h5>
            <el-row justify="center">
              <el-col :span="14">
                <el-carousel :interval="4000" type="card" height="500px" trigger="click">
                  <el-carousel-item v-for="item in technologys" :key="item" >
                    <div class="my-jishu">
                      <img :src="item.img" alt="">
                      <div class="jishu-content">
                        <h4>{{ item.title }}</h4>
                        <p>{{ item.content }}</p>
                      </div>
                    </div>
                  </el-carousel-item>
                </el-carousel>
              </el-col>
            </el-row>
          </el-col>
        </el-row>
        <el-row>
          <el-col :span="24">
            <img src="images/banner2.png" class="my-banner2" alt="">
          </el-col>
        </el-row>
        <el-row class="choose">
          <el-col :span="24">
            <h3>为什么选择我们</h3>
            <h5>始于尊贵，一对一接待服务，定制专属的会员式就诊流程</h5>
            <el-row justify="center" class="my-choose">
              <el-col :span="7">
                <img src="images/xuanze.png" alt="">
              </el-col>
              <el-col :span="9" class="my-choose-list">
                <el-row>
                  <el-col :span="4">
                    <div class="my-choose-icon">
                      <img src="images/sheji.png" alt="">
                    </div>
                  </el-col>
                  <el-col :span="20" class="my-choose-content">
                    <h4>慎于术前，一对一专业形象设计</h4>
                    <p>综合考虑发友个人实际情况，评估植发手术风险及预后，减少术中风险，定制个性化植发方案， 打造自然美发新高度。</p>
                  </el-col>
                </el-row>
                <el-row>
                  <el-col :span="4">
                    <div class="my-choose-icon">
                      <img src="images/zhiliao.png" alt="">
                    </div>
                  </el-col>
                  <el-col :span="20" class="my-choose-content">
                    <h4>精于术中，专业医生亲诊治疗</h4>
                    <p>精心、细致完善术前准备，以精湛的技术对待每一个珍贵的毛囊，采取精细先进的植发设备与 器械，降低毛囊损伤，提高毛囊成活率，以达到</p>
                  </el-col>
                </el-row>
                <el-row>
                  <el-col :span="4">
                    <div class="my-choose-icon">
                      <img src="images/baomi.png" alt="">
                    </div>
                  </el-col>
                  <el-col :span="20" class="my-choose-content">
                    <h4>勤于术后，VIP管理信息保密</h4>
                    <p>植发术后不可懈怠，熙朵始终坚持“以人为本”的经营理念，术后为发友提供完善的术后服务， 定期回访了解毛囊生长与恢复情况，切断术后</p>
                  </el-col>
                </el-row>
              </el-col>
            </el-row>
          </el-col>
        </el-row>
      </el-main>
      <el-footer class="my-footer">
        <el-row justify="center">
          <el-col :span="4">
            <el-row>
              <el-col class="my-footer-content">
                <h4>百星品牌</h4>
                <p>中国精品植发连锁品牌</p>
                <p>成为一家可持续发展的企业</p>
                <p>成为海内外知名植发连锁品牌之一</p>
                <p>成为植发行业口碑推荐医院</p>
              </el-col>

            </el-row>
          </el-col>
          <el-col :span="6">
            <el-row justify="center">
              <el-col :span="24" class="my-wechat">
                <h4>关注微信账号</h4>
                <el-row justify="center" class="my-wechat-content">
                  <el-col :span="8">
                    <img src="images/xuanze.png" alt="">
                    <p>百星医疗微信号</p>
                  </el-col>
                  <el-col :span="8">
                    <img src="images/xuanze.png" alt="">
                    <p>百星医疗微信号</p>
                  </el-col>
                </el-row>
              </el-col>
            </el-row>
          </el-col>
          <el-col :span="4" :offset="1">
            <el-row justify="end">
              <el-col class="my-footer-content">
                <h4>联系方式</h4>
                <p>
                  <el-image src="images/adress.png" alt=""/>
                  厦门市湖里区高新技术园安岭路 嘉园大厦808号
                </p>
                <p>
                  <el-image src="images/tele.png" alt=""/>
                  400-888-6666
                </p>
                <p>
                  <el-image src="images/mail.png" alt=""/>
                  https：//www.baixingyl.com
                </p>
              </el-col>
            </el-row>
          </el-col>
        </el-row>
        <el-row justify="center" class="my-footer-foot">
          <el-col>
            访问统计：浏览总量53414次 /今日浏览66次 即时通管理 后台登录 触屏版丨电脑版 建议(1024*768) IE8.0以
          </el-col>
        </el-row>
      </el-footer>
    </el-container>
  </div>
</template>

<script>

export default {
  name: 'indexPage',
  components: {},
  data() {
    return {
      translate: 0,
      transNum: 2,
      addTranslate: 0,
      technologys: [
        {img: 'images/xuanze.png', title: '巨量隐痕提取技术', content: '单次可提取5k-6k毛囊单位'},
        {img: 'images/xuanze.png', title: '活细胞种植技术', content: '用自体活细胞提炼技术种植到新的位置，唤醒毛囊活力'},
        {img: 'images/xuanze.png', title: '头发加密技术', content: '种植区不剃发，采用见缝插针的方式种植'},
        {img: 'images/xuanze.png', title: '不剃发技术', content: '种植区，提取区不剃发'},
        {img: 'images/xuanze.png', title: '多维毛囊移植技术', content: '针对毛囊不足的严重脱发患者，采用体毛腋毛，胡须部位的毛发移植到所需部位'},
        {img: 'images/xuanze.png', title: '艺术种植', content: '效果自然真实，立体感强'},
      ]
    }
  },

  // vue的两个生命钩子，这里不多解释。
// window对象，所有浏览器都支持window对象。它表示浏览器窗口，监听滚动事件
  mounted() {
    window.addEventListener('scroll', this.scrollToTop)
  },
  unmounted() {
    window.removeEventListener('scroll', this.scrollToTop)
  },
  methods: {
    backTop() {
      let timer = setInterval(() => {
        let ispeed = Math.floor(-this.scrollTop / 5)
        document.documentElement.scrollTop = document.body.scrollTop = this.scrollTop + ispeed
        if (this.scrollTop === 0) {
          clearInterval(timer)
        }
      }, 16)
    },
    // 为了计算距离顶部的高度，当高度大于60显示回顶部图标，小于60则隐藏
    scrollToTop() {
      let scrollTop = window.scrollY || document.documentElement.scrollTop || document.body.scrollTop
      this.scrollTop = scrollTop
      if (this.scrollTop > 0) {
        this.btnFlag = true
      } else {
        this.btnFlag = false
      }
    }
  }
}
</script>

<style lang="scss">
* {
  padding: 0;
  margin: 0;
}

#app {
  margin-top: 20px !important;
}

.el-main {
  --el-main-padding: 0 !important;
}

.indexPage {
  min-width: 1500px;
  box-sizing: border-box;

  h3 {
    font-size: 52px;
    font-weight: 800;
    color: #3C3C3C;
    line-height: 93px;
  }

  h5 {
    font-size: 26px;
    font-weight: 300;
    color: #3C3C3C;
    line-height: 69px;
  }

  .my-affix {
    display: flex;
    position: fixed;
    right: 30px;
    top: 300px;
    z-index: 99;
    width: 87px;
    height: 485px;
    background: #FFFFFF;
    border: 1px solid #DCDFE7;
    box-shadow: 0px 6px 5px 0px rgba(189, 88, 30, 0.09);
    border-radius: 44px;
    padding: 30px 10px 10px;

    .affix {
      display: flex;
      flex-direction: column;
      justify-content: space-between;
    }

    .my-icon {
      display: flex;
      flex-direction: column;

      img {
        height: 33px;
      }
    }

    .my-top {
      display: flex;
      align-items: center;
      justify-content: center;
      cursor: pointer;
      color: #fff;
      width: 38px;
      height: 38px;
      background: #02B2B5;
      border-radius: 50%;
    }
  }

  .my-header {
    margin-bottom: 20px;
  }

  .my-tele {
    display: flex;
    align-items: center;
    font-size: 24px;
    font-weight: bold;
    color: #3E4045;
    margin-bottom: 10px;
    text-align: right;

    img {
      background-color: #2471C8;
      padding: 5px;
      border-radius: 5px;
    }

    span {
      margin-left: 10px;
    }
  }

  .my-banner {
    width: 100%;
    height: 750px;
  }

  .my-product {
    padding: 30px 0;
    height: 450px;

    .my-product-content {
      margin-top: 60px;
    }

    .my-icon-content {
      display: flex;
      flex-direction: column;
      align-items: center;
    }

    p {
      font-size: 22px;
      font-weight: 500;
      color: #333333;
      line-height: 69px;
    }

    .my-icon {
      display: flex;
      justify-content: center;
      align-items: center;
      width: 92px;
      height: 92px;
      background: #CACACA;
      box-shadow: 0px 6px 5px 0px rgba(246, 247, 250, 0.3);
      border-radius: 50%;
    }
  }

  .jishu {
    height: 824px;
    background: #F6F7FA;
    padding-top: 100px;

    .scroll-button {
      display: flex;
      align-items: center;
      justify-content: center;
    }

    .my-scroll-contain {
      overflow: hidden;
      width: 60%;

      .my-scroll {
        transform: translateX(0);
        transition: all .5s;
      }
    }
  }

  .my-jishu {
    width: 100%;
    height: 100%;
    background-color: #fff;
    box-shadow: 0px 6px 12px 1px rgba(136, 147, 160, 0.1);
    //margin-right: 50px;

    img {
      width: 100%;
    }

    .jishu-content {
      display: flex;
      flex-direction: column;
      justify-content: space-between;
      margin-top: 20px;
      h4 {
        font-size: 24px;
        font-weight: bold;
        color: #3C3C3C;
        line-height: 24px;
        margin-bottom: 10px;
      }

      p {
        font-size: 16px;
        font-weight: 300;
        color: #3C3C3C;
        line-height: 24px;
      }
    }

  }

  .my-banner2 {
    width: 100%;
  }

  .choose {
    height: 757px;
    background: #F6F7FA;
    padding-top: 100px;

    .my-choose {
      margin-top: 50px;

      .my-choose-list {
        display: flex;
        flex-direction: column;
        justify-content: space-between;
        height: 329px;

        .my-choose-icon {
          display: flex;
          justify-content: center;
          align-items: center;
          width: 71px;
          height: 71px;
          background: #02B2B5;
          border-radius: 50%;
        }

        .my-choose-content {
          display: flex;
          flex-direction: column;
          text-align: left;

          h4 {
            font-size: 20px;
            font-weight: 500;
            color: #555555;
            margin-bottom: 10px;
          }
        }
      }


    }
  }

  .my-footer {
    position: relative;
    height: 315px;
    color: #fff;
    background: #555B67;

    .my-footer-content {
      display: flex;
      flex-direction: column;
      text-align: left;
      padding-top: 30px;
      //background: #fff;
      h4 {
        font-size: 24px;
        font-weight: 500;
        color: #FFFFFF;
        line-height: 69px;
      }

      p {
        display: flex;
        align-items: center;
        font-size: 14px;
        font-weight: 500;
        color: #FFFFFF;
        line-height: 31px;

        img {
          display: flex;
          align-items: center;
          width: 18px;
          margin-right: 10px;
        }
      }
    }

    .my-wechat {
      display: flex;
      flex-direction: column;
      width: 100%;
      height: 100%;
      padding-top: 30px;

      h4 {
        font-size: 24px;
        font-weight: 500;
        color: #FFFFFF;
        line-height: 69px;
      }

      .my-wechat-content {
        padding: 0 60px;
        border-right: 1px #6B717B solid;
        border-left: 1px #6B717B solid;

        img {
          width: 100px;
          height: 100px;
        }
      }
    }

    .my-footer-foot {
      margin-top: 30px;
      border-top: 1px #6B717B solid;
      line-height: 60px;
    }
  }

}
</style>
