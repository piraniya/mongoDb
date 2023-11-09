# mongoDb
exercise
**Q3**
```````
 db.moviedetails.insertMany([{"Movie-Title":"Jurassic Park","Type":"Adventure","Director":"Steven spielberg","Release Year":1993},{"Movie-Title":"Forrest Gump","Type":"Drama","Director":"Robert Zemeckies","Release Year":1994},{"Movie-Title":"Titanic","Type":"Romance","Director":"James Cameron","Release Year":1997},{"Movie-Tittle":"The Dark knight","Type":"Action","Director":"Christopher Nolan","Release Year":2008},{"Movie-Title":"Avatar","Type":"Science Fiction","Director":"James Cameron","Release Year":2009}])
{
  acknowledged: true,
  insertedIds: {
    '0': ObjectId("654ca14180f5f43dd7bd457a"),
    '1': ObjectId("654ca14180f5f43dd7bd457b"),
    '2': ObjectId("654ca14180f5f43dd7bd457c"),
    '3': ObjectId("654ca14180f5f43dd7bd457d"),
    '4': ObjectId("654ca14180f5f43dd7bd457e")
  }
}




````````
**Q4**
```
movies> db.moviedetails.find()
[
  {
    _id: ObjectId("654c98ced524c42db88fb71e"),
    'Movie-Title': 'Jurassic Park ',
    'Genre/Type': 'Adventure',
    Director: 'Steven Spielberg ',
    'Release Year': '1993 '
  },
  {
    _id: ObjectId("654c98ced524c42db88fb71f"),
    'Movie-Title': 'Forrest Gump',
    'Genre/Type': 'Drama ',
    Director: 'Robert Zemeckies ',
    'Release Year': '1994 '
  },
  {
    _id: ObjectId("654c98ced524c42db88fb720"),
    'Movie-Title': 'Titanic',
    'Genre/Type': 'Romance',
    Director: 'James Cameron ',
    'Release Year': '1997 '
  },
  {
    _id: ObjectId("654c98ced524c42db88fb721"),
    'Movie-Title': 'The Dark Knight',
    'Genre/Type': 'Action',
    Director: 'Christopher Nolan ',
    'Release Year': '2008 '
  },
  {
    _id: ObjectId("654c98ced524c42db88fb722"),
    'Movie-Title': 'Avatar'
  },
  {
    _id: ObjectId("654c98ced524c42db88fb723"),
    'Genre/Type': 'Science Fiction'
  },
  {
    _id: ObjectId("654c98ced524c42db88fb724"),
    Director: 'James Cameron'
  },
  { _id: ObjectId("654c98ced524c42db88fb725"), 'Release Year': '2009' },
  {
    _id: ObjectId("654ca14180f5f43dd7bd457a"),
    'Movie-Title': 'Jurassic Park',
    Type: 'Adventure',
    Director: 'Steven spielberg',
    'Release Year': 1993
  },
  {
    _id: ObjectId("654ca14180f5f43dd7bd457b"),
    'Movie-Title': 'Forrest Gump',
    Type: 'Drama',
    Director: 'Robert Zemeckies',
    'Release Year': 1994
  },
  {
    _id: ObjectId("654ca14180f5f43dd7bd457c"),
    'Movie-Title': 'Titanic',
    Type: 'Romance',
    Director: 'James Cameron',
    'Release Year': 1997
  },
  {
    _id: ObjectId("654ca14180f5f43dd7bd457d"),
    'Movie-Tittle': 'The Dark knight',
    Type: 'Action',
    Director: 'Christopher Nolan',
    'Release Year': 2008
  },
  {
    _id: ObjectId("654ca14180f5f43dd7bd457e"),
    'Movie-Title': 'Avatar',
    Type: 'Science Fiction',
    Director: 'James Cameron',
    'Release Year': 2009
  }
]

```
**Q5**
```
movies> db.moviedetails.find({"Director":"James Cameron"})
[
  {
    _id: ObjectId("654c98ced524c42db88fb724"),
    Director: 'James Cameron'
  },
  {
    _id: ObjectId("654ca14180f5f43dd7bd457c"),
    'Movie-Title': 'Titanic',
    Type: 'Romance',
    Director: 'James Cameron',
    'Release Year': 1997
  },
  {
    _id: ObjectId("654ca14180f5f43dd7bd457e"),
    'Movie-Title': 'Avatar',
    Type: 'Science Fiction',
    Director: 'James Cameron',
    'Release Year': 2009
  }
]



```
**Q6**
```
movies> db.moviedetails.find({"Release Year":2009})
[
  {
    _id: ObjectId("654ca14180f5f43dd7bd457e"),
    'Movie-Title': 'Avatar',
    Type: 'Science Fiction',
    Director: 'James Cameron',
    'Release Year': 2009
  }
]

```
**Q7**
`db.collection_name.remove({ "Movie-Title": "The Dark Knight" })
DeprecationWarning: Collection.remove() is deprecated. Use deleteOne, deleteMany, findOneAndDelete, or bulkWrite.
{ acknowledged: true, deletedCount: 0 }
```

````
**8**
```
 db.moviedetails.insertMany([ {"Movie-Title":"Leo","Type":"action","Director":"Logesh","Release Year":2023}])
{
  acknowledged: true,
  insertedIds: { '0': ObjectId("654ca797c109ca7b87ac91b9") }
}

```
**Q9**
```
db.moviesdetails.find({"Director":"Christopher Nolan","Release Year":1994})

empty result
```
**Q10***
```
db.moviesdetails.distinct("Director")

[
  'Steven Spielberg',
  'Robert Zemeckies',
  'James Cameron',
  'Leo'
]
`
