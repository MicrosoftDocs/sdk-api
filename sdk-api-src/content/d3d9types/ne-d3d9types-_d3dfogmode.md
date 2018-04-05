---
UID: NE:d3d9types._D3DFOGMODE
title: "_D3DFOGMODE"
author: windows-driver-content
description: Defines constants that describe the fog mode.
old-location: direct3d9\D3DFOGMODE.htm
old-project: direct3d9
ms.assetid: VS|directx_sdk|~\d3dfogmode.htm
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: 8fcd2671-7cf9-412c-8a80-6c025726dbf9, D3DFOGMODE, D3DFOGMODE enumeration [Direct3D 9], D3DFOG_EXP, D3DFOG_EXP2, D3DFOG_FORCE_DWORD, D3DFOG_LINEAR, D3DFOG_NONE, LPD3DFOGMODE, LPD3DFOGMODE enumeration pointer [Direct3D 9], _D3DFOGMODE, d3d9types/D3DFOGMODE, d3d9types/D3DFOG_EXP, d3d9types/D3DFOG_EXP2, d3d9types/D3DFOG_FORCE_DWORD, d3d9types/D3DFOG_LINEAR, d3d9types/D3DFOG_NONE, d3d9types/LPD3DFOGMODE, direct3d9.D3DFOGMODE
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
req.typenames: D3DFOGMODE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	D3D9Types.h
api_name:
-	D3DFOGMODE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _D3DFOGMODE enumeration


## -description


Defines constants that describe the fog mode.


## -enum-fields




### -field D3DFOG_NONE

No fog effect. 


### -field D3DFOG_EXP

Fog effect intensifies exponentially, according to the following formula. 


<img alt="Formula of fog-effect intensity" src="images/fogexp.png"/>


### -field D3DFOG_EXP2

Fog effect intensifies exponentially with the square of the distance, according to the following formula. 


<img alt="Formula of fog-effect intensity based on square of distance" src="images/fogexp2.png"/>


### -field D3DFOG_LINEAR

Fog effect intensifies linearly between the start and end points, according to the following formula. 

<img alt="Formula of fog-effect intensity based on start and end points" src="images/fogliner.png"/>

This is the only fog mode currently supported.


### -field D3DFOG_FORCE_DWORD

Forces this enumeration to compile to 32 bits in size. Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits. This value is not used. 


## -remarks



The values in this enumerated type are used by the D3DRS_FOGTABLEMODE and D3DRS_FOGVERTEXMODE render states.

Fog can be considered a measure of visibility: the lower the fog value produced by a fog equation, the less visible an object is.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff549036">D3DRENDERSTATETYPE</a>



<a href="https://msdn.microsoft.com/ae64eb17-63a8-44c5-8d41-e021c49f338a">Direct3D Enumerations</a>
 

 

