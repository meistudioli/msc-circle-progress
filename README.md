# msc-circle-progress

[![Published on webcomponents.org](https://img.shields.io/badge/webcomponents.org-published-blue.svg)](https://www.webcomponents.org/element/msc-circle-progress) [![DeepScan grade](https://deepscan.io/api/teams/16372/projects/23113/branches/690772/badge/grade.svg)](https://deepscan.io/dashboard#view=project&tid=16372&pid=23113&bid=690772)

&lt;msc-circle-progress /> provides progress with circle shape. Developers could use it to indicate upload、form complete status for users.

![<msc-zoom />](https://blog.lalacube.com/mei/img/preview/msc-circle-progress.png)

## Basic Usage

&lt;msc-circle-progress /> is a web component. All we need to do is put the required script into your HTML document. Then follow &lt;msc-circle-progress />'s html structure and everything will be all set.

- Required Script

```html
<script
  type="module"
  src="https://your-domain/wc-msc-circle-progress.js">        
</script>
```

- Structure

Put &lt;msc-circle-progress /> into HTML document. It will have different functions and looks with attribute mutation.

```html
<msc-circle-progress>
  <script type="application/json">
    {
      "size": 16,
      "value": 33,
      "max": 100
    }
  </script>
</msc-circle-progress>
```

Otherwise, developers could also choose remoteconfig to fetch config for &lt;msc-circle-progress />.

```html
<msc-circle-progress
  remoteconfig="https://your-domain/api-path"
>
</msc-circle-progress>
```

## JavaScript Instantiation

&lt;msc-circle-progress /> could also use JavaScript to create DOM element. Here comes some examples.

```html
<script type="module">
import { MscCircleProgress } from 'https://your-domain/wc-msc-circle-progress.js';

// use DOM api
const nodeA = document.createElement('msc-circle-progress');
document.body.appendChild(nodeA);
nodeA.value = 50;
nodeA.size = 10;

// new instance with Class
const nodeB = new MscCircleProgress();
document.body.appendChild(nodeB);
nodeB.value = 60;
nodeB.size = 20;

// new instance with Class & default config
const config = {
  size: 20,
  value: 0,
  max: 100
};
const nodeC = new MscCircleProgress(config);
document.body.appendChild(nodeC);
</script>
```

## Style Customization

Developers could apply styles to decorate &lt;msc-circle-progress />'s looking.

```html
<style>
msc-circle-progress {
  --msc-circle-progress-font-size: 16px;
  --msc-circle-progress-font-color: #232a31;
  --msc-circle-progress-color: #0f69ff;
  --msc-circle-progress-placeholder-color: transparent;
}
</style>
```

Otherwise, apply pseudo class `::part(value)` to direct style text element.

```html
<style>
msc-circle-progress::part(value) {
  font-size: 40px;
  color: #fff;
  line-height: 1.5;
}
</style>
```

## Attributes

&lt;msc-circle-progress /> supports some attributes to let it become more convenience & useful.

- **size**

Set size for &lt;msc-circle-progress />. It will change progress size. Default is `20` (not set).

```html
<msc-circle-progress
  size="20"
>
  ...
</msc-circle-progress>
```

- **value**

Set value for &lt;msc-circle-progress />. Default is `0` (not set).

```html
<msc-circle-progress
  value="0"
>
  ...
</msc-circle-progress>
```

- **max**

Set max for &lt;msc-circle-progress />. Default is `100` (not set).

```html
<msc-circle-progress
  max="100"
>
  ...
</msc-circle-progress>
```

## Properties

| Property Name | Type | Description |
| ----------- | ----------- | ----------- |
| size | Number | Getter / Setter for size. Default is `20`. |
| value | Number | Getter / Setter for value. Default is `0`. |
| max | Number | Getter / Setter for max. Default is `100`. |

## Method

| Method Signature | Description |
| ----------- | ----------- |
| refresh | Force refresh &lt;msc-circle-progress />'s redering. Developers could call this method when &lt;msc-circle-progress /> mutated. |

## Reference
- [&lt;msc-circle-progress />](https://blog.lalacube.com/mei/webComponent_msc-circle-progress.html)
