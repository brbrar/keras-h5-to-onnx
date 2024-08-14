# Convert Keras h5 to ONNX format
Method I used to convert h5 to ONNX for implementation in Untiy Sentis. Uses Python3, TensorFlow, Anaconda, Jupyter Notebook. 


## Installation and method
1. Clone this repo.
2. Create and activate the Anaconda environment with required dependencies:
```
conda env create -f environment.yaml
```
```
conda activate h5-to-onnx
```
3. Place the .h5 model file in the directory.
4. Use Jupyter Notebook in the conda env (keras2onnx) to load the model and save it as SavedModel. Change the model filepath/name in the notebook if neccesary.
5. A model.onnx file should be created. If not, convert from SavedModel to ONNX using line:
```
python3 -m tf2onnx.convert --saved-model tensorflow-model-directory --output model.onnx --opset 13
```
Install additional requirements if necessary.

## Issues
May not support all custom layers.

## To-do:
- Error handling in Notebook.
- Make a script.    