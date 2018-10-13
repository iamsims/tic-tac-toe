class Board:
    player1 = 1
    player2 = 2
    player1key='O'
    player2key='X'

    def __init__(self):
        self.board_mat = [' ',' ',' ',' ',' ',' ',' ',' ',' ']
        print (' TIc -TAc-TOe')
        print(1, '|', 2, '|', 3)
        print(4, '|', 5, '|', 6)
        print(7, '|', 8, '|', 9)
        print('\n')
        print('You can choose a number mainfile the given matrix to place your key')
        print('\n')


    def reset (self):
        self.board_mat = [' ',' ',' ',' ',' ',' ',' ',' ',' ']



    def display(self):
        print(self.board_mat[0], '|', self.board_mat[1], '|', self.board_mat[2])
        print(self.board_mat[3], '|', self.board_mat[4], '|', self.board_mat[5])
        print(self.board_mat[6], '|', self.board_mat[7], '|', self.board_mat[8])
        print('\n')




    def update(self, player, chosen_spot):
        if player == self.player1 and self.board_mat[int(chosen_spot) - 1] == ' ':
            self.board_mat[int(chosen_spot) - 1] = 'O'
            return 0

        if player == self.player2 and self.board_mat[int(chosen_spot) - 1] == ' ':
            self.board_mat[int(chosen_spot) - 1] = 'X'
            return 0
        else:
            return 1

    def get_input(self,player):
        while True:
            try:
                userInput = input('choose your your spot')
                val = int(userInput)
            except ValueError:
                print("That's not an int!")
                continue
            if val not in range(0,10):
                print('enter a value between 0-9')
            elif not self.update(player,userInput):
                print('choose an empty spot')
                break 


    def check(self,playerkey):
        if self.board_mat[0]==self.board_mat[1]==self.board_mat[2]==playerkey or\
            self.board_mat[3]==self.board_mat[4]==self.board_mat[5]==playerkey or\
            self.board_mat[3]==self.board_mat[4]==self.board_mat[5]==playerkey or\
            self.board_mat[6]==self.board_mat[7]==self.board_mat[8]==playerkey or\
            self.board_mat[0]==self.board_mat[3]==self.board_mat[6]==playerkey or\
            self.board_mat[1]==self.board_mat[4]==self.board_mat[7]==playerkey or\
            self.board_mat[2]==self.board_mat[5]==self.board_mat[8]==playerkey or\
            self.board_mat[0]==self.board_mat[4]==self.board_mat[8]==playerkey or\
            self.board_mat[2]==self.board_mat[4]==self.board_mat[6]==playerkey:
            return 1
        else: return 0



def game (game_Board):
    while 1:
        playgame = input('Would  you like  to play a game (Y/N)?').upper()
        if playgame=='Y':
            for i in range(0,9):
                if i%2==0:
                    game_Board.get_input(game_Board.player1)
                    game_Board.display()
                    if game_Board.check(game_Board.player1key):
                        print('Player1 wins')
                        break



                else:
                    game_Board.get_input(game_Board.player2)
                    game_Board.display()
                    if game_Board.check(game_Board.player2key):
                        print('player2 wins')
                        break

                if i == 8:
                    print('DRAW')


        elif playgame == 'N':
            quit()

        else:print ('Enter a Y or N')

        game_Board.reset()



game_Board=Board()  #prepares the board
game (game_Board)   #initiates the game using the board






