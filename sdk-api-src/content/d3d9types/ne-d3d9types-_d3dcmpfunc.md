---
UID: NE:d3d9types._D3DCMPFUNC
title: "_D3DCMPFUNC"
author: windows-driver-content
description: Defines the supported compare functions.
old-location: direct3d9\D3DCMPFUNC.htm
old-project: direct3d9
ms.assetid: VS|directx_sdk|~\d3dcmpfunc.htm
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: 2387e88a-aa54-40ce-f122-d537d5ac6d74, D3DCMPFUNC, D3DCMPFUNC enumeration [Direct3D 9], D3DCMP_ALWAYS, D3DCMP_EQUAL, D3DCMP_FORCE_DWORD, D3DCMP_GREATER, D3DCMP_GREATEREQUAL, D3DCMP_LESS, D3DCMP_LESSEQUAL, D3DCMP_NEVER, D3DCMP_NOTEQUAL, LPD3DCMPFUNC, LPD3DCMPFUNC enumeration pointer [Direct3D 9], _D3DCMPFUNC, d3d9types/D3DCMPFUNC, d3d9types/D3DCMP_ALWAYS, d3d9types/D3DCMP_EQUAL, d3d9types/D3DCMP_FORCE_DWORD, d3d9types/D3DCMP_GREATER, d3d9types/D3DCMP_GREATEREQUAL, d3d9types/D3DCMP_LESS, d3d9types/D3DCMP_LESSEQUAL, d3d9types/D3DCMP_NEVER, d3d9types/D3DCMP_NOTEQUAL, d3d9types/LPD3DCMPFUNC, direct3d9.D3DCMPFUNC
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
req.typenames: D3DCMPFUNC
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	D3D9Types.h
api_name:
-	D3DCMPFUNC
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _D3DCMPFUNC enumeration


## -description


Defines the supported compare functions.


## -enum-fields




### -field D3DCMP_NEVER

Always fail the test. 


### -field D3DCMP_LESS

Accept the new pixel if its value is less than the value of the current pixel. 


### -field D3DCMP_EQUAL

Accept the new pixel if its value equals the value of the current pixel. 


### -field D3DCMP_LESSEQUAL

Accept the new pixel if its value is less than or equal to the value of the current pixel. 


### -field D3DCMP_GREATER

Accept the new pixel if its value is greater than the value of the current pixel. 


### -field D3DCMP_NOTEQUAL

Accept the new pixel if its value does not equal the value of the current pixel. 


### -field D3DCMP_GREATEREQUAL

Accept the new pixel if its value is greater than or equal to the value of the current pixel. 


### -field D3DCMP_ALWAYS

Always pass the test. 


### -field D3DCMP_FORCE_DWORD

Forces this enumeration to compile to 32 bits in size. Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits. This value is not used. 


## -remarks



The values in this enumerated type define the supported compare functions for the D3DRS_ZFUNC, D3DRS_ALPHAFUNC, and D3DRS_STENCILFUNC render states.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff549036">D3DRENDERSTATETYPE</a>



<a href="https://msdn.microsoft.com/ae64eb17-63a8-44c5-8d41-e021c49f338a">Direct3D Enumerations</a>
 

 

