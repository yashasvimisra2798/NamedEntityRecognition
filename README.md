# Named Entity Recognition Using LSTM's and Keras

## Introduction
Named entity recognition (NER) ‒ also called entity identification or entity extraction ‒ is an information extraction technique that automatically identifies named entities in
a text and classifies them into predefined categories. Entities can be names of people, organizations, locations, times, quantities, monetary values, percentages, and more.

### Example:

> ”Android Inc. was founded in Palo Alto, California, in October 2003 by Andy Rubin, Rich Miner, Nick Sears, and Chris White.” 

> ”**ORG**(Android Inc.) **O**(was founded in) **LOC**(Palo Alto), **LOC**(California), **O**(in) **TIME**(October 2003) **O**(by) **PER**(Andy Rubin), **PER**(Rich Miner), **PER**(Nick Sears), **O**(and) **PER**(Chris White).“ 

Dataset: `ner_dataset.csv`

Labels:   `'O', 'B-geo', 'B-gpe', 'B-per', 'I-geo', 'B-org', 'I-org', 'B-tim','B-art', 'I-art', 'I-per', 'I-gpe', 'I-tim', 'B-nat', 'B-eve','I-eve', 'I-nat' `

Used libraries: `keras, tensorflow, numpy, scikit-learn, matplotlib, pandas`


### Comparing the length of sentences
<img src="https://github.com/yashasvimisra2798/NamedEntityRecognition/blob/master/plots/Capture.PNG"/> 


## Results:

| Word      | True          | Pred    | 
| --------- |:-------------:| -------:| 
|The        |   O           |  O      |
|Vatican    |   B-org	      |  B-org  |
|has        |    O	        |  O      |
|announced  |    O	        |  O      |
|that       |    O	        |  O      |
|U.S.       |   B-org	      |  B-geo  |
|President  |   B-per	      |  B-per  |
|George     |   I-per	      |  I-per  |
|Bush       |   I-per	      |  I-per  |
|will       |    O	        |  O      |
|meet       |    O	        |  O      |
|with       |    O	        |  O      |
|Pope       |    O	        |  O      |
|Benedict   |   B-per	      |  I-per  |
|in         |   O	          |  O      | 
|June       |   B-tim	      |  B-Tim  |
