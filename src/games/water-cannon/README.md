# Water Cannon

Soak the targets on the three rails before your tank runs dry.

## How to play

- Move the mouse to aim the cannon, and click to fire a shot of water.
- You have 15 shots. The game ends when the tank is empty and the last shot has landed.
- Click again on the game over screen to play another round.

## Scoring

Each target scores 10 points for every 60 px/s of speed, rounded up:

| Rail   | Speed    | Points |
| ------ | -------- | ------ |
| Top    | 180 px/s | 30     |
| Middle | 120 px/s | 20     |
| Bottom | 60 px/s  | 10     |

Your final score is saved to the carnival's score board when the game ends.

### Prizes

When the tank runs dry, the game over screen names the prize your score won, or
says `No prize this time. Try again!` when it wins none. You win the best prize
your score reaches:

| Prize       | Lowest score |
| ----------- | ------------ |
| Rubber duck | 100          |
| Teddy bear  | 200          |
| Giant panda | 350          |

Each shot soaks at most one target, so a 15-shot round scores at most 450.
Ten hits on the bottom rail win the rubber duck, ten on the middle rail win the
teddy bear, and the giant panda needs most of your shots on the faster rails.

## Options

Add `?shots=25` to the page URL to change the size of the tank, for example
`http://localhost:5173/?shots=25#/play/water-cannon`.

## Files

- `game.ts`: the game logic (`createState`, `fire`, `step`, `scoreForHit`) and the
  `waterCannon` entry, the default export the midway finds.
- `game.test.ts`: tests for the game logic.
