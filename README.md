# 2022-HexSchool-Layout---week7

2022 六角切版直播班 - 第七週

本週學習重點：

<b>1. animation</b>
  - [基本範例](https://codepen.io/liao/pen/JjYwNVW?editors=1100)
    - `animation-name`：要執行的 animation 名稱
    - `animation-duration`：要執行 animation 過程的秒數
  - [移動速率](https://codepen.io/liao/pen/gOaZWyj?editors=1100) 
    - `@keyframes class名稱{ 起點 - 終點 }`：可以放多個數值
    - `animation-delay`：要執行的 animation 晚幾秒啟動
    - `animation-iteration-count`：要執行的 animation 要重複執行幾次（直接寫數字即可），或是用 infinite 可以持續執行（不建議放太大的圖檔太吃效能）
  - [完整解析css動畫](https://www.oxxostudio.tw/articles/201803/css-animation.html)
  - [animation-fill-mode](https://www.w3cplus.com/css3/understanding-css-animation-fill-mode-property.html)
    - `forwards`：停留在最後一個位置
    - `backwards`：回到原本位置
    - `both`：擁有上面兩個的功能
  - [Animation.css](https://animate.style/)
  
<b>2. [transform](https://codepen.io/liao/pen/VwvqWZQ) 很適合用來做動畫效果，因為移動時不會影響其他元素推擠</b>
    - `transform: rotate(旋轉角度deg);`
    - `transform: scale(放大幾倍);`
    - `transform: translateX(水平移動幾px);`
    - `transform: translateY(垂直移動幾px);`
    
<b>3. [opacity](https://codepen.io/liao/pen/jObXwPN) 半透明效果</b>

<b>4. [AOS](https://michalsnik.github.io/aos/) 當滑鼠滾到對應位置時會出現class動畫效果</b>
  - [範例](https://codepen.io/liao/pen/PoPXKvm)
  - 載入步驟
    - 在 </body>前加上以下程式碼
    ```
    <link href="https://unpkg.com/aos@2.3.1/dist/aos.css" rel="stylesheet">
    <script src="https://unpkg.com/aos@2.3.1/dist/aos.js"></script>
    <script>
      AOS.init();
    </script>
    ```
    - AOS單一設計
    ```
    <div
      data-aos="fade-up"
      data-aos-offset="200"
      data-aos-delay="50"
      data-aos-duration="1000"
      data-aos-easing="ease-in-out"
      data-aos-mirror="true"
      data-aos-once="false"
      data-aos-anchor-placement="top-center">
    </div>
    ```
    - AOS 全域設計
    ```
    AOS.init({
      // Global settings:
      disable: false, // accepts following values: 'phone', 'tablet', 'mobile', boolean, expression or function
      startEvent: 'DOMContentLoaded', // name of the event dispatched on the document, that AOS should initialize on
      initClassName: 'aos-init', // class applied after initialization
      animatedClassName: 'aos-animate', // class applied on animation
      useClassNames: false, // if true, will add content of `data-aos` as classes on scroll
      disableMutationObserver: false, // disables automatic mutations' detections (advanced)
      debounceDelay: 50, // the delay on debounce used while resizing window (advanced)
      throttleDelay: 99, // the delay on throttle used while scrolling the page (advanced)
      

      // Settings that can be overridden on per-element basis, by `data-aos-*` attributes:
      offset: 120, // offset (in px) from the original trigger point
      delay: 0, // values from 0 to 3000, with step 50ms
      duration: 400, // values from 0 to 3000, with step 50ms
      easing: 'ease', // default easing for AOS animations
      once: false, // whether animation should happen only once - while scrolling down
      mirror: false, // whether elements should animate out while scrolling past them
      anchorPlacement: 'top-bottom', // defines which position of the element regarding to window should trigger the animation

    });
    ```
      - `once` 如果滑鼠滾來滾去動畫只想要出現一次時可以改成true
      - `duration` 建議設置400-800毫秒間
      - `offset` 指要距離多少時會出現下一個動畫，建議80-120-150px
      
<b>5. [hover.css](https://ianlunn.github.io/Hover/)</b>

<b>6. [CSShake](http://elrumordelaluz.github.io/csshake/)</b>
  
