import info.gridworld.actor.Bug;
import info.gridworld.grid.Location;

/*
* This bug is part of assignment Project 13 - part 1.
* It draws the word "LIKE" on the grid,
* starting from the bug's initial location.
*/
class Bug2 extends Bug {

    // Incremented at each move, to keep track of what part of what word to draw next:
    int step=0;

    public void act()
    {
        if(step<=5)
        {
            // Draw the vertical line of letter L:
            setDirection(180);
            move();
        }
        else if(step<10)
        {
            // Draw the horizontal line of letter L:
            setDirection(90);
            move();
        }
        else if(step==11)
        {
            // Move to the start top horizontal line of letter I
            Location currentLoc = getLocation();
            moveTo(new Location(currentLoc.getRow()-6, currentLoc.getCol()+2));
        }
        else if(step<16)
        {
            // Draw the top horizontal line of letter I
            move();
        }
        else if(step==17)
        {
            // Move to the start of the vert. line for letter I
            Location currentLoc = getLocation();
            moveTo(new Location(currentLoc.getRow()+1, currentLoc.getCol()-3));
            setDirection(180);
        }
        else if(step<23)
        {
            // Draw the vert. line of letter I
            move();
        }
        else if(step==23)
        {
            // Move to the start of the bottom horiz. line of letter I
            Location currentLoc = getLocation();
            moveTo(new Location(currentLoc.getRow(), currentLoc.getCol()-2));
            setDirection(90);
        }
        else  if(step<29)
        {
            // Draw the bottom horiz. line of letter I
            move();
        }
        else if(step==29)
        {
            // Move to the start of letter K
            Location currentLoc = getLocation();
            moveTo(new Location(currentLoc.getRow()-6, currentLoc.getCol()+2));
            setDirection(180);
        }
        else if(step<37)
        {
            //  Draw the vert. line of letter K
            move();
        }
        else if(step==37)
        {
            // Change location and direction so that we could draw the top right. line of letter K
            Location currentLoc = getLocation();
            moveTo(new Location(currentLoc.getRow()-2, currentLoc.getCol()));
            setDirection(45);
        }
        else if(step<44)
        {
            //  Draw the top right. line of letter K
            move();
        }
        else if(step==44)
        {
            // Change location and direction so that we could draw the bottom right. line of letter K
            Location currentLoc = getLocation();
            moveTo(new Location(currentLoc.getRow()+5, currentLoc.getCol()-3));
            setDirection(135);
        }
        else if(step<47)
        {
            //  Draw the bottom right. line of letter K
            move();
        }
        else if(step==48)
        {
            // Move to the start of letter E
            Location currentLoc = getLocation();
            moveTo(new Location(currentLoc.getRow()-7, currentLoc.getCol()+2));
            setDirection(90);
        }
        else if(step<54)
        {
            // Draw the top horiz. line of letter E
            move();
        }
        else if(step==54)
        {
            // Move to the start of middle horiz. line of letter E
            Location currentLoc = getLocation();
            moveTo(new Location(currentLoc.getRow()+3, currentLoc.getCol()-5));
        }
        else if(step<60)
        {
            // Draw the middle horiz. line of letter E
            move();
        }
        else if(step==60)
        {
            // Move to the start of bottom horiz. line of letter E
            Location currentLoc = getLocation();
            moveTo(new Location(currentLoc.getRow()+3, currentLoc.getCol()-5));
        }
        else if(step<66)
        {
            // Draw the bottom horiz. line of letter E
            move();
        }
        else if(step==66)
        {
            // Move to the start of vert. line of letter E
            Location currentLoc = getLocation();
            moveTo(new Location(currentLoc.getRow()-6, currentLoc.getCol()-5));
            setDirection(180);
        }
        else if(step<73)
        {
            // Draw the bottom horiz. line of letter E
            move();
        }

        step++;
    }
}