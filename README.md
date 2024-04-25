<h1 align='center'>
  Divz
</h1>
<p align='center'>
  <a href='https://www.npmjs.com/package/divz'>
    <img src='https://img.shields.io/npm/v/divz.svg' alt='Latest npm version'>
  </a>
    <a href='https://github.com/lewhunt/divz/blob/main/LICENSE'>
    <img src='https://img.shields.io/badge/License-MIT-yellow.svg' alt='MIT License'>
  </a>
    <a href='https://www.npmjs.com/package/divz'>
    <img src='https://img.shields.io/npm/dm/divz.svg' alt='Monthly npm downloads'>
  </a>
</p>

<p align='center'><i><small>
A React UI component that lets you stack, swipe and zoom through HTML elements on the 3D z-axis</small></i></p>

<p dir="auto" align='center'><a href="https://lewhunt.github.io/divz/" rel="nofollow"><img  align='center' src="https://lewhunt.github.io/assets/readme/divz-demo1.gif" alt="https://lewhunt.github.io/divz/"></a></p>

<p align='center'><i><small>
Click the above to try out the demos</small></i></p>

<br/>

## Installation

```bash
npm install divz
```
<br/>

## Basic Usage

Import the component and render it in your app or page, wrapping it around your list of divs or other HTML elements:

```jsx
import { Divz } from "divz";

function App() {
  return (
    <Divz>
      <div>1</div>
      <div>2</div>
      <div>3</div>
      <div>4</div>
    </Divz>
  );
}
```

### [:point_right: Try out the demos :point_left:](https://lewhunt.github.io/divz/)

**https://lewhunt.github.io/divz**

<br/>

## Advanced Usage

The demos illustrate how the component can be initialised with more props - along with images and videos inside the child divs - for a richer user experience.

```jsx
<Divz
  autoPlay={true}
  autoPlayDuration={4000}
  onIndexChange={(i) => console.log("divz selected index: ", i)}
  onPlaying={(i) => console.log("divz playing status: ", i)}
>
  <div>
    <img src="https://image.tmdb.org/t/p/w1280/rRBD8ORo9y34tYkAQJVbn4Ml6tu.jpg" />
  </div>

  <div>
    <img src="https://image.tmdb.org/t/p/w1280/vJGgox2d4HWmm3icilCytCC6RCR.jpg" />
  </div>

  <div>
    <img src="https://image.tmdb.org/t/p/w1280/36q3LejjQbpyhhuMpJN6kALbFtR.jpg" />
  </div>
</Divz>
```

<br/>

## Why create Divz?

Divz was was initially created to quickly showcase portfolio work within a pseudo-3D environment, loosely inspired by Apple's Time Machine interface which allows the user to zoom through historical Finder windows:

[![https://en.wikipedia.org/wiki/Time_Machine_%28macOS%29](https://upload.wikimedia.org/wikipedia/en/1/1a/Timemachine_gallery_windowsquicklook20070611.jpg)](https://en.wikipedia.org/wiki/Time_Machine_%28macOS%29)

<p><i>Apple's Time Machine was the inspiration for Divz</i></p>

<br/>
  
## What Sets It Apart?

Divz is designed to be responsive and easy to use, acting as a simple wrapper around a list of HTML divs or elements. The demos illustrate how it could work as a carousel, slideshow or gallery component. Various modes of navigation are supported: touch for mobile, cursor and trackpad for desktop, plus arrow keys for big-screen devices.

<br/>

## How Does It Work?

Under the hood, Divz performs CSS3 transforms on the core component and the child HTML elements, set dynamically with React TypeScript. The component is packaged using Vite to allow npm library integration.

<br/>

## Props

| Prop                       | Description                                                                                                                                    | Default |
| -------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------- | ------- |
| `autoPlay`                 | Set to `true` to autoplay a carousel sequence of any children div elements                                                                     | `false` |
| `isAutoPlayLooped`         | Set to `true` to enable the autoPlay sequence to endlessly loop                                                                                | `true`  |
| `autoPlayDuration`         | Set the time interval in milliseconds for the autoPlay feature                                                                                 | `6000`  |
| `showPlayButton`           | Set to `true` to display the autoPlay toggle button                                                                                            | `true`  |
| `showNavButtons`           | Set to `true` to display the up/down navigational buttons for cycling between div children                                                     | `true`  |
| `showExpandButton`         | Set to `true` to display the 'full-screen' expand button which is used to toggle the scale of div items                                        | `true`  |
| `showNavButtonsOnExpanded` | Set to `true` to display the navigational buttons when div items have been expanded                                                            | `false` |
| `isExpanded`               | Set to `true` to toggle the scale of div items                                                                                                 | `false` |
| `isDarkMode`               | Set to `true` to set the buttons UI styling to dark mode                                                                                       | `false` |
| `isSnapEnabled`            | Set to `true` to ensure the transform animation is snap-fixed to only move between the div items                                               | `true`  |
| `selectIndex`              | Set the index number to force it to instantly jump to position of a div child item. By default it will instead zoom animate to the first item. | `null`  |
| `className`                | Insert additional classname values for overriding the component CSS styling                                                                    | `null`  |
| `onIndexChange`            | Called when navigation occurs and the currently selected divz item has changed index                                                           |         |
| `onPlaying`                | Called when autoPlay sequence starts or stops                                                                                                  |         |

<br/>

## Support

I hope this has given you a good intro to the component and you can get some use out of it for your own projects...

💬 Fire over a comment if you have any feedback, requests or issues 🐛

⭐ Hit me with a Github star if you like the component and please share it 🙏

<br/>
<br/>

https://github.com/lewhunt/divz/assets/9886284/1fea8f35-92f5-4915-9af6-4a3a0a820d6f

