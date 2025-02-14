# Changelog (2025-02-13 - 2025-02-14)

## Overview
This release focuses on enhancing the robustness and flexibility of the system, with significant improvements in data handling, particularly around file uploads and API interactions. Key updates include the introduction of file upload capabilities in the GraphQL API, improved input validation, and safeguards against infinite loops in API pagination.

## 🚀 New Features
• **GraphQL File Uploads**: Introduced file upload capabilities in the GraphQL API, allowing users to upload and process files directly. This includes support for Excel file processing using the `xlsx` library. [🔗](https://github.com/quantstruct/superglue/commit/497cfe4f1fa8632db72e807a3ae62cc9745751bb) [🔗](https://github.com/quantstruct/superglue/commit/cf374bca8702256de56175a03c19a156531edccd)

## 🐛 Bug Fixes
• **Pagination Logic**: Improved the handling of paginated API responses to ensure complete data retrieval without premature termination. [🔗](https://github.com/quantstruct/superglue/commit/51b8d66e89deba18f25445fb8b520653f8f714e9)
• **HTML Detection**: Enhanced the HTML detection logic in the `getDocumentation` function to correctly identify HTML content with attributes or whitespace. [🔗](https://github.com/quantstruct/superglue/commit/52b185fd87f6a4d81e8f128ccaa7f0e235609d30)

## ⚡ Performance Improvements
• **API Call Safeguards**: Added a loop counter to prevent infinite loops in API pagination, ensuring system stability and preventing excessive resource consumption. [🔗](https://github.com/quantstruct/superglue/commit>b23dcb7bba6171af75d89ac6e13d5eb94f49f552) [🔗](https://github.com/quantstruct/superglue/commit/1355334d29dc3007d7f59f6a68858ef2e8f3b982)

## 📚 Documentation
• **Complex HTML Handling**: Added a test case to ensure the `getDocumentation` utility can handle complex HTML with special characters and nested elements. [🔗](https://github.com/quantstruct/superglue/commit/96c691cb1efb4ee9bacb8f282316c9e7d8239f9c)

## 🔧 Maintenance
• **Input Validation**: Implemented input validation checks across `MemoryStore` and `RedisService` classes to prevent operations with invalid or incomplete data, enhancing system stability. [🔗](https://github.com/quantstruct/superglue/commit/b253e5d4f0f0ca7ebecad2effe6a58f2ede1700d) [🔗](https://github.com/quantstruct/superglue/commit/6819cde41fcb9b6b89dd9aec5ad22b4dbe5f6452)
• **API Configuration Refactor**: Streamlined the `callResolver` function to improve efficiency and reduce complexity in handling API endpoint configurations. [🔗](https://github.com/quantstruct/superglue/commit/f629200abd1ab4fc96554aa5af955332f9257456)
• **Test Suite Enhancements**: Expanded test coverage for extract utilities, particularly for Excel file handling, to ensure robust data processing. [🔗](https://github.com/quantstruct/superglue/commit/5c8938c7497402fd3c1854cecd6071cadd37a4e9)
• **Schema Validation**: Added a validation step in `generateSchemaResolver` to truncate excessively large `responseData`, preventing performance issues. [🔗](https://github.com/quantstruct/superglue/commit/521771b0cefe2a72556fe7ef36e191db4552e10d)

## ⚠️ Breaking Changes
None.