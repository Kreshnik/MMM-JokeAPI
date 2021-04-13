# MagicMirror² JokeAPI module
This is a module for `MagicMirror²`; the purpose of the module is to show you jokes from the V2 JokeAPI.


### Preview
![Screenshot](screenshot.png)


## Installation
1.  Clone this repository into your MagicMirror `modules` folder.
2.  Edit your configuration file under `config/config.js` with the following configuration.
```
{
    module: 'MMM-JokeAPI',
    position: 'middle_center',
}
```
You can use more detailed configuration like these; See the below section.
```
{
    module: 'MMM-JokeAPI',
    position: 'middle_center',
    config: {
        lang: "en",
        category: "Programming,Miscellaneous",
        blacklistFlags: "nsfw",
        safeMode: true,
    }
}
```

## Configuration options

| Option                 | Description
|------------------------|-----------
| `category`             | Joke Categories.<br><br>Possible values:`Any, Miscellaneous, Dark, Programming, Pun, Spooky, Christmas`<br><br> **Type:** `string` <br>**Default value:** `Any`<br>Multiple catagories can be used at once, just seperate them with commas <br><br> **Example:** `category: "Programming,Miscellaneous,Pun",`
| `fetchInterval`        | How often (in milliseconds) a new joke should be fetched.<br><br> **Type:** `number` <br>**Default value:** `10 * 1000`
| `lang`                 | Language the jokes are in.<br><br> Current languages suported are `cs, de, en, es, fr, pt`<br><br>**Type:** `string` <br>**Default value:** `en`<br><br> **Example:** `lang: "en",`
| `blacklistFlags`       | Prevent jokes of this type.<br><br> These are all the available flags: `nsfw, religious, political, racist, sexist, explicit`<br><br> **Type:** `string` <br>**Default value:** `NULL`<br>Multiple blacklistFlags can be set at one, just seperate them with commas <br><br> **Example:** `blacklistFlags: "nsfw,religious",`
| `safeMode`             | If enabled, JokeAPI will try its best to serve only jokes that are considered safe for everyone. Unsafe jokes are those who can be considered explicit in any way, either through the used language, its references or its blacklist flags. Jokes from the category Dark are also generally marked as unsafe. <br><br>**Type:** `bool` <br>**Default value:** `false`<br><br> **Example:** `safeMode: true,`

#### Credits
MagicMirror²:   [MagicMirror²](https://github.com/MichMich/MagicMirror)   
JokeAPI:    [V2 JokeAPI](https://v2.jokeapi.dev/)
