# marsh-wxpython
The folder structure should be in the following way:

### Directory layout

    marsh_excelTopython
    ├── asset                   # Image and Data files
    ├── src                     # Source files (.py files)
    ├── spec_file.txt           # Libraries that are needed to be installed through 'conda'
    └── requirements_pip.txt    # Libraries that are needed to be installed through 'pip'

### Installing the required libraries and softwares

Step 1: Install the Microsoft Visual C++ Compiler for Python 2.7 from the following [URL](https://www.microsoft.com/en-us/download/details.aspx?id=44266)
    
Step 2: Install or enable the .NET framework 3.5

Step 3: Run the following command to install the libraries through conda. An environment will be created with the name 'myenv'.
```
conda create --name myenv --file spec_file.txt
```
After creating the environment, just activate the environment by 
```
activate myenv
```

Step 4: Run the following command to install the other needed libraries through 'pip'
```
pip install requirements_pip.text
```

Step 5: Install the py2exe by running the command
```
pip install http://sourceforge.net/projects/py2exe/files/latest/download?source=files
```

### Generating the executable file

Step 1: After installing all the required libraries, navigate to src folder in the activated environment 'myenv'.

Now type
```
python setup.py py2exe
```

Step 2: With the command execution, two folders will be generated:

* **build** - *In the src directory*
* **dist** - *In the marsh_excelTopython directory*

Now navigate to the dist folder and open the excel_to_python.exe by double clicking on it.
