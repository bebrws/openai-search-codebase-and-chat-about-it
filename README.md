Setup tree sitter parsers ( I have included the build folder so you can skip the instructions from https://github.com/tree-sitter/py-tree-sitter)

But you need to clone the following repos:
```
git clone https://github.com/tree-sitter/tree-sitter-go
git clone https://github.com/tree-sitter/tree-sitter-javascript
git clone https://github.com/tree-sitter/tree-sitter-python
```

Then run the following code in python:

```
from tree_sitter import Language, Parser

Language.build_library(
    # Store the library in the `build` directory
    'build/my-languages.so',

    # Include one or more languages
    [
        'tree-sitter-go',
        'tree-sitter-javascript',
        'tree-sitter-python'
    ]
)
``` 

to rebuild your own or add new languages.

