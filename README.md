# star-orgs

Azure Active Directory Organization Chart Viewer

![example.png](example.png)

## Usage

- Install [Node.js](https://nodejs.org) and npm *(if they are not already installed)*.
- Configure Azure Active Directory:
  - Enable client credentials authentication
  - Allow necessary directory access
- Clone this repository, or download and extract it.
- Next, in the repository root folder create a `.env` text file matching the following:

```
ENDPOINT_ID=the_endpoint_id_value
CLIENT_ID=the_client_id_value
CLIENT_SECRET=the_client_secret_value
```

- Install and start:

```sh
> npm install
> npm start
```

## Organization size note

A reasonable upper level of users at this time is approximately 150. Currently the graph does not scale well to higher numbers and provides no sizing or zooming mechanisms to fit additional data. Enhancements and/or changes may be necessary for this project to work *well* with larger data sets, which may even include disabling animation for the graph.

Supporting a large graph is currently outside the scope of this project, but if your needs dictate displaying a larger data set perhaps we can work something out -- let's talk in an issue before you invest in creating a PR!

## Development notes

The application consists of two components, a *client* and a *server*.

For local development `npm run start:watch` can be useful. This will watch both `src/client` and `src/server` directories and react as necessary. For `src/server` changes the server will be restarted -- which includes retrieving data as part of server startup.

## Author

Ritter Insurance Marketing https://rimdev.io

## License

- **MIT** : http://opensource.org/licenses/MIT

## Contributing

Contributions are highly welcome!
