## Logger

A small thread-safe logging class supporting multiple streams, event handling, message groups, date and different severity types. The Logger also logs by default to standard output, which means messages will automatically appear in the Console window on console projects and if you are using Visual Studio on a winforms project, the messages will appear in the debug output. This can also be configured.

## Basic Usage
```csharp
// Add a file
Log.AddLogFile("mylog.log");

// Log info
Log.Info("my info log message");

// Log a warning
Log.Warning("my warning log message");

// Log an error
Log.Error("my error log message");

// Log a debug message
Log.Debug("my debug log message");

// Log an verbose message
Log.Verbose("my verbose log message");
```

The logger supports logging up to a configured severity level. For example, if the severity level is `Error`, then log messages with severity `Error` and below will be logged. The default severity level is

You can set the log level through the `LogLevel` property. Example:
```csharp
Log.Instance().LogLevel = Log.LogType.Verbose;
```

For more usage options, refer to the code, it is heavy documented.

## Installation
You can download the latest build here: https://github.com/snixtho/Logger/releases
After download, just add it as a reference to your project.
