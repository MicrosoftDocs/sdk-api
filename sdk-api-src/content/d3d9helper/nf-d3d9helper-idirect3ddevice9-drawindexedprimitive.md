---
UID: NF:d3d9helper.IDirect3DDevice9.DrawIndexedPrimitive
title: IDirect3DDevice9::DrawIndexedPrimitive
author: windows-sdk-content
description: Based on indexing, renders the specified geometric primitive into an array of vertices.
old-location: direct3d9\idirect3ddevice9__drawindexedprimitive.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9__drawindexedprimitive.htm
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: DrawIndexedPrimitive, DrawIndexedPrimitive method [Direct3D 9], DrawIndexedPrimitive method [Direct3D 9],IDirect3DDevice9 interface, IDirect3DDevice9 interface [Direct3D 9],DrawIndexedPrimitive method, IDirect3DDevice9.DrawIndexedPrimitive, IDirect3DDevice9::DrawIndexedPrimitive, a022738b-ecda-9413-683b-50134f542560, d3d9helper/IDirect3DDevice9::DrawIndexedPrimitive, direct3d9.idirect3ddevice9__drawindexedprimitive
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: d3d9helper.h
req.include-header: D3D9.h
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
req.lib: D3D9.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D9.lib
 - D3D9.dll
api_name:
 - IDirect3DDevice9.DrawIndexedPrimitive
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- d3d9helper.h
: 
- IDirect3DDevice9.DrawIndexedPrimitive
: 
---

# IDirect3DDevice9::DrawIndexedPrimitive


## -description


Based on indexing, renders the specified geometric primitive into an array of vertices.


## -parameters




### -param arg1 [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb172589(v=VS.85).aspx">D3DPRIMITIVETYPE</a></b>

Member of the <a href="https://msdn.microsoft.com/en-us/library/Bb172589(v=VS.85).aspx">D3DPRIMITIVETYPE</a> enumerated type, describing the type of primitive to render. D3DPT_POINTLIST is not supported with this method. See Remarks. 


### -param BaseVertexIndex [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">INT</a></b>

Offset from the start of the vertex buffer to the first vertex. See <a href="https://msdn.microsoft.com/en-us/library/Bb147325(v=VS.85).aspx">Scenario 4</a>.


### -param MinVertexIndex [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Minimum vertex index for vertices used during this call. This is a zero based index relative to BaseVertexIndex.


### -param NumVertices [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Number of vertices used during this call. The first vertex is located at index: BaseVertexIndex + MinIndex.


### -param startIndex [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Index of the first index to use when accesssing the vertex buffer. Beginning at StartIndex to index vertices from the vertex buffer.


### -param primCount [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Number of primitives to render. The number of vertices used is a function of the primitive count and the primitive type. The maximum number of primitives allowed is determined by checking the MaxPrimitiveCount member of the <a href="https://msdn.microsoft.com/en-us/library/Bb172513(v=VS.85).aspx">D3DCAPS9</a> structure. 


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be the following:
     D3DERR_INVALIDCALL.




## -remarks



This method draws indexed primitives from the current set of data input streams. MinIndex  and all the indices in the index stream are relative to the BaseVertexIndex.

The MinIndex  and NumVertices  parameters specify the range of vertex indices used for each <b>IDirect3DDevice9::DrawIndexedPrimitive</b> call. These are used to optimize vertex processing of indexed primitives by processing a sequential range of vertices prior to indexing into these vertices. It is invalid for any indices used during this call to reference any vertices outside of this range.

<b>IDirect3DDevice9::DrawIndexedPrimitive</b> fails if no index array is set.

The D3DPT_POINTLIST member of the <a href="https://msdn.microsoft.com/en-us/library/Bb172589(v=VS.85).aspx">D3DPRIMITIVETYPE</a> enumerated type is not supported and is not a valid type for this method.

When converting a legacy application to Direct3D 9, you must add a call to either <a href="https://msdn.microsoft.com/en-us/library/Bb174433(v=VS.85).aspx">IDirect3DDevice9::SetFVF</a> to use the fixed function pipeline, or <a href="https://msdn.microsoft.com/en-us/library/Bb174464(v=VS.85).aspx">IDirect3DDevice9::SetVertexDeclaration</a> to use a vertex shader before you make any Draw calls.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb174336(v=VS.85).aspx">IDirect3DDevice9</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb174371(v=VS.85).aspx">IDirect3DDevice9::DrawPrimitive</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb174595(v=VS.85).aspx">Index Buffers (Direct3D 9)</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb147325(v=VS.85).aspx">Rendering from Vertex and Index Buffers (Direct3D 9)</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb206332(v=VS.85).aspx">Vertex Buffers (Direct3D 9)</a>
 

 

