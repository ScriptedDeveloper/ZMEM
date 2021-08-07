# ZMEM
An Open-Source alternative to the popular virus MEMZ. The way ZMEM functions is very identical to the original malware.


# How to rescue data
Rescuing data (and recover your Windows partition) is very easy. For this you need an additional computer and an usb stick. Simply create a recovery drive¹ and open cmd by booting from it. From there type the following commands and reboot ```
diskpart```
```list disk```
```select disk # Choose the EFI partition```
```list partition```
```select partition # Select the Windows partition```
```shrink desired=100```
```create partition efi size=100```
```format quick fs=fat32```
```assign letter=s```
```list partition```
```exit```


# Legal
I do not hold any responsibility for the damage made by this. To reduce the possibility that this might be used to corrupt EFIs of innocent vicitims computer's, a warning message has been made before payload execution starts.


1 - https://support.microsoft.com/en-us/windows/create-a-recovery-drive-abb4691b-5324-6d4a-8766-73fab304c246
