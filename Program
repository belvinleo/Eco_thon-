# Import necessary libraries
import pygame
import random

# Define game constants
SCREEN_WIDTH = 800
SCREEN_HEIGHT = 600
FPS = 30

# Initialize Pygame
pygame.init()

# Create the game window
screen = pygame.display.set_mode((SCREEN_WIDTH, SCREEN_HEIGHT))
pygame.display.set_caption("EcoQuest: The Sustainability Challenge")

# Define game colors
WHITE = (255, 255, 255)
GREEN = (0, 255, 0)
BLUE = (0, 0, 255)

# Define player class
class Player(pygame.sprite.Sprite):
    def __init__(self):
        super().__init__()
        self.image = pygame.Surface((50, 50))
        self.image.fill(GREEN)
        self.rect = self.image.get_rect()
        self.rect.center = (SCREEN_WIDTH // 2, SCREEN_HEIGHT // 2)

    def update(self):
        # Add player movement logic here
        pass

# Define resource class
class Resource(pygame.sprite.Sprite):
    def __init__(self):
        super().__init__()
        self.image = pygame.Surface((20, 20))
        self.image.fill(BLUE)
        self.rect = self.image.get_rect()
        self.rect.center = (random.randint(0, SCREEN_WIDTH), random.randint(0, SCREEN_HEIGHT))

    def update(self):
        # Add resource interaction logic here
        pass

# Create sprite groups
all_sprites = pygame.sprite.Group()
resources = pygame.sprite.Group()

# Create player instance
player = Player()
all_sprites.add(player)

# Create resource instances
for _ in range(20):
    resource = Resource()
    all_sprites.add(resource)
    resources.add(resource)

# Game loop
running = True
clock = pygame.time.Clock()

while running:
    # Event handling
    for event in pygame.event.get():
        if event.type == pygame.QUIT:
            running = False

    # Game logic
    all_sprites.update()

    # Drawing
    screen.fill(WHITE)
    all_sprites.draw(screen)

    pygame.display.flip()

    # Cap the frame rate
    clock.tick(FPS)

# Quit the game
pygame.quit()
