# magic2sql
 Simple utility program to convert `.ipynb` sqlmagic notebooks to `.sql` files and vice-versa.
 
## Here’s what it does:

### In `to-sql` mode
1. Reads all the cells from the `.ipynb` file of your choice
2. Finds all the cells with `%%sql` at the front and puts those into a new list, stripping out the `%%sql` and adding a `;` at the end
3. Writes all these cells into a `.sql` file of your specification

### In `to-nb` mode
1. Reads in a `.sql` file
2. Chunks all the sql statements and turns them into pyspark-compliant `%%sql` cells
3. Writes all these cells into a `.ipynb` file of your specification

## Usage
And here’s an example command-line of how to use it to convert `.ipynb` to `.sql`:

```python3 jmagic2sql.py -m to-sql -n ~/some_notebook.ipynb -s ~/some_sql_file.sql```

Pretty simple!

No dependencies really, this uses vanilla python3. Have fun!
