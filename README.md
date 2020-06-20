# gac-playground
Quick example project to play with Global Assembly Cache.

To register assemblies into the GAC using `gacutil.exe`, the program must be in your environment path. This is easily accomplished by running the Visual Studio Developer Command Propmpt (or PowerShell). Also this must be run with Administrator permissions because it will be making machine modifications.

Only signed assemblies with a strong name can be registered in the GAC. This can be modified on the Signing tab of the project Properties.

To install a DLL in the GAC, use the command:
```bash
# install using filename
gacutil /i TrippSpecialLibraryForGAC.dll
```

To uninstall a DLL from the GAC, use the command:
```bash
# uninstall using the name of the library
gacutil /u TrippSpecialLibraryForGAC
```

The GAC can be found on Windows 10 in the `C:\Windows\Microsoft.NET\assembly` directory.
