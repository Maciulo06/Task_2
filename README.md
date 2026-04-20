# Heart Disease (UCI) - Drzewo decyzyjne

Projekt przedstawia analizę zbioru danych Heart Disease z repozytorium UCI oraz budowę modelu klasyfikacyjnego opartego na drzewie decyzyjnym.

## Cel projektu

Celem projektu jest przygotowanie danych do modelowania, zbudowanie modelu bazowego oraz sprawdzenie, jak wybrane hiperparametry wpływają na skuteczność klasyfikacji.

## Opis danych

Wykorzystany zbiór danych pochodzi z repozytorium UCI Machine Learning Repository.  
W analizie wykorzystano popularny podzbiór Cleveland.  
Zmienna docelowa `num` została sprowadzona do klasyfikacji binarnej:
- `0` - brak choroby,
- `1` - obecność choroby (`num > 0`).

## Zakres projektu

W notebooku wykonano:
- wczytanie danych,
- wstępną analizę danych,
- sprawdzenie brakujących wartości,
- preprocessing danych,
- imputację braków danych,
- kodowanie kategorii metodą One-Hot Encoding,
- podział danych na zbiór treningowy i testowy,
- budowę modelu `DecisionTreeClassifier`,
- ocenę modelu za pomocą accuracy, macierzy pomyłek, classification report i ROC AUC,
- eksperymenty dla parametrów `max_depth`, `min_samples_leaf` oraz `criterion`.

## Wyniki

Model bazowy osiągnął dokładność około `0.754` na zbiorze testowym.  
Najlepszy wynik dla testowanych wartości `max_depth` uzyskano dla `max_depth = 3`, gdzie accuracy wyniosło około `0.869`.  
Najlepszy wynik dla testowanych wartości `min_samples_leaf` uzyskano dla `min_samples_leaf = 10`, również z accuracy około `0.869`.  
Dla porównywanych kryteriów podziału `gini` i `entropy` uzyskano taki sam wynik testowy, około `0.787`.

## Wykorzystane technologie

- Python
- NumPy
- pandas
- matplotlib
- seaborn
- scikit-learn
- ucimlrepo
- Jupyter Notebook

## Pliki

- `heart_disease_report.ipynb` - główny notebook z analizą i eksperymentami,
- `requirements.txt` - lista wymaganych bibliotek.

## Uruchomienie projektu

Zainstaluj wymagane biblioteki:

```bash
pip install -r requirements.txt
```

Następnie uruchom Jupyter Notebook:

```bash
jupyter notebook
```

i otwórz plik `heart_disease_report.ipynb`.

## Autor

Projekt wykonany w ramach zajęć z analizy danych / uczenia maszynowego.
