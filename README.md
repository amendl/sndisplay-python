# sndisplay-python
Porting [sndisplay] library to PyROOT. All credits should go to the original code. This is just a wrapper.

Example:
```
def import_arbitrary_module(module_name,path):
    import importlib.util
    import sys

    spec = importlib.util.spec_from_file_location(module_name,path)
    imported_module = importlib.util.module_from_spec(spec)
    sys.modules[module_name] = imported_module
    spec.loader.exec_module(imported_module)

    return imported_module

# or import sndisplay
sndisplay = import_arbitrary_module('sndisplay',<path-to-sndisplay.py>)
sndisplay.sndisplay_demonstrator_test()
```

---
[adam.mendl@cvut.cz](mailto:adam.mendl@cvut.cz), [amendl@hotmail.com](mailto:amendl@hotmail.com)
