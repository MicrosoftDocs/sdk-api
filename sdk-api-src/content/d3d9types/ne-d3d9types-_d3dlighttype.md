---
UID: NE:d3d9types._D3DLIGHTTYPE
title: "_D3DLIGHTTYPE"
author: windows-driver-content
description: Defines the light type.
old-location: direct3d9\D3DLIGHTTYPE.htm
old-project: direct3d9
ms.assetid: VS|directx_sdk|~\d3dlighttype.htm
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: 6ccc2226-96ba-b87b-c7fb-31c081484045, D3DLIGHTTYPE, D3DLIGHTTYPE enumeration [Direct3D 9], D3DLIGHT_DIRECTIONAL, D3DLIGHT_FORCE_DWORD, D3DLIGHT_POINT, D3DLIGHT_SPOT, LPD3DLIGHTTYPE, LPD3DLIGHTTYPE enumeration pointer [Direct3D 9], _D3DLIGHTTYPE, d3d9types/D3DLIGHTTYPE, d3d9types/D3DLIGHT_DIRECTIONAL, d3d9types/D3DLIGHT_FORCE_DWORD, d3d9types/D3DLIGHT_POINT, d3d9types/D3DLIGHT_SPOT, d3d9types/LPD3DLIGHTTYPE, direct3d9.D3DLIGHTTYPE
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
req.typenames: D3DLIGHTTYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	D3D9Types.h
api_name:
-	D3DLIGHTTYPE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _D3DLIGHTTYPE enumeration


## -description


Defines the light type.


## -enum-fields




### -field D3DLIGHT_POINT

Light is a point source. The light has a position in space and radiates light in all directions. 


### -field D3DLIGHT_SPOT

Light is a spotlight source. This light is like a point light, except that the illumination is limited to a cone. This light type has a direction and several other parameters that determine the shape of the cone it produces. For information about these parameters, see the <a href="https://msdn.microsoft.com/25ce9d72-949c-41fc-8e3b-146d6a2de0dc">D3DLIGHT9</a>  structure. 


### -field D3DLIGHT_DIRECTIONAL

Light is a directional light source. This is equivalent to using a point light source at an infinite distance. 


### -field D3DLIGHT_FORCE_DWORD

Forces this enumeration to compile to 32 bits in size. Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits. This value is not used. 


## -remarks



Directional lights are slightly faster than point light sources, but point lights look a little better. Spotlights offer interesting visual effects but are computationally time-consuming.




## -see-also




<a href="https://msdn.microsoft.com/25ce9d72-949c-41fc-8e3b-146d6a2de0dc">D3DLIGHT9</a>



<a href="https://msdn.microsoft.com/ae64eb17-63a8-44c5-8d41-e021c49f338a">Direct3D Enumerations</a>
 

 

