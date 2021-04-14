# rollup
Rollup打包配置
```js
npm i rollup -g
npm install rollup –save-dev

rollup src/index.js -f umd -o dist/bundle.js
```
## 理解：
+ -f 。 -f 参数是 --format 的缩写，它表示生成代码的格式， amd 表示采用 AMD 标准， cjs 为 CommonJS 标准， esm （或 es）为 ES 模块标准。 -f 的值可以为 amd 、 cjs 、 system 、 esm （'es’也可以）、 iife 或 umd 中的任何一个。

+ -o 。 -o 指定了输出的路径，这里我们将打包后的文件输出到 dist 目录下的 bundle.js

+ -c 。指定 rollup 的配置文件。(默认rollup.config.js)

+ -w 。监听源文件是否有改动，如果有改动，重新打包。

## rollup.config.js配置项
```js
rollup -c // 执行相当于上述参数
```
+ input 表示入口文件的路径（老版本为 entry，已经废弃）

+ output 表示输出文件的内容，它允许传入一个对象或一个数组，当为数组时，依次输出多个文件，它包含以下内容：
    + output.file ：输出文件的路径（老版本为 dest，已经废弃）
    + output.format ：输出文件的格式
    + output.banner ：文件头部添加的内容
    + output.footer ：文件末尾添加的内容