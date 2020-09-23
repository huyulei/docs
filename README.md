﻿# MindSpore Documents

![MindSpore Logo](resource/MindSpore-logo.png)

[查看中文](./README_CN.md)

## Overview

This project provides the source files of the installation guide, tutorials, and other documents, as well as API configurations on the MindSpore official website <https://www.mindspore.cn>.

## Contributions

You are welcome to contribute documents. If you want to contribute documents, read the [CONTRIBUTING_DOC.md](./CONTRIBUTING_DOC.md). Please comply with the document writing specifications, and submit documents according to the process rules. After the documents are approved, the changes will be displayed in the document project and on the official website.

If you have any comments or suggestions on the documents, submit them in Issues.

## Directory Structure Description

```
docs
├───docs // Technical documents about architecture, network list, operator list, programming guide and so on. Configuration files for API generation.
│ 
├───install // Installation guide.
│ 
├───lite // Summary of all documents related to mindspore lite and their links.
│    
├───resource // Resource-related documents.
│      
├───tools // Automation tool.
│    
├───tutorials // Tutorial-related documents.
│      
└───README_CN.md // Docs repository description.
```

## Document Construction

MindSpore tutorials and API documents can be generated by [Sphinx](https://www.sphinx-doc.org/en/master/). The following uses the Python API document as an example to describe the procedure, and ensure that MindSpore, MindSpore Hub and MindArmour have been installed.

1. Download code of the MindSpore Docs repository.
   ```shell
   git clone https://gitee.com/mindspore/docs.git -b r1.0
   ```
2. Go to the api_python directory and install the dependency items in the `requirements.txt` file.
   ```shell
   cd docs/api_python
   pip install -r requirements.txt
   ```
3. Run the following command in the api_python directory to create the `build_zh_cn/html` directory that stores the generated document web page. You can open `build_zh_cn/html/index.html` to view the API document.
   ```
   make html
   ```
   > If you only need to generate the MindSpore API, please modify the `source_zh_cn/conf.py` file, comment the `import mindspore_hub` and `import mindarmour` statements, and then perform this step.

## License

- [Apache License 2.0](LICENSE)
- [Creative Commons License version 4.0](LICENSE-CC-BY-4.0)