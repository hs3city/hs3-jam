# SPACE SMASHER 9001!

Tested on node `v14.17.3`

You can play the game [here](https://mystifying-hypatia-4b1cef.netlify.app/) (unfortunelly I can not setup server, so this instance do not provides ranking π₯).
Please be patient. The game **will** load, but slower on the crappy, free hosting, than on localhost.

The game was created for the first edition of [Hackerspace TrΓ³jmiasto's Community](https://github.com/hs3city/hs3-jam) Jam.

![Screenshot](ss.jpg)

## How to start a game

You need the [NodeJS](https://nodejs.org/en/) installed.

The game's server do not serve game client's files. They are separately apps.
The server is responsible for authentication and storing records.
Data is stored as plain JSON files in `server/storage` directory.
You do not have to setup any external database :)

The game *should* work without server, with some limitations.
Game works fine on desktop

Steering: `WSAD + Mouse`

## Setup and run server
```sh
π§ cd server
π§ npm install # install dependencies
π§ cp .env.example .env
π§ # edit .env file - UPDATE THE SECRET!
π§ npm start # the server listening on port 3000. 
```

## Setup and run client
```sh
π§ cd .. # only if your cwd is server directory
π§ cd game
π§ npm install # install dependencies
π§ # edit first line of src/api.ts to match your server
π§ npm start # to run in Dev mode (hot reloading and recompilling)
π§ npm run build
π§ # your app is in dist directory, you need to serve it via www server
```

## Enjoy!
