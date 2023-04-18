# ODEV 6
Merhabalar,

Aşağıdaki sorgu senaryolarını dvdrental örnek veri tabanı üzerinden gerçekleştiriniz.

    film tablosunda bulunan rental_rate sütunundaki değerlerin ortalaması nedir?
    film tablosunda bulunan filmlerden kaç tanesi 'C' karakteri ile başlar?
    film tablosunda bulunan filmlerden rental_rate değeri 0.99 a eşit olan en uzun (length) film kaç dakikadır?
    film tablosunda bulunan filmlerin uzunluğu 150 dakikadan büyük olanlarına ait kaç farklı replacement_cost değeri vardır?

Kolay Gelsin.

# CEVAPLAR

## 1.Soru: 

SELECT ROUND(AVG(rental_rate), 3) FROM film;

2.980

## 2.Soru:

SELECT COUNT(title) FROM film
WHERE title LIKE 'C%';

92

## 3.Soru:

SELECT MAX(length) FROM film
WHERE rental_rate = 0.99;

184

## 4.Soru:

SELECT COUNT(DISTINCT(replacement_cost)) FROM film
WHERE length > 150;

21
