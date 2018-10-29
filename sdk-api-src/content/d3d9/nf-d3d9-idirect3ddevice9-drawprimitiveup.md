---
UID: NF:d3d9.IDirect3DDevice9.DrawPrimitiveUP
title: IDirect3DDevice9::DrawPrimitiveUP
author: windows-sdk-content
description: Renders data specified by a user memory pointer as a sequence of geometric primitives of the specified type.
old-location: direct3d9\idirect3ddevice9__drawprimitiveup.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9__drawprimitiveup.htm
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: 3c41b201-e853-6403-545b-cddcebf45ea1, DrawPrimitiveUP, DrawPrimitiveUP method [Direct3D 9], DrawPrimitiveUP method [Direct3D 9],IDirect3DDevice9 interface, IDirect3DDevice9 interface [Direct3D 9],DrawPrimitiveUP method, IDirect3DDevice9.DrawPrimitiveUP, IDirect3DDevice9::DrawPrimitiveUP, d3d9helper/IDirect3DDevice9::DrawPrimitiveUP, direct3d9.idirect3ddevice9__drawprimitiveup
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: d3d9.h
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

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb172589(v=VS.85).aspx">D3DPRIMITIVETYPE</a></b>

Member of the <a href="https://msdn.microsoft.com/en-us/library/Bb172589(v=VS.85).aspx">D3DPRIMITIVETYPE</a> enumerated type, describing the type of primitive to render. 


### -param PrimitiveCount [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Number of primitives to render. The maximum number of primitives allowed is determined by checking the MaxPrimitiveCount member of the <a href="https://msdn.microsoft.com/en-us/library/Bb172513(v=VS.85).aspx">D3DCAPS9</a> structure. 


### -param pVertexStreamZeroData [in]

Type: <b>const void*</b>

User memory pointer to the vertex data.


### -param VertexStreamZeroStride [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The number of bytes of data for each vertex. This value may not be 0.


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be: D3DERR_INVALIDCALL.




## -remarks



This method is intended for use in applications that are unable to store their vertex data in vertex buffers. This method supports only a single vertex stream. The effect of this call is to use the provided vertex data pointer and stride for vertex stream 0. It is invalid to have the declaration of the current vertex shader refer to vertex streams other than stream 0.

Following any <b>IDirect3DDevice9::DrawPrimitiveUP</b> call, the stream 0 settings, referenced by <a href="https://msdn.microsoft.com/en-us/library/Bb174409(v=VS.85).aspx">IDirect3DDevice9::GetStreamSource</a>, are set to <b>NULL</b>.

The vertex data passed to <b>IDirect3DDevice9::DrawPrimitiveUP</b> does not need to persist after the call. Direct3D completes its access to that data prior to returning from the call.

When converting a legacy application to Direct3D 9, you must add a call to either <a href="https://msdn.microsoft.com/en-us/library/Bb174433(v=VS.85).aspx">IDirect3DDevice9::SetFVF</a> to use the fixed function pipeline, or <a href="https://msdn.microsoft.com/en-us/library/Bb174464(v=VS.85).aspx">IDirect3DDevice9::SetVertexDeclaration</a> to use a vertex shader before you make any Draw calls.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb174336(v=VS.85).aspx">IDirect3DDevice9</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb174370(v=VS.85).aspx">IDirect3DDevice9::DrawIndexedPrimitiveUP</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb147325(v=VS.85).aspx">Rendering from Vertex and Index Buffers (Direct3D 9)</a>
 

 

