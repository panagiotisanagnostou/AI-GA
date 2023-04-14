AI-GA: AI-Generated Abstracts dataset
=====================================

The AI-GA (Artificial Intelligence Generated Abstracts) dataset is a collection of abstracts and titles, with half of the abstracts being AI-generated and the other half being original. This dataset is designed to be used for research and experimentation in the field of natural language processing, particularly in the context of language generation and machine learning.

Dataset Description
-------------------

The AI-GA dataset contains a total of *28662* samples, with each sample consisting of an abstract, a title, and a label. The dataset is split evenly into two categories: "AI-generated abstracts" and "original abstracts". The label indicates whether the sample is an original abstract (labeled as 0) or an AI-generated abstract (labeled as 1). The AI-generated abstracts are generated using state-of-the-art language generation techniques specifically, the GPT-3 model. The original abstracts are sourced from a corpus of existing research papers about the COVID-19 pandemic found on [GitHub](https://github.com/allenai/cord19).

The dataset is provided in a CSV format, with each row representing a single sample. The CSV file contains three columns: `abstract`, `title`, and `label`. The `abstract` column contains the text of the abstract, the `title` column contains the title of the corresponding abstract, and the `label` column contains the label indicating the type of the abstract.


Usage Instructions
------------------

To use the AI-GA dataset, you can download the `ai-ga-dataset.csv` file and load it into your preferred programming environment or machine learning framework. The `read_data.py` is a Python script designed to clean and split the AI-GA dataset. It takes the AI-GA dataset as input and performs cleaning operations such as removing special characters, converting text to lowercase, and removing stop words. It then splits the cleaned data into train and test sets for machine learning or natural language processing tasks.

The script supports the following command line arguments:

- `clean`: A boolean argument (True/False) to specify whether to clean the text data. If set to True, the script will perform text cleaning operations. Default is False.

- `split`: A floating point argument (0.0 to 1.0) to specify the ratio for train/test splitting. The script will randomly split the data into train and test sets according to the specified ratio. Default is 0.8, which means 80% train and 20% test.

- `random_state`: An integer argument to specify the random seed for train/test splitting. The script will use this seed to ensure reproducibility of the same train/test split. Default is value of the random state is 42.

The default arguments of this script recreate the data as we used them in our experiments. The final train and test sets are saved as CSV files in the folder of the script.

### Usage

To run the script, you can use the following command:

```bash
python read_data.py [clean=True|False] [split=FLOAT] [random_state=INT]
```

The dependencies for the script are listed in the requirements.txt file. You can install the dependencies using the following command:

```bash
pip install -r requirements.txt
```

If you encounter any issues with the script, please create an issue in this repository.

### Examples

1. Run the script with default settings (no cleaning, 80% train and 20% test, no specific random seed):

```bash
python read_data.py
```

2. Clean the text data and split into 75% train and 25% test sets:

```bash
python read_data.py split=0.75
```

3. Clean the text data, split into 80% train and 20% test sets, and set the random seed to 123:

Command line execution:
```bash
python read_data.py clean=True split=0.8 random_state=123
```

Dataset License
---------------

The AI-GA dataset is released under the [MIT license](https://github.com/panagiotisanagnostou/AI-GA/blob/main/LICENSE).


Contributions
-------------

Contributions to the AI-GA dataset are welcome! If you would like to contribute to this dataset by providing additional samples or improving the existing dataset, please create an issue in this repository or contact the repository owner for more information.

Citation
--------

If you use the AI-GA dataset in your research or publications, please acknowledge its use by citing this repository.

```bibtex
@misc{theocharopoulos2023detection,
      title={Detection of Fake Generated Scientific Abstracts}, 
      author={Panagiotis C. Theocharopoulos and Panagiotis Anagnostou and Anastasia Tsoukala and Spiros V. Georgakopoulos and Sotiris K. Tasoulis and Vassilis P. Plagianakos},
      year={2023},
      eprint={2304.06148},
      archivePrefix={arXiv},
      primaryClass={cs.CL}
}
```

Contact Information
-------------------

For any questions, issues, or feedback regarding the AI-GA dataset or this repository, please contact Panagiotis Theocharopoulos [:email:](mailto:ptheochar@uth.gr) and Panagiotis Anagnostou [:email:](mailto:panagno@uth.gr).
