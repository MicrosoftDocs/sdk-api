---
UID: NE:d3d9types._D3DCULL
title: "_D3DCULL"
author: windows-driver-content
description: Defines the supported culling modes.
old-location: direct3d9\D3DCULL.htm
old-project: direct3d9
ms.assetid: VS|directx_sdk|~\d3dcull.htm
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: 161e5ddf-00e7-cee5-3e06-bec289b41693, D3DCULL, D3DCULL enumeration [Direct3D 9], D3DCULL_CCW, D3DCULL_CW, D3DCULL_FORCE_DWORD, D3DCULL_NONE, LPD3DCULL, LPD3DCULL enumeration pointer [Direct3D 9], _D3DCULL, d3d9types/D3DCULL, d3d9types/D3DCULL_CCW, d3d9types/D3DCULL_CW, d3d9types/D3DCULL_FORCE_DWORD, d3d9types/D3DCULL_NONE, d3d9types/LPD3DCULL, direct3d9.D3DCULL
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
req.typenames: D3DCULL
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	D3D9Types.h
api_name:
-	D3DCULL
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _D3DCULL enumeration


## -description


Defines the supported culling modes.


## -enum-fields




### -field D3DCULL_NONE

Do not cull back faces. 


### -field D3DCULL_CW

Cull back faces with clockwise vertices. 


### -field D3DCULL_CCW

Cull back faces with counterclockwise vertices. 


### -field D3DCULL_FORCE_DWORD

Forces this enumeration to compile to 32 bits in size. Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits. This value is not used. 


## -remarks



The values in this enumerated type are used by the D3DRS_CULLMODE render state. The culling modes define how back faces are culled when rendering a geometry.




## -see-also




<a href="https://msdn.microsoft.com/44457b7b-a1f7-4019-b971-8ec2334d3313">D3DCAPS9</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff549036">D3DRENDERSTATETYPE</a>



<a href="https://msdn.microsoft.com/ae64eb17-63a8-44c5-8d41-e021c49f338a">Direct3D Enumerations</a>
 

 

