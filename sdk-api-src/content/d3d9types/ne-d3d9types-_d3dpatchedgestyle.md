---
UID: NE:d3d9types._D3DPATCHEDGESTYLE
title: "_D3DPATCHEDGESTYLE"
author: windows-driver-content
description: Defines whether the current tessellation mode is discrete or continuous.
old-location: direct3d9\D3DPATCHEDGESTYLE.htm
old-project: direct3d9
ms.assetid: VS|directx_sdk|~\d3dpatchedgestyle.htm
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: D3DPATCHEDGESTYLE, D3DPATCHEDGESTYLE enumeration [Direct3D 9], D3DPATCHEDGE_CONTINUOUS, D3DPATCHEDGE_DISCRETE, D3DPATCHEDGE_FORCE_DWORD, LPD3DPATCHEDGESTYLE, LPD3DPATCHEDGESTYLE enumeration pointer [Direct3D 9], _D3DPATCHEDGESTYLE, d3d9types/D3DPATCHEDGESTYLE, d3d9types/D3DPATCHEDGE_CONTINUOUS, d3d9types/D3DPATCHEDGE_DISCRETE, d3d9types/D3DPATCHEDGE_FORCE_DWORD, d3d9types/LPD3DPATCHEDGESTYLE, direct3d9.D3DPATCHEDGESTYLE, f3aec000-3703-0450-f58d-4e505db26234
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
req.typenames: D3DPATCHEDGESTYLE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	D3D9Types.h
api_name:
-	D3DPATCHEDGESTYLE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _D3DPATCHEDGESTYLE enumeration


## -description


Defines whether the current tessellation mode is discrete or continuous.


## -enum-fields




### -field D3DPATCHEDGE_DISCRETE

Discrete edge style. In discrete mode, you can specify float tessellation but it will be truncated to integers. 


### -field D3DPATCHEDGE_CONTINUOUS

Continuous edge style. In continuous mode, tessellation is specified as float values that can be smoothly varied to reduce "popping" artifacts. 


### -field D3DPATCHEDGE_FORCE_DWORD

Forces this enumeration to compile to 32 bits in size. Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits. This value is not used. 


## -remarks



Note that continuous tessellation produces a completely different tessellation pattern from the discrete one for the same tessellation values (this is more apparent in wireframe mode). Thus, 4.0 continuous is not the same as 4 discrete.




## -see-also




<a href="https://msdn.microsoft.com/ae64eb17-63a8-44c5-8d41-e021c49f338a">Direct3D Enumerations</a>
 

 

