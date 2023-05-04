Download Link: https://assignmentchef.com/product/solved-csc135-assignment-3
<br>
Write the following as Prolog rules:

————————————————————————-

1. Implement a rule “pingPongMaster”.Someone is a “pingPongMaster” if they have won at least TWO games by a high margin.Ping pong games are played to 11 points, and a high margin is 11 to 5, or worse.Assume that the only types of facts available are:

“game” facts of the form game(n,a,b,s,t),meaning that player “a” defeated player “b” by a score of “s” to “t”.The field “n” is a game ID number that is unique for each game.Note that the winner is not necessarily listed first.

For example:game(893, terry, rene, 11, 2) means that in game #893, terry defeated rene 11 to 2.game(894, marge, larry, 11, 8) means that in game #894, marge defeated larry 11 to 8.game(721, marge, terry, 5, 11) means that in game #721, terry defeated marge 11 to 5.Note that game numbers 893 and 721 are high margin games.

In the presence of a set of “game” facts as described above,pingPongMaster(terry) would return true.You can assume that all game scores are integers.

2. Implement a rule “getsMailBefore”, that determines if a particular person willdefinitely receive their mail before another particular person.Assume that the only types of facts available are of the form:

deliver(carrier, thisPerson, nextPerson).

The “carrier” field is the name of a mail carrier.The “thisPerson” field is the name of a person on that carrier’s route.The “nextPerson” field is the name of the person who gets their mail immediately after “thisPerson”.For example:

deliver(fred, terry, emil).deliver(fred, emil, sally).deliver(fred, sally, cory).deliver(fred, cory, art).deliver(diane, steve, ali).deliver(diane, ali, manuel).deliver(diane, manuel, rick).

the above facts describe fred’s mail route, which starts with terry, then emil, sally, cory, and art.they also describe diane’s mail route, which starts with steve, then ali, manuel, and rick.

In the presence of the above facts:getsMailBefore(emil, art) should return true.getsMailBefore(ali, manuel) should return true.getsMailBefore(ali, rick) should return true.getsMailBefore(sally, terry) should return false.getsMailBefore(terry, rick) should return false (different mail carriers, so we don’t know the answer).

You can assume that a given mail recipient’s name is listed only once in the facts.

3. Implement a rule: “count_occur”, which takes a list of lists, and counts the number that aren’t empty.For example:count_occur([[5,2],[6],[],[7,8],[7,0,3],[]], M).should return M=4,because the list [[5,2],[6],[],[7,8],[7,0,3],[]] contains 4 non-empty lists.You can assume that the input list contains only lists.

4. Implement “listsMax” from Homework #2 as a Prolog rule.For example, the query: listsMax([2,5,11,25,9], [2,9,10,20,12], M).should result in Prolog’s response: M = [2,9,11,25,12].You only need to handle lists that contain integers.

5. Implement “cycler” from Homework #2 as a Prolog rule.For example, the query: cycler([3,8,2,6,4,5,5], 28, M).should result in Prolog’s response: M = 245.

6. Implement a rule “somefiles” that solves the following cryptarithmeticmultiplication problem:

I * M MO I I E S———M M I I S* * * * ** * * * ** * * * ** * * * *—————–S O M E F I L E S

Each of the 7 letters (S,O,M,E,F,I,L) stands for a different digit.Positions marked with an asterisk (*) can stand for any digit.The aim is to find a substitution of digits for the letterssuch that the above stated product is arithmetically correct.

It should be possible to query your solution in this manner:

?- somefiles(S,O,M,E,F,I,L).

Your solution should then produce all of the combinations ofthe digits that satisfy the multiplication problem above. Don’t getconfused between the letter “O” and the number “0” (zero).

Make sure you never let S=M, or E=F, etc… all of the distinctletters (S, O, M, E, F, I, and L) have to stand for distinct digits.

Don’t be surprised if it takes your computer a while to solvethis problem. It took Dr. Gordon’s desktop computer about a minuteto complete its answer using his solution… and he has a prettyfast computer.

Use generate-and-test!

————————————————————————-

Submit your solutions in a single file.Clearly separate your solutions with a commented line of hyphens, as for homework #2.