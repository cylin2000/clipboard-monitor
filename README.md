# clipboard_monitor

Clipboard Monitor will monitor the clipboard changes and trigger register events.
It's very easy to use, for details please refer below commands

## Usages
```python
import clipboard_monitor 

def print_text(text):
	print("got text")
	print(text)

def print_files(files):
	print("got files")
	print(files)

def print_image(image):
	print("got image")
	image.save("./test.png")

clipboard_monitor.on_update(print)
clipboard_monitor.on_text(print_text)
clipboard_monitor.on_files(print_files)
clipboard_monitor.on_image(print_image)

clipboard_monitor.wait()
```