# Topsis-Calculator
## The efficient python package to calcualate topsis scores

Technique for Order Preference by Similarity to Ideal Solution (TOPSIS) is a multi-criteria-based decision-making method. TOPSIS chooses the alternative of shortest the Euclidean distance from the ideal solution and greatest distance from the negative ideal solution. 

To make this definition easier, let’s suppose you want to buy a mobile phone, you go to a shop and analyze 5 mobile phones on basis of RAM, memory, display size, battery, and price. At last, you’re confused after seeing so many factors and don’t know how to decide which mobile phone you should purchase. TOPSIS is a way to allocate the ranks on basis of the weights and impact of the given factors.

## Published On
- [PYPI](https://pypi.org/project/Topsis-Parth-102016044/)
- [WebApp](http://topsisgenerator.pythonanywhere.com/)

## Features

- Imports an input csv file and calculates Topsis scores and ranks of it
- Output file consists of seaparate columns as Topsis scores and Ranks which is ideal for decision making



And of course Topsis itself is open source with a [public repository](https://github.com/parthvohra25/Topsis)
 on GitHub.

## Installation

Topsis requires [Python](https://www.python.org/downloads/) v3+ to run.
Use pip to install the package.

```sh
pip install Topsis-Parth-102016044
```
## Usage
```sh
import Topsis-Parth-102016044 as top
#call for topsis_score function
top.topsis_score("input.csv","weights","impact","output.csv")
```
- Make sure you enter "weights" and "impact" as string
- The result would be stored in a output csv file with ranks and topsis score respectively.

## Example
input.csv
| Model | corr | R2  | Rmse | Acc |
| --- | --- | --- | --- | --- |
| m1  | 0.79 | 0.62 | 1.25 | 60.89 |
| m2  | 0.66 | 0.44 | 2.89 | 63.07 |
| m3  | 0.56 | 0.31 | 1.57 | 62.87 |
| m4  | 0.82 | 0.67 | 2.68 | 70.19 |
| M5  | 0.75 | 0.56 | 1.3 | 80.39 |

output.csv
| Model | corr | R2  | Rmse | Acc | Topsis score | Rank |
| --- | --- | --- | --- | --- | --- | --- |
| m1  | 0.79 | 0.62 | 1.25 | 60.89 | 0.7722097345612788 | 2   |
| m2  | 0.66 | 0.44 | 2.89 | 63.07 | 0.22559875426413367 | 5   |
| m3  | 0.56 | 0.31 | 1.57 | 62.87 | 0.43889731728018605 | 4   |
| m4  | 0.82 | 0.67 | 2.68 | 70.19 | 0.5238778712729114 | 3   |
| M5  | 0.75 | 0.56 | 1.3 | 80.39 | 0.8113887082429979 | 1   |

- The output.csv contains the ranks of all the rows i.e. Model M5 is the best among the others

