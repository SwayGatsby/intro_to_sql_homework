Use the supplied data as the source of data to answer the questions.  Copy the SQL command you have used to get the answer, and paste it below the question, along with the result they gave.

## Questions

1. Return ALL the data in the 'movies' table.

`SELECT * FROM movies;`

*Result*

id |                title                | year | show_time
----+-------------------------------------+------+-----------
 1 | Iron Man                            | 2008 | 15:15
 2 | The Incredible Hulk                 | 2008 | 22:05
 3 | Iron Man 2                          | 2010 | 18:05
 4 | Thor                                | 2011 | 13:00
 5 | Captain America: The First Avenger  | 2011 | 22:15
 6 | Avengers Assemble                   | 2012 | 23:25
 7 | Iron Man 3                          | 2013 | 12:05
 8 | Thor: The Dark World                | 2013 | 13:25
 9 | Batman Begins                       | 2005 | 23:55
10 | Captain America: The Winter Soldier | 2014 | 19:40
11 | Guardians of the Galaxy             | 2014 | 18:55
12 | Avengers: Age of Ultron             | 2015 | 21:10
13 | Ant-Man                             | 2015 | 15:20
14 | Captain America: Civil War          | 2016 | 22:45
15 | Doctor Strange                      | 2016 | 22:00
16 | Guardians of the Galaxy 2           | 2017 | 15:30
(16 rows)
---------------------------------------------------

2. Return ONLY the name column from the 'people' table

`SELECT name FROM people;`

*Result*

name
-------------------
Miguel Almeida
Callum Bentley
Zackary Coleman
Daniel Colyer
Adm Conway
Peter Crowther
Marta Dabrowka
Graeme Doran
John Duncan
Kayla Fowler
Diana Prince
Diana Prince
Chris Marshall
Aline Mokfa
Joao Nequinha
Yoni Satat
Kynan Song
Craig Morton
Hamish Stewart
Huascar Suave
Rob Williams
Laurence Woodward
Andre Zyczkowski
(23 rows)
---------------------------------------------------

3. Oops! Someone at CodeClan spelled Adam's name wrong! Change it to reflect the proper spelling (change 'Adm Conway' to 'Adam Conway').

`UPDATE people
SET name = 'Adam Conway'
WHERE  name = 'Adm Conway';`

*Result*

UPDATE 1
       name
-------------------
 Miguel Almeida
 Callum Bentley
 Zackary Coleman
 Daniel Colyer
 Peter Crowther
 Marta Dabrowka
 Graeme Doran
 John Duncan
 Kayla Fowler
 Diana Prince
 Diana Prince
 Chris Marshall
 Aline Mokfa
 Joao Nequinha
 Yoni Satat
 Kynan Song
 Craig Morton
 Hamish Stewart
 Huascar Suave
 Rob Williams
 Laurence Woodward
 Andre Zyczkowski
 Adam Conway
(23 rows)
---------------------------------------------------

4. Return ONLY your name from the 'people' table.

`SELECT name FROM people
WHERE name = 'Kayla Fowler';`

*Result*

UPDATE 1
     name
--------------
 Kayla Fowler
(1 row)
---------------------------------------------------

5. The cinema is showing 'Batman Begins', but Batman is DC, not Marvel! Delete the entry from the 'movies' table.

`DELETE from movies
WHERE title = 'Batman Begins';`

*Result*

DELETE 1
 id |                title                | year | show_time
----+-------------------------------------+------+-----------
  1 | Iron Man                            | 2008 | 15:15
  2 | The Incredible Hulk                 | 2008 | 22:05
  3 | Iron Man 2                          | 2010 | 18:05
  4 | Thor                                | 2011 | 13:00
  5 | Captain America: The First Avenger  | 2011 | 22:15
  6 | Avengers Assemble                   | 2012 | 23:25
  7 | Iron Man 3                          | 2013 | 12:05
  8 | Thor: The Dark World                | 2013 | 13:25
 10 | Captain America: The Winter Soldier | 2014 | 19:40
 11 | Guardians of the Galaxy             | 2014 | 18:55
 12 | Avengers: Age of Ultron             | 2015 | 21:10
 13 | Ant-Man                             | 2015 | 15:20
 14 | Captain America: Civil War          | 2016 | 22:45
 15 | Doctor Strange                      | 2016 | 22:00
 16 | Guardians of the Galaxy 2           | 2017 | 15:30
(15 rows)
---------------------------------------------------

6. Create a new entry in the 'people' table with the name of one of the instructors.
`INSERT INTO people (name)
VALUES ('Sandy McMillan');`

*Result*

name
-------------------
Miguel Almeida
Callum Bentley
Zackary Coleman
Daniel Colyer
Adam Conway
Peter Crowther
Marta Dabrowka
Graeme Doran
John Duncan
Kayla Fowler
Diana Prince
Diana Prince
Chris Marshall
Aline Mokfa
Joao Nequinha
Yoni Satat
Kynan Song
Craig Morton
Hamish Stewart
Huascar Suave
Rob Williams
Laurence Woodward
Andre Zyczkowski
Sandy McMillan
(24 rows)
---------------------------------------------------

