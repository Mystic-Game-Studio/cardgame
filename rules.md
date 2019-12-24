# cardgame

cardgame is intended to be a game similar to Yu-Gi-Oh. Why not just play
Yu-Gi-Oh then? Well, Konami has fucked up balancing the game and kept adding
more and more stuff. They've probably done this in order to keep the game
moving and therefore keep the game interesting. In my opinion, the difference
in strength between the new and the old cards is very big. Therefore, I'll
try making a more simple game that still feels dynamic enough. The game will
feel very much like Yu-Gi-Oh, borrowing a lot of it's vocabulary and even
mechanics.

## Rules

### Exceptions

Certain cards may allow working around certain rules. The description of each
card always wins over the general rule declerations.

### The deck

The cards used by a player are called a deck. A valid deck is any deck that
has exactly 35 cards. Larger decks aren't allowed, since those
wouldn't allow for predictable strategies, as even with 30 cards the chances
of being able to execute certain strategies isn't particularly high.

Each deck needs to be well shuffled. Preferably let your enemy shuffle your
deck. In the digital version of the game, this process is automated.

Duplicates of cards are allowed. You can have each card up to 3 times.

### Turns

The game is turn based, allowing players to take as much time as they
please, unless specified otherwise. Each turn is seperated into phases.
The phases define which actions can be taken at what point.

The phases are the following:

#### Drawing

The drawing phase is the start of each turn, forcing you to draw a card from
your deck. If your deck is empty, skip to the next phase.

#### Preperation

The play phase is where you can decide to lay down cards. You can lay down
as many utility cards as you please you can also change the position of
creatures. The position of a creature can't be changed twice in the same turn.

#### Fighting

In this face, all of your creatures in attack position may attack your enemies
creatures or the enemies lifepoints directly in case there are no creatures.

#### Second Preperation

This phase has the same rules as the first preperation phase.

#### End

The end phase can be used as an event for card effects, but usually doesn't
require or allow any player interaction.

### Hand

Whenever you draw any card, it will be added to your hand. All cards in your
hand are not visible to the enemy. At the start of the game, both players have
to draw 5 cards. In each of your turns drawing phase, you have to draw another
card. If the amount of cards in your hand exceeds 8 at the end of the turn, you
have to throw way the excess cards. You can freely decide which cards to throw
away. The thrown away cards end up in the graveyard.

In the player can exchange up to two hand cards with other random cards from
the players deck.

### Who begins

You either have to mutually agree who wins or use a luck-based decision like
tossing a coin or throwing a dice. Whoever wins, can decide who starts.

### Lifepoints

Each player starts with 400 lifepoints. The lifepoint limit is at 800.

### Winning

In order to win, you have to drain your enemies lifepoints down to 0. If a
player isn't able to do any moves anymore, he automatically loses the game.
In case both players aren't able to do anything anymore, the game ends in a
tie. It doesn't matter which player has more lifepoints in case of a tie
situation.

### Mana

Certain actions require you to spend mana. You start each game with 3 mana and
gain an additional 3 mana in each of your turns. Mana costs range from 1 to 10.
Your maximum mana pool size is 12. Mana can also be gained by card effects.

### Placing cards

Each card can only be placed into a specific zone defined by the card-type.
After a card has been placed, it can't change into a different slot anymore.
A card can't be picked up after it has been placed.

### Card Types

There are four card types in total. Each of these types has unique
characteristics only allowing them to be played in a certain way.

#### Creatures

Creatures are the ones doing the fighting. They can be used to attack or to
defend your lifepoints. Each creature defines it's mana cost. You can spawn as
many creatures per turn as you mana pool allows. A creature can either be
placed in face-up or face-down position. A creature can only attack if it is
in face-up position. A creature can't attack in the same turn that you flipped
it into face-up position or placed it. If there's at least one creature on your
field, your enemy can't attack your lifepoints. If a face-down creature is
attacked, then you have to flip it.

A creature only has one stat, called `Power`. Power is it's attack strength,
defense strength and lifepoints at once. If two creatures fight, both will
lose power in the amount of the enemy creatures power. If the power drops to
0, the creatures die.

If a creature directly attacks the player, it will not lose any power. Only
the player will receive damage.

Each creature card can belong into groups. Such a group may for example be one
of the following:

* Fighter
* Mage
* Fairy
* Beast
* ...

A card can have more than one group. Groups don't affect the strength of the
card, but may play a role when effects are activated, as certain effects may
only affect cards of certain groups.

Each creature card has an effect. Each effect can be used once per round, unless
specified otherwise. Effects can be used directly after a creature has been
placed. In order to be able to activate an effect, the creature has to be in
face-up position.

Equipment cards get destroyed if a creature is moved back into face-down
position.

All creatures have to be put into the creature card zone. The creature card zone
has 5 slots. Creatures can't attack in the turn they've been placed in.

The power of a creature is always a multiple of 10.

#### Traps

Trapcards can be played in advance in order to react to events triggered by
your enemy. All trapcards must be activated manually and can only be used
in the phase defined on the card or always in case no specific phase was
defined. There is no cost to using trap cards. Trap cards can only be
activated one turn after they've been placed.

Trap cards need to be placed in the utility zone. The utility zone has 5
slots.

#### Spells

Spell cards are similar to trap cards. They can also be placed in the
utility zone. However, Spellcards can only be activated in your turn and
needn't be placed in advanced. They can be activated directly from your hand.
However, placing them is still possible in order to allow scaring your enemy
into not attacking. Spell cards can only be activated directly from your hand
in case you have a free slot in your utility zone. Activating a spell card
requires you to spend one mana.

#### Equipment

Equipment cards can be equipped on a creature directly. The creatures will be
stats or abilities will be changed according to the effect of the equipment.
Equipment can be applied to both your own creatures and the enemies creatures.
Each equipcard is placed below the creature it is equipped on. Each creature
can be equipped with up to 2 equipment cards.

If the creature who is equipped with an equipment card gets destroyed, the
equipment card gets destroyed as well.

Equipment cards may have durability. Durability can either be time or usage
based.

