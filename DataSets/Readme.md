# Datasets

The dataset contains several files with the original data from Kim et al., .


## Y79_diameter.csv

A list of diameter collected from different cultures of human retinoblastoma Y79 cells in culture.

| key         | units | Description |
|-------------|------- |------------ |
| diameter   | micrometers     | Ferret diameter of the cell                  |

To load it:
```python
import pandas as pd
spikes = pd.read_csv('Y79_diameter.csv')
spikes.describe() # to get basic statistics
```


## Y79_data.csv

Contains measurements on human retinoblastoma cells (Y79). 

| key        | units  | Description |
|------------|--------|------------ |
| uid        | --     | Unique idenfier for the recording (e.g.,Y79_009). Use it as a pandas index |
| diameter   | micrometers     | Ferret diameter of the cell                  |
| Vmb        | milivolts       | The resting membrane potential of the cell  |


To load it:
```python
import pandas as pd
spikes = pd.read_csv('Y79_data.csv', index_col = 'uid')
spikes.info() # info on fields
```
