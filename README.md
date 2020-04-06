# booktonica-api

The Express API with Postgres database used by the [booktonica-react app](https://github.com/Techtonica/booktonica-react).

## Deployment using Heroku

Create a new app and follow the Heroku CLI instructions.

### Setting up the Database

- Go to Resources -> Add-ons
- Find Postgres
- Add it
- run `heroku pg:credentials:url DATABASE` to get the remote DB url
- `psql <URL> < booktonica.sql`

### Deploying the App

After commiting changes, run: 

`git push heroku master`

## Running Locally

`heroku local`

## Integrating with React App

After your React app is deployed to Heroku, use its URL in this app's config:

 `heroku config:set REACT_CLIENT_ORIGIN=https://booktonica-react.herokuapp.com`

 This will set proper CORS headers so your React client app can make requests.
