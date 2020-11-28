# DATA511 Wildfire project

This repo contains the Jupyter Notebook used to cross-join the MNET datasets with the Wildfire Data.

## Obtaining the dataset
- Contact us for obtaining the wildfire dataset (csv format)
- The MNET datasets (nc format) are available online by on the following webpage, wget scripts are also available: http://www.climatologylab.org/gridmet.html

## Defining the datasets
Add a new entry to the following dict
```
mnet_datasets = [
    {
        'name': 'pdsi',
        'col': 'palmer_drought_severity_index',
        'ops': ['min', 'max', 'avg', 'count']
    }
]
```

- `name`: parameter is the mnet dataset prefix (will be appended with the `year` ex: pdsi -> `pdsi_2005.csv`)
- `col`: what is the column name in the dataset that refers to the numerical value we're trying to cross-join
- `ops`: what are the different operations (defined in the `execute_op` function do we want to execute on the series and add a new column to the wildfire dataset? 

## Contact
- Summer (Xinran) Ai 
- Joyce Zhang
- Jeremie Poisson
