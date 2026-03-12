# Space-tuned x86 debugger & demo tool (in bootloader)

# Demo
![rain demo](https://github.com/x2DA/x86dbgBL/blob/main/assets/demo.jpg)

## Usage:
### Highlighting:
Cursor: h, j, k, l  
Cursor highlight: v (toggle, highlights from position at the time of toggle to cursor position)
### Code:
Ideally define variables under `; -- prog_vars --` and instructions under `prog_start`. There is a referenceable `data` label (which gets dumped to the screen).

### Limitations:
The user has 256 free bytes to have instructions in.
The highlighter can only highlight down and right in relation to its starting position.

## Build:
```
nasm "bootloader.s" -f bin -o "loader.img"
```
## Run:
```
qemu-system-i386 -drive file=NAME.img,format=raw
```
