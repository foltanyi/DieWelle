## Deep Learning Homework

- Team name: DieWelle
- Team members:
    - Molnár Gábor
    - Papp Viktor
    - Foltányi Bence

### Project Specification

We chose our homework subject from the field of Natural Language Processing (NLP). We would like to determinate the age and gender of bloggers based on their blog posts.

### Data sets

We have found a data set on kaggle, with more than 170,000 blog posts, each labeled with the authors age and gender. We made the data processing on this set.

- [Link to our data set.](https://www.kaggle.com/tomlisankie/blog-posts-labeled-with-age-and-gender/)

We have also found an other [data sets which contains twitter posts.](https://www.kaggle.com/s1m0n38/twitter-text-and-gender/version/1)

### Our solution
The database we used is actually the test database from the dataset, since it already had plenty of samples. We have uploaded it to a [google drive](https://drive.google.com/drive/folders/1W9bwUnqgRu7ZzjSONEh-AsJmdULVaeln) as 'data.json'. This is what our script loads before preprocessing.

Our scrip right now loads the original data then creates a word dictionary out of all the loaded documents. This is used to gather information of the vocabulary of the dataset. After this is done we go through the documents and make sure none of them are longer than a set amount of words. This is done by saturating them to that specific size if they happen to be longer.
When this is done we save these documents with the original labels as a new database, as this task can take quite long given the size of the data.

Finally we use the now processed documents to create one-hot encoded vectors that we pad to a length set at the beginning of the script (this is the same size we set as the maximum word count for our documents).
These vectors can then be used to create our train, validation and test inputs.

### Related work

We have found [this paper](https://cs224d.stanford.edu/reports/BartleAric.pdf) in the subject that gave us some ideas to try out later at the modelling fase, for example using a convolucional neural network.

### Plans

We would like to try different kinds of networks (fully connected, convolucional) and compare the results.


