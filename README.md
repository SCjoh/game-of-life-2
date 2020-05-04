 # Utvid spillet ditt!
```template
namespace myTiles {
    //% blockIdentity=images._tile
    export const tile0 = img`
        . . . . . . . . . . . . . . . .
        . . . . . . . . . . . . . . . .
        . . . . . . . . . . . . . . . .
        . . . . . . . . . . . . . . . .
        . . . . . . . . . . . . . . . .
        . . . . . . . . . . . . . . . .
        . . . . . . . . . . . . . . . .
        . . . . . . . . . . . . . . . .
        . . . . . . . . . . . . . . . .
        . . . . . . . . . . . . . . . .
        . . . . . . . . . . . . . . . .
        . . . . . . . . . . . . . . . .
        . . . . . . . . . . . . . . . .
        . . . . . . . . . . . . . . . .
        . . . . . . . . . . . . . . . .
        . . . . . . . . . . . . . . . .
    `
    //% blockIdentity=images._tile
    export const tile1 = img`
        8 8 8 8 8 8 8 8 8 8 8 8 8 8 8 8
        8 8 8 8 8 8 8 8 8 8 8 8 8 8 8 8
        8 8 8 8 8 8 f 8 8 8 8 8 8 8 8 8
        8 f 8 8 8 8 f 8 8 f f 8 8 8 8 8
        8 f f f f f 8 f f f f f 8 8 f 8
        8 8 8 8 8 8 8 8 8 8 8 f f f 8 8
        8 8 8 8 8 8 8 8 8 8 8 8 8 8 8 8
        8 8 8 8 8 8 8 8 8 8 8 8 8 8 8 8
        8 8 8 8 8 8 8 8 8 8 8 8 8 8 8 8
        8 8 8 8 8 8 8 8 8 8 8 8 8 8 8 8
        8 8 8 f f f f f f 8 8 f f f f 8
        8 8 8 8 8 8 8 8 8 f f 8 8 8 8 8
        8 8 8 8 8 8 8 8 8 8 8 8 8 8 8 8
        8 8 8 8 8 8 8 8 8 8 8 8 8 8 8 8
        8 8 8 8 8 8 8 8 8 8 8 8 8 8 8 8
        8 8 8 8 8 8 8 8 8 8 8 8 8 8 8 8
    `
}
sprites.onOverlap(SpriteKind.Player, SpriteKind.Food, function (sprite, otherSprite) {
    otherSprite.destroy()
    info.changeScoreBy(1)
})
info.onCountdownEnd(function () {
    if (info.score() < 20) {
        game.over(false)
    } else {
        game.over(true)
    }
})
let energi: Sprite = null
tiles.setTilemap(tiles.createTilemap(
            hex`290028000000000000000000000000000000000000000000000000000000000000000000000000000000000000000102020202020202020202030000000000000000110a0a0a0a0a0a0a0a0a0a0a0a0a0a0a0a0a10000004090909090909090909090600000000000000000c12121212121212121212121212121212120f000004090909090909090909090600000000000000000c12121212121212121212121212121212120f000004090909090909090909090600000000000000000c12121212121212121212121212121212120f000004090909090909090909090600000000000000000c12121212121212121212121212121212120f000004090909090909090909090600000000000000000c12121212121212121212121212121212120f000004090909090909090909090600000000000000000c12121212121212121212121212121212120f000004090909090909090909090600000000000000000c12121212121212121212121212121212120f000004090909090909090909090600000000000000000c12121212121212121212121212121212120f0000040909090909090909090909020202020a0a0a0a1212121212121212121212121212121212120f0000040909090909090909090909050505050b0b0b0b1212121212121212121212121212121212120f000004090909090909090909090600000000000000000c12121212121212121212121212121212120f000004090909090909090909090600000000000000000c12121212121212121212121212121212120f000004090909090909090909090600000000000000000c12121212121212121212121212121212120f000004090909090909090909090600000000000000000c12121212121212121212121212121212120f000004090909090909090909090600000000000000000c12121212121212121212121212121212120f000004090909090909090909090600000000000000000c12121212121212121212121212121212120f000004090909090909090909090600000000000000000c12121212121212121212121212121212120f000004090909090909090909090600000000000000000c12121212121212121212121212121212120f000004090909090909090909090600000000000000000c12121212121212121212121212121212120f000004090909090909090909090600000000000000000c12121212121212121212121212121212120f000004090909090909090909090600000000000000000c12121212121212121212121212121212120f000004090909090909090909090600000000000000000c12121212121212121212121212121212120f000007050505050505050505050800000000000000000d0b0b0b0b0b0b0b0b0b0b0b0b0b0b0b0b0b0e00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000`,
            img`
                2 2 2 2 2 2 2 2 2 2 2 2 2 2 . . . . . . 2 2 2 2 2 2 2 2 2 2 2 2 2 2 2 2 2 2 2 2 2
                2 . . . . . . . . . . . . 2 . . . . . . 2 . . . . . . . . . . . . . . . . . . . 2
                2 . . . . . . . . . . . . 2 . . . . . . 2 . . . . . . . . . . . . . . . . . . . 2
                2 . . . . . . . . . . . . 2 . . . . . . 2 . . . . . . . . . . . . . . . . . . . 2
                2 . . . . . . . . . . . . 2 . . . . . . 2 . . . . . . . . . . . . . . . . . . . 2
                2 . . . . . . . . . . . . 2 . . . . . . 2 . . . . . . . . . . . . . . . . . . . 2
                2 . . . . . . . . . . . . 2 . . . . . . 2 . . . . . . . . . . . . . . . . . . . 2
                2 . . . . . . . . . . . . 2 . . . . . . 2 . . . . . . . . . . . . . . . . . . . 2
                2 . . . . . . . . . . . . 2 . . . . . . 2 . . . . . . . . . . . . . . . . . . . 2
                2 . . . . . . . . . . . . 2 2 2 2 2 2 2 2 . . . . . . . . . . . . . . . . . . . 2
                2 . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 2
                2 . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 2
                2 . . . . . . . . . . . . 2 2 2 2 2 2 2 2 . . . . . . . . . . . . . . . . . . . 2
                2 . . . . . . . . . . . . 2 . . . . . . 2 . . . . . . . . . . . . . . . . . . . 2
                2 . . . . . . . . . . . . 2 . . . . . . 2 . . . . . . . . . . . . . . . . . . . 2
                2 . . . . . . . . . . . . 2 . . . . . . 2 . . . . . . . . . . . . . . . . . . . 2
                2 . . . . . . . . . . . . 2 . . . . . . 2 . . . . . . . . . . . . . . . . . . . 2
                2 . . . . . . . . . . . . 2 . . . . . . 2 . . . . . . . . . . . . . . . . . . . 2
                2 . . . . . . . . . . . . 2 . . . . . . 2 . . . . . . . . . . . . . . . . . . . 2
                2 . . . . . . . . . . . . 2 . . . . . . 2 . . . . . . . . . . . . . . . . . . . 2
                2 . . . . . . . . . . . . 2 . . . . . . 2 . . . . . . . . . . . . . . . . . . . 2
                2 . . . . . . . . . . . . 2 . . . . . . 2 . . . . . . . . . . . . . . . . . . . 2
                2 . . . . . . . . . . . . 2 . . . . . . 2 . . . . . . . . . . . . . . . . . . . 2
                2 . . . . . . . . . . . . 2 . . . . . . 2 . . . . . . . . . . . . . . . . . . . 2
                2 . . . . . . . . . . . . 2 . . . . . . 2 . . . . . . . . . . . . . . . . . . . 2
                2 2 2 2 2 2 2 2 2 2 2 2 2 2 . . . . . . 2 2 2 2 2 2 2 2 2 2 2 2 2 2 2 2 2 2 2 2 2
                . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
                . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
                . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
                . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
                . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
                . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
                . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
                . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
                . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
                . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
                . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
                . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
                . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
                . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
            `,
            [myTiles.tile0,sprites.castle.tilePath1,sprites.castle.tilePath2,sprites.castle.tilePath3,sprites.castle.tilePath4,sprites.castle.tilePath8,sprites.castle.tilePath6,sprites.castle.tilePath7,sprites.castle.tilePath9,sprites.castle.tilePath5,sprites.dungeon.darkGroundNorth,sprites.dungeon.darkGroundSouth,sprites.dungeon.darkGroundWest,sprites.dungeon.darkGroundSouthWest0,sprites.dungeon.darkGroundSouthEast0,sprites.dungeon.darkGroundEast,sprites.dungeon.darkGroundNorthEast0,sprites.dungeon.darkGroundNorthWest0,sprites.dungeon.darkGroundCenter,myTiles.tile1],
            TileScale.Sixteen
        ))
let mySprite = sprites.create(img`
    . f f f . f f f f . f f f .
    f f f f f c c c c f f f f f
    f f f f b c c c c b f f f f
    f f f c 3 c c c c 3 c f f f
    . f 3 3 c c c c c c 3 3 f .
    . f c c c c 4 4 c c c c f .
    . f f c c 4 4 4 4 c c f f .
    . f f f b f 4 4 f b f f f .
    . f f 4 1 f d d f 1 4 f f .
    . . f f d d d d d d f f . .
    . . e f e 4 4 4 4 e f e . .
    . e 4 f b 3 3 3 3 b f 4 e .
    . 4 d f 3 3 3 3 3 3 c d 4 .
    . 4 4 f 6 6 6 6 6 6 f 4 4 .
    . . . . f f f f f f . . . .
    . . . . f f . . f f . . . .
