# Magazine Database Code Challenge
This code challenge involves creating a Magazine database with three models: Author, Magazine, and Article. The goal is to build a system where Authors can

have multiple Articles, and Magazines can have multiple Articles, with both Authors and Magazines being linked in a many-to-many relationship.

## Technologies used
python


## Requirements

Python 3.x

PostgreSQL (or any SQL-compatible database)

pipenv for managing dependencies

### Running the Application
Test the models by creating instances of authors, magazines, and articles:

In app.py, you can create instances of Author, Magazine, and Article, and call the methods to check their relationships. For example:
```
from models.Author import Author
from models.Magazine import Magazine
from models.Article import Article
```
### Create Author
author1 = Author(1, "John Doe")

### Create Magazine
magazine1 = Magazine(1, "Tech Monthly", "Technology")

### Create Article
article1 = Article(author1, magazine1, "The Future of AI")

### Test relationships
```
print(f"Author's Articles: {[article.title for article in author1.articles()]}")
print(f"Magazine's Articles: {[article.title for article in magazine1.articles()]}")
print(f"Magazine's Contributors: {[author.name for author in magazine1.contributors()]}")
```
## Contributing
If you would like to contribute to this project, feel free to submit a pull request. Please ensure that you follow the project's coding style and include tests for any new features or fixes.

## License
This project is licensed under the MIT License - see the LICENSE file for details.
