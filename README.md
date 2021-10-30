# coke-music-data

shared data for
[Coke Music/MyCoke](https://en.wikipedia.org/wiki/MyCoke) recreation, for use
with both [coke-music-client](https://github.com/misterhat/coke-music-client)
and [coke-music-server](https://github.com/misterhat/coke-music-server).

## faces.json
definitions for eye, head and face combinations.

```javascript
```

## furniture.json
definitions for non-rug/poster furniture and objects.

icons and sprites are located in:
https://github.com/misterhat/coke-music-client/tree/master/dist/assets/furniture

```javascript
{
    "furniture_name": { // name used in /assets/furniture/
        "title": "Display Name", // displayed in catalogue or object settings
        "description": "I'm coolin' fam.", // displayed in catalogue
        "width": 70, // sprite width
        "height": 70, // sprite height
        "tileWidth": 1, // iso width
        "tileHeight": 1, // iso height
        "angles": [1, 3], // which angles [ne, sw, nw, se] = [0, 1, 2, 3]
        "offsetX": 0, // for angles 0, 1
        "offsetY": 0, // for angles 2, 3
        "sit": false // non-blocking and sittable
    }, // ...
}
```

## posters.json
definitions for poster items.

```javascript

```

## rooms.json
definitions for character studios.

```javascript
{
    "studio_name": {
        // offset of the 0, 0 isometric grid
        "offsetX": 380,
        "offsetY": 112,

        // [y][x] obstacle map (1 is blocked, 0 is open)
        "map": [
            [1, 0, 1, 1, 1, 1], // ...
        ],

        // wall locations for custom wall textures
        "walls": [
            {
                // determines the x/y deltas per texture, and whether to use
                // _left or _right image variant
                "orientation": "left", // or right

                // absolute position first wall begins
                "offsetX": 17,
                "offsetY": 177,

                // amount of textures to repeat
                "width": 10
            }
        ],

        // exit/entrance of the room
        "exit": {
            // isometric coordinates
            "x": 0,
            "y": 1,

            // which wall (if any) the door is located (to clip out texture)
            "wall": [1, 1], // determines which wall from the definition above

            // absolute cartesian coordinates to cut from door for wall textures
            "clip": [
                { "x": 0, "y": 13 },
                { "x": 0, "y": 114 }, // ...
            ]
        },

        // absolute cartesian coordinates to cut from room to generate
        // foreground
        "foreground": [
            { "x": 452, "y": 38 },
            { "x": 452, "y": 164 }, // ...
        ]
    }
}
```

## shirts.json
definitions for wearable shirt and sleeve sprites.

`shirtIndex` determines which vertical spritesheet offset to use in
[shirts.png](https://github.com/misterhat/coke-music-client/blob/master/dist/assets/character/shirts.png).

`sleeveIndex` determines which horizontal spritesheet offset to use into
[sleeves.png](https://github.com/misterhat/coke-music-client/blob/master/dist/assets/character/sleeves.png).

```javascript
[
    {
        "shirtIndex": 0,
        "sleeveIndex": 0,
        "female": false // exclusive to female characters
    }, // ...
]
```

## license
