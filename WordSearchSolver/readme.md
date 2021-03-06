# Word Search Solver

(Adapted from http://rubyquiz.com/quiz107.html by Daniel Finnie)

A word search, word find, word seek, word sleuth or mystery word puzzle is a word game that consists of the letters of words placed in a grid, which usually has a rectangular or square shape. The objective of this puzzle is to find and mark all the words hidden inside the box. The words may be placed horizontally, vertically, or diagonally. Often a list of the hidden words is provided, but more challenging puzzles may let the player figure them out. Many word search puzzles have a theme to which all the hidden words are related. The puzzles have, like crosswords and arrowords, been very popular in the United Kingdom, and - also in common with these latter puzzles - have had complete magazines devoted to them.

Word searches are commonly found in daily newspapers and puzzle books. Some teachers use them as educational tools for children, the benefit being that young minds can learn new words and their spellings by intensively searching for them, letter by letter, in the puzzle.

# The Kata

Write a program to find all the words in a Word Search, entered in plain text.

# Puzzle

Input:

    U E W R T R B H C D
    C X G Z U W R Y E R
    R O C K S B A U C U
    S F K F M T Y S G E
    Y S O O U N M Z I M
    T C G P R T I D A N
    H Z G H Q G W T U V
    H Q M N D X Z B S T
    N T C L A T N B C E
    Y B U R P Z U X M S

    Contains: RUBY, DAN, ROCKS, MATZ

Expected output:

    + + + R + + + + + +
    + + + + U + + + + +
    R O C K S B + + + +
    + + + + + + Y + + +
    + + + + + + + + + M
    + + + + + + + D A N
    + + + + + + + T + +
    + + + + + + Z + + +
    + + + + + + + + + +
    Y B U R + + + + + +


# Stretch Goal

Too easy? How about generating a puzzle.

Input: 

    Words: THIS, PUZZLE, ROCKS, SOCKS

OUTPUT:

    Puzzle in the above form.

Accept:

- Words must be placed forwards
- Words must be placed in reverse
- Words must be placed in forwards diagonals
- Words must be placed in backwards diagonals
- Words may overlap


# Notes on Strategies

(Thanks Wikipedia! https://en.wikipedia.org/wiki/Word_search)

A common strategy for finding all the words is to go through the puzzle left to right (or vice versa) and look for the first letter of the word (if a word list is provided). After finding the letter, one should look at the eight surrounding letters to see whether the next letter of the word is there. One can then continue this method until the entire word is found.

Another strategy is to look for 'outstanding' letters within the word one is searching for (if a word list is provided). Since most word searches use capital letters, it is easiest to spot the letters that stand out from others. These letters are Q, O, U, X, and Z.[citation needed]

Lastly, the strategy of looking for double letters in the word being searched for (if a word list is provided) proves helpful, because it is easier to spot two identical side-by-side letters among a large grid of random letters.

If a word list is not provided, a way to find words is to go row by row. First, all the horizontal rows should be read both backwards and forwards, then the vertical, and so on.

Sometimes the puzzle itself will help. The puzzles generated by a computer tend to put words in patterns. Furthermore, the bigger the words and the more words, the easier they are to spot. In some computer-generated puzzles, if the person solving the puzzle sees one word, all they have to do to find more is to look in adjacent rows, columns, or diagonals. The puzzle might use every row, column, or diagonal—or just every other row, column, or diagonal.