import random

f = open("/usr/share/dict/words", "r")
content = f.read()
f.close()
words = content.lower().split("\n")

random_word = random.choice(words) 

#random_word = "apple"

num_letters = len(random_word)
anon_word = num_letters * "#"


print("Let's play some hangman")


print(anon_word)
print("There are {a} letters in this word".format(a=num_letters))

word_letters = list(random_word)

error = 0


def hangman(wordword, num_error):
    a = input("Guess the letter: ")
    if a in word_letters:
        print("yes!")
        print(a, " is in the word")
        empty_list = []
        for i, j in enumerate(word_letters):
            if j == a:
                empty_list.append(i)
        #print(empty_list)
        anon_list = list(wordword)
        for number in empty_list:
            anon_list[number] = a
        anon_word2 = "".join(anon_list)
        print(anon_word2)
        error = num_error
        if "#" in anon_word2:
            hangman(anon_word2, error)
        else:
            print("You have made it! Yeah!")


    else:
        print("no")
        error = num_error + 1
        tries_left = 10 - error
        print("you have ", tries_left, " tries left.")
        anon_list = list(wordword)
        anon_word2 = "".join(anon_list)
        print(anon_word2)
        if tries_left > 0:
            hangman(anon_word2, error)
        else:
            print("G A M E  O V E R")
            print("the correct word was: ", random_word)
       

hangman(anon_word, 0)
