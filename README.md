# OPMHDL
Official PyTorch implementation of OPMHDL: Online Partial Modal Hash Learning Framework Based on Dual Path Feature Extraction

## datasets & pre-trained cmh models
1. Download datasets and pre-trained models

```
url:  
code: 
```

2. Change the value of `root` in file `configs\config.yaml` to `/path/to/dataset`.

## pre-trained clip model
1. Download the pre-trained model from `huggingface.co`

``` bash
git lfs install
git clone https://huggingface.co/openai/clip-vit-base-patch32
```

2. Modify the value of `clip_model` in the file `configs\config.yaml`.

## requirements
```bash
python 3.11.5
torch==1.10.2+cu102 -f https://download.pytorch.org/whl/cu102/torch_stable.html
pyyaml
tqdm
h5py
numpy
```

## experimental operation
1. Offline training
```bash
  mode: 'bank_init' # bank_init/online_learning/eval
  phase: 'offline' # offline/online
  dataset_name: choose one # MIRFlickr/NUSWIDE/MSCOCO
  shuffle: False # False/True
```

2. Online training
```bash
  mode: 'online_learning' # bank_init/online_learning/eval
  phase: 'online' # offline/online
  dataset_name: choose one # MIRFlickr/NUSWIDE/MSCOCO
  shuffle: True # False/True
```

3. Eval
```bash
  mode: 'eval' # bank_init/online_learning/eval
  phase: 'online' # offline/online
  dataset_name: choose one # MIRFlickr/NUSWIDE/MSCOCO
  shuffle: True # False/True
```

## training
``` python
python main.py
```
## evaluation
``` python
python eval.py
```

## Reference
...

