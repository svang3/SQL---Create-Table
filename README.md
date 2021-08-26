# SQL---Create-Table

/* create a table named friends */
create table friends (
  id Integer,
  name Text,
  birthday Date
);

/* added a friend's name to the table */
insert into friends (id, name, birthday)
values (1, 'Ororo Munroe', '1940-05-30');

insert into friends (id, name, birthday)
values (2, 'Sandy Moore', '1983-09-16');

insert into friends (id, name, birthday)
values (3, 'Julian Moon', '1992-11-26');

/* check if friends are added to the list */
select * from friends;

/* update Ororo name */
update friends
set name = 'Storm'
where id = 1;

/* add a new column name email */
alter table friends
add column email Text;

/* update email address on table */
update friends
set email = 'storm@codecademy.com'
where id = 1;

update friends
set email = 'sandy_moore@codecademy.com'
where id = 2;

update friends
set email = 'julian_moon@codecademy.com'
where id = 3;

/* remove a friend name Storm */
delete from friends
where id = 1;

/* double check table one last time */
select * from friends;
