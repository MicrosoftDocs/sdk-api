---
UID: NF:d3d9helper.IDirect3DDevice9.DrawPrimitive
title: IDirect3DDevice9::DrawPrimitive
author: windows-sdk-content
description: Renders a sequence of nonindexed, geometric primitives of the specified type from the current set of data input streams.
old-location: direct3d9\idirect3ddevice9__drawprimitive.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9__drawprimitive.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: DrawPrimitive, DrawPrimitive method [Direct3D 9], DrawPrimitive method [Direct3D 9],IDirect3DDevice9 interface, IDirect3DDevice9 interface [Direct3D 9],DrawPrimitive method, IDirect3DDevice9.DrawPrimitive, IDirect3DDevice9::DrawPrimitive, d3d9helper/IDirect3DDevice9::DrawPrimitive, direct3d9.idirect3ddevice9__drawprimitive, f6573fdd-1724-cbca-56a1-0b336470257e
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
 - IDirect3DDevice9.DrawPrimitive
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDirect3DDevice9::DrawPrimitive


## -description


Renders a sequence of nonindexed, geometric primitives of the specified type from the current set of data input streams.


## -parameters




### -param PrimitiveType [in]

Type: <b><a href="https://msdn.microsoft.com/89e697f9-02b9-4ae1-9e86-6178da0cb008">D3DPRIMITIVETYPE</a></b>

Member of the <a href="https://msdn.microsoft.com/89e697f9-02b9-4ae1-9e86-6178da0cb008">D3DPRIMITIVETYPE</a> enumerated type, describing the type of primitive to render. 


### -param StartVertex [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Index of the first vertex to load. Beginning at StartVertex the correct number of vertices will be read out of the vertex buffer. 


### -param PrimitiveCount [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Number of primitives to render. The maximum number of primitives allowed is determined by checking the MaxPrimitiveCount member of the <a href="https://msdn.microsoft.com/44457b7b-a1f7-4019-b971-8ec2334d3313">D3DCAPS9</a> structure. PrimitiveCount is the number of primitives as determined by the primitive type. If it is a line list, each primitive has two vertices. If it is a triangle list, each primitive has three vertices. 


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be 
     D3DERR_INVALIDCALL.




## -remarks



When converting a legacy application to Direct3D 9, you must add a call to either <a href="https://msdn.microsoft.com/30c7db1d-5814-49d5-a92a-de597b31cb63">IDirect3DDevice9::SetFVF</a> to use the fixed function pipeline, or <a href="https://msdn.microsoft.com/8ca4d714-b2df-432e-9140-447cef7eaec1">IDirect3DDevice9::SetVertexDeclaration</a> to use a vertex shader before you make any Draw calls.




## -see-also




<a href="https://msdn.microsoft.com/cf951e8e-7adb-417a-bda0-9b3cde4912a7">IDirect3DDevice9</a>



<a href="https://msdn.microsoft.com/535a261a-ca4f-432b-9126-f46c44dc8430">IDirect3DDevice9::DrawIndexedPrimitive</a>



<a href="https://msdn.microsoft.com/9b94ab86-2a6a-4abd-ab56-95315f473226">Rendering from Vertex and Index Buffers (Direct3D 9)</a>
 

 

