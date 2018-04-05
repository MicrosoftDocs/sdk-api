---
UID: NE:d3d9types._D3DSTENCILOP
title: "_D3DSTENCILOP"
author: windows-driver-content
description: Defines stencil-buffer operations.
old-location: direct3d9\D3DSTENCILOP.htm
old-project: direct3d9
ms.assetid: VS|directx_sdk|~\d3dstencilop.htm
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: 1255f029-b694-ee4b-9a4d-390d6ac34f6b, D3DSTENCILOP, D3DSTENCILOP enumeration [Direct3D 9], D3DSTENCILOP_DECR, D3DSTENCILOP_DECRSAT, D3DSTENCILOP_FORCE_DWORD, D3DSTENCILOP_INCR, D3DSTENCILOP_INCRSAT, D3DSTENCILOP_INVERT, D3DSTENCILOP_KEEP, D3DSTENCILOP_REPLACE, D3DSTENCILOP_ZERO, LPD3DSTENCILOP, LPD3DSTENCILOP enumeration pointer [Direct3D 9], _D3DSTENCILOP, d3d9types/D3DSTENCILOP, d3d9types/D3DSTENCILOP_DECR, d3d9types/D3DSTENCILOP_DECRSAT, d3d9types/D3DSTENCILOP_FORCE_DWORD, d3d9types/D3DSTENCILOP_INCR, d3d9types/D3DSTENCILOP_INCRSAT, d3d9types/D3DSTENCILOP_INVERT, d3d9types/D3DSTENCILOP_KEEP, d3d9types/D3DSTENCILOP_REPLACE, d3d9types/D3DSTENCILOP_ZERO, d3d9types/LPD3DSTENCILOP, direct3d9.D3DSTENCILOP
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
req.typenames: D3DSTENCILOP
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	D3D9Types.h
api_name:
-	D3DSTENCILOP
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _D3DSTENCILOP enumeration


## -description


Defines stencil-buffer operations.


## -enum-fields




### -field D3DSTENCILOP_KEEP

Do not update the entry in the stencil buffer. This is the default value.


### -field D3DSTENCILOP_ZERO

Set the stencil-buffer entry to 0.


### -field D3DSTENCILOP_REPLACE

Replace the stencil-buffer entry with a reference value.


### -field D3DSTENCILOP_INCRSAT

Increment the stencil-buffer entry, clamping to the maximum value.


### -field D3DSTENCILOP_DECRSAT

Decrement the stencil-buffer entry, clamping to zero.


### -field D3DSTENCILOP_INVERT

Invert the bits in the stencil-buffer entry.


### -field D3DSTENCILOP_INCR

Increment the stencil-buffer entry, wrapping to zero if the new value exceeds the maximum value.


### -field D3DSTENCILOP_DECR

Decrement the stencil-buffer entry, wrapping to the maximum value if the new value is less than zero.


### -field D3DSTENCILOP_FORCE_DWORD

Forces this enumeration to compile to 32 bits in size. Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits. This value is not used.


## -remarks



Stencil-buffer entries are integer values ranging from 0 through 2ⁿ - 1, where n is the bit depth of the stencil buffer.




## -see-also




<a href="https://msdn.microsoft.com/ae64eb17-63a8-44c5-8d41-e021c49f338a">Direct3D Enumerations</a>
 

 

