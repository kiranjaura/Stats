Kiran Jaura

## Welcome to my Webpage

Assignment 6:
<br>
1)<br>
a. If the ER graph is disconnected, then the entities are not related and are independent of each other.
<br>
  b. If the ER graph has a cycle, then there is a unique path between every pair of entity sets and thus a unique relationship between every pair of entity sets.
<br>
<br>
2)
 ![image](https://user-images.githubusercontent.com/55324758/112534841-97aa1f00-8d79-11eb-87a9-ff4647e9edc8.png)
 
3) We have weak entity sets because they avoid inconsistencies caused by duplicating hte key of the strong entity, they reflect the logical structure of an entity being dependent on anotehr entity (the identifyiing relationship), and they can be deleted along with their corresponding strong entity set.<br>
4) a.i:
    <br>
    select e.ID, e.person_name
    from e
    join c on e.city=c.city
    <br>
   a.ii:
   <br>
   select e.ID, e.person_name
    from (select * from m as man join e on e.ID=m.manager_id)
    where man.city=e.city and man.street=e.street
    <br>
    a.iii:
    <br>
    select e.ID, e.person_name
    from e
    join (select avg(job.salary) as avg from working as job)
    where salary>avg
    <br>
    b. 2 sections of Game design are included but look like duplicate and are not distinguished because section is not included in the final output
