---
UID: NS:d3d9types._D3DRECTPATCH_INFO
title: "_D3DRECTPATCH_INFO"
author: windows-driver-content
description: Describes a rectangular high-order patch.
old-location: direct3d9\d3drectpatch_info.htm
old-project: direct3d9
ms.assetid: VS|directx_sdk|~\d3drectpatch_info.htm
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: D3DRECTPATCH_INFO, D3DRECTPATCH_INFO structure [Direct3D 9], LPD3DRECTPATCH_INFO, LPD3DRECTPATCH_INFO structure pointer [Direct3D 9], _D3DRECTPATCH_INFO, a232607f-3eca-c966-6afb-1b71007d142d, d3d9types/D3DRECTPATCH_INFO, d3d9types/LPD3DRECTPATCH_INFO, direct3d9.d3drectpatch_info
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
req.typenames: D3DRECTPATCH_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	D3D9Types.h
api_name:
-	D3DRECTPATCH_INFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _D3DRECTPATCH_INFO structure


## -description


Describes a rectangular high-order patch.


## -struct-fields




### -field StartVertexOffsetWidth

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Starting vertex offset width, in number of vertices. 


### -field StartVertexOffsetHeight

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Starting vertex offset height, in number of vertices. 


### -field Width

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Width of each vertex, in number of vertices. 


### -field Height

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Height of each vertex, in number of vertices. 


### -field Stride

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Width of the imaginary two-dimensional vertex array, which occupies the same space as the vertex buffer. For an example, see the diagram below. 


### -field Basis

Type: <b><a href="https://msdn.microsoft.com/18c31c77-7ba3-449c-af4a-717b8c1dced1">D3DBASISTYPE</a></b>

Member of the <a href="https://msdn.microsoft.com/18c31c77-7ba3-449c-af4a-717b8c1dced1">D3DBASISTYPE</a> enumerated type, defining the basis type for the rectangular high-order patch.



<table>
<tr>
<th>Value</th>
<th>Order supported</th>
<th>Width and height</th>
</tr>
<tr>
<td>D3DBASIS_BEZIER</td>
<td>Linear, cubic, and quintic</td>
<td>Width = height = (DWORD)order + 1</td>
</tr>
<tr>
<td>D3DBASIS_BSPLINE</td>
<td>Linear, cubic, and quintic</td>
<td>Width = height &gt; (DWORD)order</td>
</tr>
<tr>
<td>D3DBASIS_INTERPOLATE</td>
<td>Cubic</td>
<td>Width = height &gt; (DWORD)order</td>
</tr>
</table>
 


### -field Degree

Type: <b><a href="https://msdn.microsoft.com/52a9c57e-a48d-4d8a-a208-97a3d09e7abf">D3DDEGREETYPE</a></b>

Member of the <a href="https://msdn.microsoft.com/52a9c57e-a48d-4d8a-a208-97a3d09e7abf">D3DDEGREETYPE</a> enumerated type, defining the degree for the rectangular patch. 


## -remarks



The following diagram identifies the parameters that specify a rectangle patch.

<img alt="Diagram of a rectangular high-order patch and the parameters that specify it" src="images/HOP_rectpatch.png"/>
Each of the vertices in the vertex buffer is shown as a black dot. In this case, the vertex buffer has 20 vertices in it, 16 of which are in the rectangle patch. The stride is the number of vertices in the width of the vertex buffer, in this case five. The x offset to the first vertex is called the StartIndexVertexWidth and is in this case 1. The y offset to the first patch vertex is called the StartIndexVertexHeight and is in this case 0.

To render a stream of individual rectangular patches (non-mosaic), you should interpret your geometry as a long narrow (1 x N) rectangular patch. The <b>D3DRECTPATCH_INFO</b> structure for such a strip (cubic Bézier) would be set up in the following manner.

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>    
D3DRECTPATCH_INFO RectInfo;

RectInfo.Width = 4;
RectInfo.Height = 4;
RectInfo.Stride = 4;
RectInfo.Basis = D3DBASIS_BEZIER;
RectInfo.Order = D3DORDER_CUBIC;
RectInfo.StartVertexOffsetWidth = 0;
RectInfo.StartVertexOffsetHeight = 4*i;  // The variable i is the index of the 
//   patch you want to render.
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/d941d994-8a13-49ff-a0b1-b21a3f84ed78">D3DXTessellateRectPatch</a>



<a href="https://msdn.microsoft.com/0a13cb04-10cb-48a6-a709-ad4a56459f02">Direct3D Structures</a>



<a href="https://msdn.microsoft.com/478b4a3d-3366-47ec-8a66-92aa2aa06477">DrawRectPatch</a>
 

 

