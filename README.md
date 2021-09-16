## Arch Linux on Ideapad 330

### Kernel Parameters to fix Brightness and Graphics

Add the parameters to `/etc/default/grub`

```
iommu=pt acpi_backlight=native
```

`iommu=pt` Solves the Graphics issue.

`acpi_backlight=native` Solves the Brightness issue which was caused by failing of the Backlight Driver.

Make sure to run `sudo grub-mkconfig -o /boot/grub/grub.cfg` after updating kernel parameters.

### Wi-Fi Driver

Wifi driver can be installed by the module `https://aur.archlinux.org/packages/rtl8821ce-dkms-git/`
