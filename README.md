### 一、创建项目

1. 打开WebStorm软件，【新建】->【Empty Project】 Location选择创建好的项目文件夹

2. 打开下面的Terminal窗口，按如下输入

   ```
   C:\mywork\Workspaces\githubPro\vicente-demo-vue>cd ..
   C:\mywork\Workspaces\githubPro>vue init webpack vicente-demo-vue

   ? Target directory exists. Continue? Yes
   ? Project name vicente-demo-vue
   ? Project description A Vue.js project
   ? Author shiweisen <shiweisen@bluemoon.com.cn>
   ? Vue build standalone
   ? Install vue-router? Yes
   ? Use ESLint to lint your code? No
   ? Set up unit tests No
   ? Setup e2e tests with Nightwatch? No
   ? Should we run `npm install` for you after the project has been created? (recommended) npm

   C:\mywork\Workspaces\githubPro>cd vicente-demo-vue
   C:\mywork\Workspaces\githubPro\vicente-demo-vue>cnpm install
   C:\mywork\Workspaces\githubPro\vicente-demo-vue>cnpm run dev


   ```

3. 打开地址http://localhost:8080，项目初始化成功

### 二、引入Element UI 组件

npm 安装

```shell
cnpm i element-ui -S
```

在 main.js 中写入以下内容：

```javascript
import Vue from 'vue';
import ElementUI from 'element-ui';
import 'element-ui/lib/theme-chalk/index.css';
import App from './App.vue';

Vue.use(ElementUI);

new Vue({
  el: '#app',
  render: h => h(App)
});
```

以上代码便完成了 Element 的引入。需要注意的是，样式文件需要单独引入

