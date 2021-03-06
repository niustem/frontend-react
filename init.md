# frontend-react项目搭建

## Create a New React App
此项目的目的是基础配置练习，所以不使用下面的框架。  
~~npx [create-react-app](https://create-react-app.dev/) frontend-react~~  
~~npx create-react-app my-app --template redux~~

## Creating a Toolchain from Scratch
* A **package manager**, such as Yarn or npm. It lets you take advantage of a vast ecosystem of third-party packages, and easily install or update them.
* A **bundler**, such as webpack or Parcel. It lets you write modular code and bundle it together into small packages to optimize load time.
* A **compiler** such as Babel. It lets you write modern JavaScript code that still works in older browsers.

### Step 1: Initialize NPM (Node Package Manager)
    npm init -y

### Step 2: Install React, Webpack, and Babel
    npm install --save react react-dom
    npm install --save @reduxjs/toolkit redux react-redux
    npm install --save react-router-dom connected-react-router history
    npm install --save tailwindcss
    npm install --save moment
    npm install --save antd


    npm install --save-dev webpack webpack-cli webpack-dev-server
    npm install --save-dev babel-loader @babel/core @babel/preset-env @babelpreset-react
    npm install --save-dev postcss-loader postcss autoprefixer
    npm install --save-dev style-loader css-loader sass-loader node-sass
    npm install --save-dev html-webpack-plugin
    npm install --save-dev url-loader
    npm install --save-dev cross-env
    npm install --save-dev styled-components
    npm install --save-dev eslint
    eslint --init

Here's what each package does:  
`react:` UI library for creating modular components.  
`react-dom:` enables us to render the React within the browser DOM.  
`webpack:` bundler that converts your source code into production-ready output.  
`webpack-cli:`   
`webpack-dev-server:` transforms our source code and serves it on a web server as we develop it. continuously. This helps use see the output of your code in the browser.  
`html-webpack-plugin:` an extension to webpack that adds the basic index html file.  
`@babel/core:` a JavaScript transpiler to converts modern JavaScript into a production-ready version that's compatible with all browsers.  
`babel-loader:` connects Babel to webpack's build process.  
`@babel/preset-env:` group of commonly used Babel plugins bundled into a preset that converts modern JavaScript features into widely compatible syntax.  
`@babel/preset-react:` React-specific Babel plugins that convert JSX syntax into plain old JavaScript that browsers can understand.  

### Step 3: Create the files
    touch webpack.config.js
    mkdir src
    cd src
    touch index.js index.html

    npx tailwindcss init

参考
https://garrettbland.com/blog/setting-up-tailwindcss-with-webpack-and-purgecss/