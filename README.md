# herotate

A Heroku multi-login manager for `heroku-cli`

## What

`heroku-cli` reads your current logged-in Heroku user from a file
called `.netrc` that usually lives in your user's HOME directory.

This file contains the currently logged in heroku user.

`herotate` is able to manage multiple user login files via a simple
symlink based configuration system.

## How

If you already have an existing Heroku login via heroku-cli, then `herotate`
will copy your existing `.netrc` to its config directory (usually `$HOME/.config/herotate`)
and will symlink it back to the expected location at `$HOME/.netrc`

To add new configs, simply copy any newly generated `.netrc` files into the config
directory and give it a unique name.

`herotate` reserves the usage of the config name `main` as the default.

Run `herotate help` to see all commands and `herotate list` to list all configs.

## License
Apache-v2.0
```
   Copyright 2020 Peter Kenji Yamanaka

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       http://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.
```
