## Запрос для вставки данных минимум о двух книгах в коллекцию books
```
db.books.insertMany([
  {
    title: "Город",
    description: "научная фантастика",
    authors: "Клиффорд Саймак"
  },
  {
    title: "Задача трех тел",
    description: "цикл Воспоминания о прошлом земли",
    authors: "Лю Цысинь"
  }
]);
```
## Запрос для поиска полей документов коллекции books по полю title
```
db.books.find(
  {
    title: "Город"
  }
);
```
## Запрос для редактирования полей: description и authors коллекции books по _id записи
```
db.books.updateOne(
  { _id: "42342534564565765756"},
  {
    $set {
      description: "Science fiction",
      authors: "Clifford D. Simak"
    }    
  }
);
```