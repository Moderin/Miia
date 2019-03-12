# Miia
Rotation diet tool with calories counter

![Screenshot](https://github.com/Moderin/Miia/blob/master/img/screenshot.png)

### What is it?
Miia is a piece of software that runs in browser and is designed to help people which decided for some reason to go on a 4-days rotatory diet. It is usually used to overcome different food intolerances and allergies. In simple words, on this type of diet you can't eat some foods more often than one day each 4. So that you eat allergic food one day - and than you have to do a three-day rest. Miia can count for you how long ago have you eaten each type of food. Additionally it can count eaten calories and proteins each day.

### How to use it?
1. Install [CouchDB](http://couchdb.apache.org/)

2. Enable CORS in CouchDB. Some info can be found [here](https://stackoverflow.com/questions/20897033/how-to-add-cors-in-couchdb-no-access-control-allow-origin-header-is-present)

3. Restart CouchDB (or computer), go to [http://127.0.0.1:5984/_utils/](http://127.0.0.1:5984/_utils/) and create database called miia

4. In this database create a document with _id named "info", and add the following properties: 
```
  "daily_calories": 0,
  "daily_proteins": 0
```
5. Clone or download this repository, open index.html in your browser and add some food by typing "+". A form should appear with a few entries to fill. You can specify name of product, it's amount (eg. 100g, 2 pieces, 1 jar), calories and proteins it gives you. You can also check "rotate" checkbox, if you want Miia to count when you've eaten this product (so if it's allergic for u). After filling the form, press OK button. The food shoud have been added to database.

6. Now just type it's name to find it. Just click it to tell Miia that you've just eaten it. You can also type * to show all food. If you've marked a food as allergic and eaten it, Miia will highlight it first day. Enjoy!
 
