# Functions
**Dev:** *MWinn*   
**Date:** *3.3.2021*

## Introduction
In this paper, I will explain when one would use a SQL UDF Function. Then, I will explain the differences between Scalar, Inline, and Multi-Statement Functions. 

## SQL UDF Function
SQL UDF Functions allow you to create your own custom functions. You may use UDFs to store complex code such as joining many tables where some type of calculation is required, and an aggregation is returned. 

## Scalar, Inline, and Multi-Statement Functions
Scalar Functions return only a single (scalar) value from the table (Figure 1).  Scalar Functions may or not may not have parameters which are optional, but always return a single value which is mandatory. When calling a Scalar Function, you must supply a two-part name (ex. dbo.MultiplyValues). 

![alt text](Figure%201.png "tooltip text")

Figure 1: SQL query with Scalar Function

Inline Functions simply return a select statement and do not require you to specify the structure of the return table. Also, Inline Functions do not use the Begin/End block. In comparison, Multi-Statement Functions require you to declare a table variable that is to be returned and must have a Begin/End block. Within this Begin/End block, there is code that populates the table variable. 

## Summary
Scalar, Inline, and Multi-Statement Functions are 3 different types of SQL UDF Functions. SQL UDF Functions allow the user to store complex code in one structure and reduces the chances of error since the same code is not rewritten multiple times. Lastly, if the code needs to be updated, the update will be reflected each time the function is referenced in the query. 
