# Install Bionic

## Before you install

A few things are required to be installed before bionic can be used. If you already have them installed, just skip ahead.

### .Net Core SDK

Because Bionic builds on the top of the amazing Blazor project, the first thing you need to do is to install [.Net Core SDK](https://blazor.net/docs/get-started.html#setup).

!!! tip
    If you are not using Visual Studio, [installing .Net Core SDK](https://www.microsoft.com/net/download) will suffice.

Check if dotnet is installed:

```text
> dotnet --version
2.1.402
```

Blazor requires version 2.1.300 or above.

### SASS/SCSS compiler

Bionic uses SASS/SCSS for styling and requires an SCSS compiler. Please [install SASS](https://sass-lang.com/install) compiler.

Check if SCSS is installed:

```text
> sass --version
1.13.1
```

or, depending on which version you have installed:

```text
> sass --version
Ruby Sass 3.5.6
```

### NuGet

Bionic also requires NuGet to be install. In OSX and Linux, NuGet will be installed along with Mono. On Windows you will have to download the executable and place it in the Windows PATH. You can find NuGet download instructions [here](https://docs.microsoft.com/en-us/nuget/install-nuget-client-tools#nugetexe-cli).

```text
> nuget
NuGet Version: 4.7.0.5148
...
```

!!! tip
    On Ubuntu DO NOT use ```apt install nuget```. This will install version 2.8 and NuGet will not work properly.
    The current recommended version is 2.7. Bionic Framework provides a [small script](https://raw.githubusercontent.com/BionicFramework/Documentation/master/installers/nuget_linux_installer.sh) to facilitate this installation.

    You can execute the installer from your Linux terminal using:

    ```
    curl https://raw.githubusercontent.com/BionicFramework/Documentation/master/installers/nuget_linux_installer.sh | sudo bash
    ```


## Installing Bionic

Bionic releases are available through [NuGet](https://www.nuget.org/packages/Bionic).

To install it execute:
```text
> dotnet tool install --global Bionic
You can invoke the tool using the following command: bionic
Tool 'bionic' (version '1.0.17') was successfully installed.
```

And check if it was installed by executing:
```text
> bionic -v
🤖 Bionic v1.0.17
```

## Updating Bionic

To update execute:
```text
> bionic update
Tool 'bionic' was reinstalled with the latest stable version (version '1.0.17').
```

If you are on Windows, then the above command will fail. Instead use:

```text
> dotnet tool update -g bionic
Tool 'bionic' (version '1.0.25') was successfully uninstalled.
```

## Removing Bionic

To remove execute:
```text
> bionic uninstall
Tool 'bionic' (version '1.0.17') was successfully uninstalled.
```

If you are on Windows, then the above command will fail. Instead use:

```text
> dotnet tool uninstall -g bionic
Tool 'bionic' (version '1.0.25') was successfully uninstalled.
```
