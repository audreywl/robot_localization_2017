# Robot Localization 2017
### Audrey Lewis and Carl Moser

## Our goal
The particle filter is a method of localization which involves evaluating guesses ("particles") based on their correspondence with real data. In this case, the data being evaluated a laser scan, which is being compared with map data.

## Our solution

![]()

## Design decision
For the laser scan processing portion of the data, we attempted to expedite the code using matrix math. Instead of manually using trigonometry for rotate the x and y values for each particle individually, we used a rotation matrix in numpy. To do this, we had to account for the fact that although our numpy array of data would always be the same size, our sensor wasn't perfect, and we would get different amounts of valid data. To remove the invalid data from consideration without letting it affect our weighting, we used a masked array. In the end, we had to extract it in the form of a 1D array, and iterate over potential positions.

## Challenges

## Improvments

## Lessons learned
