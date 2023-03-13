---
UID: NE:d3d12.D3D12_TEXTURE_ADDRESS_MODE
title: D3D12_TEXTURE_ADDRESS_MODE (d3d12.h)
description: Identifies a technique for resolving texture coordinates that are outside of the boundaries of a texture.
helpviewer_keywords: ["D3D12_TEXTURE_ADDRESS_MODE","D3D12_TEXTURE_ADDRESS_MODE enumeration","D3D12_TEXTURE_ADDRESS_MODE_BORDER","D3D12_TEXTURE_ADDRESS_MODE_CLAMP","D3D12_TEXTURE_ADDRESS_MODE_MIRROR","D3D12_TEXTURE_ADDRESS_MODE_MIRROR_ONCE","D3D12_TEXTURE_ADDRESS_MODE_WRAP","d3d12/D3D12_TEXTURE_ADDRESS_MODE","d3d12/D3D12_TEXTURE_ADDRESS_MODE_BORDER","d3d12/D3D12_TEXTURE_ADDRESS_MODE_CLAMP","d3d12/D3D12_TEXTURE_ADDRESS_MODE_MIRROR","d3d12/D3D12_TEXTURE_ADDRESS_MODE_MIRROR_ONCE","d3d12/D3D12_TEXTURE_ADDRESS_MODE_WRAP","direct3d12.d3d12_texture_address_mode"]
old-location: direct3d12\d3d12_texture_address_mode.htm
tech.root: direct3d12
ms.assetid: 7F67C8B6-1B01-49C0-9900-AFDBEDE5508F
ms.date: 12/05/2018
ms.keywords: D3D12_TEXTURE_ADDRESS_MODE, D3D12_TEXTURE_ADDRESS_MODE enumeration, D3D12_TEXTURE_ADDRESS_MODE_BORDER, D3D12_TEXTURE_ADDRESS_MODE_CLAMP, D3D12_TEXTURE_ADDRESS_MODE_MIRROR, D3D12_TEXTURE_ADDRESS_MODE_MIRROR_ONCE, D3D12_TEXTURE_ADDRESS_MODE_WRAP, d3d12/D3D12_TEXTURE_ADDRESS_MODE, d3d12/D3D12_TEXTURE_ADDRESS_MODE_BORDER, d3d12/D3D12_TEXTURE_ADDRESS_MODE_CLAMP, d3d12/D3D12_TEXTURE_ADDRESS_MODE_MIRROR, d3d12/D3D12_TEXTURE_ADDRESS_MODE_MIRROR_ONCE, d3d12/D3D12_TEXTURE_ADDRESS_MODE_WRAP, direct3d12.d3d12_texture_address_mode
req.header: d3d12.h
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
req.typenames: D3D12_TEXTURE_ADDRESS_MODE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D12_TEXTURE_ADDRESS_MODE
 - d3d12/D3D12_TEXTURE_ADDRESS_MODE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D12.h
api_name:
 - D3D12_TEXTURE_ADDRESS_MODE
---

# D3D12_TEXTURE_ADDRESS_MODE enumeration


## -description

Identifies a technique for resolving texture coordinates that are outside of the boundaries of a texture.

## -enum-fields

### -field D3D12_TEXTURE_ADDRESS_MODE_WRAP:1

Tile the texture at every (u,v) integer junction.
            For example, for u values between 0 and 3, the texture is repeated three times.

### -field D3D12_TEXTURE_ADDRESS_MODE_MIRROR:2

Flip the texture at every (u,v) integer junction.
            For u values between 0 and 1, for example, the texture is addressed normally; between 1 and 2, the texture is flipped (mirrored); between 2 and 3, the texture is normal again; and so on.

### -field D3D12_TEXTURE_ADDRESS_MODE_CLAMP:3

Texture coordinates outside the range [0.0, 1.0] are set to the texture color at 0.0 or 1.0, respectively.

### -field D3D12_TEXTURE_ADDRESS_MODE_BORDER:4

Texture coordinates outside the range [0.0, 1.0] are set to the border color specified in <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_sampler_desc">D3D12_SAMPLER_DESC</a> or HLSL code.

### -field D3D12_TEXTURE_ADDRESS_MODE_MIRROR_ONCE:5

Similar to 
            <a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode">D3D12_TEXTURE_ADDRESS_MODE_MIRROR</a> 
            and 
            <a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode">D3D12_TEXTURE_ADDRESS_MODE_CLAMP</a>.
            Takes the absolute value of the texture coordinate (thus, mirroring around 0), and then clamps to the maximum value.

## -remarks

This enum is used by the <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_sampler_desc">D3D12_SAMPLER_DESC</a> structure.

## -see-also

<a href="/windows/desktop/direct3d12/direct3d-12-enumerations">Core Enumerations</a>
