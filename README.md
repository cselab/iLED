# iLED

This package provides an implementation of the iLED modeling approach.

Menier, E., Kaltenbach, S., Yagoubi, M., Schoenauer, M. & Koumoutsakos, P.: <em>Interpretable Learning of Effective Dynamics for multiscale systems</em>, Proceedings A, The Royal Society, 2025.

Paper available [here](https://royalsocietypublishing.org/doi/epdf/10.1098/rspa.2024.0167).

## Installation

The package can be installed by first cloning the repository:

```
git clone git@github.com:cselab/iLED.git
```

Then installing through the following command:

```
pip3 install -U .
```

or `pip3 install -e .` if you intend to contribute.

## Training a model for the FHN case

A model for the Fitz-Hugh Nagomo case can be trained as follows:

```
python examples/FHN/trainscript.py --work_dir /path/to/work/dir --run_name my_run
```

If unavailable in the specified work_dir, a data directory will be created, in which the data 
will be automatically downloaded.

Model and training options can be modified directly in the `trainscript.py` file.

After training, result plots can be generated with:

```
python examples/FHN/fhn_plotting.py --work_dir /path/to/work/dir --run_name my_run --output examples/FHN/output/
```

The images will be saved in the specified output directory.

