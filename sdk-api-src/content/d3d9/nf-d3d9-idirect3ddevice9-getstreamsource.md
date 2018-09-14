---
UID: NF:d3d9.IDirect3DDevice9.GetStreamSource
title: IDirect3DDevice9::GetStreamSource
author: windows-sdk-content
description: Retrieves a vertex buffer bound to the specified data stream.
old-location: direct3d9\idirect3ddevice9__getstreamsource.htm
tech.root: Direct3D9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9__getstreamsource.htm
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: 2e39bbb7-4148-9989-c1b0-1c60594bdf41, GetStreamSource, GetStreamSource method [Direct3D 9], GetStreamSource method [Direct3D 9],IDirect3DDevice9 interface, IDirect3DDevice9 interface [Direct3D 9],GetStreamSource method, IDirect3DDevice9.GetStreamSource, IDirect3DDevice9::GetStreamSource, d3d9helper/IDirect3DDevice9::GetStreamSource, direct3d9.idirect3ddevice9__getstreamsource
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
 - IDirect3DDevice9.GetStreamSource
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDirect3DDevice9::GetStreamSource


## -description


Retrieves a vertex buffer bound to the specified data stream.


## -parameters




### -param StreamNumber [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Specifies the data stream, in the range from 0 to the maximum number of streams minus one. 


### -param ppStreamData [in, out]

Type: <b><a href="https://msdn.microsoft.com/6efb68b4-c276-4ae2-8a53-316e41c3a77b">IDirect3DVertexBuffer9</a>**</b>

Address of a pointer to an <a href="https://msdn.microsoft.com/6efb68b4-c276-4ae2-8a53-316e41c3a77b">IDirect3DVertexBuffer9</a> interface, representing the returned vertex buffer bound to the specified data stream. 


### -param pOffsetInBytes [out]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a>*</b>

Pointer containing the offset from the beginning of the stream to the beginning of the vertex data. The offset is measured in bytes. See Remarks.


### -param pStride [out]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a>*</b>

Pointer to a returned stride of the component, in bytes. See Remarks. 


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be D3DERR_INVALIDCALL.




## -remarks



A stream is defined as a uniform array of component data, where each component consists of one or more elements representing a single entity such as position, normal, color, and so on.

When a FVF vertex shader is used, the stride of the vertex stream must match the vertex size, computed from the FVF. When a declaration is used, the stride should be greater than or equal to the stream size computed from the declaration.

 Calling this method will increase the internal reference count on the <a href="https://msdn.microsoft.com/6efb68b4-c276-4ae2-8a53-316e41c3a77b">IDirect3DVertexBuffer9</a> interface. Failure to call <a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">IUnknown::Release</a> when finished using this <b>IDirect3DVertexBuffer9</b> interface results in a memory leak.




## -see-also




<a href="https://msdn.microsoft.com/cf951e8e-7adb-417a-bda0-9b3cde4912a7">IDirect3DDevice9</a>



<a href="https://msdn.microsoft.com/535a261a-ca4f-432b-9126-f46c44dc8430">IDirect3DDevice9::DrawIndexedPrimitive</a>



<a href="https://msdn.microsoft.com/61b13680-293b-4c7e-9cf0-d91e764498fb">IDirect3DDevice9::DrawIndexedPrimitiveUP</a>



<a href="https://msdn.microsoft.com/b83110ba-85af-4f02-b651-9e64c37269f5">IDirect3DDevice9::DrawPrimitive</a>



<a href="https://msdn.microsoft.com/1be42c40-49af-458e-a5f5-1f56d2aa4f86">IDirect3DDevice9::DrawPrimitiveUP</a>



<a href="https://msdn.microsoft.com/15f4cbf8-7f14-4905-b32e-ed253bc0a3de">IDirect3DDevice9::SetStreamSource</a>



<a href="https://msdn.microsoft.com/f9274562-413c-4f0d-bdb4-dc8fa83b6063">Vertex Buffers (Direct3D 9)</a>
 

 

