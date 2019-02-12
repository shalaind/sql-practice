<!-- Clue #1: We recently got word that someone fitting Carmen Sandiego's description has been traveling through Southern Europe. She's most likely traveling someplace where she won't be noticed, so find the least populated country in Southern Europe, and we'll start looking for her there. -->

SELECT * FROM COUNTRY LIMIT 1;

<!-- Clue #2: Now that we're here, we have insight that Carmen was seen attending language classes in this country's officially recognized language. Check our databases and find out what language is spoken in this country, so we can call in a translator to work with you. -->

 SELECT name FROM country WHERE region = 'Southern Europe' ORDER BY population ASC LIMIT 1;
 
<!-- 
Clue #3: We have new news on the classes Carmen attended: our gumshoes tell us she's moved on to a different country, a country where people speak only the language she was learning. Find out which nearby country speaks nothing but that language. -->
 SELECT language FROM countrylanguage WHERE countrycode = 'VAT';
