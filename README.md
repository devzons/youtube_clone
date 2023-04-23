# Youtube Clone Project Using Mui v5

## RapidAPI

- [Youtube v3](https://rapidapi.com/ytdlfree/api/youtube-v31)

## Dependencies

- vscode extension: RapidAPI Client

`npm install @mui/material @mui/icons-material @emotion/react @emotion/styled react-router-dom react-player axios`
`npm install --legacy-peer-deps`

## Logo

- Direct Link: `https://i.ibb.co/phPysLK/logo.png`
- color: #2666eb

## Fix layout issue with playlistId

```javascript
const Videos = ({ videos }) => {
  if (!videos?.length) return <Loader />

  return (
    <Stack
      direction={direction || 'row'}
      flexWrap='wrap'
      justifyContent='start'
      alignItems='start'
      gap={2}
    >
      {videos.map((item, idx) =>
        !item.id.playlistId ? (
          <Box key={idx}>
            {item.id.videoId && <VideoCard video={item} />}
            {item.id.channelId && <ChannelCard channelDetail={item} />}
          </Box>
        ) : (
          ''
        )
      )}
    </Stack>
  )
}
```

### Live Site

[https://youtube.dimshift.com](https://youtube.dimshift.com)
