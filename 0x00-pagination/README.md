0x00-pagination

Introduction
0x00-pagination is a simple and efficient pagination library for handling pagination logic in web applications. This library provides easy-to-use functions to paginate data sets and generate pagination controls for front-end display.

Features
Paginate any iterable data source, such as arrays, lists, database query results, etc.
Customize the number of items per page.
Generate pagination controls with customizable options.
Lightweight and easy to integrate into existing projects.
Installation
You can install 0x00-pagination via npm:

Copy code
npm install 0x00-pagination
Usage
Here's a basic example of how to use 0x00-pagination:

javascript
Copy code
const Pagination = require('0x00-pagination');

// Sample data array
const data = Array.from({ length: 100 }, (_, i) => i + 1);

// Create a pagination instance
const pagination = new Pagination(data, { perPage: 10 });

// Get the current page of data
const currentPageData = pagination.getCurrentPageData(); // Returns an array of items for the current page

// Generate pagination controls
const paginationControls = pagination.getPaginationControls(); // Returns an object with pagination controls

// Example output
console.log(currentPageData);
console.log(paginationControls);
API Reference
Pagination(data, options)
Creates a new Pagination instance.

data (Array or Iterable): The data source to paginate.
options (Object): Configuration options.
perPage (Number): The number of items per page. Default is 10.
currentPage (Number): The initial current page. Default is 1.
pagination.getCurrentPageData()
Gets the data for the current page.

Returns:

An array of items for the current page.
pagination.getPaginationControls()
Generates pagination controls.

Returns:

An object with pagination controls:
currentPage: The current page number.
totalPages: The total number of pages.
hasPrevPage: Whether there is a previous page.
hasNextPage: Whether there is a next page.
prevPage: The previous page number.
nextPage: The next page number.
pages: An array of page numbers for pagination links.
License
This project is licensed under the MIT License - see the LICENSE file for details.

Contributing
Contributions are welcome! Please feel free to submit a pull request.

Credits
0x00-pagination is developed and maintained by [Your Name].

Support
For any questions or issues, please open an issue on GitHub.

Acknowledgments
Special thanks to [Acknowledged Contributors] for their contributions to this project.


