# How to Package and Distribute Python Barcode SDK

## Installing the Tools

```
python -m pip install setuptools wheel twine
```

## Steps
1. Download [Dynamsoft Barcode Reader](https://www.dynamsoft.com/Downloads/Dynamic-Barcode-Reader-Download.aspx).
1. Build Python Barcode Extension
https://github.com/dynamsoft-dbr/python-barcode-windows.
2. Copy **dbr.pyd** and **DynamsoftBarcodeReaderx64.dll** to dbr folder.
3. Run 

    ```
    python setup.py bdist_wheel --plat-name win_amd64
    ```
4. Register a [PyPI account](https://pypi.org/account/register/).
5. Release the package.

    ```
    twine upload dist/*
    ```


## References
* [Distributing Python Modules](https://docs.python.org/3.6/distributing/index.html) 
* [Packaging and distributing projects](https://packaging.python.org/tutorials/distributing-packages/)
* [Writing the Setup Script](https://docs.python.org/2/distutils/setupscript.html)
* [A sample Python project](https://github.com/pypa/sampleproject)
* [PEP 425 -- Compatibility Tags for Built Distributions](https://www.python.org/dev/peps/pep-0425/)
