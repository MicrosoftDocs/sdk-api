---
UID: NF:d3d9.IDirect3DDevice9.GetIndices
title: IDirect3DDevice9::GetIndices
author: windows-sdk-content
description: Retrieves index data.
old-location: direct3d9\idirect3ddevice9__getindices.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9__getindices.htm
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: 137303d6-63b8-2f24-bcef-26fdda3c4a15, GetIndices, GetIndices method [Direct3D 9], GetIndices method [Direct3D 9],IDirect3DDevice9 interface, IDirect3DDevice9 interface [Direct3D 9],GetIndices method, IDirect3DDevice9.GetIndices, IDirect3DDevice9::GetIndices, d3d9helper/IDirect3DDevice9::GetIndices, direct3d9.idirect3ddevice9__getindices
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
 - IDirect3DDevice9.GetIndices
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDirect3DDevice9::GetIndices


## -description


Retrieves index data.


## -parameters




### -param ppIndexData [out]

Type: <b><a href="https://msdn.microsoft.com/df1b7898-6c6b-410b-8ff9-e56625584fdc">IDirect3DIndexBuffer9</a>**</b>

Address of a pointer to an <a href="https://msdn.microsoft.com/df1b7898-6c6b-410b-8ff9-e56625584fdc">IDirect3DIndexBuffer9</a> interface, representing the returned index data. 


#### - pBaseVertexIndex [out]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a>*</b>

Pointer to a UINT value, holding the returned base value for vertex indices. This value is added to all indices prior to referencing vertex data, defining a starting position in the vertex streams. 


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be D3DERR_INVALIDCALL.




## -remarks



 Calling this method will increase the internal reference count on the <a href="https://msdn.microsoft.com/df1b7898-6c6b-410b-8ff9-e56625584fdc">IDirect3DIndexBuffer9</a> interface. Failure to call <a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">IUnknown::Release</a> when finished using this <b>IDirect3DIndexBuffer9</b> interface results in a memory leak.




## -see-also




<a href="https://msdn.microsoft.com/cf951e8e-7adb-417a-bda0-9b3cde4912a7">IDirect3DDevice9</a>



<a href="https://msdn.microsoft.com/535a261a-ca4f-432b-9126-f46c44dc8430">IDirect3DDevice9::DrawIndexedPrimitive</a>



<a href="https://msdn.microsoft.com/61b13680-293b-4c7e-9cf0-d91e764498fb">IDirect3DDevice9::DrawIndexedPrimitiveUP</a>



<a href="https://msdn.microsoft.com/b83110ba-85af-4f02-b651-9e64c37269f5">IDirect3DDevice9::DrawPrimitive</a>



<a href="https://msdn.microsoft.com/1be42c40-49af-458e-a5f5-1f56d2aa4f86">IDirect3DDevice9::DrawPrimitiveUP</a>



<a href="https://msdn.microsoft.com/b27403da-9079-4f97-8520-c2617b53e059">IDirect3DDevice9::SetIndices</a>



<a href="https://msdn.microsoft.com/baa60cd1-a1f0-4dbe-b934-aeb1a5c6b784">Index Buffers (Direct3D 9)</a>
 

 

