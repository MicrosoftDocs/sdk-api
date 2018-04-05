---
UID: NE:d3d9types._D3DBACKBUFFER_TYPE
title: "_D3DBACKBUFFER_TYPE"
author: windows-driver-content
description: Defines constants that describe the type of back buffer.
old-location: direct3d9\D3DBACKBUFFER_TYPE.htm
old-project: direct3d9
ms.assetid: VS|directx_sdk|~\d3dbackbuffer_type.htm
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: 4d4530e6-c8da-c407-71e2-12f95a816014, D3DBACKBUFFER_TYPE, D3DBACKBUFFER_TYPE enumeration [Direct3D 9], D3DBACKBUFFER_TYPE_FORCE_DWORD, D3DBACKBUFFER_TYPE_LEFT, D3DBACKBUFFER_TYPE_MONO, D3DBACKBUFFER_TYPE_RIGHT, LPD3DBACKBUFFER_TYPE, LPD3DBACKBUFFER_TYPE enumeration pointer [Direct3D 9], _D3DBACKBUFFER_TYPE, d3d9types/D3DBACKBUFFER_TYPE, d3d9types/D3DBACKBUFFER_TYPE_FORCE_DWORD, d3d9types/D3DBACKBUFFER_TYPE_LEFT, d3d9types/D3DBACKBUFFER_TYPE_MONO, d3d9types/D3DBACKBUFFER_TYPE_RIGHT, d3d9types/LPD3DBACKBUFFER_TYPE, direct3d9.D3DBACKBUFFER_TYPE
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
req.typenames: D3DBACKBUFFER_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	D3D9Types.h
api_name:
-	D3DBACKBUFFER_TYPE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _D3DBACKBUFFER_TYPE enumeration


## -description


Defines constants that describe the type of back buffer.


## -enum-fields




### -field D3DBACKBUFFER_TYPE_MONO

Specifies a nonstereo swap chain. 


### -field D3DBACKBUFFER_TYPE_LEFT

Specifies the left side of a stereo pair in a swap chain. 


### -field D3DBACKBUFFER_TYPE_RIGHT

Specifies the right side of a stereo pair in a swap chain. 


### -field D3DBACKBUFFER_TYPE_FORCE_DWORD

Forces this enumeration to compile to 32 bits in size. Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits. This value is not used.


## -remarks



Direct3D 9 does not support stereo view, so Direct3D does not use the D3DBACKBUFFER_TYPE_LEFT and D3DBACKBUFFER_TYPE_RIGHT values of this enumerated type.




## -see-also




<a href="https://msdn.microsoft.com/ae64eb17-63a8-44c5-8d41-e021c49f338a">Direct3D Enumerations</a>



<a href="https://msdn.microsoft.com/fac7f4eb-ce6f-4f9d-810c-f3a0ad155cc2">IDirect3DDevice9::GetBackBuffer</a>



<a href="https://msdn.microsoft.com/89fa363f-023d-43aa-8f09-fa80ac49ccb6">IDirect3DSwapChain9::GetBackBuffer</a>
 

 