`, SpriteKind.Player)
controller.moveSprite(mySprite)
scene.cameraFollowSprite(mySprite)
for (let index = 0; index < 20; index++) {
    energi = sprites.create(img`
        . . . . . 9 f f f f 9 9 9 9 9 9
        . . . . . 9 f 9 9 f 9 9 f f f f
        . 9 9 9 9 9 9 9 9 f 9 9 f 9 9 f
        . 9 f f f f f f f f 9 9 9 9 9 f
        . 9 9 9 9 9 9 9 9 9 9 9 9 9 9 f
        . 9 f f f f f f f f f f f f f f
        . 9 9 9 9 9 9 9 9 9 9 9 9 9 9 9
        . 9 f f f f f f f f f f f 9 . .
        . 9 9 9 9 9 9 9 9 9 9 9 f 9 . .
        . . . . . . . . 9 f 9 9 f 9 . .
        . . . . . . . . 9 f f f f 9 . .
        . . . . . . . . 9 9 9 9 9 9 . .
        . . . . . . . . . . . . . . . .
        . . . . . . . . . . . . . . . .
        . . . . . . . . . . . . . . . .
        . . . . . . . . . . . . . . . .
    `, SpriteKind.Food)
    tiles.placeOnRandomTile(energi, sprites.dungeon.darkGroundCenter)
}
for (let index = 0; index < 80; index++) {
    energi = sprites.create(img`
        . . . . . . . . . . . . . . . .
        . . . . . f f f f f . . . . . .
        . . f f f f f 1 1 f . . . . . .
        . f f f f f 1 f 1 f . . . . . .
        . f f 1 f f f f f f f f . . . .
        . f f f f f f f f f 1 f . . . .
        . f 1 f f f f f f f 1 f . . . .
        . f f f f 1 1 f f f f f . . . .
        f f f f f f f f f f f f . . . .
        f 1 f f f 1 1 1 f f f . . . . .
        f f f 1 f f f f f 1 f . . . . .
        . . f 1 f 1 1 1 f 1 f . . . . .
        . . . f f f f f f f . . . . . .
        . . . . . . . . . . . . . . . .
        . . . . . . . . . . . . . . . .
        . . . . . . . . . . . . . . . .
    `, SpriteKind.Food)
    tiles.placeOnRandomTile(energi, sprites.castle.tilePath5)
}
if (Math.randomRange(0, 10) < 8) {
    tiles.placeOnRandomTile(mySprite, sprites.dungeon.darkGroundCenter)
} else {
    tiles.placeOnRandomTile(mySprite, sprites.castle.tilePath5)
}
info.startCountdown(10)
info.setScore(6)
forever(function () {
    info.changeScoreBy(-1)
    pause(1000)
})


```
## Step 1

