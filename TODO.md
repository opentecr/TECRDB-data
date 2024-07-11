# To Do

1. Prepare the SQLite database in client:

   - [x] Build `sql.js` with FTS5 extension
   - [x] Serve site with custom `sql.js`
   - [x] Load openTECR SQLite DB
   - [x] `CREATE VIRTUAL TABLE reaction_fts FROM FTS5(description);`
   - [x] `INSERT INTO reaction_fts SELECT data.description FROM data;`
   - [x] Query

     ```sql
     SELECT highlight(reaction_fts, 0, '<b>', '</b>') AS description_, rank
     FROM reaction_fts
     WHERE reaction_fts MATCH 'glucose'
     ORDER BY rank;
     ```

2. Download data and organize into better tables
3. Enrich with identifiers and synonyms
