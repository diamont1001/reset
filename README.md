# reset in less
base style(less) for private

## install

```bash
npm i jr-reset
```

## require in js

```js
require('jr-reset/wap/reset.less');
require('jr-reset/common/mixin.less');
```

## import in less

```less
@import '~jr-reset/wap/reset.less';
@import '~jr-reset/common/mixin.less';
```

## 实际项目中推荐使用方法(webpack)

推荐目录结构：

```
--project
  --base
    --mixin.less
    --reset.less
  --modules
    --header
      --index.js
      --index.less
    --xxx
      --index.js
      --index.less
  --pages
    --home
      --index.js
      --index.less
```

核心文件：

base/reset.less:

```less
@import '~jr-reset/wap/reset.less';
@import './mixin.less';

...
```

base/mixin.less

```less
@import '~jr-reset/common/mixin.less';

@colorMain: #3aa7f9; // 主色调

...
```

modules/xxx/index.less

```less
@import '../../base/mixin.less';

...
```

pages/xxx/index.less

```less
@import '../../base/reset.less';
@import '../../base/mixin.less';

...
```
