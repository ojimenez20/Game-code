import pygame
pygame.init()

x = 50
y = 426
width = 520
height = 550
size = (width, height)
vel = 7
Walkcount = 0
left = False
right = False
up = False
down = False
screen = pygame.display.set_mode(size)
pygame.display.set_caption("Maze Runner!")

 #player walk forward/down
Walkdown = [ pygame.image.load("player_down.png"),
pygame.image.load("player_down2.png"), pygame.image.load("player_down3.png")]

 #player walk right
Walkright = [ pygame.image.load("player_right.png"),
 pygame.image.load("player_right2.png") ]

 #player walk left
Walkleft = [ pygame.image.load("player_left.png"), pygame.image.load("player_left2.png") ]

 # player Walk upward/backwards
Walkupward = [ pygame.image.load("player_upward.png"), pygame.image.load("player_upward2.png"), pygame.image.load("player_upward3.png") ]

 #grasswall
Grasswall = pygame.image.load("grass.png")

 #dirt path
Dirtpath = pygame.image.load("dirt.png")

 #Bush
bush_3 = pygame.image.load("Bush3.png")

 #enemy
enemy = pygame.image.load("sorcerer_attack_1.png")
enemyX = 191
enemyY = 128
enemyON = True


 #stones
blue_stone = pygame.image.load("blue_stone.png")
blueX = 0
blueY = 0
blue = False

grey_stone = pygame.image.load("grey_stone.png")
greyX = 0
greyY = 320
grey = False

orange_stone = pygame.image.load("orange_stone.png")
orangeX = 120
orangeY = 494
orange = False

red_stone = pygame.image.load("red_stone.png")
redX = 444
redY = 65
red = False



