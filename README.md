# SQL_2

-- SELECT *
-- FROM invoice i
-- JOIN invoice_line il ON il.invoice_id = i.invoice_id
-- WHERE il.unit_price > 0.99;

-- SELECT i.invoice_date, c.first_name, c.last_name, i.total
-- FROM invoice i
-- JOIN customer c ON i.customer_id = c.customer_id;

-- select c.first_name, c.last_name, e.first_name, e.last_name
-- from customer c
-- join employee e on c.support_rep_id = e.employee_id;

-- select al.title, ar.name
-- from album al
-- join artist ar on al.artist_id = ar.artist_id;

-- select pt.track_id
-- from playlist_track pt
-- join playlist p on pt.playlist_id = p.playlist_id
-- where p.name = 'Music';

-- select track.name, playlist_track.playlist_id
-- from track 
-- join playlist_track on track.track_id = playlist_track.track_id 
-- where playlist_id = 5

-- select t.name, p.name
-- from track t
-- join playlist_track pt on t.track_id = pt.track_id
-- join playlist p on pt.playlist_id = p.playlist_id

-- select t.name, a.title
-- from track t
-- join album a on t.album_id = a.album_id
-- join genre g on t.genre_id = g.genre_id
-- where g.name = 'Alternative & Punk'



-- select * from invoice
-- where invoice_id in (select invoice_id from invoice_line where unit_price > 0.99) 

-- select * from playlist_track
-- where playlist_id in ( select playlist_id from playlist where name = 'Music' );

-- select name from track
-- where track_id in (select track_id from playlist where playlist_id = 5)

-- select * from track
-- where genre_id in (select genre_id from genre where name = 'Comedy');

-- select * from track
-- where album_id in ( select album_id from album where title = 'Fireball' );

-- select * from track
-- where album_id in ( 
--   select album_id from album where artist_id in ( 
--     select artist_id from artist where name = 'Queen'
--   )
-- ); 

-- update customer
-- set fax = null
-- where fax is not null;

-- update customer
-- set company = 'Self'
-- where company is null

-- update customer
-- set last_name = 'Thompson'
-- where first_name = 'Julia' and last_name = 'Barnett';

-- update customer
-- set support_rep_id = 4
-- where email = 'luisrojas@yahoo.cl';

-- update track 
-- set composer = 'The darkness around us'
-- where genre_id =(select genre_id from genre where name = 'Metal')
-- and composer is null;

-- select count(*), g.name from track t
-- join genre g on t.genre_id = g.genre_id
-- group by g.name;

-- select count(*), g.name from track t
-- join genre g on g.genre_id = t.genre_id
-- where g.name = 'Pop' and g.name = 'Rock'
-- group by g.name;

-- select ar.name, count(*) from album al
-- join artist ar on ar.artist_id = al.artist_id
-- group by ar.name;


-- update customer
-- set fax = null
-- where fax is not null;

-- update customer
-- set company = 'Self'
-- where company is null

-- update customer
-- set last_name = 'Thompson'
-- where first_name = 'Julia' and last_name = 'Barnett';

-- update customer
-- set support_rep_id = 4
-- where email = 'luisrojas@yahoo.cl';

-- update track 
-- set composer = 'The darkness around us'
-- where genre_id =(select genre_id from genre where name = 'Metal')
-- and composer is null;

-- select count(*), g.name from track t
-- join genre g on t.genre_id = g.genre_id
-- group by g.name;

-- select count(*), g.name from track t
-- join genre g on g.genre_id = t.genre_id
-- where g.name = 'Pop' and g.name = 'Rock'
-- group by g.name;

-- select ar.name, count(*) from album al
-- join artist ar on ar.artist_id = al.artist_id
-- group by ar.name;


-- CREATE TABLE practice_delete ( name TEXT, type TEXT, value INTEGER );
-- INSERT INTO practice_delete ( name, type, value ) VALUES ('delete', 'bronze', 50);
-- INSERT INTO practice_delete ( name, type, value ) VALUES ('delete', 'bronze', 50);
-- INSERT INTO practice_delete ( name, type, value ) VALUES ('delete', 'bronze', 50);
-- INSERT INTO practice_delete ( name, type, value ) VALUES ('delete', 'silver', 100);
-- INSERT INTO practice_delete ( name, type, value ) VALUES ('delete', 'silver', 100);
-- INSERT INTO practice_delete ( name, type, value ) VALUES ('delete', 'gold', 150);
-- INSERT INTO practice_delete ( name, type, value ) VALUES ('delete', 'gold', 150);
-- INSERT INTO practice_delete ( name, type, value ) VALUES ('delete', 'gold', 150);
-- INSERT INTO practice_delete ( name, type, value ) VALUES ('delete', 'gold', 150);

-- SELECT * FROM practice_delete;

-- delete from practice_delete where type = 'bronze'

-- delete from practice_delete where type = 'silver'

-- delete from practice_delete where value = 150

-- select * from practice_delete

-- 

-- create table users(id serial primary key, name text, email text);
-- create table products(id serial primary key, name text, price float);
-- create table orders(id serial primary key, product_id int);

-- insert into users ( name, email ) values ('Bob', 'bob@bob.com');
-- insert into users ( name, email ) values ('Sue', 'sue@ale.com');
-- insert into users ( name, email ) values ('Frank', 'frank@eba.com');
-- insert into users ( name, email ) values ('Lisa', 'lisa@feta.com');
-- insert into users ( name, email ) values ('Charlotte', 'char@megoto.com');
-- insert into users ( name, email ) values ('Bill', 'bill@abnebe.com');

-- insert into products ( name, price ) values ('vacuum', 99.99);
-- insert into products ( name, price ) values ('couch', 509.99);
-- insert into products ( name, price ) values ('computer', 1999.59);
-- insert into products ( name, price ) values ('microwave', 299.89);
-- insert into products ( name, price ) values ('bike', 1399.49);
-- insert into products ( name, price ) values ('helmit', 49.99);

-- insert into orders ( product_id ) values (1);
-- insert into orders ( product_id ) values (2);
-- insert into orders ( product_id ) values (3);
-- insert into orders ( product_id ) values (4);
-- insert into orders ( product_id ) values (5);
-- insert into orders ( product_id ) values (6);
-- insert into orders (product_id ) values (3);

-- select * from products p
-- join orders o on p.id = o.product_id where o.id = 1;

-- select * from orders

-- select count(*), p.price from orders o
-- join products p on o.product_id = p.id where o.id = 2
-- group by p.price

-- alter table orders
-- 	add constraint fk_orders
--   foreign key (product_id)
--   references users (id)

-- select from orders o 
-- join users u on o.product_id = u.id where u.id = 2;



  
  





















