# Music-Recommendation-System

In this task, the goal is to predict the chances of a user listening to a song repetitively after the first observable listening event within a time window was triggered. If there are recurring listening event(s) triggered within a month after the user’s very first observable listening event, its target is marked 1, and 0 otherwise in the training set. The two datasets used in this project are the KKBOX and Spotify datasets.

## KKBOX Data
KKBOX provides a training data set which consists of information of the first observable listening event for each unique user-song pair within a specific time duration. Metadata of each unique user and song pair is also provided.
## Tables
### main.csv
* msno: user id
* song_id: song id
* source_system_tab: the name of the tab where the event was triggered. System tabs are used to categorize KKBOX mobile apps functions. For example, tab my library contains functions to manipulate the local storage, and tab search contains functions relating to search.
* source_screen_name: name of the layout a user sees.
* source_type: an entry point a user first plays music on mobile apps. An entry point could be album, online-playlist, song .. etc.
* target: this is the target variable. target=1 means there are recurring listening event(s) triggered within a month after the user’s very first observable listening event, target=0 otherwise .
### songs.csv 
The songs. Note that data is in unicode.
* song_id
* song_length: in ms
* genre_ids: genre category. Some songs have multiple genres and they are separated by |
* artist_name
* composer
* lyricist
* language
### members.csv
user information.
* msno
* city
* bd: age. Note: this column has outlier values, please use your judgement.
* gender
* registered_via: registration method
* registration_init_time: format %Y%m%d
* expiration_date: format %Y%m%d
* song_extra_info.csv
* song_id
* song name - the name of the song.
* isrc - International Standard Recording Code, theoretically can be used as an identity of a song. However, what worth to note is, ISRCs generated from providers have not been officially verified; therefore the information in ISRC, such as country code and reference year, can be misleading/incorrect. Multiple songs could share one ISRC since a single recording could be re-published several times.

## Spotify Data
The Spotify data contains information and audio features of songs in the dataset.
dataset
* track_id: sond id
* track_name: Song's title
* artists: Name of the artist(s)
* duration_ms: Duration of the song
* release_date: Date the song was released
* year: Year of release of the song
* acousticness: How acoustic the song is
* danceability: How easy it is to dance to the song
* energy: How energetic the song is
* instrumentalness: How instrumental in nature the song is
* liveness: How likely it is the song is a live recording
* loudness: How loud the song is
* speechiness: How much the song is focused on spoken word
* tempo: The tempo of the song
* valence: How positive the mood of the song is
* mode:
* key: The musical key the song is played in
* popularity: Popularity of the song (not a ranking)
* explicit: Whether the song contains explicit lyrics or not
* genre: Genre of song

[Download Datasets File](https://drive.google.com/drive/folders/1UROSvo7DGHmzSkI5WKBmSrEQ-jck0qfy?usp=drive_link)
