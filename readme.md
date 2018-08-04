# Spam classifier

## Implementing a spam classifier using Support Vector Machines

SVM enable detection of complex decision boundary more effectively than classic logistic regression most of the times.

## Steps

1. Normalize the email by extracting the kernel of each word ex (hosting, host, hosted,.. reduced to 'host')
2. This kernel word corresponds to an entry in a vocabulary file where each cell word is linked with an id
3. For each email, a feature vector composed of all the words present in the vocabulary file is built. If the word is present in the email the i-th row of the vector is 1, 0 otherwise.
4. A training set of vectors is fed to the svm
5. Test performance on a training set


## Run with a sample email

Simply run the `spam_classifier.m` script and the output will be displayed in the console.


## Try with your email

To classify one of your email simply copy and paste its text content into a file (let's say `my_email.txt`) under the 
`code\samples` directory. Then, modify the `spam_classifier.m` line 70 to update it with your filename:
```matlab
filename = 'samples/my_email.txt';
``` 
Then, run the `spam_classifier.m` script.


## Further readings 
Check _honey pot_ project who try to gather as much as spam emails as possible to build a better vocabulary file or other type of feature. 

## Note
This project was part of [Andrew Ng's Mooc on machine learning](https://www.coursera.org/learn/machine-learning) which I strongly recommend.