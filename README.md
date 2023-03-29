# brave-profile-list
> Get a list of existing Google brave, Google brave Canary or Chromium user profiles

## Install
```
npm install brave-profile-list
```

## Usage
```
var braveProfileList = require('brave-profile-list');
console.log(braveProfileList());

// Something like this is logged to the console:

[ { displayName: 'User',
    profileDirName: 'Default',
    profileDir: '/Users/username/Library/Application Support/BraveSoftware/Brave-Browser/User Data/Default',
    profilePictureUrl: 'https://x.googleusercontent.com/path/to/profile/picture.jpg' },
  { displayName: 'Guest',
    profileDirName: 'Guest Profile',
    profileDir: '/Users/username/Library/Application Support/BraveSoftware/Brave-Browser/User Data/Guest Profile',
    profilePictureUrl: null },
  { displayName: 'Person 1',
    profileDirName: 'Profile 1',
    profileDir: '/Users/username/Library/Application Support/BraveSoftware/Brave-Browser/User Data/Profile 1',
    profilePictureUrl: 'https://x.googleusercontent.com/path/to/profile/picture.jpg' } ]
```

## Supported environments

- node.js

## API

### braveProfileList(variant)

Returns an array of objects ({ name, path}) one for each available profile excluding the default `System Profile`.

#### arguments

*variant*   
One of `braveProfileList.variants`, defaults to `brave`

### braveProfileList.variants

An enum of possible variants to search profiles for:

- `Brave Browser`

Example:

```
var braveProfileList = require('brave-profile-list');

console.log(braveProfileList(braveProfileList.variants.CHROMIUM));

// Logs a list of available chromium profiles to the console
```

## Author

Israel Roldan

## Related
- [brave-profile-list-cli](https://www.npmjs.com/package/brave-profile-list-cli) a CLI for this module

## LICENSE

ISC