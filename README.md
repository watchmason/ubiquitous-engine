# ubiquitous-engine
Chalice API for "Gratitude App" - fucking around with Python, Chalice, AWS, Testing etc...

### Gratitude App
For now, basic rest API which will allow the consumer to: 
* See Gratitudes
* Create Gratitude
* Edit Gratitude
* Date Search Gratitudes

### Things I need to think about
* ORM / Migrations / Data seeding within an chalice app?
* Testing database interaction with Chalice locally
* Notifications at the end of a day
* Attaching users to a gratitude - Cognito!

#### Models
Models used within the gratitude app:
*gratitudes*
```
id - unique identifer for a gratitude
gratitude - text for gratitude
user_id - id of user that made the gratitude
created_at - the date and time gratitude was created
updated_at - the date and time the gratitude was last updated
```

#### Endpoints
* `GET api/v1/gratitudes` - return all gratitudes
* `GET api/v1/gratitudes/{gratitude_id}` - return single gratitude
* `POST api/v1/gratitudes` - add a new gratitude
* `PUT api/v1/gratitudes/{gratitude_id}` - edit an existing gratitude
* `GET api/v1/gratitudes?from=2019-01-01&to=2019-02-01` - return all gratitudes within a date range
* `GET api/v1/gratitudes?on=2019-01-01` - return all gratitudes from a single day (is this needed? couldn't we just have to and from as the same date?)

## Todo
* add users - Cognito?
* needs a front end mate
* remove functions out of chalice into layers that can be used elsewhere? 
* introduce ORM? <Migrations and shit>
* 