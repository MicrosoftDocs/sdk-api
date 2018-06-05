---
UID: NE:d3d11.D3D11_TEXTURE_ADDRESS_MODE
title: D3D11_TEXTURE_ADDRESS_MODE
author: windows-sdk-content
description: Identify a technique for resolving texture coordinates that are outside of the boundaries of a texture.
old-location: direct3d11\d3d11_texture_address_mode.htm
old-project: direct3d11
ms.assetid: 4877e5db-011a-4a15-a087-5a55f229fa2a
ms.author: windowssdkdev
ms.date: 04/06/2018
ms.keywords: 2e717137-eb31-02da-bc07-a90f0bfe6795, D3D11_TEXTURE_ADDRESS_BORDER, D3D11_TEXTURE_ADDRESS_CLAMP, D3D11_TEXTURE_ADDRESS_MIRROR, D3D11_TEXTURE_ADDRESS_MIRROR_ONCE, D3D11_TEXTURE_ADDRESS_MODE, D3D11_TEXTURE_ADDRESS_MODE enumeration [Direct3D 11], D3D11_TEXTURE_ADDRESS_WRAP, d3d11/D3D11_TEXTURE_ADDRESS_BORDER, d3d11/D3D11_TEXTURE_ADDRESS_CLAMP, d3d11/D3D11_TEXTURE_ADDRESS_MIRROR, d3d11/D3D11_TEXTURE_ADDRESS_MIRROR_ONCE, d3d11/D3D11_TEXTURE_ADDRESS_MODE, d3d11/D3D11_TEXTURE_ADDRESS_WRAP, direct3d11.d3d11_texture_address_mode
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
tech.root: 
req.typenames: D3D11_TEXTURE_ADDRESS_MODE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	D3D11.h
api_name:
-	D3D11_TEXTURE_ADDRESS_MODE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# D3D11_TEXTURE_ADDRESS_MODE enumeration


## -description


Identify a technique for resolving texture coordinates that are outside of the boundaries of a texture.


## -enum-fields




### -field D3D11_TEXTURE_ADDRESS_WRAP

Tile the texture at every (u,v) integer junction. For example, for u values between 0 and 3, the texture is repeated three times.


### -field D3D11_TEXTURE_ADDRESS_MIRROR

Flip the texture at every (u,v) integer junction. For u values between 0 and 1, for example, the texture is addressed normally; between 1 and 2, the texture is flipped (mirrored); between 2 and 3, the texture is normal again; and so on. 


### -field D3D11_TEXTURE_ADDRESS_CLAMP

Texture coordinates outside the range [0.0, 1.0] are set to the texture color at 0.0 or 1.0, respectively.


### -field D3D11_TEXTURE_ADDRESS_BORDER

Texture coordinates outside the range [0.0, 1.0] are set to the border color specified in <a href="https://msdn.microsoft.com/97dd6cac-6657-4a1e-b631-4e5d36994b16">D3D11_SAMPLER_DESC</a> or HLSL code.


### -field D3D11_TEXTURE_ADDRESS_MIRROR_ONCE

Similar to D3D11_TEXTURE_ADDRESS_MIRROR and D3D11_TEXTURE_ADDRESS_CLAMP. Takes the absolute value of the texture coordinate (thus, mirroring around 0), and then clamps to the maximum value.


## -see-also




<a href="https://msdn.microsoft.com/1641713a-5ac8-4597-900b-1bba54f9f522">Core Enumerations</a>
 

 

