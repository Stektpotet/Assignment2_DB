---
typora-root-url: ./
---

# Assignment 2

##Part 1

#### 1.

```sql
SELECT eno, ename FROM employees ORDER BY ename ASC
```

![Part1_1](/Part1_1.PNG)

#### 2.

```sql
SELECT DISTINCT eno FROM orders
```

![Part1_2](/Part1_2.PNG)

#### 3.

```sql
SELECT pname, qoh, price FROM parts WHERE price < 20 ORDER BY qoh ASC
```

![Part1_3](/Part1_3.PNG)

#### 4.

```sql
SELECT pno, pname FROM parts WHERE LOWER(pname) LIKE LOWER('%BE%')
```

![Part1_4](/Part1_4.PNG)

#### 5.

```sql
SELECT pname, ROUND(price * 7.7192,2) AS `Price in Kroner` FROM parts ORDER BY price DESC
```

alternatively I could order by _\`Price in Kroner`_

![Part1_5](/Part1_5.PNG)

#### 6.

```sql
SELECT * FROM odetails WHERE qty%2=1
```

![Part1_6](/Part1_6.PNG)

#### 7.

```sql
SELECT * FROM orders WHERE received LIKE '1995-01%' OR received LIKE '1995-02%'
```

alternatively

```sql
SELECT * FROM orders WHERE received BETWEEN 19950100 AND 19950300
```

![Part1_7](/Part1_7.PNG)

#### 8.

```sql
SELECT * FROM orders WHERE shipped-received <=3
```

![Part1_8](/Part1_8.PNG)

#### 9.

```sql
SELECT * FROM orders WHERE shipped IS NULL
```

![Part1_9](/Part1_9.PNG)

#### 10.

```sql
SELECT ono FROM odetails WHERE pno=10506 OR pno=10508 OR pno=10601 ORDER BY qty
```

![Part1_10](/Part1_10.PNG)

## Part 2

#### 1.

```sql
SELECT employees.eno, ename, odetails.ono, pno, qty 
FROM employees, orders, odetails 
WHERE odetails.qty = 1 AND odetails.ono = orders.ono AND employees.eno = orders.eno
```

![Part2_1](/Part2_1.PNG)

#### 2.

```sql
SELECT DISTINCT eno FROM orders
```

![Part2_2](/Part2_2.PNG)

#### 3.

```sql
SELECT pname, qoh, price FROM parts WHERE price < 20 ORDER BY qoh ASC
```

![Part2_3](/Part2_3.PNG)

#### 4.

```sql
SELECT pno, pname FROM parts WHERE LOWER(pname) LIKE LOWER('%BE%')
```

![Part2_4](/Part2_4.PNG)

#### 5.

```sql
SELECT pname, ROUND(price * 7.7192,2) AS `Price in Kroner` FROM parts ORDER BY price DESC
```

alternatively I could order by _\`Price in Kroner`_

![Part2_5](/Part2_5.PNG)

#### 6.

```sql
SELECT * FROM odetails WHERE qty%2=1
```

![Part2_6](/Part2_6.PNG)

#### 7.

```sql
SELECT * FROM orders WHERE received LIKE '1995-01%' OR received LIKE '1995-02%'
```

alternatively

```sql
SELECT * FROM orders WHERE received BETWEEN 19950100 AND 19950300
```

![Part2_7](/Part2_7.PNG)

#### 8.

```sql
SELECT * FROM orders WHERE shipped-received <=3
```

![Part2_8](/Part2_8.PNG)

#### 9.

```sql
SELECT * FROM orders WHERE shipped IS NULL
```

![Part2_9](/Part2_9.PNG)

