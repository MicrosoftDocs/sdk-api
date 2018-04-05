---
UID: NE:d3d9types._D3DTRANSFORMSTATETYPE
title: "_D3DTRANSFORMSTATETYPE"
author: windows-driver-content
description: Defines constants that describe transformation state values.
old-location: direct3d9\D3DTRANSFORMSTATETYPE.htm
old-project: direct3d9
ms.assetid: VS|directx_sdk|~\d3dtransformstatetype.htm
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: D3DTRANSFORMSTATETYPE, D3DTRANSFORMSTATETYPE enumeration [Direct3D 9], D3DTS_FORCE_DWORD, D3DTS_PROJECTION, D3DTS_TEXTURE0, D3DTS_TEXTURE1, D3DTS_TEXTURE2, D3DTS_TEXTURE3, D3DTS_TEXTURE4, D3DTS_TEXTURE5, D3DTS_TEXTURE6, D3DTS_TEXTURE7, D3DTS_VIEW, LPD3DTRANSFORMSTATETYPE, LPD3DTRANSFORMSTATETYPE enumeration pointer [Direct3D 9], _D3DTRANSFORMSTATETYPE, adcfb996-fa06-fe4a-ea0e-d334dd06ae51, d3d9types/D3DTRANSFORMSTATETYPE, d3d9types/D3DTS_FORCE_DWORD, d3d9types/D3DTS_PROJECTION, d3d9types/D3DTS_TEXTURE0, d3d9types/D3DTS_TEXTURE1, d3d9types/D3DTS_TEXTURE2, d3d9types/D3DTS_TEXTURE3, d3d9types/D3DTS_TEXTURE4, d3d9types/D3DTS_TEXTURE5, d3d9types/D3DTS_TEXTURE6, d3d9types/D3DTS_TEXTURE7, d3d9types/D3DTS_VIEW, d3d9types/LPD3DTRANSFORMSTATETYPE, direct3d9.D3DTRANSFORMSTATETYPE
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
req.typenames: D3DTRANSFORMSTATETYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	D3D9Types.h
api_name:
-	D3DTRANSFORMSTATETYPE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _D3DTRANSFORMSTATETYPE enumeration


## -description


Defines constants that describe transformation state values.


## -enum-fields




### -field D3DTS_VIEW

Identifies the transformation matrix being set as the view transformation matrix. The default value is <b>NULL</b> (the identity matrix). 


### -field D3DTS_PROJECTION

Identifies the transformation matrix being set as the projection transformation matrix. The default value is <b>NULL</b> (the identity matrix). 


### -field D3DTS_TEXTURE0

Identifies the transformation matrix being set for the specified texture stage. 


### -field D3DTS_TEXTURE1

Identifies the transformation matrix being set for the specified texture stage. 


### -field D3DTS_TEXTURE2

Identifies the transformation matrix being set for the specified texture stage. 


### -field D3DTS_TEXTURE3

Identifies the transformation matrix being set for the specified texture stage. 


### -field D3DTS_TEXTURE4

Identifies the transformation matrix being set for the specified texture stage. 


### -field D3DTS_TEXTURE5

Identifies the transformation matrix being set for the specified texture stage. 


### -field D3DTS_TEXTURE6

Identifies the transformation matrix being set for the specified texture stage. 


### -field D3DTS_TEXTURE7

Identifies the transformation matrix being set for the specified texture stage. 


### -field D3DTS_FORCE_DWORD

Forces this enumeration to compile to 32 bits in size. Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits. This value is not used. 


## -remarks



The transform states in the range 256 through 511 are reserved to store up to 256 world matrices that can be indexed using the D3DTS_WORLDMATRIX and D3DTS_WORLD macros.

<table>
<tr>
<th>Macros</th>
<th></th>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/2bf7ac8a-43d8-460e-a400-3b33e96441db">D3DTS_WORLD</a>
</td>
<td>Equivalent to D3DTS_WORLDMATRIX(0).</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/b0a1548c-de5d-4eff-baf9-4aecb5e13443">D3DTS_WORLDMATRIX</a>   (index)</td>
<td>Identifies the transform matrix to set for the world matrix at index. Multiple world matrices are used only for vertex blending. Otherwise only D3DTS_WORLD is used.</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/2bf7ac8a-43d8-460e-a400-3b33e96441db">D3DTS_WORLD</a>



<a href="https://msdn.microsoft.com/b0a1548c-de5d-4eff-baf9-4aecb5e13443">D3DTS_WORLDMATRIX</a>



<a href="https://msdn.microsoft.com/cab444c2-b245-4d1a-a90c-745c92a2ea89">D3DTS_WORLDn</a>



<a href="https://msdn.microsoft.com/ae64eb17-63a8-44c5-8d41-e021c49f338a">Direct3D Enumerations</a>



<a href="https://msdn.microsoft.com/0e91cdfc-27d7-481f-b0e0-f89f0049ffce">IDirect3DDevice9::GetTransform</a>



<a href="https://msdn.microsoft.com/a7c6b4ad-4915-402b-940a-354b44fda6a5">IDirect3DDevice9::MultiplyTransform</a>



<a href="https://msdn.microsoft.com/1dc94280-131f-47e8-8dd7-cea43dc6e6da">IDirect3DDevice9::SetTransform</a>
 

 

