# GamesLab

![cut](https://user-images.githubusercontent.com/7005867/168170246-a584b7e1-93bc-4291-808e-18f23e190236.gif)

### Running the game

##### Via make target

```sh
make run
```

##### Via maven

```sh
mvn install -f AsteroidsEntityFramework/pom.xml
mvn package -f AsteroidsEntityFramework/Core/pom.xml
java -jar bin/GameLab.jar
```

### Implemented features

- [x] Document the provided `IGamePluginService`, `IEntityProcessorService` and `IPostEntityProcessorService` interfaces.
- [x] Implement the `Player` and `Enemy` as a separate project using the provided `IGamePluginService`,
      `IEntityProcessorService` and `IPostEntityProcessorService` interfaces.
- [x] Implement randomly moving Asteroids using the `IGamePluginService` and `IEntityProcessorService` interfaces.
- [x] Implement a simple collision detection system based on Pythagoras and the provided `IPostEntityProcessorService` interface.
- [x] Identify missing components.
  - Added a life-processer that removes dead entities from the game.
- [x] Ships that collide with asteroids should be destroyed.
  - A player has 100 health, but 3 lives. They lose 100 health when colliding with an asteroid (so life becomes 2).
- [x] When fired upon Asteroids should split into two smaller Asteroids and when small enough they should be destroyed.
- [x] Last, the player ship and enemy-ships should be destroyed when hit by each others bullets a certain number of times.
- [ ] Specify at contract level (operation contracts in unified process), the required and provided interfaces based on
      identified components. That is, specify pre and post-conditions for each operation of the component.

#### Extra implemented features

- Random enemy spawn locations
- Player has 3 lives (loses 1 life when hit)
- Weapon cooldown based on game-time
