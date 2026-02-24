import turtle

# Screen setup
wn = turtle.Screen()
wn.title("Maze Game")
wn.bgcolor("black")
wn.setup(width=600, height=600)

# Player
player = turtle.Turtle()
player.shape("turtle")
player.color("white")
player.penup()
player.speed(0)

# Movement functions
def move_up():
    y = player.ycor()
    player.sety(y + 20)

def move_down():
    y = player.ycor()
    player.sety(y - 20)

def move_left():
    x = player.xcor()
    player.setx(x - 20)

def move_right():
    x = player.xcor()
    player.setx(x + 20)

# Keyboard controls
wn.listen()
wn.onkeypress(move_up, "Up")
wn.onkeypress(move_down, "Down")
wn.onkeypress(move_left, "Left")
wn.onkeypress(move_right, "Right")

wn.mainloop()
