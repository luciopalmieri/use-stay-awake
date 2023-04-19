# use-stay-awake-nextjs

[Live Demo](https://github.com/luciopalmieri/use-stay-awake-nextjs/)

> React hook that make device stay awake while actively using your website.

[![Build Status](https://travis-ci.com/roldanjr/use-stay-awake.svg?branch=master)](https://travis-ci.com/roldanjr/use-stay-awake)
[![NPM](https://img.shields.io/npm/v/use-stay-awake.svg)](https://www.npmjs.com/package/use-stay-awake) [![JavaScript Style Guide](https://img.shields.io/badge/code_style-standard-brightgreen.svg)](https://standardjs.com)
[![License](https://img.shields.io/github/license/roldanjr/use-stay-awake)](https://github.com/roldanjr/use-stay-awake/blob/master/LICENSE)

## :sparkles: Features

- [x] Typescript support
- [x] Best browser support
- [x] Easy to implement
- [x] CPU friendly
- [x] Zero dependencies

## :comet: Installation

1. Using Yarn

   ```sh
    yarn add --dev use-stay-awake
   ```

2. Using NPM

   ```sh
    npm install --save use-stay-awake
   ```

## :100: Usage

```tsx
import React from "react";
import useStayAwake from "use-stay-awake";

function App() {
  const device = useStayAwake();

  return (
    <div>
      <p>
        Status:
        <span>
          {device.canSleep
            ? "Device is allowed to sleep"
            : "Device is not allowed to sleep"}
        </span>
      </p>
      <button
        onClick={() => {
          device.preventSleeping();
        }}
      >
        Prevent Sleeping
      </button>
      <button
        onClick={() => {
          device.allowSleeping();
        }}
      >
        Allow Sleeping
      </button>
    </div>
  );
}

export default App;
```

## :spider_web: Properties

| Prop Name       | Type                      | Description                                     |
| --------------- | ------------------------- | ----------------------------------------------- |
| canSleep        | `boolean` default: `true` | Indicator if the device allowed to sleep.       |  |
| preventSleeping | `function`                | Function that prevent the device from sleeping. |
| allowSleeping   | `function`                | Function that allow the device from sleeping.   |

## :dizzy: Browser Support

- [x] Internet Explorer `v9-11`
- [x] Microsoft Edge `v12-84`
- [x] Firefox `v22-81`
- [x] Chrome `v4-87`
- [x] Safari `v4-14-TP`
- [x] Opera `v16-69`
- [x] iOS Safari `v3.2-14.0`
- [x] Android Browser `v4.4-81`
- [x] Opera Mobile `v12-46`
- [x] Chrome for Android `v84`
- [x] Firefox for Android `v68`
- [x] UC Browser for Android `v12.12`
- [x] Samsung Internet `v4-12.0`
- [x] QQ Browser `v10.4`
- [x] Baidu Browser `v7.12`
- [x] KaiOS Browser `v2.5`

## 🛠 Development

Thank you so much for contributing! :blue_heart:

### ⚡ Quick Setup

1. Clone the repository

   ```sh
    git clone https://github.com/roldanjr/use-stay-awake
   ```

2. Locate library folder

   ```sh
    cd use-stay-awake
   ```

3. Install library dependencies

   ```sh
    yarn install or npm install
   ```

4. Locate demo folder and install dependencies

   ```sh
    cd demo
    yarn install or npm install
   ```

5. Start development server under root folder

   ```sh
    yarn develop or npm run develop
   ```

## :bookmark_tabs: License

MIT © [Roldan Montilla Jr](https://github.com/roldanjr)
