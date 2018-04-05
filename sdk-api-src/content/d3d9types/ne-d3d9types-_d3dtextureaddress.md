---
UID: NE:d3d9types._D3DTEXTUREADDRESS
title: "_D3DTEXTUREADDRESS"
author: windows-driver-content
description: Defines constants that describe the supported texture-addressing modes.
old-location: direct3d9\D3DTEXTUREADDRESS.htm
old-project: direct3d9
ms.assetid: VS|directx_sdk|~\d3dtextureaddress.htm
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: 655b514e-0787-3d57-8723-4c7dcfe11098, D3DTADDRESS_BORDER, D3DTADDRESS_CLAMP, D3DTADDRESS_FORCE_DWORD, D3DTADDRESS_MIRROR, D3DTADDRESS_MIRRORONCE, D3DTADDRESS_WRAP, D3DTEXTUREADDRESS, D3DTEXTUREADDRESS enumeration [Direct3D 9], LPD3DTEXTUREADDRESS, LPD3DTEXTUREADDRESS enumeration pointer [Direct3D 9], _D3DTEXTUREADDRESS, d3d9types/D3DTADDRESS_BORDER, d3d9types/D3DTADDRESS_CLAMP, d3d9types/D3DTADDRESS_FORCE_DWORD, d3d9types/D3DTADDRESS_MIRROR, d3d9types/D3DTADDRESS_MIRRORONCE, d3d9types/D3DTADDRESS_WRAP, d3d9types/D3DTEXTUREADDRESS, d3d9types/LPD3DTEXTUREADDRESS, direct3d9.D3DTEXTUREADDRESS
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
req.typenames: D3DTEXTUREADDRESS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	D3D9Types.h
api_name:
-	D3DTEXTUREADDRESS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _D3DTEXTUREADDRESS enumeration


## -description


Defines constants that describe the supported texture-addressing modes.


## -enum-fields




### -field D3DTADDRESS_WRAP

Tile the texture at every integer junction. For example, for u values between 0 and 3, the texture is repeated three times; no mirroring is performed. 


### -field D3DTADDRESS_MIRROR

Similar to D3DTADDRESS_WRAP, except that the texture is flipped at every integer junction. For u values between 0 and 1, for example, the texture is addressed normally; between 1 and 2, the texture is flipped (mirrored); between 2 and 3, the texture is normal again; and so on. 


### -field D3DTADDRESS_CLAMP

Texture coordinates outside the range [0.0, 1.0] are set to the texture color at 0.0 or 1.0, respectively. 


### -field D3DTADDRESS_BORDER

Texture coordinates outside the range [0.0, 1.0] are set to the border color. 


### -field D3DTADDRESS_MIRRORONCE

Similar to D3DTADDRESS_MIRROR and D3DTADDRESS_CLAMP. Takes the absolute value of the texture coordinate (thus, mirroring around 0), and then clamps to the maximum value. The most common usage is for volume textures, where support for the full D3DTADDRESS_MIRRORONCE texture-addressing mode is not necessary, but the data is symmetric around the one axis. 


### -field D3DTADDRESS_FORCE_DWORD

Forces this enumeration to compile to 32 bits in size. Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits. This value is not used. 


## -see-also




<a href="https://msdn.microsoft.com/03a6a5f1-5e4f-4ba8-be4a-74d78fbc85d0">D3DSAMPLERSTATETYPE</a>



<a href="https://msdn.microsoft.com/ae64eb17-63a8-44c5-8d41-e021c49f338a">Direct3D Enumerations</a>
 

 

