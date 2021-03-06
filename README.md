# vue-input-number

#### DataCamp fork status

2020-10-07: Active use in [enterprise-frontend](https://github.com/datacamp-engineering/enterprise-frontend) — maintained by [ee-eng](https://github.com/orgs/datacamp-engineering/teams/enterprise).
<hr>

[![npm](https://img.shields.io/npm/v/vue-input-number.svg)](https://www.npmjs.com/package/vue-input-number) [![npm](https://img.shields.io/npm/dt/vue-input-number.svg)](https://www.npmjs.com/package/vue-input-number) [![JavaScript Style Guide](https://img.shields.io/badge/code_style-standard-brightgreen.svg)](https://standardjs.com)

> A custom input number component for [Vue.js 2](https://vuejs.org/).

## Install

[Yarn](https://yarnpkg.com/lang/en/)

```sh
yarn add vue-input-number --dev
```

[NPM](https://www.npmjs.com/)
```sh
npm install vue-input-number --save-dev
```

## Prerequisites

- [Vue.js 2](https://vuejs.org/)

## Usage

```html
<template>

    <input-number
        :step="1"
        :min="10"
        :max="100"
        :maxlength="3"
        :inputclass="'v-input-number-input'"
        @onInputNumberChange="onChange"></input-number>

</template>

<script>
  export default {
    methods: {
        onChange (value) {
            console.log(value)
        }
    }
  }
</script>
```

In your entry app:

```js
const Vue = require('vue')

Vue.component('vue-input-number', require('vue-input-number'))

const app = new Vue({
  el: '#app'
})
```

For more detailed example check out [the app directory](./app).

## Attributes

- __value:__ Add a default value to input. 
- __step:__ Step value for increment and decrement the input number value.
- __min:__ Minimum value for input number. `min` is only used as a placeholder if `placeholder` is empty.
- __max:__ Maximum value for input number.
- __maxlength:__ Maxlength for the input number.
- __keydown:__ Enable keydown for increment or decrement value.
- __mousedown:__ Enable mousedown for increment or decrement value.
- __integer:__ Enable integer value only.
- __placeholder:__ Set a input placeholder. If `placeholder` has some value then `min` is not used as a placeholder.
- __inputclass:__ Set a diferent class for the input element. For example, if you use Bootstrap default input class you can set `:inputclass="'form-control'"` to use `form-control` class in the input element.

## Events

#### @onInputNumberChange

Event is fired when value is changed.

## License
MIT license

© 2018 [José Luis Quintana](https://git.io/joseluisq)
