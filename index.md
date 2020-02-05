# MedSpaCy 

MedSpaCy is an open-source, interoperable, robust, and extensible clinical natural language
 processing (NLP) toolkit based on SpaCy, a widely accepted open-source library, that would provide 
 the research community with a set of commonly used cNLP modules. By establishing and promoting 
 clear and easy-to-use conventions, MedSpaCy enables rapid development of custom NLP components 
 that are directly pluggable into any pipelines that follow the same standard. Expanded user support 
 and clear documentation will serve as a demonstration of the implementation with solutions for common 
 clinical use cases.
 
 By improving the accessibility to high-performance NLP solution optimized for clinical language for 
 clinical researchers, we aim to improve the productivity of cNLP development and reduce development 
 burden. Unlocking new data elements through clinical information extraction enables researchers to 
 find answers to questions previously inaccessible for investigation.
 
 ## Note:
  
 This is an ongoing project under rapid development. The following is more like a roadmap for the project
 rather than documentation. The full tutorial and documentation is expected to come 
 within month. Please feel free to come back later to see the progress.
 
 ## Highlighted Features
 
 ### Easy install
 
 We release MedSpaCy through conda cloud and pypi.org. To install MedSpaCy, you only need one line of command: 
 
 ```shell script
 conda install medspacy
```
 
or 

 ```shell script
 pip install medspacy
```
 
 ### Concise coding 
 
 MedSpaCy inherit the concise coding style from spaCy. To launch a default clinical NLP pipeline for clinical concept recognition,
 you simply put: 
 
 ```python
import medspacy
nlp = medspacy.load('medspacy_clinic_concepts_rec')
doc = nlp("This is an sample clinical document")
```
 
 ### Easy customization
 
 MedSpaCy comes with a set of default commonly used clinical NLP pipelines, such as clinical concept recognition, adverse drug event (ADE)
 identification, chief complain detection. You can easily customize any component within a pipeline, using the same code style to
 configure a spaCy pipeline.
 
 For instance, if you want to use nltk's default sentence segmenter instead of our default clinical sentence segmenter, you can do as follows:
  
 ```python
import medspacy
nlp = medspacy.load('medspacy_clinic_concepts_rec')
nlp.add_pipe('sentence_segmenter', 'nltk')

```
 
 ### Enable machine learning integration
 
 From NLP process results to generate machine learning features for document classification  or snippet classification is also a common task 
 that clinical data scientists often face. MedSpaCy provides a handy wrapper to complete this job with one single line.
 
 ```python
from medspacy import featuregen
vectors=featuregen(doc)
```
 
 ### High performance clinical NLP components
 
 MedSpaCy inherit the spirit of spaCy, we profile its components and cythonize the bottleneck to optimize speed. In addition, we
 leveraging recent advanced data structure to improve rule processing speed. For detailed information, please refer to this published paper:
 
 
 
 
 ### Top performance clinical NLP pipelines
 MedSpaCy comes a set of commonly used clinical NLP pipelines with top performance. For instance, our previous ADE solution ranked top 5 in the n2c2 2019 ADE
 challenge. The ADE pipeline shipped with MedSpaCy includes additional improvement. 
 
 ## How MedSpaCy differs from others companions
 
 There are several similar projects available online, but differ from MedSpaCy in following ways: 
 
 
 
 
 ## Quick Start
 
 To run the default clinical concept recognition pipeline, using the following demo code: 
  ```python
 import medspacy
 nlp = medspacy.load('medspacy_clinic_concepts_rec')
 doc = nlp("This is an sample clinical document")
 ```
  
 
 ## Tutorial
 
##### Install MedSpaCy
##### Load a MedSpaCy pipeline (spaCy language model)
##### Use a customized clinical NLP component
##### Wrap a customized clinical NLP pipeline (spaCy language model)
##### Release your pipeline to spaCy universe
 
 ## User Documentation
 
 Coming soon...
 ## Developer Guide
 Coming soon...
 
 