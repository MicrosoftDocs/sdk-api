---
UID: NE:d3d9types._D3DPRIMITIVETYPE
title: "_D3DPRIMITIVETYPE"
author: windows-driver-content
description: Defines the primitives supported by Direct3D.
old-location: direct3d9\D3DPRIMITIVETYPE.htm
old-project: direct3d9
ms.assetid: VS|directx_sdk|~\d3dprimitivetype.htm
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: 1731a336-f6c0-eb10-089d-4d7b4289fa52, D3DPRIMITIVETYPE, D3DPRIMITIVETYPE enumeration [Direct3D 9], D3DPT_FORCE_DWORD, D3DPT_LINELIST, D3DPT_LINESTRIP, D3DPT_POINTLIST, D3DPT_TRIANGLEFAN, D3DPT_TRIANGLELIST, D3DPT_TRIANGLESTRIP, LPD3DPRIMITIVETYPE, LPD3DPRIMITIVETYPE enumeration pointer [Direct3D 9], _D3DPRIMITIVETYPE, d3d9types/D3DPRIMITIVETYPE, d3d9types/D3DPT_FORCE_DWORD, d3d9types/D3DPT_LINELIST, d3d9types/D3DPT_LINESTRIP, d3d9types/D3DPT_POINTLIST, d3d9types/D3DPT_TRIANGLEFAN, d3d9types/D3DPT_TRIANGLELIST, d3d9types/D3DPT_TRIANGLESTRIP, d3d9types/LPD3DPRIMITIVETYPE, direct3d9.D3DPRIMITIVETYPE
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
req.typenames: D3DPRIMITIVETYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	D3D9Types.h
api_name:
-	D3DPRIMITIVETYPE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _D3DPRIMITIVETYPE enumeration


## -description


Defines the primitives supported by Direct3D.


## -enum-fields




### -field D3DPT_POINTLIST

Renders the vertices as a collection of isolated points. This value is unsupported for indexed primitives.


### -field D3DPT_LINELIST

Renders the vertices as a list of isolated straight line segments.


### -field D3DPT_LINESTRIP

Renders the vertices as a single polyline.


### -field D3DPT_TRIANGLELIST

Renders the specified vertices as a sequence of isolated triangles. Each group of three vertices defines a separate triangle. 

Back-face culling is affected by the current winding-order render state.


### -field D3DPT_TRIANGLESTRIP

Renders the vertices as a triangle strip. The backface-culling flag is automatically flipped on even-numbered triangles. 


### -field D3DPT_TRIANGLEFAN

Renders the vertices as a triangle fan. 


### -field D3DPT_FORCE_DWORD

Forces this enumeration to compile to 32 bits in size. Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits. This value is not used. 


## -remarks



Using <a href="https://msdn.microsoft.com/3923c570-47a4-4b53-a097-731981380ae0">Triangle Strips</a> or <a href="https://msdn.microsoft.com/a1fbfd78-121f-4f79-9ba8-44f23356a432">Triangle Fans (Direct3D 9)</a> is often more efficient than using triangle lists because fewer vertices are duplicated.




## -see-also




<a href="https://msdn.microsoft.com/ae64eb17-63a8-44c5-8d41-e021c49f338a">Direct3D Enumerations</a>



<a href="https://msdn.microsoft.com/535a261a-ca4f-432b-9126-f46c44dc8430">IDirect3DDevice9::DrawIndexedPrimitive</a>



<a href="https://msdn.microsoft.com/61b13680-293b-4c7e-9cf0-d91e764498fb">IDirect3DDevice9::DrawIndexedPrimitiveUP</a>



<a href="https://msdn.microsoft.com/b83110ba-85af-4f02-b651-9e64c37269f5">IDirect3DDevice9::DrawPrimitive</a>



<a href="https://msdn.microsoft.com/1be42c40-49af-458e-a5f5-1f56d2aa4f86">IDirect3DDevice9::DrawPrimitiveUP</a>
 

 

