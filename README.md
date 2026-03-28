# Function Stomping (Local & Remote)

## Overview
This project demonstrates the **Function Stomping technique** in Windows for educational purposes.

Function stomping works by **overwriting an existing function inside a DLL with custom payload**, then executing it.

---

## Techniques Included

### 1. Local Function Stomping
- Targets a function in the current process
- Loads a DLL (`user32.dll`)
- Overwrites `MessageBoxA`
- Executes the payload using a thread

### 2. Remote Function Stomping
- Targets a function in a remote process
- Finds the target process by name
- Overwrites the function in the remote process
- Executes payload using `CreateRemoteThread`

---

## Compilation

Using MinGW:

```bash
x86_64-w64-mingw32-gcc local.c -o local.exe
x86_64-w64-mingw32-gcc remote.c -o remote.exe
```