Nå skal vi få inn flere former for energi. Energi kan være fornybar eller ikke-fornybar, så legg merke til at energisymblolet fra første versjon av spillet er byttet ut med symboler for vind og kull. 

```blocks
for (let index = 0; index < 20; index++) {
    energi = sprites.create(img`
        . . . . . . . . . . . . . . . .
        . . . . . f f f f f . . . . . .
        . . f f f f f 1 1 f . . . . . .
        . f f f f f 1 f 1 f . . . . . .
        . f f 1 f f f f f f f f . . . .
        . f f f f f f f f f 1 f . . . .
        . f 1 f f f f f f f 1 f . . . .
        . f f f f 1 1 f f f f f . . . .
        f f f f f f f f f f f f . . . .
        f 1 f f f 1 1 1 f f f . . . . .
        f f f 1 f f f f f 1 f . . . . .
        . . f 1 f 1 1 1 f 1 f . . . . .
        . . . f f f f f f f . . . . . .
        . . . . . . . . . . . . . . . .
        . . . . . . . . . . . . . . . .
        . . . . . . . . . . . . . . . .
    `, SpriteKind.Food)
    tiles.placeOnRandomTile(energi, sprites.dungeon.darkGroundCenter)
}
for (let index = 0; index < 80; index++) {
    energi = sprites.create(img`
        . . . . . 9 f f f f 9 9 9 9 9 9
        . . . . . 9 f 9 9 f 9 9 f f f f
        . 9 9 9 9 9 9 9 9 f 9 9 f 9 9 f
        . 9 f f f f f f f f 9 9 9 9 9 f
        . 9 9 9 9 9 9 9 9 9 9 9 9 9 9 f
        . 9 f f f f f f f f f f f f f f
        . 9 9 9 9 9 9 9 9 9 9 9 9 9 9 9
        . 9 f f f f f f f f f f f 9 . .
        . 9 9 9 9 9 9 9 9 9 9 9 f 9 . .
        . . . . . . . . 9 f 9 9 f 9 . .
        . . . . . . . . 9 f f f f 9 . .
        . . . . . . . . 9 9 9 9 9 9 . .
        . . . . . . . . . . . . . . . .
        . . . . . . . . . . . . . . . .
        . . . . . . . . . . . . . . . .
        . . . . . . . . . . . . . . . .
    `, SpriteKind.Food)
    tiles.placeOnRandomTile(energi, sprites.castle.tilePath5)
}
```
## Step 2

