# Text Augmentation

## 1. Kreiranje okruženja

```bash
conda create -n text-augmentation python=3.11 -y
```

## 2. Aktiviranje okruženja

```bash
conda activate text-augmentation
```

## 3. Instalacija zavisnosti

```bash
python -m pip install --upgrade pip
pip install -r requirements.txt
```

## 4. Dataset

Koristi se Kaggle skup **McDonald's Store Reviews**:

https://www.kaggle.com/datasets/nelgiriyewithana/mcdonalds-store-reviews

Fajl `McDonald_s_Reviews.csv` postaviti u isti folder kao notebook.

## 5. Gemini API ključ

Gemini eksperiment je opcionalan. Ključ ne treba upisivati direktno u notebook, već u .env:

```
GEMINI_API_KEY=KLJUC
```

## 6. Pokretanje

Otvoriti `Text_augmentation_fast_final.ipynb` i pokrenuti ćelije redom.

## Podešavanje vremena izvršavanja

Na početku notebook-a nalaze se:

```python
N_QUICK = 1000
N_ADVANCED = 500
```

`N_QUICK` određuje broj novih primera za lake EDA tehnike.

`N_ADVANCED` određuje broj novih primera za DistilRoBERTa, back-translation, FLAN-T5 i Gemini eksperimente.