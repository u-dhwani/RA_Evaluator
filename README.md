# RA_Evaluator
A Relational Algebra (RA) evaluator is a software component that processes and executes relational algebra queries. It analyzes queries, applies relational algebra operations on data, and generates result sets based on specified conditions, providing efficient retrieval of desired information from a relational database.  

The Relational Algebra Evaluator can serve as an effective practice tool for students. It allows them to input relational algebra queries and receive immediate feedback on the correctness of their queries. The evaluator examines the syntax of the query and determines if it is valid or not. If the query is correct, the evaluator displays the expected output. On the other hand, if the query is incorrect, the evaluator provides a message that the query is incorrect. This interactive approach helps students improve their understanding of relational algebra and reinforces their query-writing skills.  


Relational Algebra Evaluator consists of six basic operations : 
1. SELECT - The basic structure of SELECT query is:  
            SELECT { Predicate } [ Table ]  
            Predicate has to be specified in Curly Brackets { } and Table has to be specified in Square Brackets [ ]. Whole query should be in Balanced                       Parenthesis form.  
            Sample query for SELECT operation:  
                SELECT { Age>20 && Sex!=’M’ } [ Student ]  
            
2. PROJECT - PROJECT {Attr1, Attr2, Attr3, … } [ Table ]  
            {} should enclose the attributes and attributes should be separated by comma ‘,’.  
            Table should be provided in [ ]. Projection of attributes not existent in Table will result in error.  
            
3. RENAME - RENAME {newTableName} [ Table ]  
            RENAME {newTableName | Attr1,Attr2,Attr3, … } [ Table ]  
            
4. UNION -  UNION [ TableA , TableB ]  
            Tables should have exactly the same schema, i.e., names and datatypes of attributes and the order in which they are given should be the same,                     otherwise, it results in an error.  
            
5. CARTESIAN PRODUCT - CART [ TableA , TableB ]  
                       TableA and TableB should have completely disjoint schemas. If a user wants to product two tables with same name of attributes, then he/she                        must rename atleast one table to make this condition satisfy.  

6. SET DIFFERENCE - SDIFF [TableA, TableB]  

Nested Queries:  
Brackets have to be taken care of in Nested Queries.  
CART [ SELECT{predicate}[TableA] , PROJECT{Attr1, Attr2, … }[UNION [TableB, TableC] ] ]  

