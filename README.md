# UEDL (Ultra Efficient Data Language) Library

UEDL (Ultra Efficient Data Language) is a compact and efficient data representation language. Unlike JSON or YAML, UEDL does not use new lines and provides a compact format. This library provides functionality to parse and format UEDL data, and supports various data types including strings, integers, floating-point numbers, booleans, dates, arrays, and tables. It also includes query functionality similar to XPath or jq.

## Table of Contents

- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [API Documentation](#api-documentation)
- [Examples](#examples)
- [License](#license)

## Features

- Parse UEDL strings into JavaScript objects.
- Format JavaScript objects into UEDL strings.
- Query UEDL data using path-based queries.

## Installation

You can install the UEDL library via npm. Make sure you have Node.js and npm installed on your system.

```bash
npm install uedl-library
```

## Usage

Here's a basic example of how to use the UEDL library:

```javascript
const { parseValue } = require('uedl-library/src/uedl-parser');
const { formatValue } = require('uedl-library/src/uedl-formatter');

// Sample UEDL data
const uedlData = 'person=name="John Doe";age=30;height=5.75;active=true;birthdate=date:1994-07-30;hobbies=["reading", "cycling"];address=table{street="123 Main St";city="Metropolis"}';

// Parse data
const parsedData = parseValue(uedlData);
console.log("Parsed Data:", parsedData);

// Format data
const formattedData = formatValue(parsedData);
console.log("Formatted Data:", formattedData);
```

## API Documentation

### `parseValue(value)`

Parses a UEDL string value into a JavaScript object.

**Parameters:**

- `value` (string): The UEDL string to parse.

**Returns:**

- The corresponding JavaScript object or primitive value.

### `formatValue(value)`

Formats a JavaScript object or primitive value into a UEDL string.

**Parameters:**

- `value` (any): The JavaScript object or primitive value to format.

**Returns:**

- The UEDL string representation of the input value.

## Examples

For more detailed examples, check the [examples](examples/example.js) directory.

## License

This library is licensed under the MIT License. See the [LICENSE](LICENSE) file for more details.
