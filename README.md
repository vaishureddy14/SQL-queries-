6.select distinct s.* from salespeople s join orders o on s.snum=o.snum;
7.select c.* from customers c join salespeople s on s.snum=c.snum;
8.select s.sname,s.snum from salespeople s join customers c on s.snum=c.snum group by s.snum having count(*)>1;
9. SELECT snum, COUNT(onum)
    -> FROM orders
    -> GROUP BY snum
    -> ORDER BY COUNT(onum) DESC;
10.SELECT * FROM customer
    -> WHERE EXISTS (
    ->     SELECT * FROM customer
    ->     WHERE city = 'San Jose'
    -> );
