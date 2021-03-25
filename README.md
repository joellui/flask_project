# Flask Project
Created a whole web page using flask
## Create a virtual environment
Before using Flask create a virtual environment in the pc. 

``` python -m venv flask_project\venv ```

And then to activate the environment use this command in CMD

``` flask_project\venv\Scripts\activate.bat ```

### To install all the packages
This will help you get all the packages in the virtual environment. 

``` $ pip install -r requirements.txt ```

### For Designing the web [Bootstrap 4](https://getbootstrap.com/docs/4.0/getting-started/introduction/) was used.

### For Database we used [SQLAlchemy](https://www.sqlalchemy.org/)

## Working with DATABASE
now to create fresh database 
open python cmd in the environmnet

```python
from flaskblog import db
db.create_all()
from flaskblog.models import User, Post
```

To add data to database
```python
user=User(content)
db.session.add(user)
db.session.commit()
User.query.all()
User.query.first()
User.query.filter_by(username='joel').all()
user = User.query.filter_by(username='joel').all()
id = user.id()
User.query.get(id)
user.posts

user.id
post_1 = Post(title='Blog 1', content = 'First Post Content!', user_id=user.id)
post_2 = Post(title='Blog 2', content = 'Second Post Content!', user_id=user.id)
db.session.add(post_1)
db.session.add(post_2)
db.session.commit()
user.posts
```

to remove data
```python
db.drop_all()
```

## Check out the live demo on Heroku..

[Flask Blog](http://projectinfography.herokuapp.com/)
