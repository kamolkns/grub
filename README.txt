========================================
ARCH LINUX GRUB BACKUP
========================================

Location:
 /home/madara/Documents/linux back up/grub-backup-kit

System boot:
 - UEFI
 - ESP mounted at /boot
 - GRUB EFI: /boot/EFI/GRUB/grubx64.efi
 - GRUB EFI boot entry: Boot0000
 - Windows Boot Manager: Boot0001
 - Secure Boot enabled
 - sbctl used for signing

Matrix theme:
 /boot/grub/themes/Matrix

Backed up:
 - /etc/default/grub
 - /etc/kernel/cmdline
 - /etc/mkinitcpio.conf
 - /etc/grub.d/25_arch_uki
 - /etc/grub.d/26_windows_11
 - Matrix theme
 - working GRUB EFI
 - previous GRUB EFI backups
 - sbctl configuration/state information
 - EFI boot entries

SAFE RESTORE:
1. Mount the ESP at /boot.
2. Restore configuration files.
3. Restore Matrix theme.
4. Rebuild initramfs/UKI.
5. Regenerate grub.cfg if required.
6. Sign EFI files with sbctl.
7. Run sbctl verify.
8. Confirm Secure Boot is enabled.
9. Confirm Boot0000 is GRUB and Boot0001 is Windows.

IMPORTANT:
 - Do not disable Secure Boot.
 - Do not reset Secure Boot keys.
 - Do not change NVRAM unless absolutely necessary.
 - Do not overwrite a working EFI binary until a backup exists.

ARROW PATCH:
The experimental GRUB source patch changed:
 - Left arrow = previous menu entry
 - Right arrow = next menu entry
 - Up/Down = ignored

The experimental patch is NOT the current active configuration.
The current working GRUB EFI is the known-good baseline.

========================================
