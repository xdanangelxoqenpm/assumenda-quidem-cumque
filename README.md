# @xdanangelxoqenpm/assumenda-quidem-cumque

[![npm version](https://img.shields.io/npm/v/@xdanangelxoqenpm/assumenda-quidem-cumque.svg)](https://www.npmjs.com/package/@xdanangelxoqenpm/assumenda-quidem-cumque)
[![License](https://img.shields.io/badge/license-MIT-blue.svg)](https://github.com/yourusername/@xdanangelxoqenpm/assumenda-quidem-cumque/blob/main/LICENSE)

[__Checkout DEMO__](https://miloszsobczak.github.io/@xdanangelxoqenpm/assumenda-quidem-cumque/)

Async Promise Batch is a powerful utility for managing and controlling the concurrency of promises in your JavaScript or TypeScript projects. It allows you to efficiently process asynchronous tasks in batches, making it ideal for scenarios where you want to limit the number of concurrently executing promises.

## Installation

You can install @xdanangelxoqenpm/assumenda-quidem-cumque using npm or yarn:

```sh
npm install @xdanangelxoqenpm/assumenda-quidem-cumque
```

or

```sh
yarn add @xdanangelxoqenpm/assumenda-quidem-cumque
```

## Features

- **Promise Concurrency Control:** Limit the number of concurrent promises being executed to prevent resource overload.
- **Batch Processing:** Efficiently process promises in batches, reducing resource consumption and improving performance.
- **Async Iterator:** Provides an async iterator interface for easy integration into your async workflows.
- **Customizable:** Configure the batch size and control how promises are processed.

## Usage

Here's a simple example of how to use @xdanangelxoqenpm/assumenda-quidem-cumque:

```typescript
import asyncPromiseBatch from '@xdanangelxoqenpm/assumenda-quidem-cumque';

// Define an array of promise functions to execute
const promises = [
    () => new Promise(resolve => setTimeout(() => resolve(1), 10)),
    () => new Promise(resolve => setTimeout(() => resolve(2), 200)),
    () => new Promise(resolve => setTimeout(() => resolve('3'), 30)),
    () => new Promise(resolve => setTimeout(() => resolve(4), 40)),
];

// Set the maximum number of concurrent promises (e.g., 2)
const concurrencyLimit = 2;

// Run the promises in batches with concurrency control
const results = await asyncPromiseBatch<number | string>(promises, concurrencyLimit);

console.log(results);
// [1, 2, '3', 4]
```

## License

This package is open-source and available under the MIT License. Feel free to use it in your projects and contribute to its development.

## Contributing

Contributions, bug reports, and feature requests are welcome! If you encounter any issues or have ideas for improvements, please [create an issue](https://github.com/xdanangelxoqenpm/assumenda-quidem-cumque/issues) on GitHub.

## Acknowledgments

This package was inspired by the need for efficient promise concurrency control in JavaScript and TypeScript projects. Thanks to the open-source community for their contributions and ideas.

---

© 2023 Milo | [GitHub Repository](https://github.com/xdanangelxoqenpm/assumenda-quidem-cumque)
