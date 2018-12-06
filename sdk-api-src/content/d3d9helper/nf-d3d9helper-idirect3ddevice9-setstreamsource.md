---
UID: NF:d3d9helper.IDirect3DDevice9.SetStreamSource
title: IDirect3DDevice9::SetStreamSource
author: windows-sdk-content
description: Binds a vertex buffer to a device data stream. For more information, see Setting the Stream Source (Direct3D 9).
old-location: direct3d9\idirect3ddevice9__setstreamsource.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9__setstreamsource.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: 58d641c0-a959-cca3-67e2-7290e9426e8e, IDirect3DDevice9 interface [Direct3D 9],SetStreamSource method, IDirect3DDevice9.SetStreamSource, IDirect3DDevice9::SetStreamSource, SetStreamSource, SetStreamSource method [Direct3D 9], SetStreamSource method [Direct3D 9],IDirect3DDevice9 interface, d3d9helper/IDirect3DDevice9::SetStreamSource, direct3d9.idirect3ddevice9__setstreamsource
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
 - IDirect3DDevice9.SetStreamSource
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDirect3DDevice9::SetStreamSource


## -description


Binds a vertex buffer to a device data stream. For more information, see <a href="https://msdn.microsoft.com/ef317537-3095-435d-b0f2-83cb3b385da2">Setting the Stream Source (Direct3D 9)</a>.


## -parameters




### -param StreamNumber [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Specifies the data stream, in the range from 0 to the maximum number of streams -1.


### -param pStreamData [in]

Type: <b><a href="https://msdn.microsoft.com/6efb68b4-c276-4ae2-8a53-316e41c3a77b">IDirect3DVertexBuffer9</a>*</b>

Pointer to an <a href="https://msdn.microsoft.com/6efb68b4-c276-4ae2-8a53-316e41c3a77b">IDirect3DVertexBuffer9</a> interface, representing the vertex buffer to bind to the specified data stream. 


### -param OffsetInBytes [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Offset from the beginning of the stream to the beginning of the vertex data, in bytes. To find out if the device supports stream offsets, see the D3DDEVCAPS2_STREAMOFFSET constant in <a href="https://msdn.microsoft.com/3f3b9f86-dee3-4506-bd2e-1dcc8ba617ed">D3DDEVCAPS2</a>.


### -param Stride [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Stride of the component, in bytes. See Remarks.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be D3DERR_INVALIDCALL.




## -remarks



When a FVF vertex shader is used, the stride of the vertex stream must match the vertex size, computed from the FVF. When a declaration is used, the stride should be greater than or equal to the stream size computed from the declaration.

When calling SetStreamSource, the stride is normally required to be equal to the vertex size. However, there are times when you may want to draw multiple instances of the same or similar geometry (such as when using instancing to draw). For this case, use a zero stride to tell the runtime not to increment the vertex buffer offset (ie: use the same vertex data for all instances). For more information about instancing, see <a href="https://msdn.microsoft.com/d8d9b0c8-b1c4-406d-bf2a-9716d725aec7">Efficiently Drawing Multiple Instances of Geometry (Direct3D 9)</a>.




## -see-also




<a href="https://msdn.microsoft.com/cf951e8e-7adb-417a-bda0-9b3cde4912a7">IDirect3DDevice9</a>



<a href="https://msdn.microsoft.com/535a261a-ca4f-432b-9126-f46c44dc8430">IDirect3DDevice9::DrawIndexedPrimitive</a>



<a href="https://msdn.microsoft.com/61b13680-293b-4c7e-9cf0-d91e764498fb">IDirect3DDevice9::DrawIndexedPrimitiveUP</a>



<a href="https://msdn.microsoft.com/b83110ba-85af-4f02-b651-9e64c37269f5">IDirect3DDevice9::DrawPrimitive</a>



<a href="https://msdn.microsoft.com/1be42c40-49af-458e-a5f5-1f56d2aa4f86">IDirect3DDevice9::DrawPrimitiveUP</a>



<a href="https://msdn.microsoft.com/d64dbbc5-48db-42c5-8b2f-dc0a3068fe16">IDirect3DDevice9::GetStreamSource</a>



<a href="https://msdn.microsoft.com/f9274562-413c-4f0d-bdb4-dc8fa83b6063">Vertex Buffers (Direct3D 9)</a>
 

 

