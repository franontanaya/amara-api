Amara API
================

Provides an object to perform some of the most common interactions with Amara's API

## Example usage
```
require_once 'API.php';
$API = new FranOntanaya\Amara\API(
        'https://www.amara.org/api/',
        'username',
        'apikey'
  );
$videoInfo = $API->getVideoInfo(array(
            'video_id' => $video_id
            ));
$title = basename(str_replace('.mp4', '', $videoInfo->all_urls[0]));
$captions = $API->getSubtitle(array(
        'format' => 'srt',
        'video_id' => $video_id,
        'language_code' => $language
    ));
```
