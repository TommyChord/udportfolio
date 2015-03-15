## Website Performance Optimization portfolio project

Optimizations are done on the following:

#### index.html
1. Optimized style.css to be more specific targeted by adding a couple of new class names instead of long "chains" of targets.
1. Minimized and inlined style.css
1. Added mediaquery to print.css link
1. Added "async" attribute to the analytics js
1. Specified width and height attributes to the images

#### /img
2. Added new and optimized the prifile image (tommy.jpg)

###### Result from PS Insight:
  ```bash
  Mobile: 96/100
  Computer: 97/100
  ```

#### views/pizza.html
3. Minimized and inlined style.css
3. Minimized bootstrap-grid.css
3. Added viewport meta tag
3. Specified width and height attributes to the main image (pizzeria.jpg)

#### views/js/main.js
4. Set the floating background pizza images to size 100x77px
4. Updated updatePositions():
  ```bash
  Moved the scrollTop function out of the for loop as this is the same for all elements affected by the loop.
  ```
4. Updated changePizzaSizes(size):
  ```bash
  	Get all the pizza elements:
 	var pizzas = document.getElementsByClassName("randomPizzaContainer");
 	
 	Determine the size:
	var dx = determineDx(pizzas[0], size);
	
	Calculate the new width:
	var newwidth = (pizzas[0].offsetWidth + dx) + 'px';
	
	THEN we can loop through all the pizza elements and set the new size:
	for (var i = 0; i<pizzas.length; i++){
		pizzas[i].style.width = newwidth;
	}
  ``` 
4. Minimized the main.js (main_min.js)

#### views/images
5. Created a new smaller (100x77px) and optimized image of the floating pizzas (pizza_bg.png))
5. Resized and optimized the main image (pizzeria.jpg)

###### Result from PS Insight:
  ```bash
  Mobile: 85/100
  Computer: 95/100
  ```
  
###### Result from console.log:
  ```bash
  Time to generate pizzas on load: 14.61300000664778ms
  Time to resize pizzas: 1.5710000006947666ms
  Average time to generate last 10 frames: 0.4724999991594814ms
  ```