---
UID: NE:d3d9types._D3DFILLMODE
title: "_D3DFILLMODE"
author: windows-driver-content
description: Defines constants describing the fill mode.
old-location: direct3d9\D3DFILLMODE.htm
old-project: direct3d9
ms.assetid: VS|directx_sdk|~\d3dfillmode.htm
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: D3DFILLMODE, D3DFILLMODE enumeration [Direct3D 9], D3DFILL_FORCE_DWORD, D3DFILL_POINT, D3DFILL_SOLID, D3DFILL_WIREFRAME, LPD3DFILLMODE, LPD3DFILLMODE enumeration pointer [Direct3D 9], _D3DFILLMODE, c483e1f3-104e-ec60-a572-4c78961ba6f0, d3d9types/D3DFILLMODE, d3d9types/D3DFILL_FORCE_DWORD, d3d9types/D3DFILL_POINT, d3d9types/D3DFILL_SOLID, d3d9types/D3DFILL_WIREFRAME, d3d9types/LPD3DFILLMODE, direct3d9.D3DFILLMODE
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
req.typenames: D3DFILLMODE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	D3D9Types.h
api_name:
-	D3DFILLMODE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _D3DFILLMODE enumeration


## -description


Defines constants describing the fill mode.


## -enum-fields




### -field D3DFILL_POINT

Fill points.


### -field D3DFILL_WIREFRAME

Fill wireframes.


### -field D3DFILL_SOLID

Fill solids. 


### -field D3DFILL_FORCE_DWORD

Forces this enumeration to compile to 32 bits in size. Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits. This value is not used.


## -remarks



The values in this enumerated type are used by the D3DRS_FILLMODE render state.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff549036">D3DRENDERSTATETYPE</a>



<a href="https://msdn.microsoft.com/ae64eb17-63a8-44c5-8d41-e021c49f338a">Direct3D Enumerations</a>
 

 

