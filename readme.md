# Pyodide console

A simple clone of [pyodide console](https://pyodide.org/en/stable/console.html) based on `0.26.1`.

By default [pikepdf](https://github.com/pikepdf/pikepdf/) is also loaded.  
If you're interested on how to compile it for pyodide you can check [my fork](https://github.com/SF73/pikepdf/tree/wasm_build) for a github action.

Some useful functions were also added to "upload" files to pyodide/emscripten FS with a drag'n drop and later retrieve them using a js function.

```py
import js
with open("myFile.pdf", 'rb') as f:
    js.downloadFile("myFile.pdf", f.read())
```

Try it [here](https://sf73.github.io/pyodide-console/console) !

You can also import it using this wheel `https://sf73.github.io/pyodide-console/console/packages/pikepdf-9.1.0-cp312-cp312-pyodide_2024_0_wasm32.whl`

```python
import micropip
await micropip.install("https://sf73.github.io/pyodide-console/console/packages/pikepdf-9.1.0-cp312-cp312-pyodide_2024_0_wasm32.whl")
```