SOMPY
-----

This repository was forked from the original repository at https://github.com/sevamoo/SOMPY to modify it in order to make the package installable via pip.

### Changes
1. Changed package name to ```sompy-package``` to avoid conflict with already existing ```sompy``` package on PyPI
2. Refactored package replacing ```setup.py``` with ```pyproject.toml```
3. Updated dependencies to include ```scikit-image```
4. General code cleanup and formatting
5. Uploaded package to PyPI

### Installation
To install the package using ```pip``` you can simply do

``` pip install sompy-package ```

### Usage
You can use the package and its modules as usual:
```
import sompy
from sompy.sompy import SOMFactory
from sompy.visualization.mapview import View2D
...
``` 

No changes to the code should be necessary.

-----

All of the following is the original README file from the creator of the repo.

## Original README

A Python Library for Self Organizing Map (SOM)

As much as possible, the structure of SOM is similar to `somtoolbox` in Matlab. It has the following functionalities:

1. Only Batch training, which is faster than online training. It has parallel processing option similar to `sklearn` format and it speeds up the training procedure, but it depends on the data size and mainly the size of the SOM grid.I couldn't manage the memory problem and therefore, I recommend single core processing at the moment. But nevertheless, the implementation of the algorithm is carefully done for all those important matrix calculations, such as `scipy` sparse matrix and `numexpr` for calculation of Euclidean distance.
2. PCA (or RandomPCA (default)) initialization, using `sklearn` or random initialization.
3. component plane visualization (different modes).
4. Hitmap.
5. U-Matrix visualization.
6. 1-d or 2-d SOM with only rectangular, planar grid. (works well in comparison with hexagonal shape, when I was checking in Matlab with somtoolbox).
7. Different methods for function approximation and predictions (mostly using Sklearn).


### Dependencies:
SOMPY has the following dependencies:
- numpy
- scipy
- scikit-learn
- numexpr
- matplotlib
- pandas
- ipdb

### Installation:
```Python
python setup.py install
```


Many thanks to @sebastiandev, the library is now standardized in a pythonic tradition. Below you can see some basic examples, showing how to use the library.
But I recommend you to go through the codes. There are several functionalities already implemented, but not documented. I would be very happy to add your new examples here.

[Basic Example](https://gist.github.com/sevamoo/035c56e7428318dd3065013625f12a11)

### Citation

There is no published paper about this library. However if possible, please cite the library as follows:

```
@misc{moosavi2014sompy,
  title={SOMPY: A Python Library for Self Organizing Map (SOM)},
  author={Moosavi, V and Packmann, S and Vall{\'e}s, I},
  note={GitHub.[Online]. Available: https://github.com/sevamoo/SOMPY},
  year={2014}
}
```


For more information, you can contact me via sevamoo@gmail.com but please report an issue first.




Thanks a lot.
Best Vahid Moosavi
