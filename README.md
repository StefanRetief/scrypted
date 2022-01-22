# Scrypted Home Automation

Scrypted is a home automation platform primarily focusing on making camera experiences seamless.
 * Streams load instantly, everywhere: [Demo](https://www.reddit.com/r/homebridge/comments/r34k6b/if_youre_using_homebridge_for_cameras_ditch_it/)
 * [HomeKit Secure Video Support](#homekit-secure-video-setup)
 * Google Home support: "Ok Google, Stream Backyard"

<img width="400" alt="Scrypted_Management_Console" src="https://user-images.githubusercontent.com/73924/131903488-722d87ac-a0b0-40fe-b605-326e6b886e35.png">

## Discord

[Join Scrypted Discord](https://discord.gg/DcFzmBHYGq)

## Supported Platforms

 * Google Home
 * Apple HomeKit
 * Amazon Alexa

Supported accessories: 
 * https://github.com/koush/scrypted/tree/main/plugins

# Installation

## Run on Docker

[Docker Installation Instructions](https://github.com/koush/scrypted/wiki/Docker)

## Run Locally

[Local Installation Instructions](https://github.com/koush/scrypted/wiki/Local-Installation)

## Development

## Debug the Scrypted Server in VSCode

```sh
# check out the code
git clone https://github.com/koush/scrypted
cd scrypted
# get the dependencies for the server and various plugins
./npm-install.sh
# open server project in VS Code
code server
```

You can now launch Scrypted in VSCode.

## Debug Scrypted Plugins in VSCode

```sh
# this is an example for homekit.
# follow the steps above to set up the checkout.
# open the homekit project in VS Code
code plugins/homekit
```

You can now launch (using the Start Debugging play button) the HomeKit Plugin in VSCode. Please be aware that you do *not* need to restart the Scrypted Server if you make changes to a plugin. Edit the plugin, launch, and the updated plugin will deploy on the running server.

If you do not want to set up VS Code, you can also run build and install the plugin directly from the command line:

```sh
# currently in the plugins/homekit directory.
npm run scrypted-webpack && npm run scrypted-deploy 127.0.0.1
```

## Plugin Development

Want to write your own plugin? Full documentation is available here: https://developer.scrypted.app

