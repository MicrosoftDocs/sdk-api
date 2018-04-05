---
UID: NE:d3d9types._D3DSHADEMODE
title: "_D3DSHADEMODE"
author: windows-driver-content
description: Defines constants that describe the supported shading modes.
old-location: direct3d9\D3DSHADEMODE.htm
old-project: direct3d9
ms.assetid: VS|directx_sdk|~\d3dshademode.htm
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: D3DSHADEMODE, D3DSHADEMODE enumeration [Direct3D 9], D3DSHADE_FLAT, D3DSHADE_FORCE_DWORD, D3DSHADE_GOURAUD, D3DSHADE_PHONG, LPD3DSHADEMODE, LPD3DSHADEMODE enumeration pointer [Direct3D 9], _D3DSHADEMODE, d3d9types/D3DSHADEMODE, d3d9types/D3DSHADE_FLAT, d3d9types/D3DSHADE_FORCE_DWORD, d3d9types/D3DSHADE_GOURAUD, d3d9types/D3DSHADE_PHONG, d3d9types/LPD3DSHADEMODE, direct3d9.D3DSHADEMODE, e5f715d3-7656-f6ab-3fd6-e58e4faf7752
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
req.typenames: D3DSHADEMODE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	d3d9types.h
api_name:
-	D3DSHADEMODE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _D3DSHADEMODE enumeration


## -description


Defines constants that describe the supported shading modes.


## -enum-fields




### -field D3DSHADE_FLAT

Flat shading mode. The color and specular component of the first vertex in the triangle are used to determine the color and specular component of the face. These colors remain constant across the triangle; that is, they are not interpolated. The specular alpha is interpolated. See Remarks. 


### -field D3DSHADE_GOURAUD

Gouraud shading mode. The color and specular components of the face are determined by a linear interpolation between all three of the triangle's vertices. 


### -field D3DSHADE_PHONG

Not supported. 


### -field D3DSHADE_FORCE_DWORD

Forces this enumeration to compile to 32 bits in size. Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits. This value is not used. 


## -remarks



The first vertex of a triangle for flat shading mode is defined in the following manner. 

<ul>
<li>For a triangle list, the first vertex of the triangle 
    
    i is 
    
    i * 3.</li>
<li>For a triangle strip, the first vertex of the triangle   
    
    i  is vertex 
    
    i.</li>
<li>For a triangle fan, the first vertex of the triangle 
    
    i is vertex 
    
    i + 1.</li>
</ul>
The members of this enumerated type define the vales for the D3DRS_SHADEMODE render state.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff549036">D3DRENDERSTATETYPE</a>



<a href="https://msdn.microsoft.com/ae64eb17-63a8-44c5-8d41-e021c49f338a">Direct3D Enumerations</a>
 

 

