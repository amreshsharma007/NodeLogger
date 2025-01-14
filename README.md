# NodeLogger

NodeLogger is a base library for Node.js projects, designed to provide robust logging capabilities to enhance application monitoring and debugging.

## Features

- **Structured Logging**: Outputs logs in a structured format for easier parsing and analysis.
- **Configurable Log Levels**: Supports multiple log levels (e.g., info, debug, error) to control the verbosity of logs.
- **Timestamped Entries**: Each log entry is timestamped to facilitate chronological tracing of events.
- **Environment-Specific Configurations**: Allows customization of logging behavior based on the application's environment (development, production, etc.).

## Installation

To install NodeLogger, use npm:

```bash
npm install nodelogger
```

## Usage

First, require the NodeLogger module in your application:

```javascript
const logger = require('nodelogger');
```

Then, initialize the logger with your desired configuration:

```javascript
logger.init({
  level: 'info', // Set the default log level
  environment: 'development', // Specify the environment
  // Additional configuration options
});
```

You can now use the logger to log messages at various levels:

```javascript
logger.info('This is an info message');
logger.debug('This is a debug message');
logger.error('This is an error message');
```

## Configuration

NodeLogger can be customized through the following options:

- **level**: Sets the default log level (`info`, `debug`, `error`, etc.).
- **environment**: Specifies the application's environment (`development`, `production`, etc.).
- **logFilePath**: Defines the file path where logs should be stored.
- **maxFileSize**: Determines the maximum size of the log file before rotation occurs.
- **maxFiles**: Specifies the number of rotated log files to keep.

Example:

```javascript
logger.init({
  level: 'debug',
  environment: 'production',
  logFilePath: '/var/logs/app.log',
  maxFileSize: '10MB',
  maxFiles: 5,
});
```

## Contributing

Contributions are welcome! Please fork the repository and submit a pull request with your changes. Ensure that your code adheres to the project's coding standards and includes appropriate tests.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Acknowledgements

Special thanks to the open-source community for their invaluable contributions and inspiration.

---

*Note: This README is a template and should be updated with specific details about your project. For more information on crafting effective README files, refer to GitHub's guide on [About READMEs](https://docs.github.com/en/repositories/managing-your-repositorys-settings-and-features/customizing-your-repository/about-readmes).*