Det første vi må gjøre er å skille mellom de forskjellige typene energi. Begge skal ikke lenger være ``||sprites.Food||``. Trykk på ``||sprites:Food||`` ved siden av vindsymbolet og velg ``||sprites:Add new kind..||``. Her skriver du "Vind".

## Step 3

Gjør det samme for kull. Trykk på ``||sprites:Food||`` ved siden av kullsymbolet og velg ``||sprites:Add new kind..||``. Her skriver du "Kull". Vis hint for å se hvordan de to ``||loops:repeat||``-løkkene skal se ut nå.
```blocks
namespace SpriteKind {
    export const Kull = SpriteKind.create()
    export const Vind = SpriteKind.create()
}
for (let index = 0; index < 20; index++) {
    energi = sprites.create(img`
        . . . . . . . . . . . . . . . .
        . . . . . f f f f f . . . . . .
        . . f f f f f 1 1 f . . . . . .
        . f f f f f 1 f 1 f . . . . . .
        . f f 1 f f f f f f f f . . . .
        . f f f f f f f f f 1 f . . . .
        . f 1 f f f f f f f 1 f . . . .
        . f f f f 1 1 f f f f f . . . .
        f f f f f f f f f f f f . . . .
        f 1 f f f 1 1 1 f f f . . . . .
        f f f 1 f f f f f 1 f . . . . .
        . . f 1 f 1 1 1 f 1 f . . . . .
        . . . f f f f f f f . . . . . .
        . . . . . . . . . . . . . . . .
        . . . . . . . . . . . . . . . .
        . . . . . . . . . . . . . . . .
    `, SpriteKind.Kull)
    tiles.placeOnRandomTile(energi, sprites.dungeon.darkGroundCenter)
}
for (let index = 0; index < 80; index++) {
    energi = sprites.create(img`
        . . . . . 9 f f f f 9 9 9 9 9 9
        . . . . . 9 f 9 9 f 9 9 f f f f
        . 9 9 9 9 9 9 9 9 f 9 9 f 9 9 f
        . 9 f f f f f f f f 9 9 9 9 9 f
        . 9 9 9 9 9 9 9 9 9 9 9 9 9 9 f
        . 9 f f f f f f f f f f f f f f
        . 9 9 9 9 9 9 9 9 9 9 9 9 9 9 9
        . 9 f f f f f f f f f f f 9 . .
        . 9 9 9 9 9 9 9 9 9 9 9 f 9 . .
        . . . . . . . . 9 f 9 9 f 9 . .
        . . . . . . . . 9 f f f f 9 . .
        . . . . . . . . 9 9 9 9 9 9 . .
        . . . . . . . . . . . . . . . .
        . . . . . . . . . . . . . . . .
        . . . . . . . . . . . . . . . .
        . . . . . . . . . . . . . . . .
    `, SpriteKind.Vind)
    tiles.placeOnRandomTile(energi, sprites.castle.tilePath5)
}
```

