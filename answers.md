# Answers

## 1. Which are the different genres?

Games
Productivity
Weather
Shopping
Reference
Finance
Music
Utilities
Travel
Social Networking
Sports
Business
Health & Fitness
Entertainment
Photo & Video
Navigation
Education
Lifestyle
Food & Drink
News
Book
Medical
Catalogs

## 2. Which is the genre with more apps rated?

SELECT prime_genre, count(rating_count_tot) AS ratings FROM DATA GROUP BY prime_genre ORDER BY APPS DESC  LIMIT 1;

Games	3862


## 3. Which is the genre with more apps?

SELECT prime_genre, count(track_name) AS APPS FROM DATA GROUP BY prime_genre ORDER BY APPS DESC  LIMIT 1;

Games	3862

## 4. Which is the one with less?

SELECT prime_genre, count(prime_genre) AS APPS FROM DATA GROUP BY prime_genre ORDER BY APPS ASC  LIMIT 1;

Catalogs 10

## 5. Take the 10 apps most rated.

SELECT track_name, rating_count_tot AS RATING FROM DATA ORDER BY rating DESC  LIMIT 10;

Facebook	2974676
Instagram	2161558
Clash of Clans	2130805
Temple Run	1724546
Pandora - Music & Radio	1126879
Pinterest	1061624
Bible	985920
Candy Crush Saga	961794
Spotify Music	878563
Angry Birds	824451

## 6. Take the 10 apps best rated by users.

SELECT track_name, user_rating AS RATING FROM DATA ORDER BY rating DESC  LIMIT 10;

TurboScan™ Pro - document & receipt scanner: scan multiple pages and photos to PDF	5
Flashlight Ⓞ	5
Learn to Speak Spanish Fast With MosaLingua	5
:) Sudoku +	5
The Photographer's Ephemeris	5
King of Dragon Pass	5
Escape the Sweet Shop Series	5
Infinity Blade	5
Plants vs. Zombies HD	5
Plants vs. Zombies	5


## 7. Take a look on the data you retrieved in the question 5. Give some insights.

Social media and games seem to be the most heavy used apps and therefore people is more prompt to rate them

## 8. Take a look on the data you retrieved in the question 6. Give some insights.

THe best rated apps tend to be functionality apps or productivity apps. Simple apps that perform a basic function. Then the list is filled with games.

## 9. Now compare the data from questions 5 and 6. What do you see?

From the top 10 most rated apps none is on the best rated. So this implies that people is not so prompt to give more positive feedback than negative feedback.

## 10. How could you take the top 3 regarding the user ratings but also the number of votes?

SELECT track_name, user_rating, rating_count_tot  FROM DATA ORDER BY user_rating DESC, rating_count_tot DESC  LIMIT 3;

Head Soccer	5	481564
Plants vs. Zombies	5	426463
Sniper 3D Assassin: Shoot to Kill Gun Game	5	386521

## 11. Does people care about the price? Do some queries, comment why are you doing them and the results you retrieve. What is your conclusion?

SELECT track_name, user_rating, rating_count_tot, price  FROM DATA ORDER BY user_rating DESC, rating_count_tot DESC, price DESC LIMIT 3;

Head Soccer	5	481564	0
Plants vs. Zombies	5	426463	0.99
Sniper 3D Assassin: Shoot to Kill Gun Game	5	386521	0

