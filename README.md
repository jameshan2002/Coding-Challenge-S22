# ACM Research Coding Challenge (Spring 2022)

## [](https://github.com/ACM-Research/-DRAFT-Coding-Challenge-S22#question-one)Question

[Binary classification](https://en.wikipedia.org/wiki/Binary_classification) is a type of classification task that labels elements of a set (i.e. dataset) into two different groups. An example of this type of classification would be identifying if people had a specific disease or not based on certain health characteristics. The dataset found in `mushrooms.csv` holds data (22 different characteristics, specifically) about different types of mushrooms, including a mushroom's cap shape, cap surface texture, cap color, bruising, odor, and more. Remember to split the data into test and training sets (you can choose your own percent split). Information about the meaning of the letters under each column can be found within the file `attributelegend.txt`.

**With the file `mushrooms.csv`, use an algorithm of your choice to classify whether a mushroom is poisonous or edible.**

## Explaination for my answer
**Liberies used**
- pandas
- numpy
- Matplotlib
- seaborn
- Sk-learn package
  - preprocessing
  - model_selection
  - metrics
  - linear_model
 
**Documentations used**
- [Non numerical to Numerical Data](https://pythonprogramming.net/working-with-non-numerical-data-machine-learning-tutorial/)
- [Beginner's guide of Binary Classification](https://www.analyticsvidhya.com/blog/2021/08/a-beginners-guide-to-machine-learning-binary-classification-of-legendary-pokemon-using-multiple-ml-algorithms/)

### Approach
Before starting this challenge, I had no idea of what Machine Learning is or what binary classification was. To understand what it is, I searched "binary classification python tutorial" on youtube, and found CS Dojo's [video](https://www.youtube.com/watch?v=a9UrKTVEeZA), which helped set up the environment and learn how to use Jupiter notebook.

### Analyzing Data
After understanding how to use Jupiter notebook, I started to analyze the CSV data that will help me to understand which data can help to separate poisonous and edible mushrooms. So I graphed only the poisonous mushroom for each column and analyzed the population of each type. I discovered the Gil attachment, Gil-spacing, veil-color, ring-number, and veil-type had the largest poisonous mushroom population in each column.

### Preprocessing
I divided it into two data, one with no info on class data but with all other attribute data, one with only class data. Then I converted all non-numerical data to numerical data using [this](https://pythonprogramming.net/working-with-non-numerical-data-machine-learning-tutorial/). And finalizing by splitting the test and ML train.

### Machine Learning and Confusion Metrix
I used the Logistic Regression algorithm because it is widely used for binary classification. It uses the logit function for the outcome. A probability is generated in output and it is classified into 0 or 1, by using the sigmoid activation function. Using the Logistic Regression algorithm, I have achieved 97.05 % accuracy.

And looking at the confusion matrix, there were only 48 negatives from the result (21 False Negative, 28 False Positive).
