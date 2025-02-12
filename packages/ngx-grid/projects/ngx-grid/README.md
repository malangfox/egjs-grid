<p align="middle" ><img src="https://naver.github.io/egjs-grid/images/logo.png" /></p>
<h2 align="middle">Angular Grid</h2>
<p align="middle">
<a href="https://www.npmjs.com/package/@egjs/ngx-grid" target="_blank"><img src="https://img.shields.io/npm/v/@egjs/ngx-grid.svg?style=flat-square&color=007acc&label=version" alt="npm version" /></a>&nbsp;
<img src="https://img.shields.io/badge/language-typescript-blue.svg?style=flat-square" />&nbsp;
<a href="https://github.com/naver/egjs-grid/blob/main/LICENSE" target="_blank"><img src="https://img.shields.io/static/v1?style=flat-square&label=license&message=MIT&color=08CE5D" /></a>&nbsp;
</p>
<p align="middle">An Angular component that can arrange items according to the type of grids.</p>
<p align="middle">
    <a href="https://naver.github.io/egjs-grid" target="_blank"><strong>Demo</strong></a> /&nbsp;
    <a href="https://naver.github.io/egjs-grid/release/latest/doc/" target="_blank"><strong>API</strong></a>
</p>

## Grids

|                         <img src="https://naver.github.io/egjs-grid/images/MasonryGrid.png" />                         |                           <img src="https://naver.github.io/egjs-grid/images/JustifiedGrid.png" />                           |                       <img src="https://naver.github.io/egjs-grid/images/FrameGrid.png" />                       |                         <img src="https://naver.github.io/egjs-grid/images/PackingGrid.png" />                         |
| :--------------------------------------------------------------------------------------------------------------------: | :--------------------------------------------------------------------------------------------------------------------------: | :--------------------------------------------------------------------------------------------------------------: | :--------------------------------------------------------------------------------------------------------------------: |
| [**MasonryGrid**](http://naver.github.io/egjs-grid/storybook/?path=/story/examples-masonrygrid--masonry-grid-template) | [**JustifiedGrid**](http://naver.github.io/egjs-grid/storybook/?path=/story/examples-justifiedgrid--justified-grid-template) | [**FrameGrid**](http://naver.github.io/egjs-grid/storybook/?path=/story/examples-framegrid--frame-grid-template) | [**PackingGrid**](http://naver.github.io/egjs-grid/storybook/?path=/story/examples-packinggrid--packing-grid-template) |

- **MasonryGrid**: The MasonryGrid is a grid that stacks items with the same width as a stack of bricks. Adjust the width of all images to the same size, find the lowest height column, and insert a new item.
- **JustifiedGrid**: 'justified' is a printing term with the meaning that 'it fits in one row wide'. The JustifiedGrid is a grid that the item is filled up on the basis of a line given a size.
- **FrameGrid**: 'Frame' is a printing term with the meaning that 'it fits in one row wide'. The FrameGrid is a grid that the item is filled up on the basis of a line given a size.
- **PackingGrid**: The PackingGrid is a grid that shows the important items bigger without sacrificing the weight of the items. Rows and columns are separated so that items are dynamically placed within the horizontal and vertical space rather than arranged in an orderly fashion.

## Documents

- [Get Started and Demos](https://naver.github.io/egjs-grid/)
- [API documentation](https://naver.github.io/egjs-grid/release/latest/doc/)

## Download and Installation

Download dist files from repo directly or install it via npm.

```bash
$ npm install @egjs/ngx-grid
# Or if you are using yarn
$ yarn add @egjs/ngx-grid
# Or if you are using pnpm
$ pnpm install @egjs/ngx-grid
```

## How to use

- app.module.ts

```ts
import { BrowserModule } from '@angular/platform-browser';
import { NgModule } from '@angular/core';
import { NgxGridModule } from '@egjs/ngx-grid';

import { AppComponent } from './app.component';

@NgModule({
  imports: [BrowserModule, NgxGridModule],
  declarations: [AppComponent],
  bootstrap: [AppComponent],
})
export class AppModule {}
```

- app.component.ts

```ts
import { Component } from '@angular/core';

@Component({
  selector: 'app-root',
  templateUrl: './app.component.html',
  styleUrls: ['./app.component.css'],
})
export class AppComponent {
  gap = 5;
  align = 'justify' as const;
}
```

- app.component.html

```html
<!--NgxMasonryGrid-->
<!--NgxJustifiedGrid-->
<!--NgxFrameGrid-->
<!--NgxPackingGrid-->
<div class="container" NgxMasonryGrid [gap]="gap" [align]="align">
  <div class="item">1</div>
  <div class="item">2</div>
  <div class="item">3</div>
  <div class="item">4</div>
  <div class="item">5</div>
  <div class="item">6</div>
  <div class="item">7</div>
  <div class="item">8</div>
  <div class="item">9</div>
  <div class="item">10</div>
</div>
```

#### 2. Install dependencies

```
# Install the dependency modules.
$ npm install
```

### 3. `npm start`

Run `storybook` for development.

Open [http://localhost:6008](http://localhost:6008) to view it in the browser.

The page will reload if you make edits.\
You will also see any lint errors in the console.

#### 3. `npm build`

Use npm script to build Grid

```bash
# Build
$ npm run build
```

## Bug Report

If you find a bug, please report to us opening a new [Issues](https://github.com/naver/egjs-grid/issues) on GitHub.

## License

egjs-grid is released under the [MIT license](https://github.com/naver/egjs/blob/master/LICENSE.txt).

```
Copyright (c) 2021-present NAVER Corp.

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in
all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT.  IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
THE SOFTWARE.
```
