# shopping-admin
这是一个基于 Vue 3 + Vite 构建的电商前端项目，通常被称为“小兔鲜儿” (Little Rabbit Fresh) 或类似名称。它是一个功能完善的在线购物平台演示项目。

以下是该项目的详细技术栈和功能模块介绍：

### 1. 技术栈 (Tech Stack)
- 核心框架 : Vue 3 (Composition API)
- 构建工具 : Vite (极速开发与构建)
- 路由管理 : Vue Router 4
- 状态管理 : Pinia (配合 pinia-plugin-persistedstate 实现数据持久化)
- UI 组件库 : Element Plus (按需引入)
- HTTP 请求 : Axios (进行了二次封装，统一处理请求拦截和响应拦截)
- CSS 预处理 : Sass
- 实用工具 : VueUse (组合式 API 工具库), Day.js (日期处理)
### 2. 项目目录结构 (Project Structure)
项目结构清晰，遵循标准的 Vue 3 工程化目录规范：

- src/apis : 接口层。将 API 请求按业务模块分类（如 cart.js , user.js , home.js 等），便于管理和维护。
- src/stores : 状态管理层。使用 Pinia 管理全局状态，包括：
  - userStore : 用户登录信息、Token 等。
  - cartStore : 购物车数据、增删改查逻辑。
  - categoryStore : 首页分类导航数据。
- src/views : 视图层（页面级组件）。包含主要业务页面：
  - Home : 首页（轮播图、新鲜好物、人气推荐、产品区块）。
  - Category / SubCategory : 一级/二级分类页。
  - Detail : 商品详情页（包含 SKU 选择组件）。
  - CartList : 购物车页面。
  - Checkout : 填写订单/结算页。
  - Pay / PayBack : 支付页及支付结果回调页。
  - Login : 登录页。
  - Member : 个人中心（我的订单、个人信息）。
- src/components : 全局通用组件。
  - ImageView : 图片预览组件。
  - XtxSku : 商品规格选择组件（电商核心组件之一）。
- src/composables : 组合式函数（Hooks）。例如 useCountDown.js (倒计时逻辑复用)。
- src/utils : 工具函数。主要是 http.js (Axios 实例配置)。
- src/directives : 自定义指令。例如图片懒加载指令。
### 3. 核心功能 (Core Features)
该项目实现了一个电商闭环的核心流程：

1. 用户体系 : 账号登录、Token 管理、持久化存储、个人中心。
2. 商品浏览 : 首页楼层展示、分类筛选、商品详情展示、图片放大镜。
3. 购物车 : 加入购物车（支持本地合并到云端）、修改数量、删除商品、全选/单选、总价计算。
4. 交易流程 : 填写订单地址、生成订单、模拟支付（支付宝跳转）、支付结果展示。
5. 交互体验 : 图片懒加载、吸顶导航、骨架屏加载效果、SKU 规格联动选择。
总的来说，这是一个结构规范、技术栈主流的 Vue 3 电商实战项目，非常适合用于学习 Vue 3 全家桶、组件封装以及电商业务逻辑的实现。
