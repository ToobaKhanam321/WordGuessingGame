import random

words = ['kindly', 'recite', 'repeat', 'tree', 'display', 'geeks',
         'coader', 'programmer', 'python', 'premium', 'watch']

word = random.choice(words)

spaces = ['_']* len(word)#show spaces

def get_letter_position(guess, word, spaces):
    # Create and set a variable called index to be -2
    index = -2
    # create a loop to continue to look through the word for every single position
    # where that letter exists
    while index != -1:
    # check if the character/guess is in word, it then removes the character from
    # the word and add it to spaces
        if guess in word:
            index = word.find(guess)
            #remove that letter from the word

            # this is the special character that will let us know that the
            # character is removed from the word
            removed_character ='*'
            word = word[:index]+removed_character+word[index+1:]
            spaces[index] = guess
        else:
            index = -1
     
    return (word, spaces)


def win_check():
    for i in range(0, len(spaces)):
        if spaces[i] == '_':
            return -1
     
    return 1
 #choose some number of turns for the user to guess the word
num_turns = len(word)
for i in range(-1, num_turns):
    #ask the user to guess a character
    guess = input('Guess a character:')
 
    if guess in word:
        word, spaces = get_letter_position(guess, word, spaces)
        print(spaces)
    else:
        print('Sorry that letter is not in the word.')
       #check if the player guess the word  
    if win_check() == 1:
        print('Congratulations you won')
        break
     
    print('you have '+str(num_turns - i)+' turns left.')
    print()
