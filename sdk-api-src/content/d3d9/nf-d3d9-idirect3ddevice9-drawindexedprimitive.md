---
UID: NF:d3d9.IDirect3DDevice9.DrawIndexedPrimitive
title: IDirect3DDevice9::DrawIndexedPrimitive
author: windows-sdk-content
description: Based on indexing, renders the specified geometric primitive into an array of vertices.
old-location: direct3d9\idirect3ddevice9__drawindexedprimitive.htm
old-project: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9__drawindexedprimitive.htm
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: DrawIndexedPrimitive, DrawIndexedPrimitive method [Direct3D 9], DrawIndexedPrimitive method [Direct3D 9],IDirect3DDevice9 interface, IDirect3DDevice9 interface [Direct3D 9],DrawIndexedPrimitive method, IDirect3DDevice9.DrawIndexedPrimitive, IDirect3DDevice9::DrawIndexedPrimitive, a022738b-ecda-9413-683b-50134f542560, d3d9helper/IDirect3DDevice9::DrawIndexedPrimitive, direct3d9.idirect3ddevice9__drawindexedprimitive
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: d3d9.h
req.include-header: D3D9.h
req.redist: 
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
tech.root: 
req.typenames: D3D12_SIGNATURE_PARAMETER_DESC
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
req.lib: D3D9.lib
req.dll: 
req.irql: 
---

# IDirect3DDevice9::DrawIndexedPrimitive


## -description


Based on indexing, renders the specified geometric primitive into an array of vertices.


## -parameters




### -param param




### -param BaseVertexIndex [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">INT</a></b>

Offset from the start of the vertex buffer to the first vertex. See <a href="https://msdn.microsoft.com/9b94ab86-2a6a-4abd-ab56-95315f473226">Scenario 4</a>.


### -param MinVertexIndex




### -param NumVertices [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Number of vertices used during this call. The first vertex is located at index: BaseVertexIndex + MinIndex.


### -param startIndex




### -param primCount






#### - MinIndex [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Minimum vertex index for vertices used during this call. This is a zero based index relative to BaseVertexIndex.


#### - PrimitiveCount [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Number of primitives to render. The number of vertices used is a function of the primitive count and the primitive type. The maximum number of primitives allowed is determined by checking the MaxPrimitiveCount member of the <a href="https://msdn.microsoft.com/44457b7b-a1f7-4019-b971-8ec2334d3313">D3DCAPS9</a> structure. 


#### - StartIndex [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Index of the first index to use when accesssing the vertex buffer. Beginning at StartIndex to index vertices from the vertex buffer.


#### - Type [in]

Type: <b><a href="https://msdn.microsoft.com/89e697f9-02b9-4ae1-9e86-6178da0cb008">D3DPRIMITIVETYPE</a></b>

Member of the <a href="https://msdn.microsoft.com/89e697f9-02b9-4ae1-9e86-6178da0cb008">D3DPRIMITIVETYPE</a> enumerated type, describing the type of primitive to render. D3DPT_POINTLIST is not supported with this method. See Remarks. 


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be the following:
     D3DERR_INVALIDCALL.




## -remarks



This method draws indexed primitives from the current set of data input streams. MinIndex  and all the indices in the index stream are relative to the BaseVertexIndex.

The MinIndex  and NumVertices  parameters specify the range of vertex indices used for each <b>IDirect3DDevice9::DrawIndexedPrimitive</b> call. These are used to optimize vertex processing of indexed primitives by processing a sequential range of vertices prior to indexing into these vertices. It is invalid for any indices used during this call to reference any vertices outside of this range.

<b>IDirect3DDevice9::DrawIndexedPrimitive</b> fails if no index array is set.

The D3DPT_POINTLIST member of the <a href="https://msdn.microsoft.com/89e697f9-02b9-4ae1-9e86-6178da0cb008">D3DPRIMITIVETYPE</a> enumerated type is not supported and is not a valid type for this method.

When converting a legacy application to Direct3D 9, you must add a call to either <a href="https://msdn.microsoft.com/30c7db1d-5814-49d5-a92a-de597b31cb63">IDirect3DDevice9::SetFVF</a> to use the fixed function pipeline, or <a href="https://msdn.microsoft.com/8ca4d714-b2df-432e-9140-447cef7eaec1">IDirect3DDevice9::SetVertexDeclaration</a> to use a vertex shader before you make any Draw calls.




## -see-also




<a href="https://msdn.microsoft.com/cf951e8e-7adb-417a-bda0-9b3cde4912a7">IDirect3DDevice9</a>



<a href="https://msdn.microsoft.com/b83110ba-85af-4f02-b651-9e64c37269f5">IDirect3DDevice9::DrawPrimitive</a>



<a href="https://msdn.microsoft.com/baa60cd1-a1f0-4dbe-b934-aeb1a5c6b784">Index Buffers (Direct3D 9)</a>



<a href="https://msdn.microsoft.com/9b94ab86-2a6a-4abd-ab56-95315f473226">Rendering from Vertex and Index Buffers (Direct3D 9)</a>



<a href="https://msdn.microsoft.com/f9274562-413c-4f0d-bdb4-dc8fa83b6063">Vertex Buffers (Direct3D 9)</a>
 

 

