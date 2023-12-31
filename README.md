## Word Order and Linguistic Typology 
Despite the differences among the world's languages, there are underlying similarities that have been studied by typologists such as Joseph Greensburg, who pioneered the field of linguistic typology. One noticeable pattern observed across languages from a typological perspective is word order. For instance, English as an SVO language has prenominal modifiers, prepositions that precede nouns, whereas Japanese as an SOV language has postpositions that follow the noun.

One quintessential example of a VSO language is Irish, where modifiers typically follow head nouns, while prepositions precede nouns. Please carefully study the following sentences in Irish (with English translations given):

_Ólann an bhean tae glas._
(The lady drinks green tea.)

_Tá madra ag an mbean a ólann tae._
(The lady who drinks tea has a dog.)

_Fanann an madra san fhoirgneamh glas._
(The dog stays in the green building.)

_Fanann an bhean sa chéad fhoirgneamh._
(The lady stays in the first building.)

_Tá doras ag an bhfoirgneamh._
(The building has a door.)

_Tá úinéir an fhoirgnimh glas díreach ar thaobh na láimhe clé den madra._
(The owner of the building is immediately to the left of the dog.)

_Tá an madra in aice leis an bhean._
(The dog is next to the lady.)

_Tá madra ag an bhfear a chaitheann Camel._
(The man who smokes Camel has a dog.)

_Tá comharsa ag an bhfear a bhfuil madra aige._
(The man has a neighbor who has a dog.)


## The Infamous Riddle That Only 2% of the Population Can Solve
Now that you've familiarized yourself with the language, here's a logical puzzle written in Irish that needs your help solving:

| House 1     | House 2     | House 3     | House 4     | House 5     |
| ----------- | ----------- | ----------- | ----------- | ----------- |

There are five buildings of different colors (_dearg_ “red”, _glas_ “green”, _bán_ “white”, _buí_ “yellow”, _gorm_ “blue”) next to each other at a resort, each owned by a man of a unique occupation (_file_ “poet”, _múinteoir_ “teacher”, _péintéir_ “painter”, _feirmeoir_ “farmer”, _baincéir_ “banker”). During this time of year, all five owners come to stay in the building they own for vacation. Each owner has an exclusive favorite drink (_tae_ “tea”, _caife_ “coffee”, _bainne_ “milk”, _beoir_ “beer”, _uisce_ “water”), a distinct favorite brand of cigarettes (Pall Mars, Dunhill, Blends, Blue Master, Prince), and has a specific pet species (_madra_ “dog”, _cat_ “cat”, _capall_ “horse”, _éan_ “bird”, _iasc_ “fish”). The clues listed below are written in Irish. Can you complete the grid to solve the puzzle, and answer the question **"Who has a fish as a pet?"**

- _Fanann an file san fhoirgneamh dearg._

- _Tá madra ag an múinteoir._

- _Ólann an péintéir tae._

- _Tá an foirgneamh glas díreach ar an taobh clé den fhoirgneamh bán_

- _Ólann úinéir an fhoirgnimh glas caife._

- _Tá éan ag an úinéir a chaitheann Pall Mars._

- _Caitheann úinéir an fhoirgnimh buí Dunhill._

- _Ólann úinéir an fhoirgnimh ionaid bainne._ (_ionaid_ “center”)

- _Fanann an feirmeoir sa chéad fhoirgneamh._

- _Tá comharsa ag an úinéir a chaitheann Blends a bhfuil cat aige._

- _Tá comharsa ag úinéir an fhoirgnimh buí a bhfuil capall aige._

- _Ólann an t-úinéir a chaitheann Blue Master beoir._

- _Caitheann an baincéir Prince._

- _Tá an feirmeoir in aice leis an bhfoirgneamh gorm._

- _Tá comharsa ag an úinéir a chaitheann Blends a ólann uisce_

## Solution
From the example sentences given in the [first section](#word-order-and-linguistic-typology), the puzzle clues can be translated into English as follows (I did my best on the glossing part, but with limited data, some I am uncertain of)
<img src="https://github.com/amandalin047/cognitive-science-language/blob/master/glossing-1.png" alt="Glossing-1" width="1000">
<img src="https://github.com/amandalin047/cognitive-science-language/blob/master/glossing-2.png" alt="Glossing-2" width="1000">

For better readability, the English translations of the clues are listed below in boldface:
- **The poet stays in the red building**
- **The teacher has a dog**
- **The painter drinks tea**
- **The green building is immediately to the left of the white building**
- **The owner of the green building drinks coffee**
- **The owner who smokes Pall Mars has a bird**
- **The owner of the yellow building smokes Dunhill**
- **The owner of the center building drinks milk**
- **The farmer stays in the first building**
- **The owner who smokes Blends has a neighbor who has a cat**
- **The owner of the yelllow building has a neighbor who has a horse**
- **The owner who smokes Blue Master drinks beer**
- **The banker smokes Prince**
- **The farmer is next to the blue building**
- **The owner who smokes Blends has a neighbor who drinks water**

I prefer to convert the clues into a more "concise" form where each of the five _attributes_ in each _attribute category_ (i.e., occupation, building color, drink, cigarette brand, pet) is assigned a number from 1 to 5 indicating the building it belongs to:
```
poet = red
teacher = dog
painter = tea
white - green = 1
green = coffee
pallmars = bird
yellow = dunhill
milk = 3
farmer = 1
abs(cat - blends) = 1
abs(horse - yellow) = 1
bluemaster = beer
banker = prince
abs(farmer - blue) = 1
abs(blends - water) = 1
```
from which is easy to see that
```
blue = 2
(green, white) = (3,4) or (4,5)
```
where if `(green, white) = (3,4)`, then `coffee = green = 3 = milk`, a contradiction. Therefore
```
green = 4, white = 5
```
As such,
```
(yellow, red) = (1,3) or (3,1)
```
where if `(yellow, red) = (3,1)`, then `poet = 1 = farmer`, a contradiction. So
```
yellow = 1, red = 3
```
Thus,
```
horse = 2
poet = 3
dunhill = 1
```
and
```
cat = 1 or fish = 1
```
since
```
1 = farmer ≠ teacher = dog
```
Also `water = 1` since
```
milk = 3, coffee = 4,
1 = dunhill ≠ bluemaster = beer.x, 
1 = farmer ≠ painter = tea.x
```
From this we deduce that
```
blends = 2
beer = bluemaster = 5
```
since
```
beer = bluemaster ≠ 1 = dunhill
                  ≠ 2 = blends
                  ≠ 3 = milk
                  ≠ 4 = coffee
```
And that
```
banker = prince = 4
```
for if `banker = 3`, then `banker = 3 = poet`, a contradiction.
Further, 
```
bird = pallmars = 3
```
so
```
cat = 1
```
since `abs(cat - blends) = 1` and `cat ≠ 3 = bird`
Finally, we have
```
painter = tea = 2
dog = teacher = 5
```
which implies that
```
fish.x = 4
```

This logical puzzle is actually a variant of [Einstein's Puzzle](https://en.wikipedia.org/wiki/Zebra_Puzzle). From the above reasoning, the full solution can be tabulated as follows

| House 1     | House 2     | House 3     | House 4     | House 5     |
| ----------- | ----------- | ----------- | ----------- | ----------- |
| farmer      | painter     | poet        | banker      | teacher     |
| yellow      | blue        | red         | green       | white       |
| water       | tea         | milk        | coffee      | beer        |
| Dunhill     | Blends      | Pall Mars   | Prince      | Blue Matser |
| cat         | horse       | bird        | fish        | dog         |




