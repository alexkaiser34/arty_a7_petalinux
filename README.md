# Arty A7 Petalinux Configs

Repo holding prebuilt images in petalinux, and entire block design built in vivado.

1. Vivado Project
    - `arty_a7_vivado_2021_2.zip`
2. Petalinux Project
    - `arty_a7_petalinux_2022_2.zip`

## Building Petalinux Project

1. `petalinux-create --type project --template microblaze --name arty_petalinux`
2. `petalinux-config --get-hw-description=.`
3. `petalinux-build`
4. `petalinux-boot --jtag --fpga --kernel`

**NOTE**: Optional steps include the following.
1. Configuring the project
    - `petalinux-config`
2. Configuring the kernel
    - `petalinux-config -c kernel`
3. Configuring the rootfs
    - `petalinux-config -c rootfs`

Rebuild with `petalinux-build` after making changes to configs.
