- ## reproduce
	- ### environment setup
		- ✔️ removed conda and existed environments back-up
		- ✔️ installed miniconda and mamba (lightweight and speedy)
		- ✔️ CUDA 11.1, gcc g++ 7.5 installation on PC
	- ### code running
		- #### problems
			- ❓️ dataset (version mismatch?):
				- **no splits file** -> ✔️ read names of ply files and randomly generate train.txt and test.txt
				- received **data amount doesn't match** described in the paper (144 vs. 145)
			- ❓️incomplete code:
				- ✔️ code in  lib/ folder -> decompiled using uncompyle6
				  ```
				  uncompyle6 -o CODE_FILE_NAME.py COMPILED_FILE_NAME.pyc
				  ```
				- **config.py missing** -> ✔️ wrote config.py according to pheno4d.sh and PointContrast
				- **no pre-training code**
			- general:
				- 🧐could run the code (thought as finetune code), but **reaches CPU memory when loading data and GPU memory when training each time**, even set batch_size=1
