Interesting program, found that it creates a steady state about minute 3.  Each time unique but stable after that amount of time.
Then changing the rules to this:

# apply Conway's rules
            if grid[i, j]  == ON:
                if (total < 2) or ((total > 3) and (total < 7)):
                    newGrid[i, j] = OFF
            else:
                # Modified rule to 3, 7 and 8
                if total == 3 or total > 6:
                    newGrid[i, j] = ON
                   
 the program does not stablize but continues even after 6 minutes to create empty spaces that are stable for a 
 minute or two and then new designs come in and start the process all over.
 
 I also tried this:
 
 # apply Conway's rules
            if grid[i, j]  == ON:
                if (total < 2) or ((total > 4):
                    newGrid[i, j] = OFF
            else:
                # Modified rule to 3 or 4 instead of just 3
                if total == 3 or total == 4:
                    newGrid[i, j] = ON
 
 this very busy, dynamic state almost equal numbeer of on's and off's over the entire grid which never 
 reached a steady stable state.
