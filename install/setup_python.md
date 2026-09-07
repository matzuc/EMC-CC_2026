# Configurazione dell'ambiente Python

Questa guida permette di creare l'ambiente Python necessario per il laboratorio tramite Conda. L'ambiente è isolato dalle altre installazioni presenti sul computer.

## 1. Installare Conda

Se Conda non è già presente, installare **Miniforge** seguendo le [istruzioni ufficiali](https://github.com/conda-forge/miniforge#download). Sono adatte anche installazioni esistenti di Miniconda o Anaconda.

Al termine dell'installazione aprire **Miniforge Prompt** su Windows oppure un nuovo terminale su macOS e Linux.

## 2. Scaricare il repository

Il modo più semplice consiste nello scaricare l'[archivio ZIP del repository](https://github.com/matzuc/EMC-CC_2026/archive/refs/heads/main.zip) ed estrarlo in una cartella facilmente raggiungibile.

Chi usa Git può invece eseguire:

```bash
git clone https://github.com/matzuc/EMC-CC_2026.git
cd EMC-CC_2026
```

## 3. Creare l'ambiente

Dal terminale, spostarsi nella cartella principale del repository ed eseguire:

```bash
conda env create --file install/environment.yaml
```

La risoluzione e l'installazione dei pacchetti possono richiedere alcuni minuti.

## 4. Attivare l'ambiente

```bash
conda activate emc_cc_2026
```

L'attivazione va ripetuta ogni volta che si apre un nuovo terminale.

## 5. Verificare l'installazione

Con l'ambiente attivo, eseguire:

```bash
python --version
copernicusmarine --version
jupyter lab
```

L'ultimo comando deve aprire JupyterLab nel browser. Per interromperlo, tornare al terminale e premere `Ctrl+C`.

## Aggiornare un ambiente già creato

Se il file `environment.yaml` viene aggiornato, sincronizzare l'ambiente con:

```bash
conda env update --name emc_cc_2026 --file install/environment.yaml --prune
```

In caso di problemi, annotare il sistema operativo e copiare integralmente il messaggio di errore.
