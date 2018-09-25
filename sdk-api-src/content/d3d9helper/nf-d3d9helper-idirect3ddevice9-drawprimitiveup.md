---
UID: NF:d3d9helper.IDirect3DDevice9.DrawPrimitiveUP
title: IDirect3DDevice9::DrawPrimitiveUP
author: windows-sdk-content
description: Renders data specified by a user memory pointer as a sequence of geometric primitives of the specified type.
old-location: direct3d9\idirect3ddevice9__drawprimitiveup.htm
tech.root: Direct3D9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9__drawprimitiveup.htm
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: 3c41b201-e853-6403-545b-cddcebf45ea1, DrawPrimitiveUP, DrawPrimitiveUP method [Direct3D 9], DrawPrimitiveUP method [Direct3D 9],IDirect3DDevice9 interface, IDirect3DDevice9 interface [Direct3D 9],DrawPrimitiveUP method, IDirect3DDevice9.DrawPrimitiveUP, IDirect3DDevice9::DrawPrimitiveUP, d3d9helper/IDirect3DDevice9::DrawPrimitiveUP, direct3d9.idirect3ddevice9__drawprimitiveup
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
 - IDirect3DDevice9.DrawPrimitiveUP
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDirect3DDevice9::DrawPrimitiveUP


## -description


Renders data specified by a user memory pointer as a sequence of geometric primitives of the specified type.


## -parameters




### -param PrimitiveType [in]

Type: <b><a href="https://msdn.microsoft.com/89e697f9-02b9-4ae1-9e86-6178da0cb008">D3DPRIMITIVETYPE</a></b>

Member of the <a href="https://msdn.microsoft.com/89e697f9-02b9-4ae1-9e86-6178da0cb008">D3DPRIMITIVETYPE</a> enumerated type, describing the type of primitive to render. 


### -param PrimitiveCount [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Number of primitives to render. The maximum number of primitives allowed is determined by checking the MaxPrimitiveCount member of the <a href="https://msdn.microsoft.com/44457b7b-a1f7-4019-b971-8ec2334d3313">D3DCAPS9</a> structure. 


### -param pVertexStreamZeroData [in]

Type: <b>const void*</b>

User memory pointer to the vertex data.


### -param VertexStreamZeroStride [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The number of bytes of data for each vertex. This value may not be 0.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be: D3DERR_INVALIDCALL.




## -remarks



This method is intended for use in applications that are unable to store their vertex data in vertex buffers. This method supports only a single vertex stream. The effect of this call is to use the provided vertex data pointer and stride for vertex stream 0. It is invalid to have the declaration of the current vertex shader refer to vertex streams other than stream 0.

Following any <b>IDirect3DDevice9::DrawPrimitiveUP</b> call, the stream 0 settings, referenced by <a href="https://msdn.microsoft.com/d64dbbc5-48db-42c5-8b2f-dc0a3068fe16">IDirect3DDevice9::GetStreamSource</a>, are set to <b>NULL</b>.

The vertex data passed to <b>IDirect3DDevice9::DrawPrimitiveUP</b> does not need to persist after the call. Direct3D completes its access to that data prior to returning from the call.

When converting a legacy application to Direct3D 9, you must add a call to either <a href="https://msdn.microsoft.com/30c7db1d-5814-49d5-a92a-de597b31cb63">IDirect3DDevice9::SetFVF</a> to use the fixed function pipeline, or <a href="https://msdn.microsoft.com/8ca4d714-b2df-432e-9140-447cef7eaec1">IDirect3DDevice9::SetVertexDeclaration</a> to use a vertex shader before you make any Draw calls.




## -see-also




<a href="https://msdn.microsoft.com/cf951e8e-7adb-417a-bda0-9b3cde4912a7">IDirect3DDevice9</a>



<a href="https://msdn.microsoft.com/61b13680-293b-4c7e-9cf0-d91e764498fb">IDirect3DDevice9::DrawIndexedPrimitiveUP</a>



<a href="https://msdn.microsoft.com/9b94ab86-2a6a-4abd-ab56-95315f473226">Rendering from Vertex and Index Buffers (Direct3D 9)</a>
 

 

