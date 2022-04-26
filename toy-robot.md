# Toy Robot Simulator

The application is a simulation of a toy robot moving on a square tabletop, of dimensions 5 units x 5 units. There are no other obstructions on the table surface. The robot is free to roam around the surface of the table, but must be prevented from falling to destruction. Any movement that would result in the robot falling from the table must be prevented, however further valid movement commands must still be allowed.

Create an application that can read in commands of the following form:

```
PLACE X,Y,F
MOVE
LEFT
RIGHT
REPORT
```

`PLACE` will put the toy robot on the table in position `X,Y` and facing (F) `NORTH`, `SOUTH`, `EAST` or `WEST`.

- The origin (0,0) can be considered to be the south west most corner.

- The first valid command to the robot is a `PLACE` command, after that, any sequence of commands may be issued, in any order, including another `PLACE` command

- The application should discard all commands in the sequence until a valid `PLACE` command has been executed.

- `MOVE` will move the toy robot one unit forward in the direction it is currently facing.

- `LEFT` and `RIGHT` will rotate the robot 90 degrees in the specified direction without changing the position of the robot.

- `REPORT` will announce the `X`,`Y` and `F` of the robot

- This can be in any form, but standard output is sufficient.

- A robot that is not on the table can choose the ignore the `MOVE`, `LEFT`, `RIGHT` and `REPORT` commands.

- Input can be from a file, or from standard input, as the developer chooses.

- Provide test data to exercise the application.

**Constraints:**

The toy robot must not fall off the table during movement. This also includes the initial placement of the toy robot. Any move that would cause the robot to fall must be ignored.

**Example Input and Output:**

Example a)
```
PLACE 0,0,NORTH
MOVE
REPORT

> 0,1,NORTH
```

Example b)
```
PLACE 0,0,NORTH
LEFT
REPORT

> 0,0,WEST
```

Example c)
```
PLACE 1,2,EAST
MOVE
MOVE
LEFT
MOVE
REPORT

> 3,3,NORTH
```

## Deliverables

You must create a new public Github repository and push your commits to this repo. Give us the URL to the repository so we can clone it.

We would appreciate if you could deliver the exercise in `Ruby` or `JavaScript`, but feel free to deliver it in any other modern language that you feel comfortable using and happy to talk through.

## What are we looking for?

- Ability to write clean, well designed and well tested code. 
- Commit history.

We respect your time so, as a guideline, please don't spend more than 2-3 hours working on this. We'd rather you submitted something partially complete after that time for us to discuss than spend days of your own time working on it. Instead we will discuss any improvements that you would make if you had more time.

## What comes next?

During the interview we will review the code together and discuss your approach to engineering and testing the solution and any assumptions made. 

**Thanks for applying for a job at EMS and good luck! :-)**
