# Snake-Water-and-Gun-game
Snake Water and gun game in python 3.8

import random as r

def swg(comp, mine):
    if comp == 'snake' and mine == 'gun':
        return True
    elif comp == 'water' and mine == 'snake':
        return True
    elif comp == 'gun' and mine == 'water':
        return True
    elif comp == mine:
        return None
    else:
        return False

choice = ('snake', 'water', 'gun')
comp = r.randint(0, 2)
comp = choice[comp]

print()
mine = input('Enter your choice as snake, water or gun: ')
print()

win = swg(comp, mine)
print(f'You choose {mine} and the computer choose {comp}')

if win is None:
    print('Match Drawn\n')
elif win:
    print('You won\n')
else:
    print('You lose\n')
