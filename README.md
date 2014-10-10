An experiment with 'tool tip' using Web Components

What I wanted to do:

    <span is="tool-tip" tip="hello world!">Hello World!</span>
    <div is="tool-tip" tip="hello world!">Hello World!</div>
    <img src="hello.png" is="tool-tip" tip="hello world!">

- Create a tool tip component that can be declaratively and flexibly designed.
- Define one component to get one attribute working across multiple HTML tags.

# How to use
- Download this repository (I won't register this to bower registry)
- Run `bower install`
- Launch a local server, then access `index.html`

# Take aways
- You can't extend multiple HTML tags (such as by using wildcards), so you basically
have to register similar extension elements one by one.
- When using `platform.js`, do following to get imported html's `document`.

    var currentScript = document._currentScript || document.currentScript
    var importDoc = currentScript.importDoc;
