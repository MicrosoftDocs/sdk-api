---
UID: NE:d3d9types._D3DBASISTYPE
title: "_D3DBASISTYPE"
author: windows-driver-content
description: Defines the basis type of a high-order patch surface.
old-location: direct3d9\D3DBASISTYPE.htm
old-project: direct3d9
ms.assetid: VS|directx_sdk|~\d3dbasistype.htm
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: D3DBASISTYPE, D3DBASISTYPE enumeration [Direct3D 9], D3DBASIS_BEZIER, D3DBASIS_BSPLINE, D3DBASIS_CATMULL_ROM, D3DBASIS_FORCE_DWORD, LPD3DBASISTYPE, LPD3DBASISTYPE enumeration pointer [Direct3D 9], _D3DBASISTYPE, c3545f8d-251d-8e10-1c67-2f77dbb6471c, d3d9types/D3DBASISTYPE, d3d9types/D3DBASIS_BEZIER, d3d9types/D3DBASIS_BSPLINE, d3d9types/D3DBASIS_CATMULL_ROM, d3d9types/D3DBASIS_FORCE_DWORD, d3d9types/LPD3DBASISTYPE, direct3d9.D3DBASISTYPE
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
req.typenames: D3DBASISTYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	D3D9Types.h
api_name:
-	D3DBASISTYPE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _D3DBASISTYPE enumeration


## -description


Defines the basis type of a high-order patch surface.


## -enum-fields




### -field D3DBASIS_BEZIER

Input vertices are treated as a series of Bézier patches. The number of vertices specified must be divisible by 4. Portions of the mesh beyond this criterion will not be rendered. Full continuity is assumed between sub-patches in the interior of the surface rendered by each call. Only the vertices at the corners of each sub-patch are guaranteed to lie on the resulting surface. 


### -field D3DBASIS_BSPLINE

Input vertices are treated as control points of a B-spline surface. The number of apertures rendered is two fewer than the number of apertures in that direction. In general, the generated surface does not contain the control vertices specified. 


### -field D3DBASIS_CATMULL_ROM

An interpolating basis defines the surface so that the surface goes through all the input vertices specified. In DirectX 8, this was D3DBASIS_INTERPOLATE.


### -field D3DBASIS_FORCE_DWORD

Forces this enumeration to compile to 32 bits in size. Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits. This value is not used. 


## -remarks



The members of <b>D3DBASISTYPE</b> specify the formulation to be used in evaluating the high-order patch surface primitive during tessellation.




## -see-also




<a href="https://msdn.microsoft.com/5f195009-d047-4dc0-a386-e1a434914e34">D3DRECTPATCH_INFO</a>



<a href="https://msdn.microsoft.com/3f97120b-3b32-4f95-8614-7b263ff330db">D3DTRIPATCH_INFO</a>



<a href="https://msdn.microsoft.com/ae64eb17-63a8-44c5-8d41-e021c49f338a">Direct3D Enumerations</a>
 

 

