# Ball-1
import pygame
import random
import math
import time

# Initialize pygame
pygame.init()

# Screen dimensions
WIDTH, HEIGHT = 600, 600
FPS = 60

# Colors
WHITE = (255, 255, 255)
RED = (255, 0, 0)
BLACK = (0, 0, 0)

# Circle properties
CIRCLE_RADIUS = 250
CENTER_X, CENTER_Y = WIDTH // 2, HEIGHT // 2
OPENING_WIDTH = 20  # width of the opening in the circle
OPENING_ANGLE = math.pi / 4  # angle of the opening in radians

# Ball properties
BALL_RADIUS = 10
BALL_COLOR = RED
MAX_BALLS = 50

# Ball class to handle bouncing behavior
class Ball:
    def __init__(self, x, y, vx, vy):
        self.x = x
        self.y = y
        self.vx = vx
        self.vy = vy

    def move(self):
        self.x += self.vx
        self.y += self.vy

    def check_collision(self):
        dist = math.sqrt((self.x - CENTER_X) ** 2 + (self.y - CENTER_Y) ** 2)
        if dist + BALL_RADIUS >= CIRCLE_RADIUS:
            # Reflect the ball's velocity vector upon collision
            n
