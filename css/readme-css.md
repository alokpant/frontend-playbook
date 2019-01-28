# Playbook - CSS

All CSS are organized based on Component-based architecture. Main objective is write code that can be shared across multiple projects within the company.

We write CSS (Cascading Style Sheets) in:
- Sass (Syntactically Awesome StyleSheets)
- CSS Module

## BEM Methodology

For CSS naming, we use Block Element Modifier (BEM) methodology.

### Naming Rules

- Names are written in lowercase Latin letters.
```css
<div class="menu menu_theme_islands"> ... </div>
```

- Words are separated by a hyphen (-).
```css
<div class="site-search__field"> ... </div>
```
- The block name defines the namespace for its elements and modifiers.

- The element name is separated from the block name by a double underscore (__).
```css
<div class="nav>
  <div class="nav__item"> ... </div>
  ...
</div>
```

- The modifier name is separated from the block or element name by a double dashes (-).
```css
<div class="nav>
  <div class="nav__item nav__item--disabled"> ... </div>
  ...
</div>
```
* Alternative: * The modifier value is separated from the modifier name by a single underscore (_).
```css
<div class="nav>
  <div class="nav__item nav__item_disabled"> ... </div>
  ...
</div>
```

- For boolean modifiers, the value is not included in the name.

*NOTE:*
An element is always part of a block, and you shouldn't use it separately from the block.

```
<!-- Correct. Elements are located inside the `search-form` block -->
<!-- `search-form` block -->
<form class="search-form">
    <!-- `input` element in the `search-form` block -->
    <input class="search-form__input">

    <!-- `button` element in the `search-form` block -->
    <button class="search-form__button">Search</button>
</form>

<!--
    Incorrect. Elements are located outside of the context of
    the `search-form` block
-->
<!-- `search-form` block -->
<form class="search-form">
</form>

<!-- `input` element in the `search-form` block -->
<input class="search-form__input">

<!-- `button` element in the `search-form` block-->
<button class="search-form__button">Search</button>
```




## Resources

https://en.bem.info/methodology/quick-start/#guidelines-for-using-elements


## Resources

http://nicolasgallagher.com/about-html-semantics-front-end-architecture/


Main table of contents

