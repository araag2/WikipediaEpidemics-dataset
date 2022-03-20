# Wikipedia Epidemics Dataset

This dataset was built based on a segment of the collection of surveys/articles available on https://en.wikipedia.org/wiki/List_of_epidemics#Chronology.

The dataset is split in two directories:

  * `references`: reference key-phrases for evaluation purposes
  * `test`: test set of articles in raw .txt format

In order to build the test set, surveys were extracted in pdf form and converted in .txt format using https://pypi.org/project/pdfminer/.

As for reference key-phrases, they're in the JSON (https://www.json.org/json-en.html) format and are named accordingly:

    test[-stem]?.json

All key-phrases were provided by the source surveys. Stemming was done using the nltk PorterStemmer https://www.nltk.org/_modules/nltk/stem/porter.html.

Within the JSON files, the formatting is as follows:

    {
        "document identifier": [
            [
                "kp1"
            ],
            [
                "kp2"
            ],
            ...
        ],
        ...
    }

### Dataset Info

| Name | Language | Documents | Avg. KPs | Absent KPs | Avg. Words |
| :---: | :---: | :---: | :---: | :---: | :---: |
| WikiEpid | EN | - | - | - | - |
