# Project Title

This is a PHP wrapper for the Brightcove Playback API

File caching layer is activated by adding require_once('bc-papi-cache.php') to get-brightcove-media.php

## Getting Started

Add files to project folder. Access as follows (e.g. files placed in folder named brightcove-playback-api):

```
require_once($_SERVER['DOCUMENT_ROOT'] . '/brightcove-playback-api/get-brightcove-media.php');
//find video by video id
$videoid = 12345;
$video = $bc->find('find_video_by_id', 'videos', $videoid);
// e.g. get video poster and display
echo '<img src="' . $video->poster . '" />';

//find video by reference id
$refid = ref123;
$video = $bc->find('find_video_by_reference_id', 'videos', $ref123);

//find playlist by video id
$videoid = 54321;
$playlist = $bc->find('find_playlist_by_id', 'playlists', $54321);
echo '<img src="' . $playlist->videos[0]->poster . '" />';

//find playlist by reference id
$refid = ref321;
$playlist = $bc->find('find_playlist_by_reference_id', 'playlists', $ref321);

```


## Authors

* **Theresa Newman** - *Initial work* - [Brightcove-Playback-API-Wrapper](https://github.com/theresaweb/Brightcove-Playback-API-Wrapper)

## Acknowledgments

* Based on the PHP Wrapper for the Media API which is being deprecated (https://github.com/BrightcoveOS/PHP-MAPI-Wrapper)
