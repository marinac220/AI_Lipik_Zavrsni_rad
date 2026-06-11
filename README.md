# Klasifikacija glazbenih žanrova primjenom konvolucijskih neuronskih mreža
## Završni rad iz kolegija Duboko učenje

### Opis problema i cilj
Klasifikacija glazbenih žanrova predstavlja izazovan problem u području obrade audio signala i strojnog učenja. Cilj ovog projekta je razviti model temeljen na dubokom učenju koji automatski prepoznaje glazbeni žanr audio zapisa.

Model je treniran za prepoznavanje 10 različitih glazbenih žanrova korištenjem spektrograma kao ulaznih podataka te konvolucijske neuronske mreže (CNN) za klasifikaciju.

Dodatni cilj projekta bio je istražiti robusnost modela testiranjem na umjetno generiranim hibridnim žanrovima izrađenim pomoću Suno AI alata.


### Opis podataka
Za treniranje modela korišten je skup podataka koji sadrži audio zapise podijeljene u 10 glazbenih žanrova:

- Blues
- Classical
- Country
- Disco
- Hip Hop
- Jazz
- Metal
- Pop
- Reggae
- Rock

Audio datoteke pretvorene su u spektrograme koji služe kao ulaz u neuronsku mrežu.

Dataset
https://www.kaggle.com/datasets/andradaolteanu/gtzan-dataset-music-genre-classification

### Što model radi

Model:

1. Učitava audio zapis.
2. Pretvara audio signal u spektrogram.
3. Koristi konvolucijsku neuronsku mrežu (CNN) za ekstrakciju značajki.
4. Klasificira zapis u jedan od 10 glazbenih žanrova.
5. Vraća predviđeni žanr.

Arhitektura modela sastoji se od:

- Conv2D slojeva
- MaxPooling slojeva
- Flatten sloja
- Dense slojeva
- Softmax izlaza za klasifikaciju

### Kako pokrenuti projekt
Preduvjeti za lokalno pokretanje:

1. Osigurati da je na računalu preuzet minimalno verzija Pythona 3.10.0.
2. Instalirati potrebne biblioteke:

"pip install tensorflow keras librosa numpy pandas matplotlib seaborn scikit-learn"

### Pokretanje
1. Preuzeti dataset.
2. Postaviti putanje do dataset-a u notebooku.
3. Pokrenuti Jupyter Notebook:
4. Otvoriti datoteku:
    Test_Glazbeni_zanr.ipynb
5. Pokrenuti sve ćelije redom
6. Umjesto X u ćeliji slijedećeg sadržaja zamijeniti imenom zvuka koji želimo testirati
    from IPython.display import Audio
    file_path = "./Test_Music/X.mp3"
    y, sr = librosa.load(file_path, sr=44100)
    Audio(data=y, rate=sr)
7. Pokrenuti sve ćelije još jednom

### Rezultati

Model postiže visoku točnost klasifikacije na testnom skupu podataka te pokazuje zanimljivo ponašanje prilikom klasifikacije umjetno generiranih hibridnih glazbenih žanrova.

### Autor

Klarić Marinko

Završni rad – AI Center Lipik
