---
UID: NE:d3d12.D3D12_TEXTURE_ADDRESS_MODE
title: D3D12_TEXTURE_ADDRESS_MODE
author: windows-sdk-content
description: Identifies a technique for resolving texture coordinates that are outside of the boundaries of a texture.
old-location: direct3d12\d3d12_texture_address_mode.htm
old-project: direct3d12
ms.assetid: 7F67C8B6-1B01-49C0-9900-AFDBEDE5508F
ms.author: windowssdkdev
ms.date: 07/24/2018
ms.keywords: D3D12_TEXTURE_ADDRESS_MODE, D3D12_TEXTURE_ADDRESS_MODE enumeration, D3D12_TEXTURE_ADDRESS_MODE_BORDER, D3D12_TEXTURE_ADDRESS_MODE_CLAMP, D3D12_TEXTURE_ADDRESS_MODE_MIRROR, D3D12_TEXTURE_ADDRESS_MODE_MIRROR_ONCE, D3D12_TEXTURE_ADDRESS_MODE_WRAP, d3d12/D3D12_TEXTURE_ADDRESS_MODE, d3d12/D3D12_TEXTURE_ADDRESS_MODE_BORDER, d3d12/D3D12_TEXTURE_ADDRESS_MODE_CLAMP, d3d12/D3D12_TEXTURE_ADDRESS_MODE_MIRROR, d3d12/D3D12_TEXTURE_ADDRESS_MODE_MIRROR_ONCE, d3d12/D3D12_TEXTURE_ADDRESS_MODE_WRAP, direct3d12.d3d12_texture_address_mode
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: d3d12.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: D3D12_TEXTURE_ADDRESS_MODE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D12.h
api_name:
 - D3D12_TEXTURE_ADDRESS_MODE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# D3D12_TEXTURE_ADDRESS_MODE enumeration


## -description


Identifies a technique for resolving texture coordinates that are outside of the boundaries of a texture.
        


## -enum-fields




### -field D3D12_TEXTURE_ADDRESS_MODE_WRAP

Tile the texture at every (u,v) integer junction.
            For example, for u values between 0 and 3, the texture is repeated three times.
          


### -field D3D12_TEXTURE_ADDRESS_MODE_MIRROR

Flip the texture at every (u,v) integer junction.
            For u values between 0 and 1, for example, the texture is addressed normally; between 1 and 2, the texture is flipped (mirrored); between 2 and 3, the texture is normal again; and so on.
          


### -field D3D12_TEXTURE_ADDRESS_MODE_CLAMP

Texture coordinates outside the range [0.0, 1.0] are set to the texture color at 0.0 or 1.0, respectively.
          


### -field D3D12_TEXTURE_ADDRESS_MODE_BORDER

Texture coordinates outside the range [0.0, 1.0] are set to the border color specified in <a href="https://msdn.microsoft.com/96261FE1-89D4-4135-B5C4-2D788DF4FA12">D3D12_SAMPLER_DESC</a> or HLSL code.
          


### -field D3D12_TEXTURE_ADDRESS_MODE_MIRROR_ONCE

Similar to 
            <a href="https://msdn.microsoft.com/en-us/library/Dn770441(v=VS.85).aspx">D3D12_TEXTURE_ADDRESS_MODE_MIRROR</a> 
            and 
            <a href="https://msdn.microsoft.com/en-us/library/Dn770441(v=VS.85).aspx">D3D12_TEXTURE_ADDRESS_MODE_CLAMP</a>.
            Takes the absolute value of the texture coordinate (thus, mirroring around 0), and then clamps to the maximum value.
          


## -remarks



This enum is used by the <a href="https://msdn.microsoft.com/96261FE1-89D4-4135-B5C4-2D788DF4FA12">D3D12_SAMPLER_DESC</a> structure.
      




## -see-also




<a href="https://msdn.microsoft.com/76E76C85-128E-4F0E-9711-C72C4CF6C835">Core Enumerations</a>
 

 

