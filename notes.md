# blogroom

python3.6 manage.py migrate
`This command creates the following in the database`
auth_group                 | table | postgres
 public | auth_group_permissions     | table | postgres
 public | auth_permission            | table | postgres
 public | auth_user                  | table | postgres
 public | auth_user_groups           | table | postgres
 public | auth_user_user_permissions | table | postgres
 public | django_admin_log           | table | postgres
 public | django_content_type        | table | postgres
 public | django_migrations          | table | postgres
 public | django_session             | table | postgres

blogshome - app
### accessing the shell environment
`python manage.py shell`

### createing the database
`from blogshome.models import User` - Importing the model added in the models.py file in app/models

### creating a user
`us1 = User(first_name = 'James',last_name = 'Muriuki',email ='james@moringaschool.com')`

### save a user once created
`us1.save()`

### Retrieving all objects
`User.objects.all()`

### Retrieving single object
`User.objects.get(pk = 1)` - where pk = 1 is the primary key

### Filtering Data
`User.objects.filter(first_name = 'James')`

### Ordering Data
`User.objects.order_by('first_name')` - Ordering query by any field, eg. first_name

### Slicing data
`User.objects.all()[:]`

### Update
`User.objects.filter(id = 2).update(first_name ='Kim')` - change email or any field

### Delete
`User.objects.filter(id = 2).delete()`

### ManyToManyField
`Tells Django to create a separate join table`

