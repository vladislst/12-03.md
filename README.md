# Домашнее задание к занятию "`SQL. Часть 1`" - `Степанов Владислав`

### Задание 1

select distinct district from sakila.address where district like 'K%a' and district not like '% %' ;

### Задание 2  

select payment_id, cast(payment_date as date),amount from sakila.payment where amount > 10 and payment_date between '2005-06-15' and '2005-06-18';

### Задание 3

select * from sakila.payment order by payment_date desc limit 5;

### Задание 4

select replace(lower(first_name),'ll','pp'),lower(last_name) from sakila.customer where first_name like 'Kelly' or first_name like 'Willie';

### Задание 5

select substring_index(email, '@', 1),substring_index(email, '@', -1) from sakila.customer;

### Задание 6

select concat(upper(left(substring_index(email, '@', 1),1)),lower(substring(substring_index(email, '@', 1),2))) 1part_email,concat(upper(left(substring_index(email, '@', -1),1)),lower(substring(substring_index(email, '@', -1),2))) 2part_email  from sakila.customer;