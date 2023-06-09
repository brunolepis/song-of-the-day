# Song of the Day

Daily unique song generator website

## How it works

Every day, a song is put on the website from a list that can be accessed via the REST API.

## Rest API

#### [`GET /api/song`](https://song-of-the-day.vercel.app/api/song)

Get today's song of the day

#### Example Response

```js
{
  name: "Never Gonna Give You Up",
  artist: "Rick Astley",
  cover: "ab67616d00001e02baf89eb11ec7c657805d2da0", // The hash of the album cover image
  trackId: "4cOdK2wGLETKBW3PvgPWqT", // The Spotify track ID
  videoId: "dQw4w9WgXcQ", // The YouTube video ID
  date: "1970-01-01", // The date when the song is the song of the day (YYYY-MM-DD)
},
```

#### [`GET /api/songs`](https://song-of-the-day.vercel.app/api/songs)

Get every song that is on the list

#### [`GET /api/previous`](https://song-of-the-day.vercel.app/api/previous)

Get yesterday's song of the day

#### [`GET /api/next`](https://song-of-the-day.vercel.app/api/next)

Get tomorrow's song of the day

#### [`GET /api/shuffle`](https://song-of-the-day.vercel.app/api/shuffle)

Get every song that is on the list shuffled and the dates edited to be up-to-date

> **Note** This doesn't actually change the list that is stored on the server. This is useful when there are no more songs left on the list.

## Running locally

1. Clone the repository.

```
git clone https://github.com/brunolepis/song-of-the-day
```

2. Go into the directory.
3. Then install the dependencies and start the development server.

> **Note** This project uses [pnpm](https://pnpm.io) as the package manager. If you want to use [npm](https://docs.npmjs.com/downloading-and-installing-node-js-and-npm) as the package manager, go to step 4.

```
pnpm install
pnpm dev
```

4. Using npm, install the dependencies and start the development server.

> **Note** It is recommended to delete the file called `pnpm-lock.yaml`.

```
npm install
npm run dev
```

## Contributing

Contributions are always welcome in the form of requests to add new songs to the list or anything else that can be fixed or improved.
