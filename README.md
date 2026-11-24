# gap_sdk_private v5.21.2

## clone
```
git clone --recursive git@github.com:LorenzoLamberti94/5.21.2.git
```

## python env

```
conda create -n gap_sdk_5.21.2 python=3.10.16
conda activate gap_sdk_5.21.2
```

To run deployment in jupyter notebooks run

```
conda activate gap_sdk_5.21.2
conda install ipykernel jupyter
python -m ipykernel install --user --name gap_sdk_5.21.2 --display-name "gap_sdk_5.21.2"
# open jupyter as follows
jupyter notebook
```

## Run code 

1. Init cmake build directory, named "build"
2. Configure the application, using build directory "build" --> here you may choose the plaform (board or gvsoc)
3. Run the target

```
cmake -B build
cmake --build build --target menuconfig
cmake --build build --target run
```
## How to run on finsteraarhorn

ssh finsteraarhorn

```
source /gap/5.21.2/source_5.21.2.sh 
cd /gap/5.21.2/gap_sdk/examples/gap9/basic/helloworld
cmake -B build
cmake --build build --target menuconfig
cmake --build build --target run
```
