#### VUE3

## INSTALL


## FEATURE

***學習文件
*[開發生態圈](https://github.com/vue3/vue3-News#%E8%BF%8E%E6%8E%A5Vue3.0%E7%B3%BB%E5%88%97)
*[Vue Compostition API](https://composition-api.vuejs.org/)
*[Vue Mastery Courses](https://www.vuemastery.com/courses-path/advanced) 
*[Object.defineProperty](https://juejin.im/post/5da29a87518825094e37301c)
*[exciting new features in Vue3](https://vueschool.io/articles/vuejs-tutorials/exciting-new-features-in-vue-3/)

VUE3

***為什麼要重寫？

I. 利用新語言的特性
ES proxy
框架允許偵聽元件的操作行為，並直接反應於DOM，提供更好的效能。
過去VUE2是透過setter getter屬性，做到直接反應，但無法檢測新產出的物件
但是新的特性是沒有辨法相容於舊版瀏覽器，仍需調整VUE3的框架以符合更多舊版瀏覽器

II. 重構基礎建設的問題
在維護vue2的過程中，發現幾個問題：
1. 很難製作適當的soure-map
2. 雖支援非DOM的渲染，但需拆分代碼庫而且重複一部分的代碼，然而為解決這個問題幾乎要重寫重構
3. 在模塊與浮動代碼間累積下來的技術債，看起不屬於任何地方，這些孤立的代碼使得維護人員更加難看懂


***有哪些新特性？

I. Suspense
頁面渲染完後，再將後備內容返回
[來自react的啟發](https://reactjs.org/docs/concurrent-mode-suspense.html)

II. Proxy Based Observers
使用proxy實現數據監聽
vue2採用Object.defineProperty，需使用遍歷取得元件的所有屬性,且新增屬性後要手動Observe
vue3採用proxy則可以直接代理元件，
但IE不支援，需透過[Polyfill](https://github.com/GoogleChrome/proxy-polyfill)

III. Composition API
取代了生命週期的寫法(Options API)
[Composition API文件](https://vue-composition-api-rfc.netlify.app/)

IV. Fragments (無根元件)

V. Global mounting/configuration API change

VI. Multiple v-models
VII. Portals
VIII. New custom directives API

Tree Shaking