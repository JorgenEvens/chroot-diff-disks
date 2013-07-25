# chroot-diff-disks

## Contains

- A helper script to set up functioning chroot directories with ease.
- A script to make many small copies of an existing chroot by using diff images.

The installation of `avfs` is required for the `new` script to work.



## Usage

### enter
`enter` simply executes the chroot command on the directory but mounts `/sys`, `/proc` and `/dev` in the chroot and also cleans up after you exit the chroot.

### new

`new` allows you to create a diff image on top of a base chroot directory.

`new` creates a new directory in `<base-dir>/vm/<chroot-name>` and uses this as mount point.

`<base-dir>/diff/<chroot-name> is the directory that holds the diff files.

`<base-dir>/base/<type-name>` holds the different base directories that can be used.
You can create new base images/types in this folder using `debootstrap` and `enter`.