# README for ptest

### This is code to explore conda environments and making my own packages.

### It follows this awesome [where_to_put_your_code](https://pythonchb.github.io/PythonTopics/where_to_put_your_code.html) that Rob Hetland pointed me to. Thanks!!

#### I made testenv.yml with minimal packages, and then working from the command line in ptest I ran

```
conda env create -f testenv.yml
```

to activate this do

```
conda activate testenv
```

and to deactivate it do

```
conda deactivate
```

Anytime you change the .yml list just do

```
conda env update -f testenv.yml --prune
```

The -e flag in the .yml for doing the pip install of my_code (my "package") means that you can add new modules to it (it is "editable") and they will be immediately available.

To use the modules in the package just run

```
python test_it.py
```

NOTE: The ability to load the modules persists in the environment even after I remove my_code from the .yml file and update it. But if you do

```
pip uninstall my_code
```

it does get rid of them.

### This is so cool!
