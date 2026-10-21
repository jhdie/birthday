# 陈浩杰，生日快乐

一个纯前端的生日祝福小页面：卡通贴纸字、手绘蛋糕、满屏彩纸，还有一圈会一直上下浮动的祝福气泡。

- 单文件，无任何依赖（`index.html` 直接双击就能看）
- 手机竖屏 / 横屏都做过适配
- 点屏幕任意处会撒彩纸，点祝福气泡会撒一把彩纸，右上角 ♪ 是现场合成的《生日快乐》

## 本地查看

双击 `index.html` 即可，不需要服务器。

## 想改内容

打开 `index.html`，拉到最下面 `<script>` 里的 `CONFIG` 和 `BLESSINGS`：

```js
var CONFIG = {
  name: "陈浩杰",          // 名字小标签上的全名
  short: "浩杰",           // 信件里的称呼
  sign: "—— 你的同学JHD",  // 落款
  date: "2026 · 10 · 21"   // 日期
};

var BLESSINGS = [
  ["愿望成真", "#E8477B"],
  ["天天开心", "#E07A2B"],
  ...
];
```

`BLESSINGS` 最多 8 条，第 1~4 条显示在左边，第 5~8 条显示在右边；第二个值是文字颜色。

信件的正文在 `index.html` 里搜 `card-scroll`，直接改那几段 `<p>` 就行。

## 部署到 GitHub Pages

1. 新建一个仓库（比如 `happy-birthday`），把这个文件夹里的文件全部上传（`index.html` 必须在根目录）。
2. 仓库 → **Settings** → 左侧 **Pages**。
3. **Source** 选 `Deploy from a branch`，Branch 选 `main`、目录选 `/ (root)`，保存。
4. 等一两分钟，访问 `https://你的用户名.github.io/happy-birthday/`，把链接发给同学就行。

> `.nojekyll` 是空的占位文件，别删，它能让 Pages 原样输出文件。

## 小提示

- 卡通字体走的是 Google Fonts，网络不通时会自动退回系统字体（微软雅黑 / 苹方），页面和动效完全不受影响。
- 微信里直接发 `.html` 文件对方可能打不开，发链接最稳。
