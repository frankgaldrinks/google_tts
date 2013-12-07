google_tts
==========

Using the Google Translate API as it's speech engine, this quick hack takes any string and converts it into a MP3 voice file.

Usage
==

```ruby
require_relative 'google_tts'

# Downloads MP3 to current directory
"Hello World!".to_mp3

# Downloads MP3 to stated location
"Hello World!".to_mp3 "my_directory/my_file_name.mp3"

# Supports large amounts of text. Google Translate only allows 100 characters per request 
# so it will batch up requests and then combine the results into one MP3 when complete
text = "A clean up operation is under way on the east coast of England after widespread flooding following the worst tidal surge for 60 years. The surge led to thousands abandoning their homes, although officials hailed improved flood defences."
text.to_mp3
```

