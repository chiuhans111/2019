<template>
  <div>
    <div class="cfp-main-container">
      <div class="landing-bg" :style="{ 'transform' : `translate(${bg.x}px, ${bg.y}px) rotate(-30deg)`}"></div>
      <div class="cfp-paper-container">
        <div class="cfp-header">
          <div class="logo">
            <img src="@/assets/images/SVG/sitcon-box.svg" alt="">
            <img src="@/assets/images/SVG/stone.svg" alt="" class="egg" :class="{ 'activity': eggClickCount % 4 === 0 }">
            <div class="paper" @click="eggClickCount++" :class="{ 'activity': eggClickCount % 2 === 0 }">
              <h1>
                Call<br />
                for<br />
                paper
              </h1>
              <h3>&amp;sponsor</h3>
            </div>
          </div>
          <div class="content">
            <h1>
              Algorithm<br />
              in a box
            </h1>
            <h1>開箱演算法</h1>
            <div class="info-box date">
              <img src="@/assets/images/SVG/date-box.svg" alt="">
              <h2>3/24（日）</h2>
            </div>
            <div class="info-box place">
              <img src="@/assets/images/SVG/place-box.svg" alt="">
              <h2>
                中央研究院<br />
                人文社會科學館
              </h2>
            </div>
          </div>
        </div>
        <div class="cfp-content">
          <h2>關於 SITCON</h2>
          <p>
            SITCON 學生計算機年會係一學生自發組成的研討會，秉持著以學生為主軸的核心價值，藉以凝聚與傳遞學生的力量。希望藉由提供一個經驗交流與資訊技術實務分享的平台，使已有成就者能夠傳承己身經驗，嶄露頭角者在激盪中獲得靈感與啟發，並同時讓初入茅廬者得以對資訊科學有更深入的了解；進而達到「學以致用、教學相長」的目標。
          </p>
        </div>
        <div class="cfp-action">
          <div class="button" @click="openWindow('https://docs.google.com/forms/d/e/1FAIpQLSebYH6_wfpgBAyI9j6FZgW8u6MnkR686WbDXBEGDjButnxiGQ/viewform')">
            <h2>我要投稿</h2>
            <img src="@/assets/images/SVG/sitcon-mailbox.svg" width="70%" alt="">
          </div>
          <div class="button" @click="sponsor = true">
            <h2>我想贊助</h2>
            <img src="@/assets/images/SVG/sitcon-box-open.svg" alt="">
          </div>
        </div>
        <div class="cfp-content">
          <h2>重要資訊</h2>
          <ul>
            <li>即日起開始徵稿</li>
            <li>2019/01/14（一）06:40 投稿截止</li>
            <li>2019/02/03（日）審稿結束</li>
            <li>2019/02/13（三）公告完整議程</li>
          </ul>
          <p>
            有定時舉辦之投稿者小聚，<br />
            有問題或需投稿建議都歡迎寄信議程組 <a href="mailto:session@sitcon.org">session@sitcon.org</a>
          </p>
          <h2>年會主題</h2>
          <p>
            「Algorithm in a Box 開箱演算法」是 2019 的主題，投稿不一定要以此為主題，但若有與主題關聯之投稿，能夠與之相呼應，我們非常歡迎！
          </p>
          <p>
            「Algorithm in a Box」的「Box」發想自「黑箱 Black Box」，點出近年來我們的閱聽內容與生活愈發受到演算法支配，但我們卻無從得知，這些藏在黑箱中的演算法具體是什麼模樣；同時，「黑箱」也代表了只知其用法，卻對演算法的原理和細節不求甚解。另一方面，「Box」也可以解釋成「工具箱 Toolbox」，將演算法當成工具箱中的常備道具，也就是演算法的應用層面。我們希望能藉由「開箱」演算法，拆解「支配人們的演算法」的箱子，也要來拆解「不求甚解」的箱子、探究演算法的內涵與精神。
          </p>
          <h2>投稿主題範例</h2>
          <p>
            我們特別期待以學生為主體的投稿，可以是從學生角度出發的經驗分享、技術分享，或是探討學生相關議題等等，不過廣義來說，只要是與資訊技術、電腦相關的講題，都歡迎投稿！<br />
            以下的投稿範例可以提供一些靈感，或是您可以參與投稿者小聚，亦可前往 SITCON 前幾屆的網站（ <a target="_blank" href="https://sitcon.org/2013">2013</a> 、 <a target="_blank" href="https://sitcon.org/2014">2014</a> 、 <a target="_blank" href="https://sitcon.org/2015">2015</a> 、 <a target="_blank" href="https://sitcon.org/2016">2016</a> 、 <a target="_blank" href="https://sitcon.org/2017">2017</a> 、 <a target="_blank" href="https://sitcon.org/2018">2018</a> ）查看過去的議程。
          </p>
          <p>以下是我們以往的熱門議程，可供您參考：</p>
          <ul>Presentation：
            <li>奔跑吧！台北：遊戲開發經驗分享（<a href="https://sitcon.org/2018/#/agenda/sub/d946b6e1-d826-4c64-86a4-bf013bcc0c06" target="_blank">Link</a>、<a href="https://www.youtube.com/watch?v=85bW97XI4i0" target="_blank">Video</a>）</li>
            <li>Club Mate 與德國駭客精神：34C3 大會實錄（<a href="https://sitcon.org/2018/#/agenda/sub/35598abf-4efe-48fc-93a4-3d539e6f6c47" target="_blank">Link</a>、<a href="https://www.youtube.com/watch?v=8xrYLc4num8" target="_blank">Video</a>）</li>
            <li>由淺入坑區塊鏈～從認識架構到應用智能合約！（<a href="https://sitcon.org/2018/#/agenda/sub/08c2816d-ea25-4169-89e6-dc0e0bc7b9a4" target="_blank">Link</a>、<a href="https://www.youtube.com/watch?v=B3fXXElzc9Q" target="_blank">Video</a>）</li>
            <li>開發學校雲端服務的奇技淫巧（<a href="https://www.youtube.com/watch?v=msrsjX8mddE" target="_blank">Video</a>）</li>
            <li>校園資訊系統的困境與嘗試改善（<a href="https://www.youtube.com/watch?v=1N3HZsPzKrI" target="_blank">Video</a>）</li>
            <li>cjdns: 重新發明網路（<a href="https://sitcon.org/2017/#schedule-page" target="_blank">Link</a>、<a href="https://www.youtube.com/watch?v=l75ArFBCMlM" target="_blank">Video</a>）</li>
          </ul>
          <ul>Espresso：
            <li>校園駭客-看你學號() return 你家住址; （<a href="https://sitcon.org/2018/#/agenda/sub/b8998705-c6e2-4c48-ae76-984f23b54719" target="_blank">Link</a>、<a href="https://www.youtube.com/watch?v=yahEwM88q-Q" target="_blank">Video</a>）</li>
            <li>600秒學會UI設計（<a href="https://sitcon.org/2018/#/agenda/sub/d6daa14b-39ef-410b-883c-0b1c3ae02a60" target="_blank">Link</a>、<a href="https://www.youtube.com/watch?v=hqhmwt7SCJc" target="_blank">Video</a>）</li>
            <li>深度學習如何深度學習（<a href="https://sitcon.org/2018/#/agenda/sub/f3c6853d-2b0e-464c-8837-9411455961d8" target="_blank">Link</a>、<a href="https://www.youtube.com/watch?v=H5o5Oa_nbqs" target="_blank">Video</a>）</li>
            <li>格鬥遊戲 AI 開發經驗談（<a href="https://www.youtube.com/watch?v=ryLLzSwQ54w" target="_blank">Video</a>）</li>
            <li>第一次做光劍就上手（<a href="https://www.youtube.com/watch?v=vokwxRmT2WU" target="_blank">Video</a>）</li>
            <li>從零開始的線上字型（<a href="https://www.youtube.com/watch?v=HiQ35KuORFM" target="_blank">Video</a>）</li>
          </ul>
          <h2>Code of Conduct 行為準則</h2>
          <p>
            SITCON 非常歡迎女性、跨性別與多元背景的投稿者。為了讓大家都能愉快的參加 SITCON，我們鼓勵所有參與者閱讀年會的<a target="_blank" href="https://sitcon.org/code-of-conduct/">行為準則（Code of Conduct）</a>，共同創造一個友善的環境。
          </p>
          <h2>議程種類</h2>
          <h3>Presentation</h3>
          <p>
            Presentation 會有完整 30 分鐘的議程加上 10 分鐘的問答時間，讓您有充分的時間展示想法以及與會眾互動。
          </p>
          <h3>Espresso</h3>
          <p>
            Espresso 為包含問答時間僅有 10 分鐘的短講，挑戰講者提供最為濃縮與精華的議程。
          </p>
          <h2>投稿方式</h2>
          <p>
            稿件均經議程組形式審查，交予該領域之審稿委員審稿；審稿委員由業界人士、學界人士及 SITCON 議程組員組成。
          </p>
          <h3>格式</h3>
          <p>Espresso 與 Presentation 的投稿格式相同</p>
          <ul>
            <li><b>投稿類型</b>：必填，請寫明所欲投稿為 Presentation 或 Espresso。</li>
            <li><b>題目 Title</b>：必填，20 全形字以下。</li>
            <li><b>摘要 Abstract</b>：必填，含標點符號 150 ~ 250 全形字，使用於宣傳以及網站。</li>
            <li><b>演講大綱 Outline</b>：必填，請說明該議程的大綱以及時間長度規劃。</li>
            <li><b>目標受眾 Target Audience</b>：必填，請說明該演講的目標受眾為怎麼樣的人。</li>
            <li><b>詳細說明 Description</b>：必填，不限字數，請說明這個議程你認爲重要的相關細節，以利審稿委員更瞭解你的作品。我們強烈建議您詳細填寫此項，以增加入選機率。</li>
            <li><b>關鍵字 Key Words</b>：選填，請提供幾個與議程直接相關的關鍵字。</li>
            <li><b>附件 Attachment</b>：選填，可以附上程式碼、投影片草稿或任何你認爲有助於我們瞭解你的議程的附件。</li>
          </ul>
          <h3>個人資料</h3>
          <p>請至 Profile 中填寫，以下只列出必填項目</p>
          <ul>
            <li><b>電子郵件 Email</b>：能讓大會聯絡的電子信箱。</li>
            <li><b>暱稱／名字 Name</b>：公開於講者海報及網站的稱呼。</li>
            <li><b>電話號碼 Phone</b>：用於大會聯絡、確認資訊用的電話號碼。</li>
            <li><b>其他聯絡方式 Anything else we can contact you</b>：其他任何我們能聯絡您的方式。</li>
          </ul>
          <p>一個半形字元計為 0.5 個全形字元，一切投稿相關規定事項以本文件為準。</p>
          <h2>審稿方式</h2>
          <p>審稿委員主要針對以下項目進行篩選：</p>
          <ul>
            <li><b>稿件內容</b>：包含的知識分享、經驗案例、想法觀點是否獨特等；題目鼓勵與年會主題相關，但不影響評分。</li>
            <li><b>表達能力</b>：提供的資料是否有條理、文句暢通，提供資料（尤其是稿件的詳細說明）之完整度，我們偏好完整的資料，讓審稿委員更清楚了解演講細節。</li>
            <li><b>適合聽眾</b>：稿件是否適合 SITCON 大多數的會眾，若經我們評估比較小眾的議程可能會被安排至較小的演講廳。</li>
          </ul>
          <h2>投稿注意事項</h2>
          <ul>
            <li>SITCON 2019 採用 Google Forms 接收投稿。</li>
            <li>同一帳號僅能為一人使用，一人能投多份稿件。</li>
            <li>SITCON 2019 將會有 4 軌議程同時進行。</li>
            <li>上述審稿方式不考慮稿件內容的技術難度，我們仍以稿件是否能夠吸引人、高品質、適合聽眾（即上述篩選方式）為考量。</li>
            <li>為鼓勵投稿，大會提供投稿人一組邀請碼 （一人一組，非一稿一組），可優先報名參與本年會，獲選講者請使用講者身分入場，並可將邀請碼給他人使用。</li>
            <li>在截稿之前，投稿者可以隨時修改已投的稿件。</li>
            <li>SITCON 議程組得經作者同意，轉換 Presentation 或 Espresso 稿件之投稿類型。</li>
            <li>凡稿件經接受者，年會將頒予感謝狀以表彰投稿人之熱情付出與貢獻。</li>
            <li>議程題目跟摘要會放置於官網以及會前發行的電子報中。</li>
          </ul>
          <p>
            若有任何問題或需投稿建議請 Email 至 SITCON 議程組信箱 <a href="mailto:session@sitcon.org">session@sitcon.org</a>。
          </p>
          <h3>錄影以及記錄</h3>
          <p>
            所有議程皆會錄影並以 CC BY 3.0 授權釋出，若不希望被錄影與釋出可以與議程組聯絡。
          </p>
          <p>
            本屆 SITCON 提供入選講者試講及彩排的機會。試講除了讓大會工作人員先行對議程內容、演講習慣有初步了解外，也可以讓講者熟悉現場流程、找出能讓簡報更生動精采的模式。彩排則讓講者熟悉現場設備環境、攝影機位置，並且測試 Live Demo 情境。希望講者能夠共同參與試講及彩排，一起使年會議程品質更臻完美。
          </p>
          <h3>試講</h3>
          <p>
            試講讓講者在演講前有練習的機會，比照年會時間安排供講者講完整場演講，並有議程組人員提供建議（如簡報、台風等），講者可以自由參加，自行選擇最接近的場次，入選後將由議程組與您協調精確時間。
          </p>
          <p>
            所有場次將依報名情況舉辦，並提供投影機、音響、簡報筆、倒數計時器等設備。預計舉辦北部、中部、南部、東部場等，時間約為二月份或三月初，地點另行通知。
          </p>
          <p>
            補助：依照客運價格標準補助講者至最近試講場地的全額或部分車馬費。
          </p>
          <h3>彩排</h3>
          <ul>
            <li><b>日期</b>：2019/3/23（六）。</li>
            <li><b>場地</b>：使用場地與正式年會相同，細節將於稿件錄取後通知。</li>
            <li><b>時間</b>：一人約 5～10 分鐘，如有 Live Demo 或是特殊需求，可提前與議程組安排時間。</li>
            <li><b>流程</b>：講者可以嘗試操作設備，測試 Live Demo 連結及切換方式，也可以演練部分簡報內容。</li>
            <li><b>提供設備</b>：與年會當天場地的設備相同，有麥克風、倒數計時器、簡報筆等。</li>
          </ul>
          <h3>注意</h3>
          <ul>
            <li>除非內容明顯偏離講題或不符事實，我們不會要求講者對演講內容進行修正。</li>
            <li>為了維護所有講者的權利，試講時間恕不接受更改，請各位講者者準時參與。</li>
          </ul>
        </div>
        <div class="cfp-message" v-show="sponsor">
          <div class="close" @click="sponsor = false"></div>
          <div class="cfp-message-content">
            <img src="@/assets/images/SVG/stone-half.svg" alt="" class="cover-bg">
            <div class="close-btn">
              <img src="@/assets/images/SVG/close.svg" @click="sponsor = false" alt="">
            </div>
            <div class="content">
              <h2>贊助歡迎聯繫</h2>
              <p>SITCON 的運作，除了眾多努力的志工，也還是少不了金錢的支持。</p>
              <p>如果認同 SITCON 的理念與作為，歡迎加入成為支持 SITCON 運作的一份子！</p>
              <p class="split">
                <span>企業贊助</span>
                <a href="mailto:contact@sitcon.org">contact@sitcon.org</a>
              </p>
              <p class="split">
                <span>個人贊助</span>
                <a target="_blank" href="https://sitcon.kktix.cc/events/sitcon2019-individual-sponsor">個人贊助方案</a>
                <a target="_blank" href="https://sitcon.kktix.cc/events/sitcon2019-individual-sponsor1">個人贊助方案 — 純粹贊助</a>
              </p>
            </div>
          </div>
        </div>
      </div>
    </div>
    <Footer />
  </div>
</template>

<script>
import Footer from '@/components/CFPFooter.vue'
export default {
  data () {
    return {
      sponsor: false,
      bg: {
        x: 0,
        y: 0
      },
      eggClickCount: 1
    }
  },
  components: {
    Footer
  },
  mounted () {
    const deviceX = document.querySelector('html').clientWidth
    const deviceY = document.querySelector('html').clientHeight
    document.addEventListener('mousemove', (event) => {
      this.bgEffect(event.clientX, event.clientY, deviceX, deviceY)
    })

    this.metaSetter()
  },
  methods: {
    bgEffect (x, y, deviceX, deviceY) {
      this.bg.x = (x - (deviceX / 2)) * 0.05
      this.bg.y = (y - (deviceY / 2)) * 0.05
    },

    metaSetter () {
      let meta = document.querySelectorAll('meta')
      let title = document.querySelector('head>title')

      title.innerHTML = meta[2].content = '學生計算機年會 2019 徵稿｜SITCON 2019 CFP'
      meta[4].content = 'https://sitcon.org/2019/cfp/'
      meta[5].content = 'https://sitcon.org/2019/static/img/metaBanner-CFP.png'
    },

    openWindow (url) {
      window.open(url, '_blank')
    }
  }
}
</script>
