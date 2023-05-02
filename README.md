# kata-zig


## Creating a Project
Zig projects need a build.zig file, which tells the compiler how to build the project.
Usually, it is called `build.zig`.

build.zig file can be created based on a library or executable template with this command:
```bash
mkdir hello-world
cd hello-world
zig init-exec # or zig init-lib
```

## Building the project
Run this command:

```bash
zig build 
```

## Run
```bash
zig build run
```

## Debug
Install `CodeLLDB` by *Vadim Chugunov* plugin in VSCode.


Add an entry in launch.json file:
```json
{
  "type": "lldb",
  "request": "launch",
  "name": "Debug",
  "program": "./zig-lang/hello-world/zig-out/bin/hello-world",
  "args": [],
  "cwd": "${workspaceFolder}"
}
```