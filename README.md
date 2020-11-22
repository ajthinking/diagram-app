## How to use [React Diagrams](https://github.com/projectstorm/react-diagrams) with Laravel
As of 22th november 2020.

<img src="https://raw.githubusercontent.com/projectstorm/react-diagrams/master/.gitbook/assets/example1.jpg">

### Setup up React
```
laravel new diagram-app
cd diagram-app
composer require laravel/ui
php artisan ui react
yarn && yarn watch
```

In welcome.blade.php do the following changes
* ```<div id="app"></div>```

* ```<script type="text/javascript" src="/js/app.js"></script>```
* ```<link href="/css/app.css" rel="stylesheet">```
* ```<link href="https://unpkg.com/tailwindcss@^2/dist/tailwind.min.css" rel="stylesheet">```
        


### Installing the package
```
yarn add @projectstorm/react-diagrams@next
npm install closest lodash react dagre pathfinding paths-js resize-observer-polyfill ml-matrix @emotion/core@10.1.1 @emotion/styled@10.0.3
```

### Adding a diagram!
Copy [this sample](https://github.com/projectstorm/react-diagrams/blob/master/packages/diagrams-demo-gallery/demos/demo-simple/index.tsx) from the demos and save it as a component `Diagram.js`

Make the following modifications
* Remove the `DemoCanvasWidget` import & wrapper in `render`
* Remove ts typehint `<DefaultLinkModel>`
* Add a style `fullsize` in app.scss:
```css
.fullsize {
    width: 100vw;
    height: 70vh;
}
```
* Apply that class to `CanvasWidget` in your `Diagram` component.

* Finally rename `ExampleComponent` to `App` and render the Diagram inside :rocket:


## Or...
you can use this repo as a starting point.
