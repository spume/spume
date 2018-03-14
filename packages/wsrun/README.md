# @spume/wsrun

Based on https://github.com/whoeverest/wsrun, but:

- easier to run specific scripts from any package within the workspace (e.g. `wsrun @spume/lib build`)
- usable options defined in `package.toml:script-options` will be passed to the script (e.g `esrun test MODE=ci`)
- will only run the script in the package if it is described in `package.toml`, otherwise skips it (forceable with `-f`)
- scripts are run in the order passed, and by default in serial, but if `-p` is passed, they will run in parallel
