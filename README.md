# For make this app install flask

	pip install Flask


# For database install sqlalchemy
	
	pip install flask-sqlalchemy
	

# make database like this

	
	db = SQLAlchemy(app)

	class todo(db.Model):
    		sno = db.Column(db.Integer, primary_key=True)
    		title = db.Column(db.String(200), nullable=False)
    		desc = db.Column(db.String(500), nullable=False)
    		Date = db.Column(db.DateTime, default = datetime.utcnow())

    	def __repr__(self) -> str:
        	return f"{self.sno} - {self.title}"


# TO configure sqlalchemy

	app.config['SQLALCHEMY_DATABASE_URI'] = "sqlite:///form.db"
	app.config['SQLALCHEMY_TRACK_MODIFICATIONS'] = False 


#To set a database to app

to set database with app you need to create a sqllite database

	
	python
	from app import db
	db.create_all()
	exit()
	

# to show database contant

upload your database to this website
[view database](https://inloop.github.io/sqlite-viewer/)
	
