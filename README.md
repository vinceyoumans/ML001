# ML GoLang Exaample.

This code example shows reading a BASKET with n Items.  In this case 3 Items.

The App reads the basket, then runs Go Routine on Each Item in Parallel.
I am using pointers to the original Basket.  Passing the calues to be modified by reference.

When the WG.Done() is execute, the code Prints the modified Basket.

I also demonstrate MAXPROCS.  In this case, I set MAXPROCS to 100, which is over kill.
I could have set it to 4 and it should work fine.  1 for main process. 3 for each of the Items.

This is my thoughts on what you were hinting at for your solution.


***Modification : I added unit testing to the app.***


TODO:
Dockerfy the project in a Docker-Compose file.

If BB wants to see some real fireworks... 

1. add a redis container where the baskets will be hosted.
2. Create alternative approach where a single, Long running Go Application spawns new Go Routines.  This was my original Idea, and differ from spawning individual GoLang containers.
3. Create a Leader board application that is listening to Channels.
4. Add unit Testing - done





