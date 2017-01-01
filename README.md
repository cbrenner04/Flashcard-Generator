# Flashcard-Generator

NU Coding BootCamp Homework 9

## Running the app

Run and follow the instructions

```
node app.js
```

The first prompt will ask you what you would like to do. If you choose to
`add-flashcard`, you will be prompted to pick which type of flashcard you would
like to create. The options will be `basic-flashcard` or `cloze-flashcard`. More
information about these types below. Once you've created the flashcard it will
be appended to the `log.txt` file. You will then be asked if you would like to
`create-new-flashcard`, `show-all-cards`, `nothing`. Nothing will end the app,
`create-new-flashcard` will restart the flashcard creation process described
above.

If you choose to `show-all-cards`, each of the flashcards will be displayed to
you as a question (`front`) of the card. Your response will be compared to the
correct response (`back`) of the card. You will be shown each card until they
are exhausted. When they are exhausted the app will quit.

### Basic Flashcard

A basic flashcard has a `front` and a `back`. A basic flashcard is created
through a constructor `BasicFlashcard` which takes two arguments: `front` and
`back`, respectively. `BasicFlashcard` has a `create` function which uses `fs`
to append the flashcard to the `log.txt` file.

Simply enough, to create a new basic flashcard:

```
var newBasic = new BasicFlashcard('What is your favorite color?`, 'Blue');
newBasic.create();
```

### Cloze Flashcard

A cloze flashcard has a piece of text removed. A cloze flashcard is created
through a constructor `ClozeFlashcard` which takes two arguments: `text` and
`cloze`, respectively. The `ClozeFlashcard` has property `clozeDeleted` which
takes the `text` and replaces the `cloze` portion with `_____`.`ClozeFlashcard`
also has a `create` function which uses `fs` to append the flashcard to the
`log.txt` file.

Again, pretty simply, to create a new cloze flashcard:

```
var newCloze = new ClozeFlashcard('My favorite color is blue.`, 'blue');
newBasic.create();
```
