---
UID: NS:d3d9types._D3DTRIPATCH_INFO
title: "_D3DTRIPATCH_INFO"
author: windows-driver-content
description: Describes a triangular high-order patch.
old-location: direct3d9\d3dtripatch_info.htm
old-project: direct3d9
ms.assetid: VS|directx_sdk|~\d3dtripatch_info.htm
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: 922edaf4-10ff-69f0-1ac9-63f98b6b4640, D3DTRIPATCH_INFO, D3DTRIPATCH_INFO structure [Direct3D 9], LPD3DTRIPATCH_INFO, LPD3DTRIPATCH_INFO structure pointer [Direct3D 9], _D3DTRIPATCH_INFO, d3d9types/D3DTRIPATCH_INFO, d3d9types/LPD3DTRIPATCH_INFO, direct3d9.d3dtripatch_info
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
req.typenames: D3DTRIPATCH_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	D3D9Types.h
api_name:
-	D3DTRIPATCH_INFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _D3DTRIPATCH_INFO structure


## -description


Describes a triangular high-order patch.


## -struct-fields




### -field StartVertexOffset

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Starting vertex offset, in number of vertices. 


### -field NumVertices

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Number of vertices.


### -field Basis

Type: <b><a href="https://msdn.microsoft.com/18c31c77-7ba3-449c-af4a-717b8c1dced1">D3DBASISTYPE</a></b>

Member of the <a href="https://msdn.microsoft.com/18c31c77-7ba3-449c-af4a-717b8c1dced1">D3DBASISTYPE</a> enumerated type, which defines the basis type for the triangular high-order patch. The only valid value for this member is D3DBASIS_BEZIER.


### -field Degree

Type: <b><a href="https://msdn.microsoft.com/52a9c57e-a48d-4d8a-a208-97a3d09e7abf">D3DDEGREETYPE</a></b>

Member of the <a href="https://msdn.microsoft.com/52a9c57e-a48d-4d8a-a208-97a3d09e7abf">D3DDEGREETYPE</a> enumerated type, defining the degree type for the triangular high-order patch.

<table>
<tr>
<th>Value</th>
<th>Number of vertices</th>
</tr>
<tr>
<td>D3DDEGREE_CUBIC</td>
<td>10</td>
</tr>
<tr>
<td>D3DDEGREE_LINEAR</td>
<td>3</td>
</tr>
<tr>
<td>D3DDEGREE_QUADRATIC</td>
<td>N/A</td>
</tr>
<tr>
<td>D3DDEGREE_QUINTIC</td>
<td>21</td>
</tr>
</table>
 

N/A - Not available. Not supported.


## -remarks



For example, the following diagram identifies the vertex order and segment numbers for a cubic Bézier triangle patch. The vertex order determines the segment numbers used by <a href="https://msdn.microsoft.com/9076fbe6-0f14-4b28-8f34-145e4eac6f22">DrawTriPatch</a>. The offset is the number of bytes to the first triangle patch vertex in the vertex buffer.

<img alt="Diagram of a triangular high-order patch with nine vertices" src="images/HOP_tripatch_info.png"/>



## -see-also




<a href="https://msdn.microsoft.com/bcc9143f-fec0-491a-8d32-1df961b8dade">D3DXTessellateTriPatch</a>



<a href="https://msdn.microsoft.com/0a13cb04-10cb-48a6-a709-ad4a56459f02">Direct3D Structures</a>



<a href="https://msdn.microsoft.com/9076fbe6-0f14-4b28-8f34-145e4eac6f22">DrawTriPatch</a>
 

 

