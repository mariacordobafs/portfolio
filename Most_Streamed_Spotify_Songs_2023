--Dataset: Most Streamed Spotify Songs 2023
--Source: Kaggle https://www.kaggle.com/datasets/nelgiriyewithana/top-spotify-songs-2023
--Queried using: BigQuery

# What is the Mode usage percentage for the top 50 songs? 
SELECT
  key,
  mode,
  ROUND((COUNT(top) / 50.0) * 100, 2) AS mode_usage_percentage
FROM
  `my-project-291195.spotify_2023.top_spotify_23`
WHERE
  top BETWEEN 1 AND 50
GROUP BY
  mode, key;


# What is the Mode usage percentage for the top 10 songs? 


SELECT
  key,
  mode,
  ROUND((COUNT(top) / 10.0) * 100, 2) AS mode_usage_percentage
FROM
  `my-project-291195.spotify_2023.top_spotify_23`
WHERE
  top BETWEEN 1 AND 10
GROUP BY
  mode, key;


# What is the Key usage percentage for the top 10 songs? 

SELECT
  key,
  ROUND((COUNT(top) / 10.0) * 100, 2) AS key_usage_percentage
FROM
  `my-project-291195.spotify_2023.top_spotify_23`
WHERE
  top BETWEEN 1 AND 10
GROUP BY
  key;



# What is the Key usage percentage for the top 50 songs? 

SELECT
  key,
  ROUND((COUNT(top) / 50.0) * 100, 2) AS key_usage_percentage
FROM
  `my-project-291195.spotify_2023.top_spotify_23`
WHERE
  top BETWEEN 1 AND 50
GROUP BY
  key;



# What is the BPM usage percentage for the top 10 songs? 

SELECT
  bpm,
  ROUND((COUNT(top) / 10.0) * 100, 2) AS bpm_usage_percentage
FROM
  `my-project-291195.spotify_2023.top_spotify_23`
WHERE
  top BETWEEN 1 AND 10
GROUP BY
  bpm;



# What is the BPM usage percentage for the top 50 songs? 

Sum of  streams per key
 bpm,
  ROUND((COUNT(top) / 50.0) * 100, 2) AS bpm_usage_percentage
FROM
  `my-project-291195.spotify_2023.top_spotify_23`
WHERE
  top BETWEEN 1 AND 50
GROUP BY
  bpm;


# What are the top 10 more streamed BPMs?

SELECT
  CAST(bpm AS STRING) AS bpm,
  SUM(CAST(cleaned_streams AS FLOAT64)) AS streams_bpm
FROM
  `spotify_2023.Cleaned_spotify`
GROUP BY
  bpm
ORDER BY
  streams_bpm DESC
LIMIT 10


# What’s the amount of streams per mode?   (Which one is preferred by the listeners?)


SELECT
 mode,
  SUM(CAST(cleaned_streams AS FLOAT64)) AS streams_mode
FROM
  `my-project-291195.spotify_2023.Cleaned_spotify`
GROUP BY
  mode
ORDER BY
  streams_mode DESC


# What’s the danceability value for the top 10 songs? 


SELECT
  track_name,
  danceability__
FROM
  `my-project-291195.spotify_2023.top_spotify_23`
WHERE
  top BETWEEN 1 AND 10
ORDER BY
  top ASC;


# What’s the danceability value for the top 50 songs? 


SELECT
  track_name,
  danceability__
FROM
  `my-project-291195.spotify_2023.top_spotify_23`
WHERE
  top BETWEEN 1 AND 50
ORDER BY
  top ASC;




# What’s the energy value for the top 10 songs? 


SELECT
  track_name,
  energy__
FROM
  `my-project-291195.spotify_2023.top_spotify_23`
WHERE
  top BETWEEN 1 AND 10
ORDER BY
  top ASC;


# What’s the energy value for the top 50 songs? 


SELECT
  track_name,
  energy__
FROM
  `my-project-291195.spotify_2023.top_spotify_23`
WHERE
  top BETWEEN 1 AND 50
ORDER BY
  top ASC;



# What’s the speechiness value for the top 10 songs? 


SELECT
  track_name,
  speechiness__
FROM
  `my-project-291195.spotify_2023.top_spotify_23`
WHERE
  top BETWEEN 1 AND 10
ORDER BY
  top ASC;


# What’s the speechiness value for the top 50 songs? 
SELECT
  track_name,
  speechiness__
FROM
  `my-project-291195.spotify_2023.top_spotify_23`
WHERE
  top BETWEEN 1 AND 50
ORDER BY
  top ASC;


# What’s the amount of Spotify Playlists for the top 10 songs?


SELECT
  track_name,
  in_spotify_playlists
FROM
  `my-project-291195.spotify_2023.top_spotify_23`
WHERE
  top BETWEEN 1 AND 10
ORDER BY
  top ASC;


# What’s the relationship between the amount of playlists a song is on Spotify and the streams?
SELECT
  track_name,
  in_spotify_playlists AS playlist_status,
  AVG(streams) AS average_streams,
 
FROM
  `my-project-291195.spotify_2023.top_spotify_23`
WHERE
  top BETWEEN 1 AND 10
GROUP BY
  track_name, playlist_status;
