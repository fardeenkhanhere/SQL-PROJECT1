# SQL-PROJECT1
CREATE TABLE SALES (
  PRODUCT varchar(255),
  QUARTER varchar(255),
  REGION varchar(255),
  SALE INT );
  
  INSERT INTO SALES VALUES('A','Q1','Europe',10);
  INSERT INTO SALES VALUES('A','Q4','Europe',10);
  INSERT INTO SALES VALUES('B','Q2','America',100);
  INSERT INTO SALES VALUES('B','Q3','Europe',10);
  INSERT INTO SALES VALUES('A','Q1','America',20);
  INSERT INTO SALES VALUES('A','Q3','Europe',30);
  INSERT INTO SALES VALUES('B','Q1','America',10);
  INSERT INTO SALES VALUES('A','Q2','Europe',10);
  INSERT INTO SALES VALUES('B','Q1','America',40);
  INSERT INTO SALES VALUES('A','Q2','Europe',10);
  INSERT INTO SALES VALUES('B','Q1','Europe',50);
  INSERT INTO SALES VALUES('A','Q4','America',10);
  INSERT INTO SALES VALUES('B','Q3','Europe',20);
  INSERT INTO SALES VALUES('A','Q1','America',10);

SELECT * FROM SALES

SELECT quarter,region, SUM(sale)
FROM SALES
GROUP by cube ( quarter, region)


SELECT quarter,region, SUM(sale)
FROM SALES
GROUP by ROLLUP( quarter, region)
