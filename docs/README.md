![build](https://github.com/matyalatte/UE4-DDS-tools/actions/workflows/build.yml/badge.svg)
![test](https://github.com/matyalatte/UE4-DDS-tools/actions/workflows/test.yml/badge.svg)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

# UE4-DDS-Tools ver0.6.1

Texture modding tools for UE games.  
You can inject texture files (.dds, .tga, .hdr, etc.) into UE assets.  

## Features

- Inject any size textures into assets
- Extract textures from assets
- Check the UE versions of assets
- Convert textures with [texconv](https://github.com/microsoft/DirectXTex/wiki/Texconv)

## Supported UE versions

- UE5.0 ~ 5.4
- UE4.0 ~ 4.27
- FF7R
- Borderlands3

## Supported File Formats

This tool can convert textures between the following file formats.  

- .uasset (for texture assets)
- .dds
- .tga
- .hdr
- .bmp
- .jpg
- .png

> Note that it can not convert non-official DXGI formats (e.g. ASTC_4x4) from and to non-dds files.  
> It means you can not use .tga, .hdr, .bmp, .png, and .jpg for them.  

## Supported Pixel Formats

<details>
<summary>The List of supported pixel formats</summary>

- DXT1 (BC1)
- DXT3 (BC2)
- DXT5 (BC3)
- BC4 (ATI1)
- BC5 (ATI2)
- BC6H
- BC7
- A1
- A8
- G8 (R8)
- R8G8
- G16
- G16R16
- B8G8R8A8
- A2B10G10R10
- A16B16G16R16
- FloatRGB (FloatR11G11B10)
- FloatRGBA
- A32B32G32R32F
- B5G5R5A1_UNORM
- ASTC_4x4
- ASTC_6x6
- ASTC_8x8
- ASTC_10x10
- ASTC_12x12
- ETC1
- ETC2_RGB
- ETC2_RGBA

</details>

> Note that Unreal Engine supports more [pixel formats](https://docs.unrealengine.com/5.0/en-US/API/Runtime/Core/EPixelFormat/).  
> You will get `Unsupported pixel format.` errors for them.  

## Supported Texture Classes

<details>
<summary>The List of supported texture classes</summary>

- Texture2D
- TextureCube
- LightMapTexture2D
- ShadowMapTexture2D
- Texture2DArray
- TextureCubeArray
- VolumeTexture

</details>

## Download

Download one of the zip files from [here](https://github.com/matyalatte/UE4-DDS-tools/releases)

- `UE4-DDS-tools-*-Batch.zip` is for batch file users.
- `UE4-DDS-tools-*-GUI.zip` is for GUI users.

> `GUI.exe` only works on Windows10 or later.  
> If you use windows 8 or older, you can copy an executable from [Tuw-*-Windows-x64.zip](https://github.com/matyalatte/tuw/releases).

> Released packages only work on Windows.
> See here if you use macOS or Linux.  
> [For Unix Systems · matyalatte/UE4-DDS-Tools Wiki](https://github.com/matyalatte/UE4-DDS-Tools/wiki/For-Unix-Systems)


## Getting Started

- [For GUI users](https://github.com/matyalatte/UE4-DDS-Tools/wiki/How-to-Use)
- [For batch file users](https://github.com/matyalatte/UE4-DDS-Tools/wiki/Batch-files)

## FAQ

[FAQ · matyalatte/UE4-DDS-Tools Wiki](https://github.com/matyalatte/UE4-DDS-Tools/wiki/FAQ)

## External Projects

### Texconv-Custom-DLL

[Texconv](https://github.com/microsoft/DirectXTex/wiki/Texconv)
is a texture converter developed by Microsoft.  
It's the best DDS converter as far as I know.  
And [Texconv-Custom-DLL](https://github.com/matyalatte/Texconv-Custom-DLL) is a cross-platform implementation I made.  
The official Texconv only supports Windows but you can use it on other platforms.  

### Tuw

[Tuw](https://github.com/matyalatte/tuw) is a GUI wrapper for command-line tools.  
It can define a simple GUI with a json file.  

## License

* The files in this repository (including all submodules) are available under the [MIT license](https://github.com/matyalatte/UE4-DDS-Tools/blob/main/LICENSE).
* Released packages contain [Tuw](https://github.com/matyalatte/tuw) (`GUI.exe`) for GUI. It is released under the [MIT license](https://github.com/matyalatte/UE4-DDS-Tools/blob/main/LICENSE).
* Released packages contain [Windows embeddable package](https://www.python.org/downloads/windows/) for python. It is released under the [PSF license](https://docs.python.org/3/license.html).
