# rpcfit
`rpcfit` is a python module corresponding to the IGARSS 2021 paper submission 
*Robust Rational Polynomial Camera Modelling for SAR and Pushbroom Imaging*

Preprint available at [arxiv](https://arxiv.org/abs/2102.13423)  

To install requirements : 
	`pip install -r requirements.txt`

To test the installation: `python usage.py`

The package contains: 
- `gridata.py`: Has the necessary functions to construct the 3D+2D point grid correspondence (CoNtrol Point & ChecK Point). Needs a projection function or a localization function from a physical sensor model. A physical sensor model for the Sentinel-1 satellite may be made available in the future. Otherwise, consider using snappy for Sentinel\-1.

- `Lcurve.py`: Has the necessary function to do the Lcurve criterion with the standard Tikhonov, or with a set of discrete points by using the spline curve interpolation.

- `rpc_fit`: Has the necessary functions to fit the rpc on the constructed grids. use `calibrate_rpc`. Other functions are internal helper funcs.

The **data** folder contains datasets for the test in `usage.py`: 
- *2d* refers to image coordinates *x, y*
- *3d* refers to *lon, lat, height* coordinates
- *train* refers to the *training set*
- *test* refers to the *test set*



