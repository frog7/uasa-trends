# Trends in UA/SA methods and approaches

Accompanying repository for a paper in progress.

To get things up and running, you can clone this repository and install dependencies:

```bash
$ pip install git+https://github.com/ConnectedSystems/metaknowledge.git@add-collections
$ pip install git+https://github.com/titipata/wos_parser.git@master
$ pip install git+https://github.com/ConnectedSystems/restful_wos.git@master
$ pip install git+https://github.com/ConnectedSystems/wosis.git@master
$ pip install ipykernel jupyter notebook ipywidgets
$ git clone https://github.com/frog7/uasa-trends.git
$ python -m ipykernel install --name uasa-trends --display-name "biblio"
```

Analysis was conducted through Jupyter Notebooks which can be found in the `notebooks` directory.

The Wosis relies on NLTK for lemmatization and stemming, and requires the WordNet data to be downloaded.

```python
import nltk

# Display list of locations NLTK searches for language data
print(nltk.data.path)

# Example only
# ['C:\\nltk_data',
#  'D:\\nltk_data',
#  'E:\\nltk_data']

# Select a desired location from the above and run the below
# Here, I selected the second item in the list (Python is a zero-indexed language)
download_location = nltk.data.path[1]
nltk.download('wordnet', download_dir=download_location)
```


(c) 2018 Dominique Douglas-Smith and Takuya Iwanaga