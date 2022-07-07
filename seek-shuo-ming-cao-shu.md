# Seek 说明(草书)



* edge 和 seek 客户端通讯 是通过调用 api 接口

```
文件 : src\renderer\assets\config\api.js
```

* seek 页面渲染进程和主进程通讯 通过 ipcRenderer 和 ipcMain 通讯

```
 目录 src\main\ipcManager
```

* 每次新建tab页面 都会创建一个自定义 View 实例, 里面储存诸如:
  * Url - 自定义变量
  *   BrowserWindow - electron 原生实例变量 > View 内部储存的 BrowserWindows 负责收集所有tab(View)及相关数据

      <img src="https://i.loli.net/2020/02/11/q7noLVHvcsQRUfj.png" alt="https://i.loli.net/2020/02/11/q7noLVHvcsQRUfj.png" data-size="original">
  * BroswerView - electron 原生实例变量,
  * initBrowserView() - 自定义方法,
  * updateEvent()- 自定义方法
