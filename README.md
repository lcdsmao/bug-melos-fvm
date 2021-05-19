https://github.com/leoafarias/fvm/issues/296

## Reproduce

### Dependencies

```sh
dart pub global activate fvm
dart pub global activate melos

fvm use --force
```

### Execute command

```sh
melos exec -- exec fvm flutter
```

Randomly fail:
```
$ melos exec
   └> exec fvm flutter
       └> RUNNING (in 4 packages)

--------------------------------------------------------------------------------
[pkg3]: 
[pkg3]: Could not install 2.0.6
[pkg3]: 
[pkg3]: #0      ensureCacheWorkflow (package:fvm/src/workflows/ensure_cache.workflow.dart:61:5)
[pkg3]: <asynchronous suspension>
[pkg3]: #1      FlutterCommand.run (package:fvm/src/commands/flutter_command.dart:30:28)
[pkg3]: <asynchronous suspension>
[pkg3]: #2      CommandRunner.runCommand (package:args/command_runner.dart:196:13)
[pkg3]: <asynchronous suspension>
[pkg3]: #3      FvmCommandRunner.run (package:fvm/src/runner.dart:73:24)
[pkg3]: <asynchronous suspension>
[pkg3]: #4      main (file:///Users/mao/.pub-cache/hosted/pub.dartlang.org/fvm-2.0.4/bin/main.dart:6:8)
[pkg3]: <asynchronous suspension>
[pkg3]: 
[pkg3]: 
[pkg2]: Waiting for another flutter command to release the startup lock...
[pkg4]: Waiting for another flutter command to release the startup lock...
[pkg1]: Manage your Flutter app development.
[pkg1]: 
[pkg1]: Common commands:
[pkg1]: 
[pkg1]:   flutter create <output directory>
[pkg1]:     Create a new Flutter project in the specified directory.
[pkg1]: 
[pkg1]:   flutter run [options]
[pkg1]:     Run your Flutter application on an attached device or in an emulator.
[pkg1]: 
[pkg1]: Usage: flutter <command> [arguments]
[pkg1]: 
[pkg1]: Global options:
[pkg1]: -h, --help                  Print this usage information.
[pkg1]: -v, --verbose               Noisy logging, including all shell commands executed.
[pkg1]:                             If used with --help, shows hidden options.
[pkg1]: -d, --device-id             Target device id or name (prefixes allowed).
[pkg1]:     --version               Reports the version of this tool.
[pkg1]:     --suppress-analytics    Suppress analytics reporting when this command runs.
[pkg1]: 
[pkg1]: Available commands:
[pkg1]:   analyze           Analyze the project's Dart code.
[pkg1]:   assemble          Assemble and build Flutter resources.
[pkg1]:   attach            Attach to a running app.
[pkg1]:   bash-completion   Output command line shell completion setup scripts.
[pkg1]:   build             Build an executable app or install bundle.
[pkg1]:   channel           List or switch Flutter channels.
[pkg1]:   clean             Delete the build/ and .dart_tool/ directories.
[pkg1]:   config            Configure Flutter settings.
[pkg1]:   create            Create a new Flutter project.
[pkg1]:   devices           List all connected devices.
[pkg1]:   doctor            Show information about the installed tooling.
[pkg1]:   downgrade         Downgrade Flutter to the last active version for the current channel.
[pkg1]:   drive             Run integration tests for the project on an attached device or emulator.
[pkg1]:   emulators         List, launch and create emulators.
[pkg1]:   format            Format one or more Dart files.
[pkg1]:   gen-l10n          Generate localizations for the current project.
[pkg1]:   install           Install a Flutter app on an attached device.
[pkg1]:   logs              Show log output for running Flutter apps.
[pkg1]:   precache          Populate the Flutter tool's cache of binary artifacts.
[pkg1]:   pub               Commands for managing Flutter packages.
[pkg1]:   run               Run your Flutter app on an attached device.
[pkg1]:   screenshot        Take a screenshot from a connected device.
[pkg1]:   symbolize         Symbolize a stack trace from an AOT-compiled Flutter app.
[pkg1]:   test              Run Flutter unit tests for the current project.
[pkg1]:   upgrade           Upgrade your copy of Flutter.
[pkg1]: 
[pkg1]: Run "flutter help <command>" for more information about a command.
[pkg1]: Run "flutter help -v" for verbose help output, including less commonly used options.
[pkg2]: Manage your Flutter app development.
[pkg2]: 
[pkg2]: Common commands:
[pkg2]: 
[pkg2]:   flutter create <output directory>
[pkg2]:     Create a new Flutter project in the specified directory.
[pkg2]: 
[pkg2]:   flutter run [options]
[pkg2]:     Run your Flutter application on an attached device or in an emulator.
[pkg2]: 
[pkg2]: Usage: flutter <command> [arguments]
[pkg2]: 
[pkg2]: Global options:
[pkg2]: -h, --help                  Print this usage information.
[pkg2]: -v, --verbose               Noisy logging, including all shell commands executed.
[pkg2]:                             If used with --help, shows hidden options.
[pkg2]: -d, --device-id             Target device id or name (prefixes allowed).
[pkg2]:     --version               Reports the version of this tool.
[pkg2]:     --suppress-analytics    Suppress analytics reporting when this command runs.
[pkg2]: 
[pkg2]: Available commands:
[pkg2]:   analyze           Analyze the project's Dart code.
[pkg2]:   assemble          Assemble and build Flutter resources.
[pkg2]:   attach            Attach to a running app.
[pkg2]:   bash-completion   Output command line shell completion setup scripts.
[pkg2]:   build             Build an executable app or install bundle.
[pkg2]:   channel           List or switch Flutter channels.
[pkg2]:   clean             Delete the build/ and .dart_tool/ directories.
[pkg2]:   config            Configure Flutter settings.
[pkg2]:   create            Create a new Flutter project.
[pkg2]:   devices           List all connected devices.
[pkg2]:   doctor            Show information about the installed tooling.
[pkg2]:   downgrade         Downgrade Flutter to the last active version for the current channel.
[pkg2]:   drive             Run integration tests for the project on an attached device or emulator.
[pkg2]:   emulators         List, launch and create emulators.
[pkg2]:   format            Format one or more Dart files.
[pkg2]:   gen-l10n          Generate localizations for the current project.
[pkg2]:   install           Install a Flutter app on an attached device.
[pkg2]:   logs              Show log output for running Flutter apps.
[pkg2]:   precache          Populate the Flutter tool's cache of binary artifacts.
[pkg2]:   pub               Commands for managing Flutter packages.
[pkg2]:   run               Run your Flutter app on an attached device.
[pkg2]:   screenshot        Take a screenshot from a connected device.
[pkg2]:   symbolize         Symbolize a stack trace from an AOT-compiled Flutter app.
[pkg2]:   test              Run Flutter unit tests for the current project.
[pkg2]:   upgrade           Upgrade your copy of Flutter.
[pkg2]: 
[pkg2]: Run "flutter help <command>" for more information about a command.
[pkg2]: Run "flutter help -v" for verbose help output, including less commonly used options.
[pkg4]: Manage your Flutter app development.
[pkg4]: 
[pkg4]: Common commands:
[pkg4]: 
[pkg4]:   flutter create <output directory>
[pkg4]:     Create a new Flutter project in the specified directory.
[pkg4]: 
[pkg4]:   flutter run [options]
[pkg4]:     Run your Flutter application on an attached device or in an emulator.
[pkg4]: 
[pkg4]: Usage: flutter <command> [arguments]
[pkg4]: 
[pkg4]: Global options:
[pkg4]: -h, --help                  Print this usage information.
[pkg4]: -v, --verbose               Noisy logging, including all shell commands executed.
[pkg4]:                             If used with --help, shows hidden options.
[pkg4]: -d, --device-id             Target device id or name (prefixes allowed).
[pkg4]:     --version               Reports the version of this tool.
[pkg4]:     --suppress-analytics    Suppress analytics reporting when this command runs.
[pkg4]: 
[pkg4]: Available commands:
[pkg4]:   analyze           Analyze the project's Dart code.
[pkg4]:   assemble          Assemble and build Flutter resources.
[pkg4]:   attach            Attach to a running app.
[pkg4]:   bash-completion   Output command line shell completion setup scripts.
[pkg4]:   build             Build an executable app or install bundle.
[pkg4]:   channel           List or switch Flutter channels.
[pkg4]:   clean             Delete the build/ and .dart_tool/ directories.
[pkg4]:   config            Configure Flutter settings.
[pkg4]:   create            Create a new Flutter project.
[pkg4]:   devices           List all connected devices.
[pkg4]:   doctor            Show information about the installed tooling.
[pkg4]:   downgrade         Downgrade Flutter to the last active version for the current channel.
[pkg4]:   drive             Run integration tests for the project on an attached device or emulator.
[pkg4]:   emulators         List, launch and create emulators.
[pkg4]:   format            Format one or more Dart files.
[pkg4]:   gen-l10n          Generate localizations for the current project.
[pkg4]:   install           Install a Flutter app on an attached device.
[pkg4]:   logs              Show log output for running Flutter apps.
[pkg4]:   precache          Populate the Flutter tool's cache of binary artifacts.
[pkg4]:   pub               Commands for managing Flutter packages.
[pkg4]:   run               Run your Flutter app on an attached device.
[pkg4]:   screenshot        Take a screenshot from a connected device.
[pkg4]:   symbolize         Symbolize a stack trace from an AOT-compiled Flutter app.
[pkg4]:   test              Run Flutter unit tests for the current project.
[pkg4]:   upgrade           Upgrade your copy of Flutter.
[pkg4]: 
[pkg4]: Run "flutter help <command>" for more information about a command.
[pkg4]: Run "flutter help -v" for verbose help output, including less commonly used options.
--------------------------------------------------------------------------------

$ melos exec
   └> exec fvm flutter
       └> FAILED (in 1 packages)
           └> pkg3 (with exit code 64)
```


