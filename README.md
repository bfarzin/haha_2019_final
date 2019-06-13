# haha_2019
Using Fastai library to classify Twitter jokes in Spanish

Code assocaited with 3rd place finish in F1 score.

1. Install conda with `conda env create -f environment.yml`
3. place twitter data in `./data/all_file.txt`
2. `source activate fastaiv1_dev`
3. `jupter notebook` in the home directory, go to the `LM Train in Notebook` and run
4. Put `haha_2019_train.csv` and `haha_2019_test.csv` in `./data/` directory
5. Run `Finetune LM` notebook
6. `$cd ./prod/'  run `$./mult_seed_run_fwd_finetune.sh | tee --append out_fwd_1.txt`
7. run run `$./mult_seed_regr_finetune.sh | tee --append out_reg_1.txt`
Generate Submission entry:
8. Run the `Ensemble 20 Seeds select best F1 0610.ipynb` Notebook for the classification
9. Run the `Ensemble 20 modesl select best MSE 0610.ipynb` Notebook for the regression outputs on the test set

Note:
* Data is installed in the same directory in `./data/` directory (but not checked into this repo.)
