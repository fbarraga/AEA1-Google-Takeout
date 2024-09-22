# google-location-history-analysis

En aquest repositori trobaràs els scripts de Python i Jupyter notebooks per analitzar [Google Location History](https://support.google.com/accounts/answer/4388034?hl=en) les dades recuperades de [Google Takeout](https://takeout.google.com/settings/takeout). 

Pots utilitzar l'script [prepare_data.py](prepare_data.py) per llegir la informació de Takeout que es troba enzippada i reescriure-la en format CSV. Després pots utilitzar els notebooks de juypter [analyze_activities](analyze_activities.ipynb) i [analyze_places](analyze_places.ipynb) per analitzar les dades interactivament.

Aquest projecte utilitza [Pandas](https://pandas.pydata.org/), [Matplotlib](https://matplotlib.org/), i [bokeh](https://bokeh.org) llibreries que s'han provat amb versions de Python 3.11. **La versió mínima de Python requerida es la 3.10 degut a [un bug a la llibreria Zipfile](https://bugs.python.org/issue40564) que existia abans de la versió 3.10**

# Setup

Clone this repository:
```shell
git clone https://github.com/Stefan4472/google-location-history-analysis.git
```

Create a python virtual environment:
```shell
cd google-location-history-analysis
python -m venv env
# Windows
call env\Scripts\activate
```

Install the required packages:
```shell
python -m pip install -r requirements.txt
```

Prepare your Takeout data:
```shell
python prepare_data.py <INSERT_PATH_TO_TAKEOUT_ZIP>
```

Start Jupyter Notebook:
```shell
python -m jupyter notebook
```

Go to the link shown in the command line, e.g. `http://localhost:8888/?token=...` and try out the `analyze_activities.ipynb` and `analyze_places.ipynb` notebooks on your own data!