def drawwindow():
  global Walkcount
  #grass
  if drawtiles ==1: 
    screen.blit(Grasswall, (0,0)) 
    screen.blit(Grasswall, (64,0)) 
    screen.blit(Grasswall, (128,0)) 
    screen.blit(Grasswall, (190,0)) 
    screen.blit(Grasswall, (253,0)) 
    screen.blit(Grasswall, (317,0)) 
    screen.blit(Grasswall, (380,0)) 
    screen.blit(Grasswall, (444,0)) 
    screen.blit(Grasswall, (0,59))
    screen.blit(Grasswall, (64,60))
    screen.blit(Grasswall, (128,60))
    screen.blit(Grasswall, (190,60))
    screen.blit(Grasswall, (253,60))
    screen.blit(Grasswall, (317,60))
    screen.blit(Grasswall, (380,60))
    screen.blit(Grasswall, (444,60))
    screen.blit(Grasswall, (0,124))
    screen.blit(Grasswall, (64,124))
    screen.blit(Grasswall, (128,124))
    screen.blit(Grasswall, (190,124))
    screen.blit(Grasswall, (253,124))
    screen.blit(Grasswall, (317,124))
    screen.blit(Grasswall, (380,124))
    screen.blit(Grasswall, (444,124))
    screen.blit(Grasswall, (0,188))
    screen.blit(Grasswall, (64,188))
    screen.blit(Grasswall, (128,188))
    screen.blit(Grasswall, (190,188))
    screen.blit(Grasswall, (253,188))
    screen.blit(Grasswall, (317,188))
    screen.blit(Grasswall, (380,188))
    screen.blit(Grasswall, (444,188))
    screen.blit(Grasswall, (0,251))
    screen.blit(Grasswall, (64,251))
    screen.blit(Grasswall, (128,251))
    screen.blit(Grasswall, (190,251))
    screen.blit(Grasswall, (253,251))
    screen.blit(Grasswall, (317,251))
    screen.blit(Grasswall, (380,251))
    screen.blit(Grasswall, (444,251))
    screen.blit(Grasswall, (0,315))
    screen.blit(Grasswall, (64,315))
    screen.blit(Grasswall, (128,315))
    screen.blit(Grasswall, (190,315))
    screen.blit(Grasswall, (253,315))
    screen.blit(Grasswall, (317,315))
    screen.blit(Grasswall, (380,315))
    screen.blit(Grasswall, (444,315))
    screen.blit(Grasswall, (0,379))
    screen.blit(Grasswall, (64,379))
    screen.blit(Grasswall, (128,379))
    screen.blit(Grasswall, (190,379))
    screen.blit(Grasswall, (253,379))
    screen.blit(Grasswall, (317,379))
    screen.blit(Grasswall, (380,379))
    screen.blit(Grasswall, (444,379))
    screen.blit(Grasswall, (0,442))
    screen.blit(Grasswall, (64,442))
    screen.blit(Grasswall, (128,442))
    screen.blit(Grasswall, (190,442))
    screen.blit(Grasswall, (253,442))
    screen.blit(Grasswall, (317,442))
    screen.blit(Grasswall, (380,442))
    screen.blit(Grasswall, (444,442))
    screen.blit(Grasswall, (0,500))
    screen.blit(Grasswall, (64,500))
    screen.blit(Grasswall, (128,500))
    screen.blit(Grasswall, (190,500))
    screen.blit(Grasswall, (253,500))
    screen.blit(Grasswall, (317,500))
    screen.blit(Grasswall, (380,500))
    screen.blit(Grasswall, (444,500))
    
    #path
    screen.blit(Dirtpath, (0,0))
    screen.blit(Dirtpath, (0,64))
    screen.blit(Dirtpath, (0,128))
    screen.blit(Dirtpath, (64,128))
    screen.blit(Dirtpath, (64,192))
    screen.blit(Dirtpath, (64,256))
    screen.blit(Dirtpath, (128,128))
    screen.blit(Dirtpath, (191,128))
    screen.blit(Dirtpath, (191,0))
    screen.blit(Dirtpath, (191,64))
    #screen.blit(Dirtpath, (64,320))
    screen.blit(Dirtpath, (0,320))
    screen.blit(Dirtpath, (255,128))
    screen.blit(Dirtpath, (291,192))
    screen.blit(Dirtpath, (291,209))
    screen.blit(Dirtpath, (261,273))
    screen.blit(Dirtpath, (325,273))
    screen.blit(Dirtpath, (380,273))
    screen.blit(Dirtpath, (319,128))
    screen.blit(Dirtpath, (444,64)) #gateway to next level
    screen.blit(Dirtpath, (384,0))
    screen.blit(Dirtpath, (380,64))
    screen.blit(Dirtpath, (320,0))
    screen.blit(Dirtpath, (383,128))
    screen.blit(Dirtpath, (64,320))
    screen.blit(Dirtpath, (120,320))
    screen.blit(Dirtpath, (120,366))
    screen.blit(Dirtpath, (120,430))
    screen.blit(Dirtpath, (120,494))
    screen.blit(Dirtpath, (184,430))
    screen.blit(Dirtpath, (248,370))
    screen.blit(Dirtpath, (248,430))
    screen.blit(Dirtpath, (312,430))
    
    
    #bush
    screen.blit(bush_3, (70,0))
    screen.blit(bush_3, (70,26))
    screen.blit(bush_3, (70,39))
    screen.blit(bush_3, (70,60))
    screen.blit(bush_3, (120,0))
    screen.blit(bush_3, (120,33))
    screen.blit(bush_3, (120,66))
    screen.blit(bush_3, (125,196))
    screen.blit(bush_3, (166,196))
    screen.blit(bush_3, (125,222))
    screen.blit(bush_3, (166,230))
    screen.blit(bush_3, (125,240))
    screen.blit(bush_3, (166,255))
    screen.blit(bush_3, (125,267))
    screen.blit(bush_3, (179,295))
    screen.blit(bush_3, (220,320))
    screen.blit(bush_3, (200,320))
    screen.blit(bush_3, (183,350))
    screen.blit(bush_3, (183,380))
    screen.blit(bush_3, (280,320))
    screen.blit(bush_3, (330,320))
    screen.blit(bush_3, (400,320))
    screen.blit(bush_3, (440,320))
    screen.blit(bush_3, (326,320))
    screen.blit(bush_3, (446,15))
    screen.blit(bush_3, (444,240))
    screen.blit(bush_3, (444,270))
    screen.blit(bush_3, (444,280))
    screen.blit(bush_3, (444,360))
    screen.blit(bush_3, (444,200))
    screen.blit(bush_3, (444,160))
    screen.blit(bush_3, (444,130))
    screen.blit(bush_3, (386,360))
    screen.blit(bush_3, (386,180))
    screen.blit(bush_3, (386,200))
    screen.blit(bush_3, (386,227))
    screen.blit(bush_3, (346,180))
    screen.blit(bush_3, (346,200))
    screen.blit(bush_3, (346,227))
    screen.blit(bush_3, (189,189))
    screen.blit(bush_3, (200,196))
    screen.blit(bush_3, (229,200))
    screen.blit(bush_3, (229,225))
    screen.blit(bush_3, (229,240))
    screen.blit(bush_3, (233,248))
    screen.blit(bush_3, (209,290))
    screen.blit(bush_3, (186,315))
    screen.blit(bush_3, (340,360))
    screen.blit(bush_3, (337,360))
    screen.blit(bush_3, (314,360))
    screen.blit(bush_3, (314,387))
    screen.blit(bush_3, (328,387))
    screen.blit(bush_3, (376,387))
    screen.blit(bush_3, (444,387))
    screen.blit(bush_3, (376,420))
    screen.blit(bush_3, (396,420))
    screen.blit(bush_3, (444,420))
    screen.blit(bush_3, (376,455))
    screen.blit(bush_3, (396,455))
    screen.blit(bush_3, (444,455))
    screen.blit(bush_3, (180,469))
    screen.blit(bush_3, (230,469))
    screen.blit(bush_3, (290,469))
    screen.blit(bush_3, (350,469))
    screen.blit(bush_3, (400,469))
    screen.blit(bush_3, (444,469))
    screen.blit(bush_3, (180,500))
    screen.blit(bush_3, (230,500))
    screen.blit(bush_3, (290,500))
    screen.blit(bush_3, (350,500))
    screen.blit(bush_3, (400,500))
    screen.blit(bush_3, (444,500))
    screen.blit(bush_3, (0,165))
    screen.blit(bush_3, (0,200))
    screen.blit(bush_3, (0,235))
    screen.blit(bush_3, (0,260))
    screen.blit(bush_3, (0,276))
    screen.blit(bush_3, (0,375))
    screen.blit(bush_3, (38,375))
    screen.blit(bush_3, (0,404))
    screen.blit(bush_3, (38,407))
    screen.blit(bush_3, (0,437))
    screen.blit(bush_3, (38,437))
    screen.blit(bush_3, (0,468))
    screen.blit(bush_3, (38,468))
    screen.blit(bush_3, (0,500))
    screen.blit(bush_3, (38,500))
    screen.blit(bush_3, (250,0))
    screen.blit(bush_3, (250,30))
    screen.blit(bush_3, (250,59))
    screen.blit(bush_3, (250,78))
    screen.blit(bush_3, (309,59))
    screen.blit(bush_3, (309,77))
  
  elif drawtiles == 2:
    
    screen.blit(Grasswall, (0,0)) 
    screen.blit(Grasswall, (64,0)) 
    screen.blit(Grasswall, (128,0)) 
    screen.blit(Grasswall, (190,0)) 
    screen.blit(Grasswall, (253,0)) 
    screen.blit(Grasswall, (317,0)) 
    screen.blit(Grasswall, (380,0)) 
    screen.blit(Grasswall, (444,0)) 
    screen.blit(Grasswall, (0,59))
    screen.blit(Grasswall, (64,60))
    screen.blit(Grasswall, (128,60))
    screen.blit(Grasswall, (190,60))
    screen.blit(Grasswall, (253,60))
    screen.blit(Grasswall, (317,60))
    screen.blit(Grasswall, (380,60))
    screen.blit(Grasswall, (444,60))
    screen.blit(Grasswall, (0,124))
    screen.blit(Grasswall, (64,124))
    screen.blit(Grasswall, (128,124))
    screen.blit(Grasswall, (190,124))
    screen.blit(Grasswall, (253,124))
    screen.blit(Grasswall, (317,124))
    screen.blit(Grasswall, (380,124))
    screen.blit(Grasswall, (444,124))
    screen.blit(Grasswall, (0,188))
    screen.blit(Grasswall, (64,188))
    screen.blit(Grasswall, (128,188))
    screen.blit(Grasswall, (190,188))
    screen.blit(Grasswall, (253,188))
    screen.blit(Grasswall, (317,188))
    screen.blit(Grasswall, (380,188))
    screen.blit(Grasswall, (444,188))
    screen.blit(Grasswall, (0,251))
    screen.blit(Grasswall, (64,251))
    screen.blit(Grasswall, (128,251))
    screen.blit(Grasswall, (190,251))
    screen.blit(Grasswall, (253,251))
    screen.blit(Grasswall, (317,251))
    screen.blit(Grasswall, (380,251))
    screen.blit(Grasswall, (444,251))
    screen.blit(Grasswall, (0,315))
    screen.blit(Grasswall, (64,315))
    screen.blit(Grasswall, (128,315))
    screen.blit(Grasswall, (190,315))
    screen.blit(Grasswall, (253,315))
    screen.blit(Grasswall, (317,315))
    screen.blit(Grasswall, (380,315))
    screen.blit(Grasswall, (444,315))
    screen.blit(Grasswall, (0,379))
    screen.blit(Grasswall, (64,379))
    screen.blit(Grasswall, (128,379))
    screen.blit(Grasswall, (190,379))
    screen.blit(Grasswall, (253,379))
    screen.blit(Grasswall, (317,379))
    screen.blit(Grasswall, (380,379))
    screen.blit(Grasswall, (444,379))
    screen.blit(Grasswall, (0,442))
    screen.blit(Grasswall, (64,442))
    screen.blit(Grasswall, (128,442))
    screen.blit(Grasswall, (190,442))
    screen.blit(Grasswall, (253,442))
    screen.blit(Grasswall, (317,442))
    screen.blit(Grasswall, (380,442))
    screen.blit(Grasswall, (444,442))
    screen.blit(Grasswall, (0,500))
    screen.blit(Grasswall, (64,500))
    screen.blit(Grasswall, (128,500))
    screen.blit(Grasswall, (190,500))
    screen.blit(Grasswall, (253,500))
    screen.blit(Grasswall, (317,500))
    screen.blit(Grasswall, (380,500))
    screen.blit(Grasswall, (444,500))
    
    #path
    screen.blit(Dirtpath, (0,64))
    screen.blit(Dirtpath, (64,64))
    screen.blit(Dirtpath, (128,64))
    screen.blit(Dirtpath, (190,64))
    screen.blit(Dirtpath, (253,64))
    screen.blit(Dirtpath, (317,64))
    screen.blit(Dirtpath, (380,64))
    screen.blit(Dirtpath, (444,64))
    screen.blit(Dirtpath, (444,128))
    screen.blit(Dirtpath, (444,192))
    screen.blit(Dirtpath, (444,256))
    screen.blit(Dirtpath, (444,320))
    screen.blit(Dirtpath, (380,209))
    screen.blit(Dirtpath, (316,209))
    screen.blit(Dirtpath, (252,209))
    screen.blit(Dirtpath, (252,273))
    screen.blit(Dirtpath, (252,337))
    #screen.blit(Dirtpath, (444,64))
    #screen.blit(Dirtpath, (384,0))
    #screen.blit(Dirtpath, (380,64))
    #screen.blit(Dirtpath, (320,0))
    #screen.blit(Dirtpath, (383,128))
    #screen.blit(Dirtpath, (64,320))
    #screen.blit(Dirtpath, (120,320))
    #screen.blit(Dirtpath, (120,366))
    #screen.blit(Dirtpath, (120,430))
    #screen.blit(Dirtpath, (120,494))
    #screen.blit(Dirtpath, (184,430))
    #screen.blit(Dirtpath, (248,370))
    #screen.blit(Dirtpath, (248,430))
    #screen.blit(Dirtpath, (312,430))
    
    
    #bush
    #screen.blit(bush_3, (70,0))
    #screen.blit(bush_3, (70,26))
    #screen.blit(bush_3, (70,39))
    #screen.blit(bush_3, (70,60))
    #screen.blit(bush_3, (120,0))
    #screen.blit(bush_3, (120,33))
    #screen.blit(bush_3, (120,66))
    #screen.blit(bush_3, (125,196))
    #screen.blit(bush_3, (166,196))
    #screen.blit(bush_3, (125,222))
    #screen.blit(bush_3, (166,230))
    #screen.blit(bush_3, (125,240))
    #screen.blit(bush_3, (166,255))
    #screen.blit(bush_3, (125,267))
    #screen.blit(bush_3, (179,295))
    #screen.blit(bush_3, (220,320))
    #screen.blit(bush_3, (200,320))
    #screen.blit(bush_3, (183,350))
    #screen.blit(bush_3, (183,380))
    #screen.blit(bush_3, (280,320))
    #screen.blit(bush_3, (330,320))
    #screen.blit(bush_3, (400,320))
    #screen.blit(bush_3, (440,320))
    #screen.blit(bush_3, (326,320))
    #screen.blit(bush_3, (446,15))
    #screen.blit(bush_3, (444,240))
    #screen.blit(bush_3, (444,270))
    #screen.blit(bush_3, (444,280))
    #screen.blit(bush_3, (444,360))
    #screen.blit(bush_3, (444,200))
    #screen.blit(bush_3, (444,160))
    #screen.blit(bush_3, (444,130))
    #screen.blit(bush_3, (386,360))
    #screen.blit(bush_3, (386,180))
    #screen.blit(bush_3, (386,200))
    #screen.blit(bush_3, (386,227))
    #screen.blit(bush_3, (346,180))
    #screen.blit(bush_3, (346,200))
    #screen.blit(bush_3, (346,227))
    #screen.blit(bush_3, (189,189))
    #screen.blit(bush_3, (200,196))
    #screen.blit(bush_3, (229,200))
    #screen.blit(bush_3, (229,225))
    #screen.blit(bush_3, (229,240))
    #screen.blit(bush_3, (233,248))
    #screen.blit(bush_3, (209,290))
    #screen.blit(bush_3, (186,315))
    #screen.blit(bush_3, (340,360))
    #screen.blit(bush_3, (337,360))
    #screen.blit(bush_3, (314,360))
    #screen.blit(bush_3, (314,387))
    #screen.blit(bush_3, (328,387))
    #screen.blit(bush_3, (376,387))
    #screen.blit(bush_3, (444,387))
    #screen.blit(bush_3, (376,420))
    #screen.blit(bush_3, (396,420))
    #screen.blit(bush_3, (444,420))
    #screen.blit(bush_3, (376,455))
    #screen.blit(bush_3, (396,455))
    #screen.blit(bush_3, (444,455))
    #screen.blit(bush_3, (180,469))
    #screen.blit(bush_3, (230,469))
    #screen.blit(bush_3, (290,469))
    #screen.blit(bush_3, (350,469))
    #screen.blit(bush_3, (400,469))
    #screen.blit(bush_3, (444,469))
    #screen.blit(bush_3, (180,500))
    #screen.blit(bush_3, (230,500))
    #screen.blit(bush_3, (290,500))
    #screen.blit(bush_3, (350,500))
    #screen.blit(bush_3, (400,500))
    #screen.blit(bush_3, (444,500))
    #screen.blit(bush_3, (0,165))
    #screen.blit(bush_3, (0,200))
    #screen.blit(bush_3, (0,235))
    #screen.blit(bush_3, (0,260))
    #screen.blit(bush_3, (0,276))
    #screen.blit(bush_3, (0,375))
    #screen.blit(bush_3, (38,375))
    #screen.blit(bush_3, (0,404))
    #screen.blit(bush_3, (38,407))
    #screen.blit(bush_3, (0,437))
    #screen.blit(bush_3, (38,437))
    #screen.blit(bush_3, (0,468))
    #screen.blit(bush_3, (38,468))
    #screen.blit(bush_3, (0,500))
    #screen.blit(bush_3, (38,500))
    #screen.blit(bush_3, (250,0))
    #screen.blit(bush_3, (250,30))
    #screen.blit(bush_3, (250,59))
    #screen.blit(bush_3, (250,78))
    #screen.blit(bush_3, (309,59))
    #screen.blit(bush_3, (309,77))
  

