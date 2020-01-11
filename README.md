# Detecting Water Wells in Need of Repair in Tanzania

Only 50% of the Tanzanian population has access to safe water. Out of 59,400 total wells in the dataset, 27,141 in need or repair (46%). Our goal is to build a predictive model to indicate the point when a functional well begins to need repairs.

This `README.md` file will serve as a roadmap to this repository. The repository is open and available to the public.

Directories and files to be aware of:

1. An `environment.yml` file that contains the `conda` packages necessary to running the executables

2. An `src/` directory that contains a `.py` module
    -  In the root directory of this folder on your local machine, in your terminal please run `pip install -e .` to allow the notebooks to access our functions. This will run our `setup.py` file in the root directory

2. A `notebooks/` directory that contains three Jupyter notebooks
    - A data exploration notebook
    - A modeling notebook, containing five models
    - A presentation notebook, containing our final report and model

3. A `data/` directory containing three data files
    - Due to GitHub upload restrictions, these are included as .gitignore files. They are, in brief:
       - Training set target labels
       - Training set features
       - Test set features
    - The data files described above can be found on https://www.drivendata.org/competitions/7/pump-it-up-data-mining-the-water-table/data/. An account setup is required for download.
    - A data dictionary can be found here: https://www.drivendata.org/competitions/7/pump-it-up-data-mining-the-water-table/page/25/
    
4. A `reports/` directory containing a one-page `.md` memo written summarizing the models’ results, written for non-technical stakeholders

5. An “Executive Summary” slideshow PDF available as `presentation.pdf`

Methodology
>  We performed a thorough EDA of the dataset, and built several models to detect if a water well is in need of repairs. We tried 5 different classification models, settling on a random forest classifier as the best performer. It had a higher overall F1 Score, as well as the best recall for the 'Needs Repair' category. Higher recall means fewer false negatives - we believe that this is the best metric by which to evaluate the performance of the model; a well needing repairs yet being labeled as 'Functional' could have devastating effects to a local community. Conversely, a well erroneously labeled 'Needs Repair' would not have nearly as harmful an effect.

Result Metrics
> Our random forest classifier model had an 82% accuracy overall, with an F1-Score for the true 'Functional' label of 84% and 79% for the true 'Needs Repair' label. The metric best for our business case, true “Needs Repair” recall, performed the worst, unfortunately, at 77%. While this is still a good predictive model, if given more time we would like to perform more feature engineering to increase this recall score.
