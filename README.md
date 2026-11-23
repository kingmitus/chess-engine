# chess engine
https://chessprogramming.org/Getting_Started as my first resource

step 1: board representation 
    gonna use a bitboard approach: 
        64 bit word for each peice type where one bit assosicates occupancy
numver scheme: 0 - 63

1. square = 8(rank) + file 
2. file = square mod 8 
3. rank = [square/8]

a1 = 0 
b1 = 1
h1 = 7
a2 = 8
e4 = 28
h8 = 63

off set table:
north + 8
south - 8
east + 1
west + 1
northeast + 9
northwest + 7
southeast - 7 
southwest - 9

detecting off the board rule: 
    i think making this based off the offset table and making sure the board position is
    in line with it based on a basic calculation to check if move is in bounds
peice encoding and helper operations:
    hard encoding maybe? 