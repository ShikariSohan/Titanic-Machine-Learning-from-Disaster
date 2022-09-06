# Titanic - Machine Learning from Disaster  
It is getting a start problem of  [Kaggle](https://kaggle.com)  
Read the problem description to the understand the problem   
Link of the problem [Titanic](https://www.kaggle.com/competitions/titanic)  

### Score of the provided code : *0.76555*  
### Max Score of mine : *0.76794*  
![max_score](https://github.com/ShikariSohan/Titanic-Machine-Learning-from-Disaster/blob/master/max_score.png)
## Idea / Approach :   
	> I have no idea How to run a model or what a model is. 
    So I approached this problem with my basic sense of if-else conditions and loops.  
I chose 7 columns from the data to start with.  
`col = ['Pclass','Sex', 'Age', 'SibSp','Parch', 'Embarked']`  
I then use the provided test data to determine the survival rate for each column value.  
`Ex- Sex column :  
female    0.742038   
male      0.188908  
`  
After that I have the surviving rate of each value of some selected columns. Then I calculate the sum of all the survival rate of a row.    

```
Ex - 
Sex : male  (0.188908)
Embarked  : S (0.336957)
Pclass : 2 (0.472826)

If a row has these values of those corresponding columns then sum of survival rate is   
0.188908+0.336957+0.472826=0.998691  
```
Its time to predict . So I give a threshold value that determines a person is surivived or not.   
` if threshold <= sum of survial rate ? Survived : Not Survived `  
To find a ideal threshold value I loop through 1 to 3 interval of 0.01 and compare the prediction of mine and actual survived column   
and find the accuracy from the train data.  
`Ideal Threshold :2.5600000000000014 - Train Data Accuracy : 0.8114478114478114`  
By using this theshold I predict the survival of the train data and managed to score **0.76555**  
After that I randomly tweaked the threshold value between 2.4 - 2.5 and achived my personal max score **0.76794**  