## Step 4

Nå vil vi plassere 40 av hver energitype i det lyse området, og 10 av hver i det mørke området. Da trenger vi til sammen 4 ``||loops:repeat||`` -løkker, så vi velger å bruke funksjoner til dette. Lag en funksjon for å plassere ut vindsymboler ved å trykke på **Advanced** og velge ``||Functions:Functions||`` og ``||Functions:Make a function...||``. Kall den for **plasserVind**.
```blocks
function plasserVind () {
	
}
```
## Step 5    

Kopier ``||loops:repeat||``-blokken med vindsymbol to ganger og legg i ``||functions:plasserVind||``. Gjør slik at det blir plassert 10 vind-sprites i det mørke området og 40 i det lyse.
```blocks
namespace SpriteKind {
    export const Kull = SpriteKind.create()
    export const Vind = SpriteKind.create()
}
function plasserVind () {
    for (let index = 0; index < 10; index++) {
        energi = sprites.create(img`
            . . . . . 9 f f f f 9 9 9 9 9 9
            . . . . . 9 f 9 9 f 9 9 f f f f
            . 9 9 9 9 9 9 9 9 f 9 9 f 9 9 f
            . 9 f f f f f f f f 9 9 9 9 9 f
            . 9 9 9 9 9 9 9 9 9 9 9 9 9 9 f
            . 9 f f f f f f f f f f f f f f
            . 9 9 9 9 9 9 9 9 9 9 9 9 9 9 9
            . 9 f f f f f f f f f f f 9 . .
            . 9 9 9 9 9 9 9 9 9 9 9 f 9 . .
            . . . . . . . . 9 f 9 9 f 9 . .
            . . . . . . . . 9 f f f f 9 . .
            . . . . . . . . 9 9 9 9 9 9 . .
            . . . . . . . . . . . . . . . .
            . . . . . . . . . . . . . . . .
            . . . . . . . . . . . . . . . .
            . . . . . . . . . . . . . . . .
        `, SpriteKind.Vind)
        tiles.placeOnRandomTile(energi, sprites.dungeon.darkGroundCenter)
    }
    for (let index = 0; index < 40; index++) {
        energi = sprites.create(img`
            . . . . . 9 f f f f 9 9 9 9 9 9
            . . . . . 9 f 9 9 f 9 9 f f f f
            . 9 9 9 9 9 9 9 9 f 9 9 f 9 9 f
            . 9 f f f f f f f f 9 9 9 9 9 f
            . 9 9 9 9 9 9 9 9 9 9 9 9 9 9 f
            . 9 f f f f f f f f f f f f f f
            . 9 9 9 9 9 9 9 9 9 9 9 9 9 9 9
            . 9 f f f f f f f f f f f 9 . .
            . 9 9 9 9 9 9 9 9 9 9 9 f 9 . .
            . . . . . . . . 9 f 9 9 f 9 . .
            . . . . . . . . 9 f f f f 9 . .
            . . . . . . . . 9 9 9 9 9 9 . .
            . . . . . . . . . . . . . . . .
            . . . . . . . . . . . . . . . .
            . . . . . . . . . . . . . . . .
            . . . . . . . . . . . . . . . .
        `, SpriteKind.Vind)
        tiles.placeOnRandomTile(energi, sprites.castle.tilePath5)
    }
}
```

