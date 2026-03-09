### Register the kernel with VS Code (optional but recommended)

```bash
    uv run python -m ipykernel install --user --name=my-project --display-name "Python (my-project)"
```

### Tip
If you want JupyterLab instead of classic notebooks:

```bash
    uv add jupyterlab
    uv run jupyter lab
```

### To remove the kernel after you're done

#### 1. List all registered kernels


```bash
    jupyter kernelspec list
```
This shows all kernels and their paths, e.g.:
```
Available kernels:
  my-project    /Users/you/Library/Jupyter/kernels/my-project
  python3       /usr/local/share/jupyter/kernels/python3
```

#### 2. Remove the specific kernel

```bash 
    hypyter kernelspec remove my-project
```

Or if you don't have jupyter available globally, run it through uv:

```
 uv run jupyter kernelspec remove my-project
```