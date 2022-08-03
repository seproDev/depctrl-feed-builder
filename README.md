# DepCtrl Feed Builder

Github Automation to automatically update a [DependencyControl](https://github.com/TypesettingTools/DependencyControl) feed.

### Intended Structure
 - A macros and a modules folder which contain the scripts
 - A main/stable branch and a dev branch
 - Macros are named `{namespace}.lua` or `{namespace}.moon`
 - Modules are placed located in the path corresponding to their namespace. So `sepro.color` would be placed in `modules/sepro/color.lua`
 - After pushing changes to the dev branch the `Release Update` workflow is used to push the changes to the main branch and update the DepCtrl feed

### Current shortcomings
 - `requiredModules` are currently not extracted from the script and need to be manually entered
 - The info extraction is done with regex and thus prone to breaking
 - Modules with multiple files are not supported
