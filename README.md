### 透過 Hugo Markdown 中使用 Shortcode 畫出 ABC Notation
ABC Notation 是一個可以透過文字畫出樂譜的語法
本 Repo 則是實現能夠在你的 Hugo 網站，撰寫 Markdown 時經由 Shortcode 產出可以渲染的 ABC Notation 圖片
相關效果以及撰寫，請參考 [ABC Notation](https://abcnotation.com/examples)

此專案是從 [abcjs-music](https://github.com/abcjs-music) 拉出來改成 hugo 的 shortcode

***聲明*** 目前尚未支援 midi 播放

### 如何使用

#### 寫入 hugo shortcode 檔案
請下載這份檔案 [abcjs.html](https://github.com/yoyoshenTW/hugo-shortcode-abcjs/blob/main/layouts/shortcodes/abcjs.html)
並將他放在你 Hugo 網站的根目錄的 *layouts/shortcodes* 底下

#### 導入 abcjs-basic.js
將 abcjs 上釋出的 js 檔案 [abcjs-basic.js](https://github.com/paulrosen/abcjs/blob/main/dist/abcjs-basic.js)
並將他放在你 Hugo 網站的根目錄的 *static/js* 底下

#### 在 Hugo 中使用 ABC Notation
接著在你的 markdown 文件中(例如 index.md)
引用此 shortcode {{< abcjs >}}，並在中間寫入你的樂譜內容
經過渲染後即可實現

#### Example
```
{{< abcjs >}}
T: 鳳陽花鼓
X: 1
M: 4/4
L: 1/8
GEDEG2|EGAcG2|
{{< /abcjs >}}
```
<hr/>

### Rendering ABC Notation Using Shortcode in Hugo Markdown
ABC Notation is a syntax that allows you to render sheet music using text.
This repository implements a feature that allows you to render ABC Notation images in your Hugo website by writing Markdown with Shortcode.
For related effects and writing instructions, please refer to [ABC Notation](https://abcnotation.com/examples).

This project is adapted from [abcjs-music](https://github.com/abcjs-music) into a Hugo shortcode.

***Disclaimer*** MIDI playback is not yet supported.

### How to Use

#### Write the Hugo Shortcode File
Please download this file [abcjs.html](https://github.com/yoyoshenTW/hugo-shortcode-abcjs/blob/main/layouts/shortcodes/abcjs.html)
and place it under *layouts/shortcodes* in the root directory of your Hugo website.

#### Import abcjs-basic.js
Download the JavaScript file released by abcjs [abcjs-basic.js](https://github.com/paulrosen/abcjs/blob/main/dist/abcjs-basic.js)
and place it under *static/js* in the root directory of your Hugo website.

#### Using ABC Notation in Hugo
Then, in your Markdown files (e.g., index.md), reference this shortcode {{< abcjs >}} and write your sheet music content inside.
It will be rendered accordingly.

#### Example
```
{{< abcjs >}}
T: 鳳陽花鼓
X: 1
M: 4/4
L: 1/8
GEDEG2|EGAcG2|
{{< /abcjs >}}
```
