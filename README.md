# Using Variables: The Solar System

![solar system](https://s3.amazonaws.com/upperline/curriculum-assets/p5js/labs/solar-system.png)

The code below builds a model of the solar system. It's not a very accurate model though because it shows all the planets as the same size. In reality the planet's range in size from Jupiter, over 11 times the size of Earth, to Pluto, with a diameter of only 0.2 times Earth's. Also, in the real solar system the planets are not evenly spaced apart. Pluto, for example, is almost 40 times as far from the sun as Earth is. Considering that Earth is 92.96 million miles from the sun, that's pretty far!!

```javascript
var centerY;

function setup() {
  createCanvas(24000, 600);
  centerY = height/2;
}

function draw() {
  background(0);

  // sun
  stroke(250, 225, 0);
  strokeWeight(50);
  line(0, 0, 0, height);

  noStroke();

  // mercury
  fill(125);
  ellipse(200, centerY, 50, 50);

  // venus
  fill(220, 155, 100);
  ellipse(400, centerY, 50, 50);

  // earth
  fill(0, 100, 200);
  ellipse(600, centerY, 50, 50);

  // mars
  fill(200, 50, 0);
  ellipse(800, centerY, 50, 50);

  // jupiter
  fill(195, 160, 140);
  ellipse(1000, centerY, 50, 50);

  // saturn
  fill(240, 215, 160);
  ellipse(1200, centerY, 50, 50);

  // uranus
  fill(150, 250, 250);
  ellipse(1400, centerY, 50, 50);

  // neptune
  fill(55, 130, 250);
  ellipse(1600, centerY, 50, 50);

  // pluto
  fill(250, 200, 160);
  ellipse(1800, centerY, 50, 50);

}
```

## Your Task

Your task is to alter the code using the chart below so that you can show a more accurate model of the solar system. The chart shows the *Diameter* of each planet in relation to Earth's diameter, and the *Distance from the Sun* of each planet in relation to Earth's distance.

Assume that in the code *the ellipse that represents Earth is in the correct position and the correct size.* Place the other planets in the appropriate position with the appropriate size in relation to Earth.


## Planetary Facts - Ratio to Earth
*ratios* | MERCURY | VENUS | EARTH | MARS | JUPITER | SATURN | URANUS | NEPTUNE | PLUTO
 --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
 **Diameter** | 0.4 |	0.9 |	1	| 0.5 | 11.2 | 9.5 | 4.0 | 3.9 |	0.2
 **Distance from Sun** | 0.4 | 0.7 | 1 | 1.5 |	5.2 | 9.6 |	19.2 |	30.1 |	39.5

## Tips
Let's say a new planet was discovered that was 2.6 times the size of Earth.  I could pull out my calculator and multiply Earth's width (50px) by 2.6. Then I could pass the result, 130, to the `ellipse` function.  

This would be really tedious to do for every planet, and why should we do all that math ourselves when the computer can do it for us.  What if you made a variable `earthDiameter` that you could just multiply by 2.6 or whatever each planet's diameter is?

## Additional Goals

You will probably start out by having at least two variables representing Earth's diameter and Earth's distance from the sun.  Can you make additional variables for each planet so that your code is extremely *easy to read* for other programmers?

Rather than hard-coding in Earth's diameter and distance, could you make those values be proportional to the size of the canvas so that the solar system stayed proportional no matter how you changed the canvas size?

## Expert Challenges

If you accomplish all of these goals here are some suggestions on how you could expand on this project

- 3D planets. p5 allows you to build three dimensional objects. Check the documentation for 3-D Primitives such as [`sphere`](https://p5js.org/reference/#/p5/sphere) and other functions such as [`rotateX`](https://p5js.org/reference/#/p5/rotateX) and [`rotateY`](https://p5js.org/reference/#/p5/rotateY)

- When a planet is clicked on, it could display an "Information Bubble" with some facts about that planet. The data for this lab came from this [NASA Planetary Fact Sheet](https://nssdc.gsfc.nasa.gov/planetary/factsheet/planet_table_ratio.html)

- Could you add shooting starts in the background or an asteroid belt?

Don't stop there, these ideas are meant to be open ended to get you started thinking about all you can do with code!
