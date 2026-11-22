# MG7
## Devlog
Write your Devlog here. :3

For the birds, I put a TreeOfBirds script on the Tree GameObject so the sparrows pop out when the player walks up. I didn't want a variable for every bird, so I used a public GameObject[] birds array and dragged in all the Sparrows except Sparrow_Start in the Inspector.
In Update(), a for loop goes through the array, from 0 to birds.Length - 1, and skips empty slots and birds that are already on. For the rest, Vector3.Distance gets the distance between bird.transform.position and player.position. If it's within interactionDistance, I call SetActive(true). That triggers OnEnable() in the Bird script and plays the pop-up animation.

## Open-Source Assets
- [Forest Nature Pack](https://kaylousberg.itch.io/kaykit-forest) - environment 3D models
- [Quirky Series](https://assetstore.unity.com/packages/3d/characters/animals/quirky-series-free-animals-pack-178235) - animal 3D models
