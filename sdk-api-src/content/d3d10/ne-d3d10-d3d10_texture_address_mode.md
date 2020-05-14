---
UID: NE:d3d10.D3D10_TEXTURE_ADDRESS_MODE
title: D3D10_TEXTURE_ADDRESS_MODE (d3d10.h)
description: Identify a technique for resolving texture coordinates that are outside of the boundaries of a texture.helpviewer_keywords: ["D3D10_TEXTURE_ADDRESS_BORDER","D3D10_TEXTURE_ADDRESS_CLAMP","D3D10_TEXTURE_ADDRESS_MIRROR","D3D10_TEXTURE_ADDRESS_MIRROR_ONCE","D3D10_TEXTURE_ADDRESS_MODE","D3D10_TEXTURE_ADDRESS_MODE enumeration [Direct3D 10]","D3D10_TEXTURE_ADDRESS_WRAP","d3d10/D3D10_TEXTURE_ADDRESS_BORDER","d3d10/D3D10_TEXTURE_ADDRESS_CLAMP","d3d10/D3D10_TEXTURE_ADDRESS_MIRROR","d3d10/D3D10_TEXTURE_ADDRESS_MIRROR_ONCE","d3d10/D3D10_TEXTURE_ADDRESS_MODE","d3d10/D3D10_TEXTURE_ADDRESS_WRAP","d54f3184-32a0-80ea-d0db-214c902889c1","direct3d10.d3d10_texture_address_mode"]
old-location: direct3d10\d3d10_texture_address_mode.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10_texture_address_mode.htm
ms.date: 12/05/2018
ms.keywords: D3D10_TEXTURE_ADDRESS_BORDER, D3D10_TEXTURE_ADDRESS_CLAMP, D3D10_TEXTURE_ADDRESS_MIRROR, D3D10_TEXTURE_ADDRESS_MIRROR_ONCE, D3D10_TEXTURE_ADDRESS_MODE, D3D10_TEXTURE_ADDRESS_MODE enumeration [Direct3D 10], D3D10_TEXTURE_ADDRESS_WRAP, d3d10/D3D10_TEXTURE_ADDRESS_BORDER, d3d10/D3D10_TEXTURE_ADDRESS_CLAMP, d3d10/D3D10_TEXTURE_ADDRESS_MIRROR, d3d10/D3D10_TEXTURE_ADDRESS_MIRROR_ONCE, d3d10/D3D10_TEXTURE_ADDRESS_MODE, d3d10/D3D10_TEXTURE_ADDRESS_WRAP, d54f3184-32a0-80ea-d0db-214c902889c1, direct3d10.d3d10_texture_address_mode
f1_keywords:
- d3d10/D3D10_TEXTURE_ADDRESS_MODE
dev_langs:
- c++
req.header: d3d10.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- D3D10.h
api_name:
- D3D10_TEXTURE_ADDRESS_MODE
targetos: Windows
req.typenames: D3D10_TEXTURE_ADDRESS_MODE
req.redist: 
ms.custom: 19H1
---

# D3D10_TEXTURE_ADDRESS_MODE enumeration


## -description


Identify a technique for resolving texture coordinates that are outside of the boundaries of a texture.


## -enum-fields




### -field D3D10_TEXTURE_ADDRESS_WRAP

Tile the texture at every integer junction. For example, for u values between 0 and 3, the texture is repeated three times.


### -field D3D10_TEXTURE_ADDRESS_MIRROR

Flip the texture at every integer junction. For u values between 0 and 1, for example, the texture is addressed normally; between 1 and 2, the texture is flipped (mirrored); between 2 and 3, the texture is normal again; and so on. 


### -field D3D10_TEXTURE_ADDRESS_CLAMP

Texture coordinates outside the range [0.0, 1.0] are set to the texture color at 0.0 or 1.0, respectively.


### -field D3D10_TEXTURE_ADDRESS_BORDER

Texture coordinates outside the range [0.0, 1.0] are set to the border color specified in <a href="https://docs.microsoft.com/windows/desktop/api/d3d10/ns-d3d10-d3d10_sampler_desc">D3D10_SAMPLER_DESC</a> or HLSL code.


### -field D3D10_TEXTURE_ADDRESS_MIRROR_ONCE

Similar to D3D10_TEXTURE_ADDRESS_MIRROR and D3D10_TEXTURE_ADDRESS_CLAMP. Takes the absolute value of the texture coordinate (thus, mirroring around 0), and then clamps to the maximum value.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/direct3d10/d3d10-graphics-reference-d3d10-core-enums">Core Enumerations</a>
 

 

