 Q1: Top 5 Most popular Songs?

SELECT artist, song, popularity
FROM song
ORDER BY popularity DESC
LIMIT 10;

 Q2: Most popular genre?

SELECT genre, AVG(popularity) AS average_popularity
FROM song
GROUP BY genre
ORDER BY average_popularity DESC
LIMIT 5;

 Q3:Top 10 Most Popular Artist.

SELECT artist, AVG(popularity) AS average_popularity
FROM song
GROUP BY artist
ORDER BY average_popularity DESC
LIMIT 10; 

 Q4: Dose songs lenght effects popularity of song?

SELECT 
    ROUND(duration_ms / 60000, 2) AS duration_minutes,
    popularity
FROM song
ORDER BY duration_minutes 

 Q5: Which version of songs are more popular?

SELECT explicit, AVG(popularity) AS average_popularity
FROM song
GROUP BY explicit
ORDER BY average_popularity DESC;

 Q6: Who is most popular artist between 2010 to 2020 years?

SELECT artist, AVG(popularity) AS average_popularity
FROM song
WHERE year BETWEEN 2010 AND 2020
GROUP BY artist
ORDER BY average_popularity DESC
LIMIT 1;

SELECT artist, year, MAX(popularity) AS max_popularity
FROM song
WHERE year BETWEEN 2010 AND 2020
GROUP BY artist, year
HAVING MAX(popularity) = (
  SELECT MAX(popularity)
  FROM song
  WHERE year BETWEEN 2010 AND 2020
)
ORDER BY year;

 Q7: Energy and loudness affects song genre?

SELECT genre, AVG(energy) AS average_energy, AVG(loudness) AS average_loudness
FROM song
GROUP BY genre
ORDER BY genre;
