# ESH Traits Plugin for Ares

## Credits

Clockwork@AresCentral
Rucket82 for Sheet Template Updates

## Overview

 This plugin creates a series of commands for setting Powers, Skills, Advantages, and Flaws on characters. It also contains instructions on integrating these into the web portal and character generation.

 **NOTE:** This plugin requires the insertion of code into several areas reserved for custom web hooks. It should not cause any merge conflicts as it does not modify the core code; however, the custom files will require updating per the instructions below.

## Installation

Disable the FS3 plugins, as explained in [Enabling and Disabling Plugins](https://aresmush.com/tutorials/config/plugins/).

In the game, run 'plugin/install https://github.com/clockworkejd/ares-eshtraits-plugin`.

### Updating Custom Profile and Chargen Areas

If you do not have any existing edits to these custom files, you can use the files in the custom_files folder of this repository as-is. If you do, then you may use them as templates to add the lines of code needed for eshtraits.

File: aresmush/plugins/profile/custom_char_fields.rb

Use: custom_files/custom_char_fields.rb

File: aresmush/plugins/chargen/custom_app_review.rb

Use: custom_files/custom_app_review.rb

### Updating Custom Web Portal Chargen and Profile Areas

File: ares-webportal/app/components/chargen-custom.js

Use: custom_files/chargen-custom.js

File: ares-webportal/app/templates/components/chargen-custom.hbs

Use: custom_files/chargen-custom.hbs

File: ares-webportal/app/templates/components/chargen-custom-tabs.hbs

Use: custom_files/chargen-custom-tabs.hbs

File: ares-webportal/app/templates/components/profile-custom.hbs

Use: custom_files/profile-custom.hbs

File: ares-webportal/app/templates/components/profile-custom-tabs.hbs

Use: custom_files/profile-custom-tabs.hbs

### Configuration

Go to Admin > Setup menu and edit chargen.yml and replace two FS3 [chargen stages](https://aresmush.com/tutorials/config/chargen.html) with the eshtraits stage.

Remove these two items:

    sheet:
      help: sheets
    abilities:
      help:skills

Add this item below the "groups" section:

    eshtraits:
      help: eshtraits



## Uninstalling

Removing the plugin requires some code fiddling. See [Uninstalling Plugins](https://www.aresmush.com/tutorials/code/extras.html#uninstalling-plugins).

## License

Same as [AresMUSH](https://aresmush.com/license).