# Analiza skuteczności wybranych metod osadzania słów w zadaniach przetwarzania języka naturalnego

[Sprawdź Raport](https://github.com/mateuszdrozd/)

## Opis pracy

Badania skupiają się na analizie i porównaniu skuteczności różnych metod osadzania słów (statystycznych, statycznych i kontekstowych) w zadaniu klasyfikacji emocji w tekście. Praca obejmuje również weryfikację współczesnych modeli tłumaczenia maszynowego w celu obsługi wielojęzycznych danych tekstowych w aplikacjach działających w czasie rzeczywistym.

## Przebieg badań

Realizacja projektu została podzielona na dwa kluczowe etapy:

1. **Analiza eksploracyjna i modelowanie**:

* **Przygotowanie danych**: Czyszczenie i normalizacja zbioru Twitter Emotion Dataset, który kategoryzuje tekst na sześć emocji: radość, smutek, złość, strach, miłość oraz zaskoczenie.
* **Korekta etykiet**: Implementacja zautomatyzowanego systemu rozwiązywania konfliktów w celu poprawy błędów anotacji przy użyciu algorytmu KNN (k=20, metryka kosinusowa) oraz modelu GPT-4o-mini.
* **Reprezentacja tekstu**: Ekstrakcja cech za pomocą metod statystycznych (TF-IDF), modeli statycznych (Word2Vec o wymiarach 128 i 512) oraz architektur kontekstowych (Sentence-BERT, OpenAI `text-embedding-3-small`).
* **Klasyfikacja**: Trenowanie i ewaluacja modeli regresji logistycznej, XGBoost oraz sieci neuronowych typu Multi-Layer Perceptron (MLP) w oparciu o metryki F1-macro, Accuracy (dokładność) i Balanced Accuracy (dokładność zbalansowana).
* **Ewaluacja tłumaczenia**: Ocena architektur tłumaczeniowych (autorska sieć RNN, M2M-100, mBART) z wykorzystaniem metryki BLEU na polsko-angielskim zbiorze danych Tatoeba.

2. **Implementacja systemu czasu rzeczywistego**:

* Stworzenie interaktywnej aplikacji internetowej przy użyciu języka Python i frameworka Streamlit.
* Aplikacja przetwarza wielojęzyczne dane tekstowe wejściowe (polski, angielski, mandaryński, niemiecki).
* Potok przetwarzania tłumaczy tekst na język angielski za pomocą modelu mBART-50, generuje wektory semantyczne przy użyciu Sentence-BERT i przewiduje rozkład prawdopodobieństwa dominującej emocji przy pomocy sieci MLP.
* Wdrożenie gotowego rozwiązania na platformie Hugging Face Spaces.

## Struktura repozytorium

* `Praca_Inzynierska.pdf`: Pełny tekst pracy inżynierskiej.

## Użyte technologie

* **Język**: Python
* **Framework webowy**: Streamlit
* **Środowisko hostingowe**: Hugging Face Spaces
* **Modele uczenia maszynowego**: XGBoost, regresja logistyczna, MLP (gęste sieci neuronowe)
* **Reprezentacja tekstu**: TF-IDF, Word2Vec, Sentence-BERT (SBERT), OpenAI API
* **Architektury tłumaczeniowe**: mBART-50, M2M-100


----------------------------------------------------------

# Analysis of the Effectiveness of Selected Word Embedding Methods in Natural Language Processing Tasks

[Check Raport](https://github.com/mateuszdrozd/thesis-text-representation-analysis-classification/Praca_Inzynierska.pdf)
## Thesis Overview

The research focuses on analyzing and comparing the effectiveness of various word embedding methods (statistical, static, and contextual) in the task of text emotion classification. It also includes the verification of modern machine translation models to support multilingual text inputs in real-time applications.

## Research Workflow

The project implementation was divided into two key stages:

1. **Exploratory Analysis & Modeling**:
* **Data Preparation**: Cleaning and normalizing the Twitter Emotion Dataset, which categorizes text into six emotions: joy, sadness, anger, fear, love, and surprise.

* **Label Correction**: Implementing an automated conflict-resolution system to fix annotation errors using the KNN algorithm (k=20, cosine metric) and the GPT-4o-mini model.

* **Text Representation**: Extracting features using statistical methods (TF-IDF) , static models (Word2Vec at 128 and 512 dimensions) , and contextual architectures (Sentence-BERT, OpenAI `text-embedding-3-small`).

* **Classification**: Training and evaluating Logistic Regression, XGBoost, and Multi-Layer Perceptron (MLP) networks based on F1-macro, Accuracy, and Balanced Accuracy metrics.

* **Translation Evaluation**: Assessing translation architectures (custom RNN, M2M-100, mBART) using the BLEU metric on the Tatoeba Polish-English dataset.


2. **Real-Time System Implementation**:
* Developed an interactive web application using Python and the Streamlit framework.


* The application processes multilingual text inputs (Polish, English, Mandarin, German).


* The pipeline translates text to English using mBART-50 , generates semantic vectors via Sentence-BERT , and predicts the dominant emotion probability distribution using an MLP network.


* Deployed the final solution on the Hugging Face Spaces platform.

## Repository Structure

* `Praca_Inzynierska.pdf`: Full text of the engineering thesis.

## Technologies Used

* **Language**: Python 

* **Web Framework**: Streamlit 

* **Hosting Environment**: Hugging Face Spaces 

* **Machine Learning Models**: XGBoost , Logistic Regression , MLP (Dense Neural Networks) 

* **Text Representation**: TF-IDF , Word2Vec , Sentence-BERT (SBERT) , OpenAI API 

* **Translation Architectures**: mBART-50 , M2M-100
