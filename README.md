# Resume-and-CV-Parsing-with-Spacy

What is Resume Parsing ?

Resume Parsing is conversion of a free-form resume document into a structured set of information suitable for storage, reporting, and manipulation by software. Resume parsing helps recruiters to efficiently manage electronic resume documents sent electronically. Resume parsers are an integral part of Application Tracking System (ATS) which is used by most of the recruiters.

What is spaCy ?

spaCy is an open-source software library for advanced natural language processing, written in the programming languages Python and Cython. spaCy comes with pretrained pipelines and currently supports tokenization and training for 60+ languages. It features state-of-the-art speed and neural network models for tagging, parsing, named entity recognition, text classification and more.

Steps for Resume Parsing

1. Converting .pdf data to plain text
Generally resumes are in .pdf format. Before parsing resumes it is necessary to convert them in plain text. For this PyMuPDF module can be used.

2. Extracting name
   
One of the key features of spaCy is Named Entity Recognition. Named Entity Recognition (NER) can be used for information extraction, locate and classify named entities in text into pre-defined categories such as the names of persons, organizations, locations, date, numeric values etc.

3. Extracting email and mobile number
   
Email and mobile numbers have fixed patterns. To extract them regular expression(RegEx) can be used. Regular Expressions(RegEx) is a way of achieving complex string matching based on simple or complex patterns. In spaCy, it can be leveraged in a few different pipes (depending on the task at hand as we shall see), to identify things such as entities or pattern matching.

4. Extracting Skills
spaCy’s pretrained models mostly trained for general purpose datasets. Often times the domains in which we wish to deploy models, off-the-shelf models will fail because they have not been trained on domain-specific texts. This can be resolved by spaCy’s entity ruler.

The Entity Ruler is a spaCy factory that allows one to create a set of patterns with corresponding labels. Users can create an Entity Ruler, give it a set of instructions, and then use these instructions to find and label entities. Once the user has created the EntityRuler and given it a set of instructions, the user can then add it to the spaCy pipeline as a new pipe.

In the end, as spaCy’s pretrained models are not domain specific, it is not possible to extract other domain specific entities such as education, experience, designation with them accurately. In order to get more accurate results one needs to train their own model. For training the model, an annotated dataset which defines entities to be recognized is required.


