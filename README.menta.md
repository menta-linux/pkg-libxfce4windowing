# pkg-libxfce4windowing (Menta Linux)

Debian packaging of libxfce4windowing 4.20.7 (from xfce-team/desktop/libxfce4windowing on Salsa, 4.20.7-1).

- Package and soname names are identical to Debian (`libxfce4windowing-0-0`, `libxfce4windowing-0-dev`, ...),
  so `libxfce4windowing-0-dev (>= 4.20.2)` is satisfied by this build on Debian 13 (trixie).
- Configured with `--enable-wayland=yes --enable-x11=yes`: configure fails instead of silently
  skipping Wayland (wlr/ext foreign-toplevel protocols need wayland-protocols from trixie-backports).
- No Menta dependencies.
- Versioning: `<upstream>-<rev>mentaN`; CI appends `~deb13` for the trixie build.
- CI builds on push to `master` (rolling release `latest` = unstable, `latest-trixie`); tag `menta/<version>` publishes a GitHub release.
