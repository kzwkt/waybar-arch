# https://gitlab.archlinux.org/archlinux/packaging/packages/pkgname/-/blob/main/PKGBUILD?ref_type=heads

pkgname=base-busybox-artix
pkgver=99
pkgrel=1
arch=('any')
depends=(
  'filesystem' 'gcc-libs' 'glibc' 
  'mkinitcpio-busybox' 'pacman' 'archlinux-keyring' 
)
provides=(base coreutils bash gawk gettext util-linux findutils file grep procps-ng sed tar xz gzip bzip2 psmisc pciutils util-linux-libs)

post_install() {
  # Install symlinks using busybox
  /usr/bin/busybox --install -s /usr/bin
  /usr/bin/busybox --install -s /usr/sbin
}