## Step 6
Lag en funksjon som du kaller ``||functions:plasserKull||``, og få det til å bli plassert 10 kull-sprites i det mørke området og 40 i det lyse.
```blocks
namespace SpriteKind {
    export const Kull = SpriteKind.create()
    export const Vind = SpriteKind.create()
}
function plasserKull () {
    for (let index = 0; index < 10; index++) {
        energi = sprites.create(img`
            . . . . . . . . . . . . . . . .
            . . . . . f f f f f . . . . . .
            . . f f f f f 1 1 f . . . . . .
            . f f f f f 1 f 1 f . . . . . .
            . f f 1 f f f f f f f f . . . .
            . f f f f f f f f f 1 f . . . .
            . f 1 f f f f f f f 1 f . . . .
            . f f f f 1 1 f f f f f . . . .
            f f f f f f f f f f f f . . . .
            f 1 f f f 1 1 1 f f f . . . . .
            f f f 1 f f f f f 1 f . . . . .
            . . f 1 f 1 1 1 f 1 f . . . . .
            . . . f f f f f f f . . . . . .
            . . . . . . . . . . . . . . . .
            . . . . . . . . . . . . . . . .
            . . . . . . . . . . . . . . . .
        `, SpriteKind.Kull)
        tiles.placeOnRandomTile(energi, sprites.dungeon.darkGroundCenter)
    }
    for (let index = 0; index < 40; index++) {
        energi = sprites.create(img`
            . . . . . . . . . . . . . . . .
            . . . . . f f f f f . . . . . .
            . . f f f f f 1 1 f . . . . . .
            . f f f f f 1 f 1 f . . . . . .
            . f f 1 f f f f f f f f . . . .
            . f f f f f f f f f 1 f . . . .
            . f 1 f f f f f f f 1 f . . . .
            . f f f f 1 1 f f f f f . . . .
            f f f f f f f f f f f f . . . .
            f 1 f f f 1 1 1 f f f . . . . .
            f f f 1 f f f f f 1 f . . . . .
            . . f 1 f 1 1 1 f 1 f . . . . .
            . . . f f f f f f f . . . . . .
            . . . . . . . . . . . . . . . .
            . . . . . . . . . . . . . . . .
            . . . . . . . . . . . . . . . .
        `, SpriteKind.Kull)
        tiles.placeOnRandomTile(energi, sprites.castle.tilePath5)
    }
}
```

## Step 7

