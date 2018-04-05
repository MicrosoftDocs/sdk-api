---
UID: NE:d3d9types._D3DSAMPLER_TEXTURE_TYPE
title: "_D3DSAMPLER_TEXTURE_TYPE"
author: windows-driver-content
description: Defines the sampler texture types for vertex shaders.
old-location: direct3d9\D3DSAMPLER_TEXTURE_TYPE.htm
old-project: direct3d9
ms.assetid: VS|directx_sdk|~\d3dsampler_texture_type.htm
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: D3DSAMPLER_TEXTURE_TYPE, D3DSAMPLER_TEXTURE_TYPE enumeration [Direct3D 9], D3DSTT_2D, D3DSTT_CUBE, D3DSTT_FORCE_DWORD, D3DSTT_UNKNOWN, D3DSTT_VOLUME, LPD3DSAMPLER_TEXTURE_TYPE, LPD3DSAMPLER_TEXTURE_TYPE enumeration pointer [Direct3D 9], _D3DSAMPLER_TEXTURE_TYPE, d3d9types/D3DSAMPLER_TEXTURE_TYPE, d3d9types/D3DSTT_2D, d3d9types/D3DSTT_CUBE, d3d9types/D3DSTT_FORCE_DWORD, d3d9types/D3DSTT_UNKNOWN, d3d9types/D3DSTT_VOLUME, d3d9types/LPD3DSAMPLER_TEXTURE_TYPE, direct3d9.D3DSAMPLER_TEXTURE_TYPE, f9cfd299-8bbb-9fce-6a77-95662c3e17eb
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
req.typenames: D3DSAMPLER_TEXTURE_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	D3D9Types.h
api_name:
-	D3DSAMPLER_TEXTURE_TYPE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _D3DSAMPLER_TEXTURE_TYPE enumeration


## -description


Defines the sampler texture types for vertex shaders.


## -enum-fields




### -field D3DSTT_UNKNOWN

Uninitialized value. The value of this element is D3DSP_TEXTURETYPE_SHIFT.


### -field D3DSTT_2D

Declaring a 2D texture. The value of this element is D3DSP_TEXTURETYPE_SHIFT * 4.


### -field D3DSTT_CUBE

Declaring a cube texture. The value of this element is D3DSP_TEXTURETYPE_SHIFT * 8.


### -field D3DSTT_VOLUME

Declaring a volume texture. The value of this element is D3DSP_TEXTURETYPE_SHIFT * 16.


### -field D3DSTT_FORCE_DWORD

Forces this enumeration to compile to 32 bits in size. Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits. This value is not used.


## -see-also




<a href="https://msdn.microsoft.com/ae64eb17-63a8-44c5-8d41-e021c49f338a">Direct3D Enumerations</a>
 

 

