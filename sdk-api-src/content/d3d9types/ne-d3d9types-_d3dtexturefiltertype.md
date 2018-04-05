---
UID: NE:d3d9types._D3DTEXTUREFILTERTYPE
title: "_D3DTEXTUREFILTERTYPE"
author: windows-driver-content
description: Defines texture filtering modes for a texture stage.
old-location: direct3d9\D3DTEXTUREFILTERTYPE.htm
old-project: direct3d9
ms.assetid: VS|directx_sdk|~\d3dtexturefiltertype.htm
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: 9588a60c-f2d5-03ee-d03c-3d6213b0c72e, D3DTEXF_ANISOTROPIC, D3DTEXF_CONVOLUTIONMONO, D3DTEXF_FORCE_DWORD, D3DTEXF_GAUSSIANQUAD, D3DTEXF_LINEAR, D3DTEXF_NONE, D3DTEXF_POINT, D3DTEXF_PYRAMIDALQUAD, D3DTEXTUREFILTERTYPE, D3DTEXTUREFILTERTYPE enumeration [Direct3D 9], LPD3DTEXTUREFILTERTYPE, LPD3DTEXTUREFILTERTYPE enumeration pointer [Direct3D 9], _D3DTEXTUREFILTERTYPE, d3d9types/D3DTEXF_ANISOTROPIC, d3d9types/D3DTEXF_CONVOLUTIONMONO, d3d9types/D3DTEXF_FORCE_DWORD, d3d9types/D3DTEXF_GAUSSIANQUAD, d3d9types/D3DTEXF_LINEAR, d3d9types/D3DTEXF_NONE, d3d9types/D3DTEXF_POINT, d3d9types/D3DTEXF_PYRAMIDALQUAD, d3d9types/D3DTEXTUREFILTERTYPE, d3d9types/LPD3DTEXTUREFILTERTYPE, direct3d9.D3DTEXTUREFILTERTYPE
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: d3d9types.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: D3DTEXTUREFILTERTYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	D3D9Types.h
api_name:
-	D3DTEXTUREFILTERTYPE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _D3DTEXTUREFILTERTYPE enumeration


## -description


Defines texture filtering modes for a texture stage.


## -enum-fields




### -field D3DTEXF_NONE

When used with <a href="https://msdn.microsoft.com/03a6a5f1-5e4f-4ba8-be4a-74d78fbc85d0">D3DSAMP_MIPFILTER</a>, disables mipmapping.


### -field D3DTEXF_POINT

When used with <a href="https://msdn.microsoft.com/03a6a5f1-5e4f-4ba8-be4a-74d78fbc85d0">D3DSAMP_ MAGFILTER</a> or <a href="https://msdn.microsoft.com/03a6a5f1-5e4f-4ba8-be4a-74d78fbc85d0">D3DSAMP_MINFILTER</a>, 
        specifies that point filtering is to be used as the texture magnification or minification filter respectively. When used 
        with <b>D3DSAMP_MIPFILTER</b>, enables mipmapping and specifies that the rasterizer chooses the color from the 
        texel of the nearest mip level.


### -field D3DTEXF_LINEAR

When used with <a href="https://msdn.microsoft.com/03a6a5f1-5e4f-4ba8-be4a-74d78fbc85d0">D3DSAMP_ MAGFILTER</a> or <a href="https://msdn.microsoft.com/03a6a5f1-5e4f-4ba8-be4a-74d78fbc85d0">D3DSAMP_MINFILTER</a>, 
        specifies that linear filtering is to be used as the texture magnification or minification filter respectively. When used 
        with <b>D3DSAMP_MIPFILTER</b>, enables mipmapping and trilinear filtering; it specifies that the rasterizer 
        interpolates between the two nearest mip levels.


### -field D3DTEXF_ANISOTROPIC

When used with <a href="https://msdn.microsoft.com/03a6a5f1-5e4f-4ba8-be4a-74d78fbc85d0">D3DSAMP_ MAGFILTER</a> or <a href="https://msdn.microsoft.com/03a6a5f1-5e4f-4ba8-be4a-74d78fbc85d0">D3DSAMP_MINFILTER</a>, 
        specifies that anisotropic texture filtering used as a texture magnification or minification filter respectively. 
        Compensates for distortion caused by the difference in angle between the texture polygon and the plane of the screen. 
        Use with <b>D3DSAMP_MIPFILTER</b> is undefined.


### -field D3DTEXF_PYRAMIDALQUAD

