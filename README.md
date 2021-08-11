**FPL optimisation**

Experimenting with Sertalp B Cay's python code for optimising projected points in Fantasy Premier League (https://github.com/sertalpbilal/FPL-Optimization-Tools) 

Model walkthroughs and package dependencies are detailed in Sertalp's video series: https://www.youtube.com/channel/UCpBAdn3PO9N6vikTXKgsH4Q - you'll need Python 3.9.4, Pandas, CBC and Sasoptpy to run this code.

For the pre-season problem, I wanted to add bench weights, and multipliers for money in the bank and free transfers, to stop the optimiser from being too greedy. 

Bench weights are set in the dictionary section. They are in order of GK, Sub1, Sub2, Sub3. These are static weights, so don't change depending on how nailed your players are. A better way of handling this would be to use xMins to determine the chance that one or more subs will be needed. I hope to get to that in future, likely once the season has started.

There's also a multiplier for money in the bank, passed through as a parameter in the function. Don't go higher than 0.2pts/£m otherwise the optimiser will hoard cash! There's an additional constraint to keep money ITB < £2m - you can change this.

And finally there's a multiplier for the number of spare free transfers. I've set this at 1.6pts/transfer but you can obviously change it.
