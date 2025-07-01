# pacman-contrib

Contrib repository for the pacman package management project.

## How to build

```sh
./autogen.sh
./configure --prefix=/usr \
            --sysconfdir=/etc \
            --localstatedir=/var
make
make check
make install DESTDIR="$pkgdir"
```

## Contributions

- systemd services and timers for paccache and `pacman -Fy`.

- Vim runtime files for PKGBUILD and SRCINFO files.

### Scripts

checkupdates
: Print a list of pending updates without touching the system sync databases
  (for safety on rolling release distributions).

paccache
: Flexible package cache cleaning utility that allows greater control over which
  packages are removed.

pacdiff
: pacnew/pacsave updater for /etc/.

paclist
: List all packages installed from a given repository. Useful for seeing which
  packages you may have installed from the testing repositories, for instance.

paclog-pkglist
: List currently installed packages based pacman's log.

pacscripts
: Print the {pre,post}\_{install,remove,upgrade} scripts of a given package.

pacsearch
: Colorized search combining both -Ss and -Qs output. Installed packages are
  easily identified with a `[installed]`, and local-only packages are also
  listed.

pacsort
: Concatenate the given files, sort them, and write them to standard output.

pactree
: Package dependency tree viewer.

rankmirrors
: Rank pacman mirrors by their connection and opening speed.

updpkgsums
: Perform an in-place update of the checksums in a PKGBUILD.
