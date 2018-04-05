---
UID: NE:d3d9types._D3DSAMPLERSTATETYPE
title: "_D3DSAMPLERSTATETYPE"
author: windows-driver-content
description: Sampler states define texture sampling operations such as texture addressing and texture filtering.
old-location: direct3d9\D3DSAMPLERSTATETYPE.htm
old-project: direct3d9
ms.assetid: VS|directx_sdk|~\d3dsamplerstatetype.htm
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: 247408e1-4c94-67a9-b72f-0ea9a25d075e, D3DSAMPLERSTATETYPE, D3DSAMPLERSTATETYPE enumeration [Direct3D 9], D3DSAMP_ADDRESSU, D3DSAMP_ADDRESSV, D3DSAMP_ADDRESSW, D3DSAMP_BORDERCOLOR, D3DSAMP_DMAPOFFSET, D3DSAMP_ELEMENTINDEX, D3DSAMP_FORCE_DWORD, D3DSAMP_MAGFILTER, D3DSAMP_MAXANISOTROPY, D3DSAMP_MAXMIPLEVEL, D3DSAMP_MINFILTER, D3DSAMP_MIPFILTER, D3DSAMP_MIPMAPLODBIAS, D3DSAMP_SRGBTEXTURE, LPD3DSAMPLERSTATETYPE, LPD3DSAMPLERSTATETYPE enumeration pointer [Direct3D 9], _D3DSAMPLERSTATETYPE, d3d9types/D3DSAMPLERSTATETYPE, d3d9types/D3DSAMP_ADDRESSU, d3d9types/D3DSAMP_ADDRESSV, d3d9types/D3DSAMP_ADDRESSW, d3d9types/D3DSAMP_BORDERCOLOR, d3d9types/D3DSAMP_DMAPOFFSET, d3d9types/D3DSAMP_ELEMENTINDEX, d3d9types/D3DSAMP_FORCE_DWORD, d3d9types/D3DSAMP_MAGFILTER, d3d9types/D3DSAMP_MAXANISOTROPY, d3d9types/D3DSAMP_MAXMIPLEVEL, d3d9types/D3DSAMP_MINFILTER, d3d9types/D3DSAMP_MIPFILTER, d3d9types/D3DSAMP_MIPMAPLODBIAS, d3d9types/D3DSAMP_SRGBTEXTURE, d3d9types/LPD3DSAMPLERSTATETYPE, direct3d9.D3DSAMPLERSTATETYPE
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
req.typenames: D3DSAMPLERSTATETYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	D3D9Types.h
api_name:
-	D3DSAMPLERSTATETYPE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _D3DSAMPLERSTATETYPE enumeration


## -description


Sampler states define texture sampling operations such as texture addressing and texture filtering. Some sampler states set-up vertex processing, and some set-up pixel processing. Sampler states can be saved and restored using stateblocks (see <a href="https://msdn.microsoft.com/6b1917a8-8685-40c3-983d-6bd2fed95642">State Blocks Save and Restore State (Direct3D 9)</a>).


## -enum-fields




### -field D3DSAMP_ADDRESSU

Texture-address mode for the u coordinate. The default is D3DTADDRESS_WRAP. For more information, see <a href="https://msdn.microsoft.com/5c03c55f-4a74-4b0e-ba05-e4a6582ff47c">D3DTEXTUREADDRESS</a>.


### -field D3DSAMP_ADDRESSV

Texture-address mode for the v coordinate. The default is D3DTADDRESS_WRAP. For more information, see <a href="https://msdn.microsoft.com/5c03c55f-4a74-4b0e-ba05-e4a6582ff47c">D3DTEXTUREADDRESS</a>.


### -field D3DSAMP_ADDRESSW

Texture-address mode for the w coordinate. The default is D3DTADDRESS_WRAP. For more information, see <a href="https://msdn.microsoft.com/5c03c55f-4a74-4b0e-ba05-e4a6582ff47c">D3DTEXTUREADDRESS</a>.


### -field D3DSAMP_BORDERCOLOR

Border color or type <a href="https://msdn.microsoft.com/a4425774-fd4b-4f5c-9e10-7679bc2795f6">D3DCOLOR</a>. The default color is 0x00000000.


### -field D3DSAMP_MAGFILTER

Magnification filter of type <a href="https://msdn.microsoft.com/4e0420fa-ac76-4be4-90d7-944d8d5a5de1">D3DTEXTUREFILTERTYPE</a>. The default value is D3DTEXF_POINT.


### -field D3DSAMP_MINFILTER

Minification filter of type <a href="https://msdn.microsoft.com/4e0420fa-ac76-4be4-90d7-944d8d5a5de1">D3DTEXTUREFILTERTYPE</a>. The default value is D3DTEXF_POINT.


### -field D3DSAMP_MIPFILTER

Mipmap filter to use during minification. See <a href="https://msdn.microsoft.com/4e0420fa-ac76-4be4-90d7-944d8d5a5de1">D3DTEXTUREFILTERTYPE</a>. The default value is D3DTEXF_NONE.


### -field D3DSAMP_MIPMAPLODBIAS

Mipmap level-of-detail bias. The default value is zero.


### -field D3DSAMP_MAXMIPLEVEL

level-of-detail index of largest map to use. Values range from 0 to (n - 1) where 0 is the largest. The default value is zero.


### -field D3DSAMP_MAXANISOTROPY

DWORD maximum anisotropy. Values range from 1 to the value that is specified in the <b>MaxAnisotropy</b> member of the <a href="https://msdn.microsoft.com/44457b7b-a1f7-4019-b971-8ec2334d3313">D3DCAPS9</a> structure. The default value is 1.


### -field D3DSAMP_SRGBTEXTURE

Gamma correction value. The default value is 0, which means gamma is 1.0 and no correction is required. Otherwise, this value means that the sampler should assume gamma of 2.2 on the content and convert it to linear (gamma 1.0) before presenting it to the pixel shader.


### -field D3DSAMP_ELEMENTINDEX

When a multielement texture is assigned to the sampler, this indicates which element index to use.  The default value is 0.


### -field D3DSAMP_DMAPOFFSET

Vertex offset in the presampled displacement map. This is a constant used by the tessellator, its default value is 0.


### -field D3DSAMP_FORCE_DWORD

Forces this enumeration to compile to 32 bits in size. Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits. This value is not used.


## -see-also




<a href="https://msdn.microsoft.com/ae64eb17-63a8-44c5-8d41-e021c49f338a">Direct3D Enumerations</a>
 

 

