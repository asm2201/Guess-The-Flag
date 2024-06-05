# Guess-The-Flag
A game to guess the flag of different countries.

## Variables Used
1. countries = ["Estonia", "France", "Germany", "Ireland", "Italy", "Nigeria", "Poland", "Spain", "UK", "Ukraine"]
2. correctAnswer : generates a random integer between 0 and 2 (there are 3 flags to be guessed from)
3. showingScore : toggles from true and false to display the alert message
4. scoreTitle : Tells whether the guess was correct or not

## New Concepts Learnt
1. Alert
2. Buttons with labels as images
3. radial gradiant with custom declared colours
4. .foregroundStyle(.secondary)
5. Enclosing an entire VStack with card effect using .background(.regularMaterial)

## Flow Of Program
1. Declare the background of this app within ZStack. 
2. Create a Nested VStack to store the Title of the app
3. Create another nested VStack within the above VStack for storing the card which holds the flags of the country to be tapped and guessed
4. How will the flags be generated and revised after each guess for next round? <br/>
   4.1  At the beginning of each round a correctAnswer number will be generated from 0...2 <br/>
   4.2  The list is shuffled and countries[correctAnswer] is picked as the country to be guessed <br/>
   4.3  Declare a ForEach loop which will run from  0..<3 <br/>
   4.4  For each iteration i.e 0,1,2, a button will be generated <br/>
   4.5  The buttons will have images of countries[0], countries[1], countries[2] <br/>
   4.6  Remember that there are 12 countries which are shuffled after each round and top 3 countries are selected for the round <br/>
   4.7  when the user taps a button, it is checked if the number and correctAnswer matches using flagTapped() func. <br/>
   4.8  After the flagTapped function terminates, an alert is generated declaring whether the guess was right or not. <br/>
   4.9  this alert in turn calls askQuestion function which shuffles the list of countries and generates a new value for correctAnswer variable. <br/>
