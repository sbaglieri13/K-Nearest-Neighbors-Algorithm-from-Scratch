# K-Nearest Neighbors Algorithm
The K-Nearest Neighbors algorithm, also known as KNN, is a non-parametric, supervised learning classifier, which uses proximity to make classifications or predictions about the grouping of an individual data point.<br><br> 
While it can be used for either regression or classification problems, it is typically used as a classification algorithm, working off the assumption that similar points can be found near one another.<br><br>
KNN tries to predict the correct class for the test data by calculating the distance between the test data and all the training points. Then select the K number of points which is closet to the test data.<br><br>
There are other ways of calculating distance, and one way might be preferable depending on the problem we are solving.<br>
In this notebook i used Manhattan Distance and Euclidean Distance.<br><br>

<table align="center">
<tr>
  <th>Euclidean Distance</th>
  <th>Manhattan Distance</th>
</tr>
<tr>
 <td>
  $$\sqrt{\sum_{i=1}^n (x_i-y_i)^2}$$    
 </td>
 <td>
  $$\left(\sum_{i=1}^n |x_i-y_i|^p\right)^{1/p}$$
 </td>
</tr>
</table>   

<br>**KNN algorithm step by step:**
* *#1:* Select the number K of the neighbors
* *#2:* Calculate the Euclidean distance of K number of neighbors
* *#3:* Take the K nearest neighbors as per the calculated Euclidean distance
* *#4:* Among these k neighbors, count the number of the data points in each category
* *#5:* Assign the new data points to that category for which the number of the neighbor is maximum

<hr>

We use the dataset *'Pokemon with stats'* to predict whether a pokemon is legendary or not.

**About Dataset**

This data set includes 721 Pokemon, including their number, name, first and second type, and basic stats: HP, Attack, Defense, Special Attack, Special Defense, and Speed.

Columns of dataset:
* **#:** ID for each pokemon
* **Name:** Name of each pokemon
* **Type 1:** Each pokemon has a type, this determines weakness/resistance to attacks
* **Type 2:** Some pokemon are dual type and have 2
* **Total:** sum of all stats that come after this, a general guide to how strong a pokemon is
* **HP:** hit points, or health, defines how much damage a pokemon can withstand before fainting
* **Attack:** the base modifier for normal attacks (eg. Scratch, Punch)
* **Defense:** the base damage resistance against normal attacks
* **SP Atk:** special attack, the base modifier for special attacks (e.g. fire blast, bubble beam)
* **SP Def:** the base damage resistance against special attacks
* **Speed:** determines which pokemon attacks first each round
