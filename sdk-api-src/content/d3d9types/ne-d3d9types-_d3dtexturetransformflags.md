---
UID: NE:d3d9types._D3DTEXTURETRANSFORMFLAGS
title: "_D3DTEXTURETRANSFORMFLAGS"
author: windows-driver-content
description: Defines texture coordinate transformation values.
old-location: direct3d9\D3DTEXTURETRANSFORMFLAGS.htm
old-project: direct3d9
ms.assetid: VS|directx_sdk|~\d3dtexturetransformflags.htm
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: 96302bad-3e15-fc8d-86d4-482118ce89dd, D3DTEXTURETRANSFORMFLAGS, D3DTEXTURETRANSFORMFLAGS enumeration [Direct3D 9], D3DTTFF_COUNT1, D3DTTFF_COUNT2, D3DTTFF_COUNT3, D3DTTFF_COUNT4, D3DTTFF_DISABLE, D3DTTFF_FORCE_DWORD, D3DTTFF_PROJECTED, LPD3DTEXTURETRANSFORMFLAGS, LPD3DTEXTURETRANSFORMFLAGS enumeration pointer [Direct3D 9], _D3DTEXTURETRANSFORMFLAGS, d3d9types/D3DTEXTURETRANSFORMFLAGS, d3d9types/D3DTTFF_COUNT1, d3d9types/D3DTTFF_COUNT2, d3d9types/D3DTTFF_COUNT3, d3d9types/D3DTTFF_COUNT4, d3d9types/D3DTTFF_DISABLE, d3d9types/D3DTTFF_FORCE_DWORD, d3d9types/D3DTTFF_PROJECTED, d3d9types/LPD3DTEXTURETRANSFORMFLAGS, direct3d9.D3DTEXTURETRANSFORMFLAGS
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
req.typenames: D3DTEXTURETRANSFORMFLAGS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	D3D9Types.h
api_name:
-	D3DTEXTURETRANSFORMFLAGS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _D3DTEXTURETRANSFORMFLAGS enumeration


## -description


Defines texture coordinate transformation values.


## -enum-fields




### -field D3DTTFF_DISABLE

Texture coordinates are passed directly to the rasterizer. 


### -field D3DTTFF_COUNT1

The rasterizer should expect 1D texture coordinates. This value is used by fixed function vertex processing; it should be set to 0 when using a programmable vertex shader.


### -field D3DTTFF_COUNT2

The rasterizer should expect 2D texture coordinates. This value is used by fixed function vertex processing; it should be set to 0 when using a programmable vertex shader.


### -field D3DTTFF_COUNT3

The rasterizer should expect 3D texture coordinates. This value is used by fixed function vertex processing; it should be set to 0 when using a programmable vertex shader.


### -field D3DTTFF_COUNT4

The rasterizer should expect 4D texture coordinates. This value is used by fixed function vertex processing; it should be set to 0 when using a programmable vertex shader.


### -field D3DTTFF_PROJECTED

This flag is honored by the fixed function pixel pipeline, as well as the programmable pixel pipeline in versions ps_1_1 to ps_1_3. When texture projection is enabled for a texture stage, all four floating point values must be written to the corresponding texture register. Each texture coordinate is divided by the last element before being passed to the rasterizer. For example, if this flag is specified with the D3DTTFF_COUNT3 flag, the first and second texture coordinates are divided by the third coordinate before being passed to the rasterizer. 


### -field D3DTTFF_FORCE_DWORD

Forces this enumeration to compile to 32 bits in size. Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits. This value is not used. 


## -remarks



Texture coordinates can be transformed using a 4 x 4 matrix before the results are passed to the rasterizer. The texture coordinate transforms are set by calling <a href="https://msdn.microsoft.com/303f7a80-edaf-4106-a4ce-8fb7a7d30a5a">IDirect3DDevice9::SetTextureStageState</a>, and by passing in the D3DTSS_TEXTURETRANSFORMFLAGS texture stage state and one of the values from <b>D3DTEXTURETRANSFORMFLAGS</b>. For more information about texture transforms, see <a href="https://msdn.microsoft.com/f36439de-e37a-457c-9485-a435847eb01e">Texture Coordinate Transformations (Direct3D 9)</a>.




## -see-also




<a href="https://msdn.microsoft.com/87a5a1bb-e748-4c72-8320-ea82250dcc0e">D3DTEXTURESTAGESTATETYPE</a>



<a href="https://msdn.microsoft.com/ae64eb17-63a8-44c5-8d41-e021c49f338a">Direct3D Enumerations</a>
 

 

