# Intro to SQL

## What does SQL stand for?
Structured Query Language

## What do we use SQL for?
Store/persist data information
aggregate data
manipulating data

# What are some of the operations we can do in SQL?
Create Data
Read Data
Update Data
Delete data

1. Install the SQLite Browser if you haven't already [here](http://sqlitebrowser.org/)
2. Open the SQLite Browser and click 'File -> Open DataBase'
3. Choose the `chinook.db` file from this repo. This database is open source and maintained by Microsoft (SQL is no fun if you don't have any data)
4. Click the tab that says 'Execute SQL'. Type SQL queries in the box above. Press the play button. See the results of that query in the box below

## Challenges

1. Write the SQL to return all of the rows in the artists table?

```SQL

SELECT * FROM artists

```

2. Write the SQL to select the artist with the name "Black Sabbath"

```SQL

SELECT * FROM artists WHERE name= 'Black Sabbath'

```

3. Write the SQL to create a table named 'fans' with an autoincrementing ID that's a primary key and a name field of type text

```SQL

CREATE TABLE fans (
  id INTEGER PRIMARY KEY,
  name TEXT
);

```

4. Write the SQL to alter the fans table to have a artist_id column type integer?

```SQL

ALTER TABLE fans
ADD artist_id INTEGER;

```

5. Write the SQL to add yourself as a fan of the Black Eyed Peas? ArtistId **169**

```sql
INSERT INTO fans (name,artist_id) VALUES ("Anna",169);
```

6. Using SQL, how would you update your name in the fans table to be an alias?

```sql
UPDATE fans SET name="Skyler" WHERE name="Anna"
```

7. Write the SQL to return fans that are not fans of the black eyed peas.

```SQL
SELECT * FROM fans WHERE artist_id IS NOT 169
OR
SELECT * FROM fans WHERE artist_id != NOT 169

```

8. Write the SQL to display an artists name next to their album title

```SQL
SELECT artists.name, albums.title FROM artists INNER JOIN albums ON artist_id=artists.id
```


## BONUS

9. Write the SQL to display artist name, album name and number of tracks on that album

```sql

```

10. Write the SQL to return the name of all of the artists in the 'Pop' Genre

```sql

```

11. I want to return the names of the artists and their number of rock tracks
    who play Rock music
    and have move than 30 tracks
    in order of the number of rock tracks that they have
    from greatest to least

```sql

```