Nå skal du erstatte ``||loops:repeat||``-blokkene som ligger under ``||loops:on start||``. Den første med ``||functions.call plasserVind||`` og den andre med ``||functions.call plasserKull||``. Disse finner du under ``||functions.Functions||``.
```blocks

function plasserVind () {

}
function plasserKull () {
 
}

namespace SpriteKind {
    export const Kull = SpriteKind.create()
    export const Vind = SpriteKind.create()
}
tiles.setTilemap(tiles.createTilemap(
            hex`290028000000000000000000000000000000000000000000000000000000000000000000000000000000000000000102020202020202020202030000000000000000110a0a0a0a0a0a0a0a0a0a0a0a0a0a0a0a0a10000004090909090909090909090600000000000000000c12121212121212121212121212121212120f000004090909090909090909090600000000000000000c12121212121212121212121212121212120f000004090909090909090909090600000000000000000c12121212121212121212121212121212120f000004090909090909090909090600000000000000000c12121212121212121212121212121212120f000004090909090909090909090600000000000000000c12121212121212121212121212121212120f000004090909090909090909090600000000000000000c12121212121212121212121212121212120f000004090909090909090909090600000000000000000c12121212121212121212121212121212120f000004090909090909090909090600000000000000000c12121212121212121212121212121212120f0000040909090909090909090909020202020a0a0a0a1212121212121212121212121212121212120f0000040909090909090909090909050505050b0b0b0b1212121212121212121212121212121212120f000004090909090909090909090600000000000000000c12121212121212121212121212121212120f000004090909090909090909090600000000000000000c12121212121212121212121212121212120f000004090909090909090909090600000000000000000c12121212121212121212121212121212120f000004090909090909090909090600000000000000000c12121212121212121212121212121212120f000004090909090909090909090600000000000000000c12121212121212121212121212121212120f000004090909090909090909090600000000000000000c12121212121212121212121212121212120f000004090909090909090909090600000000000000000c12121212121212121212121212121212120f000004090909090909090909090600000000000000000c12121212121212121212121212121212120f000004090909090909090909090600000000000000000c12121212121212121212121212121212120f000004090909090909090909090600000000000000000c12121212121212121212121212121212120f000004090909090909090909090600000000000000000c12121212121212121212121212121212120f000004090909090909090909090600000000000000000c12121212121212121212121212121212120f000007050505050505050505050800000000000000000d0b0b0b0b0b0b0b0b0b0b0b0b0b0b0b0b0b0e00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000`,
            img`
                2 2 2 2 2 2 2 2 2 2 2 2 2 2 . . . . . . 2 2 2 2 2 2 2 2 2 2 2 2 2 2 2 2 2 2 2 2 2
                2 . . . . . . . . . . . . 2 . . . . . . 2 . . . . . . . . . . . . . . . . . . . 2
                2 . . . . . . . . . . . . 2 . . . . . . 2 . . . . . . . . . . . . . . . . . . . 2
                2 . . . . . . . . . . . . 2 . . . . . . 2 . . . . . . . . . . . . . . . . . . . 2
                2 . . . . . . . . . . . . 2 . . . . . . 2 . . . . . . . . . . . . . . . . . . . 2
                2 . . . . . . . . . . . . 2 . . . . . . 2 . . . . . . . . . . . . . . . . . . . 2
                2 . . . . . . . . . . . . 2 . . . . . . 2 . . . . . . . . . . . . . . . . . . . 2
                2 . . . . . . . . . . . . 2 . . . . . . 2 . . . . . . . . . . . . . . . . . . . 2
                2 . . . . . . . . . . . . 2 . . . . . . 2 . . . . . . . . . . . . . . . . . . . 2
                2 . . . . . . . . . . . . 2 2 2 2 2 2 2 2 . . . . . . . . . . . . . . . . . . . 2
                2 . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 2
                2 . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 2
                2 . . . . . . . . . . . . 2 2 2 2 2 2 2 2 . . . . . . . . . . . . . . . . . . . 2
                2 . . . . . . . . . . . . 2 . . . . . . 2 . . . . . . . . . . . . . . . . . . . 2
                2 . . . . . . . . . . . . 2 . . . . . . 2 . . . . . . . . . . . . . . . . . . . 2
                2 . . . . . . . . . . . . 2 . . . . . . 2 . . . . . . . . . . . . . . . . . . . 2
                2 . . . . . . . . . . . . 2 . . . . . . 2 . . . . . . . . . . . . . . . . . . . 2
                2 . . . . . . . . . . . . 2 . . . . . . 2 . . . . . . . . . . . . . . . . . . . 2
                2 . . . . . . . . . . . . 2 . . . . . . 2 . . . . . . . . . . . . . . . . . . . 2
                2 . . . . . . . . . . . . 2 . . . . . . 2 . . . . . . . . . . . . . . . . . . . 2
                2 . . . . . . . . . . . . 2 . . . . . . 2 . . . . . . . . . . . . . . . . . . . 2
                2 . . . . . . . . . . . . 2 . . . . . . 2 . . . . . . . . . . . . . . . . . . . 2
                2 . . . . . . . . . . . . 2 . . . . . . 2 . . . . . . . . . . . . . . . . . . . 2
                2 . . . . . . . . . . . . 2 . . . . . . 2 . . . . . . . . . . . . . . . . . . . 2
                2 . . . . . . . . . . . . 2 . . . . . . 2 . . . . . . . . . . . . . . . . . . . 2
                2 2 2 2 2 2 2 2 2 2 2 2 2 2 . . . . . . 2 2 2 2 2 2 2 2 2 2 2 2 2 2 2 2 2 2 2 2 2
                . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
                . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
                . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
                . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
                . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
                . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
                . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
                . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
                . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
                . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
                . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
                . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
                . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
                . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
            `,
            [myTiles.tile0,sprites.castle.tilePath1,sprites.castle.tilePath2,sprites.castle.tilePath3,sprites.castle.tilePath4,sprites.castle.tilePath8,sprites.castle.tilePath6,sprites.castle.tilePath7,sprites.castle.tilePath9,sprites.castle.tilePath5,sprites.dungeon.darkGroundNorth,sprites.dungeon.darkGroundSouth,sprites.dungeon.darkGroundWest,sprites.dungeon.darkGroundSouthWest0,sprites.dungeon.darkGroundSouthEast0,sprites.dungeon.darkGroundEast,sprites.dungeon.darkGroundNorthEast0,sprites.dungeon.darkGroundNorthWest0,sprites.dungeon.darkGroundCenter,myTiles.tile1],
            TileScale.Sixteen
        ))
let mySprite = sprites.create(img`
    . f f f . f f f f . f f f .
    f f f f f c c c c f f f f f
    f f f f b c c c c b f f f f
    f f f c 3 c c c c 3 c f f f
    . f 3 3 c c c c c c 3 3 f .
    . f c c c c 4 4 c c c c f .
    . f f c c 4 4 4 4 c c f f .
    . f f f b f 4 4 f b f f f .
    . f f 4 1 f d d f 1 4 f f .
    . . f f d d d d d d f f . .
    . . e f e 4 4 4 4 e f e . .
    . e 4 f b 3 3 3 3 b f 4 e .
    . 4 d f 3 3 3 3 3 3 c d 4 .
    . 4 4 f 6 6 6 6 6 6 f 4 4 .
    . . . . f f f f f f . . . .
    . . . . f f . . f f . . . .
