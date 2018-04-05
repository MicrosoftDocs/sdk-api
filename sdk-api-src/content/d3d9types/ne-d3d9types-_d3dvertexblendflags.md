---
UID: NE:d3d9types._D3DVERTEXBLENDFLAGS
title: "_D3DVERTEXBLENDFLAGS"
author: windows-driver-content
description: Defines flags used to control the number or matrices that the system applies when performing multimatrix vertex blending.
old-location: direct3d9\D3DVERTEXBLENDFLAGS.htm
old-project: direct3d9
ms.assetid: VS|directx_sdk|~\d3dvertexblendflags.htm
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: 132ef4d7-bb51-c289-ffe6-85bb630e6213, D3DVBF_0WEIGHTS, D3DVBF_1WEIGHTS, D3DVBF_2WEIGHTS, D3DVBF_3WEIGHTS, D3DVBF_DISABLE, D3DVBF_TWEENING, D3DVERTEXBLENDFLAGS, D3DVERTEXBLENDFLAGS enumeration [Direct3D 9], LPD3DVERTEXBLENDFLAGS, LPD3DVERTEXBLENDFLAGS enumeration pointer [Direct3D 9], _D3DVERTEXBLENDFLAGS, d3d9types/D3DVBF_0WEIGHTS, d3d9types/D3DVBF_1WEIGHTS, d3d9types/D3DVBF_2WEIGHTS, d3d9types/D3DVBF_3WEIGHTS, d3d9types/D3DVBF_DISABLE, d3d9types/D3DVBF_TWEENING, d3d9types/D3DVERTEXBLENDFLAGS, d3d9types/LPD3DVERTEXBLENDFLAGS, direct3d9.D3DVERTEXBLENDFLAGS
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
req.typenames: D3DVERTEXBLENDFLAGS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	D3D9Types.h
api_name:
-	D3DVERTEXBLENDFLAGS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _D3DVERTEXBLENDFLAGS enumeration


## -description


Defines flags used to control the number or matrices that the system applies when performing multimatrix vertex blending.


## -enum-fields




### -field D3DVBF_DISABLE

Disable vertex blending; apply only the world matrix set by the <a href="https://msdn.microsoft.com/b0a1548c-de5d-4eff-baf9-4aecb5e13443">D3DTS_WORLDMATRIX</a> macro, where the index value for the transformation state is 0. 


### -field D3DVBF_1WEIGHTS

Enable vertex blending between the two matrices set by the <a href="https://msdn.microsoft.com/b0a1548c-de5d-4eff-baf9-4aecb5e13443">D3DTS_WORLDMATRIX</a> macro, where the index value for the transformation states are 0 and 1. 


### -field D3DVBF_2WEIGHTS

Enable vertex blending between the three matrices set by the <a href="https://msdn.microsoft.com/b0a1548c-de5d-4eff-baf9-4aecb5e13443">D3DTS_WORLDMATRIX</a> macro, where the index value for the transformation states are 0, 1, and 2. 


### -field D3DVBF_3WEIGHTS

Enable vertex blending between the four matrices set by the <a href="https://msdn.microsoft.com/b0a1548c-de5d-4eff-baf9-4aecb5e13443">D3DTS_WORLDMATRIX</a> macro, where the index value for the transformation states are 0, 1, 2, and 3. 


### -field D3DVBF_TWEENING

Vertex blending is done by using the value assigned to D3DRS_TWEENFACTOR. 


### -field D3DVBF_0WEIGHTS

Use a single matrix with a weight of 1.0. 


### -field D3DVBF_FORCE_DWORD




## -remarks



Members of this type are used with the D3DRS_VERTEXBLEND render state.

Geometry blending (multimatrix vertex blending) requires that your application use a vertex format that has blending (beta) weights for each vertex.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff549036">D3DRENDERSTATETYPE</a>



<a href="https://msdn.microsoft.com/2bf7ac8a-43d8-460e-a400-3b33e96441db">D3DTS_WORLD</a>



<a href="https://msdn.microsoft.com/b0a1548c-de5d-4eff-baf9-4aecb5e13443">D3DTS_WORLDMATRIX</a>



<a href="https://msdn.microsoft.com/cab444c2-b245-4d1a-a90c-745c92a2ea89">D3DTS_WORLDn</a>



<a href="https://msdn.microsoft.com/ae64eb17-63a8-44c5-8d41-e021c49f338a">Direct3D Enumerations</a>
 

 

