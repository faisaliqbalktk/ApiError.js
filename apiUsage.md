Importing the ApiError class:
import { ApiError } from './apiError.js';
Creating an API error:
// Creating an API error with default message and status code
const error = new ApiError(404);

// Creating an API error with custom message and status code
const customError = new ApiError(500, 'Internal Server Error');
Accessing error properties:
console.log(error.statusCode); // Output: 404
console.log(error.message); // Output: something went wrong
Handling the error:
You can handle the error in your code using standard error handling techniques in JavaScript.

Customization:
You can customize the ApiError class by providing custom error messages, status codes, and error details.

Notes:
The stack property of the error object captures the stack trace for debugging purposes.
The errors property can be used to provide additional details about the error.

# Usage Guide for API Response

The `ApiResponse` class allows you to create custom response objects for handling API responses.

## Example Usage:

### Importing the `ApiResponse` class:
```javascript
import { ApiResponse } from './apiResponse.js';
Creating an API response:
// Creating an API response with default status code (200)
const response = new ApiResponse(200);

// Creating an API response with custom status code, data, and message
const customResponse = new ApiResponse(201, { id: 1 }, 'Resource created successfully');
Accessing response properties:
console.log(response.statusCode); // Output: 200
console.log(response.success); // Output: true
Handling the response:
You can handle the response in your code according to the status code and data provided.

Customization:
You can customize the ApiResponse class by providing custom status codes, data, and messages.

Notes:
The success property indicates whether the request was successful based on the status code.
The data property contains the response data.