A 4-sample tent filter used as a texture magnification or minification filter. 
        Use with <a href="https://msdn.microsoft.com/03a6a5f1-5e4f-4ba8-be4a-74d78fbc85d0">D3DSAMP_MIPFILTER</a> is undefined.


### -field D3DTEXF_GAUSSIANQUAD

A 4-sample Gaussian filter used as a texture magnification or minification filter. 
        Use with <a href="https://msdn.microsoft.com/03a6a5f1-5e4f-4ba8-be4a-74d78fbc85d0">D3DSAMP_MIPFILTER</a> is undefined.


### -field D3DTEXF_CONVOLUTIONMONO

Convolution filter for monochrome textures.  See <a href="https://msdn.microsoft.com/a222e3bb-310c-4019-93ee-6a2da2a46ded">D3DFMT_A1</a>.
          

<table>
<tr>
<td>
Differences between Direct3D 9 and Direct3D 9Ex:

This flag is available in Direct3D 9Ex only.

</td>
</tr>
</table>
 


          Use with <a href="https://msdn.microsoft.com/03a6a5f1-5e4f-4ba8-be4a-74d78fbc85d0">D3DSAMP_MIPFILTER</a> is undefined.
        


### -field D3DTEXF_FORCE_DWORD

Forces this enumeration to compile to 32 bits in size. Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits. This value is not used. 


## -remarks



D3DTEXTUREFILTERTYPE is used by <a href="https://msdn.microsoft.com/2aee31b4-dab0-4a73-ae8a-1bee1876ed8c">IDirect3DDevice9::SetSamplerState</a> along with <a href="https://msdn.microsoft.com/03a6a5f1-5e4f-4ba8-be4a-74d78fbc85d0">D3DSAMPLERSTATETYPE</a> to define texture filtering modes for a texture stage. 

To check if a format supports texture filter types other than D3DTEXF_POINT (which is always supported), call <a href="https://msdn.microsoft.com/39115099-de14-424c-95a8-c5699f5c4c65">IDirect3D9::CheckDeviceFormat</a> with D3DUSAGE_QUERY_FILTER.

Set a texture stage's magnification filter by calling <a href="https://msdn.microsoft.com/2aee31b4-dab0-4a73-ae8a-1bee1876ed8c">IDirect3DDevice9::SetSamplerState</a> with the D3DSAMP_MAGFILTER value as the second parameter and one member of this enumeration as the third parameter.

Set a texture stage's minification filter by calling <a href="https://msdn.microsoft.com/2aee31b4-dab0-4a73-ae8a-1bee1876ed8c">IDirect3DDevice9::SetSamplerState</a> with the D3DSAMP_MINFILTER value as the second parameter and one member of this enumeration as the third parameter.

Set the texture filter to use between-mipmap levels by calling <a href="https://msdn.microsoft.com/2aee31b4-dab0-4a73-ae8a-1bee1876ed8c">IDirect3DDevice9::SetSamplerState</a> with the D3DSAMP_MIPFILTER value as the second parameter and one member of this enumeration as the third parameter.

Not all valid filtering modes for a device will apply to volume maps. In general, D3DTEXF_POINT and D3DTEXF_LINEAR magnification filters will be supported for volume maps. If D3DPTEXTURECAPS_MIPVOLUMEMAP is set, then the D3DTEXF_POINT mipmap filter and D3DTEXF_POINT and D3DTEXF_LINEAR minification filters will be supported for volume maps. The device may or may not support the D3DTEXF_LINEAR mipmap filter for volume maps. Devices that support anisotropic filtering for 2D maps do not necessarily support anisotropic filtering for volume maps. However, applications that enable anisotropic filtering will receive the best available filtering (probably linear) if anisotropic filtering is not supported.




## -see-also




<a href="https://msdn.microsoft.com/03a6a5f1-5e4f-4ba8-be4a-74d78fbc85d0">D3DSAMPLERSTATETYPE</a>



<a href="https://msdn.microsoft.com/ae64eb17-63a8-44c5-8d41-e021c49f338a">Direct3D Enumerations</a>



<a href="https://msdn.microsoft.com/155724ba-71be-4e9f-8c84-bb04f8eec578">ID3DXPatchMesh::GetDisplaceParam</a>



<a href="https://msdn.microsoft.com/4c78e5b3-fb63-4341-a811-5531cf9564e7">ID3DXPatchMesh::SetDisplaceParam</a>



<a href="https://msdn.microsoft.com/2aee31b4-dab0-4a73-ae8a-1bee1876ed8c">IDirect3DDevice9::SetSamplerState</a>
 

 

