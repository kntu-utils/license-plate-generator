# Persian Licence Plate Generator
This repository helps you generate persian licence plates.
You're almost done with this part, training your own CNN would be the next step.

## Incentives 
Generated sample:\
![Sample](https://github.com/Amir-Mehrpanah/atumated_lp/blob/master/README_contents/simple_out.png)

For the sake of ease, generated licence plates come with their annotations: \
![Annotation sample](https://github.com/Amir-Mehrpanah/atumated_lp/blob/master/README_contents/ann_simple_out.png) 

Generated sample with perspective transformations:\
![Annotation sample](https://github.com/Amir-Mehrpanah/atumated_lp/blob/master/README_contents/transform.gif) 

On top of all that, it automatically generates associated xml files in pascal voc format: \
![Sample](https://github.com/Amir-Mehrpanah/atumated_lp/blob/master/README_contents/pascal_voc_bbox.png)

## How to Use
```html
*Note: if you have trouble installing jsonnet on windows 
use win_conf.json instead and remove jsonnet dependencies
(For installing jsonnet on windows run: "pip install jsonnet-binary")
```
0. **Create your virtual environment: (recommended)**\
    ```$ python -m venv venv```\
    ```$ source venv/bin/activate``` (or ```.\venv\Scripts\activate.bat``` for windows)

1. **Got all requirements installed:**\
    ```$ pip3 install --upgrade -r requirements.txt```
    
2. **Tweak configuration file: (optional)**
    * project_configurations.jsonnet
    
3. **Out-of-the-box data generation:**
    * With default parameters:\
    ```$ python3 main.py```
    * Override config parameters:\
    ```$ python3 main.py --count 10000```\
    ```$ python3 main.py --no-noise```\
    ```$ python3 main.py --no-dirt``` \
    ```$ python3 main.py --outdir 'output'``` (doesn't already exist) \
    ```$ python3 main.py --no-transform``` \
    ```$ python3 main.py --no-fill``` \
    ```$ python3 main.py --package 8000```
