# Just a little quiz thing 🤷🏻‍♂️

## DOM

### 1. What will happen when you run the following code?

```javascript
const buttons = document.getElementsByClassName('button')
buttons.addEventListener("click", function(e){
    console.log(e.target)
})    
```
```
Will add an event listener to the first button
```

### Use the following HTML to answer the rest of the questions.

```html
<div id="container">
    <h4>This is a cool heading!</h4>
    <ul class="list">
        <li>The first list item</li>
        <li>The second list item</li>
    </ul>
    <p>This is a random "p" tag with a <span>SPAN</span> inside of it for some reason!</p>
    <li>This list item clearly makes no sense here!!! Who wrote this horrible code?</li>
</div>
```

### 2. Provide the JavaScript code that would get the second list item from the DOM and save it to a variable called `secondListItem`.

```javascript
document.querySeletorAll('li')[1]
```

### 3. Once you have the `secondListItem` node, how could you traverse the DOM tree to get the `<p>` tag.


```javascript
const secondListItem = document.querySelectorALl('li')[1]
secondListItem.parentNode.nextElementSibling
```

### 4. What query could you do to get just the `li` tags that are inside the `ul` and not that random janky one that's near the bottom for some reason?


```javascript
document.querySelectorAll('.ul>li')
```

## Events

### 5. Why do we use a `DOMContentLoaded` listener?

```
To ensure that the load order doesn't affect certain functions
```

### 6. What type of element does a `submit` event happen to?

```
a form
```

### 7. What attribute of an `input` element can we use to easily retrieve data from form inputs?

```
name attribute
```

### 8. What are the 2 required parameters we have to pass into a call to `addEventListener`?

```
(event, callBack())
```

## Fetch

### 9. Write the code to do a GET `fetch` request to "notarealwebsite.com" and log the response from the server to the console.

```javascript
fetch("notarealwebsite.com")
.then(function(response) {
  return response.json();
})
.then(function(json){
    console.log(json)
})
```

### 10. Following RESTful conventions (see [restular.com](http://www.restular.com) if you need a bit of help with that), write the `fetch` request to update the `user` record with an id of 1 at the URL "notarealwebsite.com".

```javascript

```

### 11. What effect does the following fetch request have in the database? What does the following fetch request *return*? 

```javascript
fetch("notarealwebsite.com/dogs/25", {
    method: "DELETE"
})
```
deletes the dog with an id of 25. returns a promise.s
```

```

## Datasets

### 12. Write the HTML to create a `div` element with a dataset property of "awesome" set to a value of "Steven is".

```HTML
<div data-awesome="Steven is">Steven</div> 

```

### 13. In Ja<div data-awesome="Steven is">Steven</div> vaScript, how would you get the `div` element from the question above from the DOM using `document.querySelector` and the dataset?

```javascript
let div = document.querySelector('div[data-awesome="Steven id"]') 
```

### 14. Write the JavaScript to create a `marquee` element with a dataset property of "jaws" set to a value of "great movie".

```javascript
document.createElement('marquee')
marquee.dataset.jaws="greatmovie"
```

### 15. In JavaScript, how would you access the "jaws" dataset property? How would you change its value to "overrated maybe"?

```javascript
let specMarquee = document.querySelector('[data-jaws="great movie"]')
marquee.dataset.jaws = "great movie"
```

