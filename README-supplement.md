# Tested by KiokAHn
##  Environment
- MS Windows 10 Pro    
- Python 3.10.7    
- PyTorch 1.12    
- torchvision 0.13.1    
- torchaudio 0.12.1    
- CUDA 11.6    


## Install PyTorch   
```
pip3 install torch torchvision torchaudio --extra-index-url https://download.pytorch.org/whl/cu116
```

## Install torch_geometric   
https://pytorch-geometric.readthedocs.io/en/latest/notes/installation.html    
```
pip install torch-scatter torch-sparse torch-cluster torch-spline-conv torch-geometric -f https://data.pyg.org/whl/torch-1.12.0+cu116.html
```


### code modified
./layers.py, line number of 31.    

```
#data.edge_index, edge_attr = coalesce(edge_index, edge_attr, n, n, op='min', fill_value=fill)
data.edge_index, edge_attr = coalesce(edge_index, edge_attr, n, n, op='min')
```