7. Craig Morton, has decided to hijack our movie evening, Remove him from the table of people.

`DELETE from people
WHERE name = 'Craig Morton';`

*Result*

DELETE 1
       name
-------------------
 Miguel Almeida
 Callum Bentley
 Zackary Coleman
 Daniel Colyer
 Adm Conway
 Peter Crowther
 Marta Dabrowka
 Graeme Doran
 John Duncan
 Kayla Fowler
 Diana Prince
 Diana Prince
 Chris Marshall
 Aline Mokfa
 Joao Nequinha
 Yoni Satat
 Kynan Song
 Hamish Stewart
 Huascar Suave
 Rob Williams
 Laurence Woodward
 Andre Zyczkowski
 Sandy McMillan
(23 rows)
---------------------------------------------------

8. Somehow the list of people includes two people named 'Diana Prince'. Change these entries to the proper names ('Tony Stark' and 'David Banner')

`UPDATE people
SET name = 'Tony Stark'
WHERE id = 11;

UPDATE people
SET name = 'David Banner'
WHERE id = 12;`

*Result*

id |       name
----+-------------------
 1 | Miguel Almeida
 2 | Callum Bentley
 3 | Zackary Coleman
 4 | Daniel Colyer
 6 | Peter Crowther
 7 | Marta Dabrowka
 8 | Graeme Doran
 9 | John Duncan
10 | Kayla Fowler
13 | Chris Marshall
14 | Aline Mokfa
15 | Joao Nequinha
16 | Yoni Satat
17 | Kynan Song
19 | Hamish Stewart
20 | Huascar Suave
21 | Rob Williams
22 | Laurence Woodward
23 | Andre Zyczkowski
 5 | Adam Conway
24 | Sandy McMillan
11 | Tony Stark
12 | David Banner
(23 rows)
---------------------------------------------------

9. The cinema has just heard that they will be holding an exclusive midnight showing of 'Guardians of the Galaxy 2'!! Create a new entry in the 'movies' table to reflect this.

`INSERT INTO movies (title, show_time)
VALUES ('Guardians of the Galaxy 2', '00:00')`

*Result*

INSERT 0 1
 id |                title                | year | show_time
----+-------------------------------------+------+-----------
  1 | Iron Man                            | 2008 | 15:15
  2 | The Incredible Hulk                 | 2008 | 22:05
  3 | Iron Man 2                          | 2010 | 18:05
  4 | Thor                                | 2011 | 13:00
  5 | Captain America: The First Avenger  | 2011 | 22:15
  6 | Avengers Assemble                   | 2012 | 23:25
  7 | Iron Man 3                          | 2013 | 12:05
  8 | Thor: The Dark World                | 2013 | 13:25
 10 | Captain America: The Winter Soldier | 2014 | 19:40
 11 | Guardians of the Galaxy             | 2014 | 18:55
 12 | Avengers: Age of Ultron             | 2015 | 21:10
 13 | Ant-Man                             | 2015 | 15:20
 14 | Captain America: Civil War          | 2016 | 22:45
 15 | Doctor Strange                      | 2016 | 22:00
 16 | Guardians of the Galaxy 2           | 2017 | 15:30
 17 | Guardians of the Galaxy 2           |      | 12:00
(16 rows)
---------------------------------------------------

10. The cinema would also like to make the Guardian movies a back to back feature. Update the 'Guardians of the Galaxy' show time from 18:55 to 21:30

`UPDATE movies
SET show_time = '21:30'
WHERE title = "Guardians of the Galaxy";`

*Result*

UPDATE 1
 id |                title                | year | show_time
----+-------------------------------------+------+-----------
  1 | Iron Man                            | 2008 | 15:15
  2 | The Incredible Hulk                 | 2008 | 22:05
  3 | Iron Man 2                          | 2010 | 18:05
  4 | Thor                                | 2011 | 13:00
  5 | Captain America: The First Avenger  | 2011 | 22:15
  6 | Avengers Assemble                   | 2012 | 23:25
  7 | Iron Man 3                          | 2013 | 12:05
  8 | Thor: The Dark World                | 2013 | 13:25
 10 | Captain America: The Winter Soldier | 2014 | 19:40
 12 | Avengers: Age of Ultron             | 2015 | 21:10
 13 | Ant-Man                             | 2015 | 15:20
 14 | Captain America: Civil War          | 2016 | 22:45
 15 | Doctor Strange                      | 2016 | 22:00
 16 | Guardians of the Galaxy 2           | 2017 | 15:30
 17 | Guardians of the Galaxy 2           |      | 00:00
 11 | Guardians of the Galaxy             | 2014 | 21:30
(16 rows)
---------------------------------------------------

## Extension

1. Research how to delete multiple entries from your table in a single command.

`DELETE from tablename WHERE id IN (1,2,3,...,254);

 DELETE from tablename WHERE id BETWEEN 1 AND 254;

 DELETE from tablename WHERE id BETWEEN 1 AND 254 AND id<>10;`
