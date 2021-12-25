# Quarrelsome Deep Wish

## Description

This project was build build familiarity with CSS refactoring and compliance with HTML5 standards. Primarily, large portions of the project were using multiples of the same attributes, such as the same color and fonts.

From this learned a couple of key things:

- The Cascading nature of CSS allows for easy ways to reuse attributes. So rather than constantly repeating for certain elements we can simplify them to a lot fewer rulesets. Given the following:

  ```html
  <aside class="left">
    ...
  </aside>
  <aside class="right">
    ...
  </aside>
  <aside class="center">
    ...
  </aside>
  ```

  ```css
  aside left {
      color: #00FF80;
  }
  aside right {
      color: #00FF80;
  }
  aside center {
      color: #00FF80;
  }
  ```

  we can do

  ```css
  aside left,
  aside right,
  aside center {
      color: #00FF80;
  }
  ```

  or alternatively

  ```css
  aside {
      color: #00FF80;
  }
  ```

- CSS supports use of font variables. Many examples use colors as variables. However I was surprised to see that storing fonts in variables. It should be noted that [Internet Explorer does not support the use of variables](https://caniuse.com/css-variables), however even Microsoft acknowledges that [it is time to leave IE behind](https://support.microsoft.com/en-us/microsoft-edge/make-the-switch-from-internet-explorer-to-microsoft-edge-a6f7173e-e84a-36a3-9728-3df20ade9b3c).

- HTML5 supports semantic HTML. Making sure it is compliance with W3 specifications is important. It makes sure your code is in spec and other browsers/devices can properly interpret your website. Moreover making use of proper tags helps devices and seo tools to parse your content. For which tags to use, it would help to hash this out during the designing and wireframing phases to help structure the skeleton of the pages.
