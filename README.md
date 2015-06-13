To create a dmg simply put the latest version of XQuartz + FontForge inside the FontForge Installer so you have

```
FontForge Installer.app
  Contents/
  FontForge.app
  XQuartz.pkg
```

Then click the command file and FontForgeInstaller.dmg will be created on your desktop.

To codesign an app you need an Apple Dev account and the certificates installed on your mac. 
Run `certtool y | grep Developer\ ID` terminal and copy  `Developer ID Application: Your Name (Numbers'n'Letters)` 

Then type `codesign -s "Developer ID Application: Your Name (Numbers'n'Letters)" path/to/app` and the app is signed.
