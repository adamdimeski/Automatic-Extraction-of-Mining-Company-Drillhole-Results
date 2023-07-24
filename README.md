# Automatic-Extraction-of-Mining-Company-Drillhole-Results
## About
This is the repository for the corpus for extracting drillhole results from Australian mining companies. This corpus is further discussed in a short paper shown below. There is also a short blog post about our research found [here](https://adamdimeski.github.io/2022/12/18/Automatic-Extraction-of-Mineral-Results.html).

## Paper Details  
Paper Title: Automatic Extraction of Structured Mineral Drillhole Results from Unstructured Mining Company Reports  

Authors: Adam Dimeski  a.dimeski@uqconnect.edu.au,  Afshin Rahimi a.rahimi@uq.edu.au  
Link to Paper: https://aclanthology.org/2022.wnut-1.16/  

Mining companies provide reports about their mineral exploration programs, commonly through annual reports and assay reports. These reports contain "drill-hole sentences" which are phrases containing a unique drillhole code, depth, material, type and material percentage. See the example extract below.

![Example Sentence](drillhole.svg)

## Dataset
Contained in the data folder is the annotated mining report data in csv format. Three splits have been done to separate the annotated data by random, by material type and by company. Over 23 ASX-listed companies are contained in the dataset containing a total of 50 reports. In total the corpus contains over 600K words and 22.7K sentences with 10.8K word tagged as part of a drillhole sentence. 

## Annotation Schema
The IOB format was used to tag the dataset with 5 types of tags.  
H - Hole ID  
M - Material  
P - Percentage  
D - Depth  
E - Extra  

## Benchmark Models
Two models were used to assess the performance of neural network models for extracting drillhole data.
1. Bi-LSTM-CRF based on https://github.com/Gxzzz/BiLSTM-CRF
2. BERT model based on  https://github.com/guillaumegenthial/tf_ner
