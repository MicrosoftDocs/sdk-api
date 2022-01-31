---
UID: NE:d3d11.D3D11_TEXTURE_ADDRESS_MODE
title: D3D11_TEXTURE_ADDRESS_MODE (d3d11.h)
description: Identify a technique for resolving texture coordinates that are outside of the boundaries of a texture.
helpviewer_keywords: ["2e717137-eb31-02da-bc07-a90f0bfe6795","D3D11_TEXTURE_ADDRESS_BORDER","D3D11_TEXTURE_ADDRESS_CLAMP","D3D11_TEXTURE_ADDRESS_MIRROR","D3D11_TEXTURE_ADDRESS_MIRROR_ONCE","D3D11_TEXTURE_ADDRESS_MODE","D3D11_TEXTURE_ADDRESS_MODE enumeration [Direct3D 11]","D3D11_TEXTURE_ADDRESS_WRAP","d3d11/D3D11_TEXTURE_ADDRESS_BORDER","d3d11/D3D11_TEXTURE_ADDRESS_CLAMP","d3d11/D3D11_TEXTURE_ADDRESS_MIRROR","d3d11/D3D11_TEXTURE_ADDRESS_MIRROR_ONCE","d3d11/D3D11_TEXTURE_ADDRESS_MODE","d3d11/D3D11_TEXTURE_ADDRESS_WRAP","direct3d11.d3d11_texture_address_mode"]
old-location: direct3d11\d3d11_texture_address_mode.htm
tech.root: direct3d11
ms.assetid: 4877e5db-011a-4a15-a087-5a55f229fa2a
ms.date: 12/05/2018
ms.keywords: 2e717137-eb31-02da-bc07-a90f0bfe6795, D3D11_TEXTURE_ADDRESS_BORDER, D3D11_TEXTURE_ADDRESS_CLAMP, D3D11_TEXTURE_ADDRESS_MIRROR, D3D11_TEXTURE_ADDRESS_MIRROR_ONCE, D3D11_TEXTURE_ADDRESS_MODE, D3D11_TEXTURE_ADDRESS_MODE enumeration [Direct3D 11], D3D11_TEXTURE_ADDRESS_WRAP, d3d11/D3D11_TEXTURE_ADDRESS_BORDER, d3d11/D3D11_TEXTURE_ADDRESS_CLAMP, d3d11/D3D11_TEXTURE_ADDRESS_MIRROR, d3d11/D3D11_TEXTURE_ADDRESS_MIRROR_ONCE, d3d11/D3D11_TEXTURE_ADDRESS_MODE, d3d11/D3D11_TEXTURE_ADDRESS_WRAP, direct3d11.d3d11_texture_address_mode
req.header: d3d11.h
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
targetos: Windows
req.typenames: D3D11_TEXTURE_ADDRESS_MODE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D11_TEXTURE_ADDRESS_MODE
 - d3d11/D3D11_TEXTURE_ADDRESS_MODE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D11.h
api_name:
 - D3D11_TEXTURE_ADDRESS_MODE
---

# D3D11_TEXTURE_ADDRESS_MODE enumeration


## -description

Identify a technique for resolving texture coordinates that are outside of the boundaries of a texture.

## -enum-fields

### -field D3D11_TEXTURE_ADDRESS_WRAP:1

Tile the texture at every (u,v) integer junction. For example, for u values between 0 and 3, the texture is repeated three times.

### -field D3D11_TEXTURE_ADDRESS_MIRROR:2

Flip the texture at every (u,v) integer junction. For u values between 0 and 1, for example, the texture is addressed normally; between 1 and 2, the texture is flipped (mirrored); between 2 and 3, the texture is normal again; and so on.

### -field D3D11_TEXTURE_ADDRESS_CLAMP:3

Texture coordinates outside the range [0.0, 1.0] are set to the texture color at 0.0 or 1.0, respectively.

### -field D3D11_TEXTURE_ADDRESS_BORDER:4

Texture coordinates outside the range [0.0, 1.0] are set to the border color specified in <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_sampler_desc">D3D11_SAMPLER_DESC</a> or HLSL code.

### -field D3D11_TEXTURE_ADDRESS_MIRROR_ONCE:5

Similar to D3D11_TEXTURE_ADDRESS_MIRROR and D3D11_TEXTURE_ADDRESS_CLAMP. Takes the absolute value of the texture coordinate (thus, mirroring around 0), and then clamps to the maximum value.

## -see-also

<a href="/windows/desktop/direct3d11/d3d11-graphics-reference-d3d11-core-enums">Core Enumerations</a>
