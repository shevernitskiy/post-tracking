# 📦RussianPost tracking API client

[![npm](https://img.shields.io/npm/v/@shevernitskiy/post-tracking?logo=npm&style=flat&labelColor=000)](https://www.npmjs.com/package/@shevernitskiy/post-tracking)
[![JSR](https://jsr.io/badges/@shevernitskiy/post-tracking)](https://jsr.io/@shevernitskiy/post-tracking)
![dependencies](https://img.shields.io/badge/dependencies-0-green?style=flat&labelColor=000)
[![license](https://img.shields.io/github/license/shevernitskiy/amo?style=flat&labelColor=000)](https://github.com/shevernitskiy/post-tracking/blob/main/LICENSE)

This is super simple API client for RussianPost Traking API.
It just fetch the tracking history from the API.

# Installation

## Node.js

```sh
npm i @shevernitskiy/post-tracking
```

```sh
npx jsr add @shevernitskiy/post-tracking
```

## Deno

```sh
deno add @shevernitskiy/post-tracking
```

# Usage

Create an instance and call method `tracking`. That's it.

```ts
const client = new PostTracking("your_login", "your_password");
const history = await client.tracking(1116949696969);
console.log(history);
```

You can pass `options` object as a third argument.

```ts
const client = new PostTracking("your_login", "your_password", { language: "ENG" });
```

As as result you will get the history:

```js
{
  history: [
    {
      index: 111024,
      place: "Москва 24",
      operation: "Обработка",
      datetime: 2024-07-10T13:08:20.000Z
    },
    {
      index: 111974,
      place: "Москва МСП-3 Цех-4 МПКО-Восток",
      operation: "Обработка",
      datetime: 2024-07-10T14:18:07.001Z
    },
    {
      index: 111974,
      place: "Москва МСП-3 Цех-4 МПКО-Восток",
      operation: "Обработка",
      datetime: 2024-07-10T14:32:54.000Z
    },
    {
      index: 108960,
      place: "ЛЦ Внуково-2",
      operation: "Обработка",
      datetime: 2024-07-11T00:56:17.001Z
    },
    {
      index: 104040,
      place: "Шереметьево АОПП",
      operation: "Обработка",
      datetime: 2024-07-11T05:49:58.001Z
    },
  ],
  last_operation: "Обработка",
  duration: 434992
}
```

# Contribution

Pull request, issues and feedback are very welcome. Code style is formatted with deno fmt.

# License

Copyright 2024, shevernitskiy. MIT license.
