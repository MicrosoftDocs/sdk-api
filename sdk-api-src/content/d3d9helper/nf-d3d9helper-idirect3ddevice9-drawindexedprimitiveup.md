---
UID: NF:d3d9helper.IDirect3DDevice9.DrawIndexedPrimitiveUP
title: IDirect3DDevice9::DrawIndexedPrimitiveUP
author: windows-driver-content
description: Renders the specified geometric primitive with data specified by a user memory pointer.
old-location: direct3d9\idirect3ddevice9__drawindexedprimitiveup.htm
old-project: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9__drawindexedprimitiveup.htm
ms.author: windowsdriverdev
ms.date: 4/10/2018
ms.keywords: DrawIndexedPrimitiveUP, DrawIndexedPrimitiveUP method [Direct3D 9], DrawIndexedPrimitiveUP method [Direct3D 9],IDirect3DDevice9 interface, IDirect3DDevice9 interface [Direct3D 9],DrawIndexedPrimitiveUP method, IDirect3DDevice9.DrawIndexedPrimitiveUP, IDirect3DDevice9::DrawIndexedPrimitiveUP, a76e7ddd-b096-aabd-099d-4ef12355b8c1, d3d9helper/IDirect3DDevice9::DrawIndexedPrimitiveUP, direct3d9.idirect3ddevice9__drawindexedprimitiveup
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
req.typenames: D3DVSHADERCAPS2_0
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	D3D9.lib
-	D3D9.dll
api_name:
-	IDirect3DDevice9.DrawIndexedPrimitiveUP
product: Windows
targetos: Windows
req.lib: D3D9.lib
req.dll: 
req.irql: 
---

# IDirect3DDevice9::DrawIndexedPrimitiveUP


## -description


Renders the specified geometric primitive with data specified by a user memory pointer.


## -parameters




### -param PrimitiveType [in]

Type: <b><a href="https://msdn.microsoft.com/89e697f9-02b9-4ae1-9e86-6178da0cb008">D3DPRIMITIVETYPE</a></b>

Member of the <a href="https://msdn.microsoft.com/89e697f9-02b9-4ae1-9e86-6178da0cb008">D3DPRIMITIVETYPE</a> enumerated type, describing the type of primitive to render. 


### -param MinVertexIndex [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Minimum vertex index. This is a zero-based index.


### -param NumVertices [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

 Number of vertices used during this call. The first vertex is located at index: MinVertexIndex.


### -param PrimitiveCount [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Number of primitives to render. The maximum number of primitives allowed is determined by checking the MaxPrimitiveCount member of the <a href="https://msdn.microsoft.com/44457b7b-a1f7-4019-b971-8ec2334d3313">D3DCAPS9</a> structure (the number of indices is a function of the primitive count and the primitive type).


### -param pIndexData [in]

Type: <b>const void*</b>

User memory pointer to the index data. 


### -param IndexDataFormat [in]

Type: <b><a href="https://msdn.microsoft.com/a222e3bb-310c-4019-93ee-6a2da2a46ded">D3DFORMAT</a></b>

Member of the <a href="https://msdn.microsoft.com/a222e3bb-310c-4019-93ee-6a2da2a46ded">D3DFORMAT</a> enumerated type, describing the format of the index data. The valid settings are either: 


<ul>
<li>
<a href="https://msdn.microsoft.com/a222e3bb-310c-4019-93ee-6a2da2a46ded">D3DFMT_INDEX16</a>
</li>
<li>
<a href="https://msdn.microsoft.com/a222e3bb-310c-4019-93ee-6a2da2a46ded">D3DFMT_INDEX32</a>
</li>
</ul>

### -param pVertexStreamZeroData [in]

Type: <b>const void*</b>

User memory pointer to the vertex data. The vertex data must be in stream 0.


### -param VertexStreamZeroStride [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The number of bytes of data for each vertex. This value may not be 0.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be the following:
     D3DERR_INVALIDCALL.




## -remarks



This method is intended for use in applications that are unable to store their vertex data in vertex buffers. This method supports only a single vertex stream, which must be declared as stream 0.

Following any <b>IDirect3DDevice9::DrawIndexedPrimitiveUP</b> call, the stream 0 settings, referenced by <a href="https://msdn.microsoft.com/d64dbbc5-48db-42c5-8b2f-dc0a3068fe16">IDirect3DDevice9::GetStreamSource</a>, are set to <b>NULL</b>. Also, the index buffer setting for <a href="https://msdn.microsoft.com/b27403da-9079-4f97-8520-c2617b53e059">IDirect3DDevice9::SetIndices</a> is set to <b>NULL</b>.

The vertex data passed to <b>IDirect3DDevice9::DrawIndexedPrimitiveUP</b> does not need to persist after the call. Direct3D completes its access to that data prior to returning from the call.

When converting a legacy application to Direct3D 9, you must add a call to either <a href="https://msdn.microsoft.com/30c7db1d-5814-49d5-a92a-de597b31cb63">IDirect3DDevice9::SetFVF</a> to use the fixed function pipeline, or <a href="https://msdn.microsoft.com/8ca4d714-b2df-432e-9140-447cef7eaec1">IDirect3DDevice9::SetVertexDeclaration</a> to use a vertex shader before you make any Draw calls.




## -see-also




<a href="https://msdn.microsoft.com/cf951e8e-7adb-417a-bda0-9b3cde4912a7">IDirect3DDevice9</a>



<a href="https://msdn.microsoft.com/b83110ba-85af-4f02-b651-9e64c37269f5">IDirect3DDevice9::DrawPrimitive</a>



<a href="https://msdn.microsoft.com/9b94ab86-2a6a-4abd-ab56-95315f473226">Rendering from Vertex and Index Buffers (Direct3D 9)</a>
 

 