#enemies
  #if enemyON:
    #screen.blit(enemy, (enemyX,enemyY))




  #stones
  if blue == False:
    screen.blit(blue_stone, (blueX,blueY))

  if grey == False:
    screen.blit(grey_stone, (greyX,greyY))

  if red == False:
    screen.blit(red_stone, (redX,redY))

  if orange == False:
    screen.blit(orange_stone,(orangeX,orangeY))
  

  if Walkcount + 1 >= 27:
    Walkcount = 0

  if left:
    screen.blit(Walkleft[Walkcount%2], (x,y))
    Walkcount += 1

  if right:
    screen.blit(Walkright[Walkcount%2], (x,y))
    Walkcount += 1

  if up:
    screen.blit(Walkupward[Walkcount%3], (x,y))
    Walkcount += 1

  if down:
    screen.blit(Walkdown[Walkcount%3], (x,y))
    Walkcount += 1
  pygame.display.update()


  

#pygame.display.update()
drawtiles =1

 #main Loop 
run = True
while run:
  pygame.time.delay(100)

  for event in pygame.event.get():
      if event.type == pygame.QUIT:
          run = False

  keys = pygame.key.get_pressed()
  if blue == True and red == True and orange == True and grey == True:
    print ("rocks got")
    if x + 64 >= redX and x <= redX + 64 and y + 64 >= redY and y <= redY + 64:
      print("go to next level")
      drawtiles = 2
  #move player_left
  if keys[pygame.K_LEFT] and x > vel:
    x -= vel
    left = True
    right = False
    up = False
    down = False

  #move player_right
  if keys[pygame.K_RIGHT] and x <  width - vel - 64:
    x += vel
    left = False
    right = True
    up = False
    down = False

  #move player up
  if keys[pygame.K_UP] and y > vel:
    y -= vel
    left = False
    right= False
    up = True
    down = False
  #move player down
  if keys[pygame.K_DOWN] and y <  height - vel - 64:
    y += vel
    left = False
    right = False
    up = False
    down = True

  if x <= orangeX + 65 and x + 64 >= orangeX -1 and y <= orangeY + 65 and y + 64 >= orangeY -1:
    orange = True

  if x <= redX + 65 and x + 64 >= redX -1 and y <= redY + 65 and y + 64 >= redY -1:
    red= True
  
  if x <= blueX + 65 and x + 64 >= blueX -1 and y <= blueY + 65 and y + 64 >= blueY -1:
    blue = True

  if x <= greyX + 65 and x + 64 >= greyX -1 and y <= greyY + 65 and y + 64 >= greyY -1:
    grey = True
   


  screen.fill((0,0,0))
  drawwindow()
pygame.quit
