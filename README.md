JAVA Implementation for APRIORI Algorithm
===

APRIORI Algorithm is divided into 3 parts
===
1. Defining Minimum Support and Minimum Confidence.
2. Finding Frequent Itemset
   * Find items whose occurrence is more than the support specified
   * Finding item set i.e. combinations of items from items generated from previous iterations
3. Generating Association Rules.

DATASET
====
```
iPhone Samsung Lenevo
Nokia iPhone Samsung LG Lenevo
Nokia Samsung
iPhone Samsung Nokia
Lenevo
Samsung LG
Samsung Lenevo
```
Each line specifies a Transaction which is seperated by a space.

OUTPUT
===
```
No of Items = 5
No of Transactions = 7
Minimum Support = 2
Minimum Confidence = 0.45

'Items present in the Database'
------> iPhone
------> Samsung
------> Lenevo
------> Nokia
------> LG

TRANSACTION       ITEMSET
Transaction 1 = iPhone Samsung Lenevo
Transaction 2 = Nokia iPhone Samsung LG Lenevo
Transaction 3 = Nokia Samsung
Transaction 4 = iPhone Samsung Nokia
Transaction 5 = Lenevo
Transaction 6 = Samsung LG
Transaction 7 = Samsung Lenevo
```
```
Frequent Itemset 1 => Item = 'iPhone' => support = 3
Frequent Itemset 1 => Item = 'Samsung' => support = 6
Frequent Itemset 1 => Item = 'Lenevo' => support = 4
Frequent Itemset 1 => Item = 'Nokia' => support = 3
Frequent Itemset 1 => Item = 'LG' => support = 2
```
```
Frequent Itemset 2 => Itemset = 'iPhone Samsung' => support = 3
Frequent Itemset 2 => Itemset = 'iPhone Lenevo' => support = 2
Frequent Itemset 2 => Itemset = 'iPhone Nokia' => support = 2
Frequent Itemset 2 => Itemset = 'Samsung Lenevo' => support = 3
Frequent Itemset 2 => Itemset = 'Samsung Nokia' => support = 3
Frequent Itemset 2 => Itemset = 'Samsung LG' => support = 2
```
```
Frequent Itemset 3 => Itemset = 'iPhone Samsung Lenevo' => support = 2
Frequent Itemset 3 => Itemset = 'iPhone Samsung Nokia' => support = 2
```
```
Association Rules for Frequent Itemset

'iPhone -> Samsung' = {Confidence = 1.0 and Support = 3}
'Samsung -> iPhone' = {Confidence = 0.5 and Support = 3}
'iPhone -> Lenevo' = {Confidence = 0.6666666666666666 and Support = 2}
'Lenevo -> iPhone' = {Confidence = 0.5 and Support = 2}
'iPhone -> Nokia' = {Confidence = 0.6666666666666666 and Support = 2}
'Nokia -> iPhone' = {Confidence = 0.6666666666666666 and Support = 2}
'Samsung -> Lenevo' = {Confidence = 0.5 and Support = 3}
'Lenevo -> Samsung' = {Confidence = 0.75 and Support = 3}
'Samsung -> Nokia' = {Confidence = 0.5 and Support = 3}
'Nokia -> Samsung' = {Confidence = 1.0 and Support = 3}
'LG -> Samsung' = {Confidence = 1.0 and Support = 2}
'iPhone ->  Samsung Lenevo' = {Confidence = 0.6666666666666666 and Support = 2}
'Samsung Lenevo -> iPhone' = {Confidence = 0.6666666666666666 and Support = 2}
'iPhone Samsung ->  Lenevo' = {Confidence = 0.6666666666666666 and Support = 2}
'Lenevo -> iPhone Samsung' = {Confidence = 0.5 and Support = 2}
'iPhone ->  Samsung Nokia' = {Confidence = 0.6666666666666666 and Support = 2}
'Samsung Nokia -> iPhone' = {Confidence = 0.6666666666666666 and Support = 2}
'iPhone Samsung ->  Nokia' = {Confidence = 0.6666666666666666 and Support = 2}
'Nokia -> iPhone Samsung' = {Confidence = 0.6666666666666666 and Support = 2}
```