`, SpriteKind.Player)
controller.moveSprite(mySprite)
scene.cameraFollowSprite(mySprite)
plasserKull()
plasserVind()
if (Math.randomRange(0, 10) < 8) {
    tiles.placeOnRandomTile(mySprite, sprites.dungeon.darkGroundCenter)
} else {
    tiles.placeOnRandomTile(mySprite, sprites.castle.tilePath5)
}
info.startCountdown(10)
info.setScore(6)
```


## Step 8

Til slutt skal vi forandre litt på hva som skjer når spiller-spriten overlapper med energi-spritene. Først, gå til ``||sprites:on sprite of kind...||``-blokken og forandre ``||variables:otherSprite||`` til å være av typen ``||sprites:Kull||``. Du kan også legge inn at du får 5 poeng for kull.
```blocks
namespace SpriteKind {
    export const Kull = SpriteKind.create()
    export const Vind = SpriteKind.create()
}
sprites.onOverlap(SpriteKind.Player, SpriteKind.Kull, function (sprite, otherSprite) {
    otherSprite.destroy()
    info.changeScoreBy(5)
})
```

## Step 9 

Så trenger vi å definere hva som skjer når spilleren treffer et vindsymbol. Siden vind er en fornybar energiklide vil vi at den ikke skal forsvinne, men dukke opp på ny. Først kan du **kopiere**  ``||sprites:on sprite of kind...||``-blokken og forandre ``||variables:otherSprite||`` til å være av typen ``||sprites:Vind||``. Denne gir 1 poeng.
```blocks
namespace SpriteKind {
    export const Kull = SpriteKind.create()
    export const Vind = SpriteKind.create()
}
sprites.onOverlap(SpriteKind.Player, SpriteKind.Vind, function (sprite, otherSprite) {
    otherSprite.destroy()
    info.changeScoreBy(1)
})

```

## Step 10

Slett ``||sprites:destroy||``-blokken og erstatt med en ``||logic:if-then-else||``-blokk.

```blocks
namespace SpriteKind {
    export const Kull = SpriteKind.create()
    export const Vind = SpriteKind.create()
}
sprites.onOverlap(SpriteKind.Player, SpriteKind.Vind, function (sprite, otherSprite) {
    if (true) {
        
    } else {
       
    }
    info.changeScoreBy(1)
})
```

## Step 11

Der hvor det står ``||logic:True||`` skal du legge en ``||scene:tile to left of...||``-blokk. Denne finner du i ``||scene:Scene||``-menyen. Forandre ``||scene:left||`` til ``||scene:center||``, og velg lys bakgrunn. Hvis ``||variables:sprite||`` er på lys bakgrunn skal ``||variables:otherSprite||`` plasseres på tilfeldig brikke med lys bakgrunn. Ellers (``||logic:else||``) skal den plasseres på tilfeldig brikke med mørk bakgrunn.

```blocks
namespace SpriteKind {
    export const Kull = SpriteKind.create()
    export const Vind = SpriteKind.create()
}
sprites.onOverlap(SpriteKind.Player, SpriteKind.Vind, function (sprite, otherSprite) {
    if (sprite.tileKindAt(TileDirection.Center, sprites.castle.tilePath5)) {
        tiles.placeOnRandomTile(otherSprite, sprites.castle.tilePath5)
    } else {
        tiles.placeOnRandomTile(otherSprite, sprites.dungeon.darkGroundCenter)
    }
    info.changeScoreBy(1)
})
```