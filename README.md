# curated-aur

A [curated](https://www.reddit.com/r/archlinux/comments/v97zei/launching_a_curated_aur_hosted_on_github/) repository of package recipies for Arch Linux. This complements the [AUR](https://wiki.archlinux.org/title/Arch_User_Repository).

## Usage

The primary way is to use the [ymerge](https://github.com/flying-dude/ymerge) package manager to install and remove packages.

Alternatively, you can work with the git repository directly, if you want. Use `git clone` to fetch packages and `git pull` to keep updated.
This is how you would install the [odin](https://github.com/flying-dude/curated-aur/tree/main/pkg/odin) package:

```
git clone https://github.com/flying-dude/curated-aur
cd curated-aur/pkg/odin
makepkg -si
```

## Whitelisting AUR Packages

The file
[aur-whitelist.json](https://github.com/flying-dude/curated-aur/tree/main/aur-whitelist.json)
contains a (long) list of packages from the Arch Linux
[AUR](https://wiki.archlinux.org/title/Arch_User_Repository),
that have been reviewed and accepted for usage with packages in this repository.

You can add more entries to the list of accepted packages by using the
[aur-whitelist](https://github.com/flying-dude/curated-aur/tree/main/scripts/aur-whitelist)
script. The script will automatically update `aur-whitelist.json` and print new entries to command line.

Example use:

```
$ ./scripts/aur-whitelist xmake build2 archivemount mount-zip
2ae835df306f3541e0384f6803f5972fedc3aad8 xmake
4424cce8e2f4d87fa54b1b53a354dec7d784e8f9 build2
e04e7dacb8d60a0c263fefb94f0dac20829ce515 archivemount
59809caf1ab342df88d60beb6dcc26fa8d2b8572 mount-zip
```